```rust
use std::collections::HashMap;

fn print_section(title: &str, items: &[&str]) {
    println!("{title}:");
    for item in items {
        println!("- {item}");
    }
}

fn print_contact(title: &str, contact: &HashMap<&str, &str>) {
    println!("{title}:");
    for (key, value) in contact {
        let formatted = value.replace(" at ", "@").replace(" dot ", ".");
        println!("- {key}: {formatted}");
    }
}

fn main() {
    let about = [
        "I'm a master's student of Big Data Technology and Engineering, founder \
         of Zako Club and Mia Institute.",
    ];

    let doing = [
        "Nothing.",
    ];

    let device = [
        "Samsung Galaxy S25",
        "ASUS TUF Gaming A14 (2024)",
    ];

    let contact = [
        ("Email", "779 at zako dot club"),
        ("X", "https://x.com/KujouYuko"),
        ("Bilibili", "https://space.bilibili.com/19036404"),
    ].into_iter().collect();

    print_section("About", &about);
    print_section("Doing", &doing);
    print_section("Device", &device);
    print_contact("Contact", &contact);
}
```
