# Using the Nois Toolbox in a CosmWasm smart-contract

#### coinflip

Takes a randomness and returns the result of a coinflip (heads or tails)

```rust
use nois::coinflip;

let side = coinflip(randomness);
if side.is_heads(){
    println!("heads")
}
if side.is_tails(){
    println!("tails")
}
```

#### int_in_range

Derives a random integer in the given range. Use this method to avoid a modulo
bias.

```rust
use nois::int_in_range;

// Half-open interval [1, 7)
let dice1 = int_in_range(randomness, 1..7);
assert!(dice1 >= 1);
assert!(dice1 < 7);

// Closed interval [1, 6]
let dice2 = int_in_range(randomness, 1..=6);
assert!(dice2 >= 1);
assert!(dice2 <= 6);
```

#### ints_in_range

Derives random integers in the given range. Use this method to avoid a modulo
bias. Using this is potentially more efficient than multiple calls of
_int_in_range_.

```rust
use nois::ints_in_range;


let [dice1, dice2] = ints_in_range(randomness, 1..=6);
assert!(dice1 >= 1 && dice1 <= 6);
assert!(dice2 >= 1 && dice2 <= 6);
```

#### random_decimal

Returns a Decimal d with 0 <= d < 1

```rust
use nois::random_decimal;

let d = random_decimal(randomness);
```

#### shuffle

Shuffles a vector using the Fisher-Yates algorithm

```rust
use nois::shuffle;

//We are randomly shuffling a vector of integers [1,2,3,4]
let mut data = vec![1, 2, 3, 4];
shuffle(randomness, &mut data);
// The length of the vector is the same but the order of the elements has changed
assert_eq!(data.len(), 4);
assert_ne!(data, vec![1, 2, 3, 4]);
```

#### sub_randomness_with_key

Takes a randomness and a key. Returns an arbitrary number of sub-randomnesses.
The key is mixed into the randomness such that calling this function with
different keys leads to different outputs. Calling it with the same key and
randomness leads to the same outputs.

```rust
use nois::{sub_randomness_with_key, int_in_range};


let mut provider = sub_randomness_with_key(randomness, "Key");

let dice1_subrandomness = provider.provide();
let dice2_subrandomness = provider.provide();

let dice1_result = int_in_range(dice1_subrandomness, 1..7);
let dice2_result = int_in_range(dice2_subrandomness, 1..7);
```

#### sub_randomness

Takes a randomness and a key. Returns an arbitrary number of sub-randomnesses.
This is equivalent to calling _sub_randomness_with_key_ with key b"_^default^_".

```rust
use nois::{sub_randomness, int_in_range};

let mut provider = sub_randomness(randomness);

let dice1_subrandomness = provider.provide();
let dice2_subrandomness = provider.provide();

let dice1_result = int_in_range(dice1_subrandomness, 1..7);
let dice2_result = int_in_range(dice2_subrandomness, 1..7);
```
