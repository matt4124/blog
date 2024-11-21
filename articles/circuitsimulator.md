## Making a Circuit Simulator ##
*June 2024* 

As a personal project in order to get better at my circuit theory and programming experience I thought coding a circuit simulator would be a worthwhile endeavour. 

I decided to program this simulator in RUST, mostly because I like the language

![](./images/rust-web-logo.jpg)

Programming in rust brought a few unique challenges:
1) The ownership model, oh my god this is probably the biggest problem. I wanted to keep to the standard library in rust, and analysing a circuit meant first converting it to a graph data structure
2) 