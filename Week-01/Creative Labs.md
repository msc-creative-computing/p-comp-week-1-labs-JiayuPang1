#### **WEEK ONE: CREATIVE LABS**

# **Don't Choose**
-----------------
#### Make decisions efficiently and minimize the energy consumption of human choice.

## Operating mode

#### The switch controls whether the entire circuit can operate. 
#### After pressing the switch, the circuit runs autonomously, and the small light bulbs will light up in sequence according to the code instructions.
![week 01 creative labs_1](https://user-images.githubusercontent.com/92034503/141812064-9a639762-640e-4f34-95ac-d4cb36efaced.gif)

## Concept of Design

#### In life, people are always easy to face choices, and will struggle and hesitate in the process. A lot of human time and energy are consumed. 
#### Maybe in the future, in the era of big data, people will hand this problem to computers. 
#### All choices are left to the machine, whether it is: What do you want for breakfast today? Where to go on weekends? Who do you choose to be my boy/girlfriend?
#### As long as you press the switch, the computer will automatically match and select all the user's personal information entered in the background.
#### People have relieved a lot of thinking burden, but is the choice under such big data valuable? It is worth thinking about.


## Code
-----------

`int AnimationSpeed = 0;`

```
void setup()
{
  pinMode(2, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(13, OUTPUT);
}
```

```
void loop()
{
  AnimationSpeed = 400;
  if (digitalRead(2) == HIGH) {
    digitalWrite(LED_BUILTIN, HIGH);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(LED_BUILTIN, LOW);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(12, HIGH);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(12, LOW);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(11, HIGH);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(11, LOW);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(10, HIGH);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(10, LOW);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(9, HIGH);
    delay(AnimationSpeed); // Wait for AnimationSpeed millisecond(s)
    digitalWrite(9, LOW);
  } else {
    digitalWrite(13, LOW);
  }
}
```


## Engineering Circuit Diagram
------------------

<img width="799" alt="week01-Engineering circuit diagram" src="https://user-images.githubusercontent.com/92034503/141814761-2f81da53-bb4a-4473-95ae-4d6f93faa792.png">



