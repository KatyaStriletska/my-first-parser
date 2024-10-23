### My parser 

It is a simple parser for education purposes. It allows you to parse numbers in string format.

![alt text](image-1.png)

### Examples
Parsing the correct list:
```rust
use my_parser_striletska::list_parser;
fn main() {
    assert_eq!(list_parser::list("[1,1,2,3,5,8]"), Ok(vec![1, 1, 2, 3, 5, 8]));
}
```
Handling parsing errors:
```rust
use my_parser_striletska::list_parser;
fn main() {
    let input = "[1,a]";
    match list_parser::list(input) {
        Ok(parsed) => println!("Parsed list: {:?}", parsed),
        Err(err) => println!("Error: {:?}", err),
    }
}
```