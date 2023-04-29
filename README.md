# Hi there! 👋

I'm Viet, but you can call me Ramen if you want to.

I'm a self-taught dev from Vietnam 🇻🇳, and I love food, coding, and unrealistic expectations that I unapologetically set for myself and other people.

### And now for a random programming joke that may or may not have been posted to r/ProgrammerHumor:
```rust
use life::Human;
use rand::Rng;
use std::time::Duration;

pub fn adhd_mechanism(human: &mut Human) {
    thread::spawn(|| {
        let mut rng = rand::thread_rng();
        if rng.gen::<u8>() % 2 == 0 {
            human.focused = false;
            human.have_midlife_existential_crisis();
            human.stomach.gargle();
            human.google_search("webmd gargling stomach");
            // Note that since this is a separate thread, it will not panic!() the whole program.
            panic!("Human might have a burst appendix or have cancer that starts in the abdomen");
        }
    }).join().expect("The human probably did have an appendix burst");
}

pub fn procrastinate(human: &mut Human) {
    thread::sleep(Duration::from_secs(rand::thread_rng().gen::<u64>()));
}

pub fn main() {
    let mut me: Human = Human::new(); // My future children, this is how all humans are made.
    
    while me.focused {
        adhd_mechanism(&mut me);
        
        me.eat();
        me.check_for_doppelgangers();
        me.sleep(Duration::from_secs(2 * 60 * 60)); // I sleep for 2 hours and I barely function during the day, so why sleep more?
        
        procrastinate(&mut me);
        me.code();
    }
}
```
