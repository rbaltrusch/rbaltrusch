# Hello World :ok_hand:

I am Richard Baltrusch, a German software engineer that likes to build all kinds of stuff, preferably in Python.

You can contact me using the following links:

- Email: [richard@baltrusch.net](mailto:richard@baltrusch.net?subject=[Github])
- [LinkedIn](https://www.linkedin.com/in/richard-baltrusch-aa809a131/)
- [YouTube](https://www.youtube.com/channel/UCBB1v2nSWPvX_9Km-AMGkGQ)

## Languages

- Professionally Python, Java and MATLAB/Simulink.
- Currently:
  - Developing a full stack web application using Java (Spring Boot) and Javascript.
  - Learning [machine learning](https://github.com/rbaltrusch/gameML) in Python (with Tensorflow/Keras and from scratch).
  - Exploring development of [C-extensions](https://github.com/rbaltrusch/python_performance_examples/tree/master/source/c_extension_example) for Python.
  - Tinkering with Julia and Haskell.
- Interested in Scala, Go and Rust.

## Interests

- Games: I wrote a game engine and used it for my first game, [Bullet Sudoku](https://github.com/rbaltrusch#bullet-sudoku), a 2D top-down platformer.
- Languages: I am interested in constructed languages and [custom programming languages](https://github.com/rbaltrusch/natscript).
- Music: I compose and [procedurally generate music](https://github.com/rbaltrusch/music_generation). The music generated by my neural network [Bach generator](https://github.com/rbaltrusch/bach_generator) is at least "interesting" :)

## Games

### Bullet Sudoku

Bullet Sudoku is a small game I wrote in summer 2020 using my custom made game engine written in Python. A free demo of the game is available on [itch.io](https://richardbaltrusch.itch.io/bullet-sudoku). It is currently sitting at almost 100 downloads!

![Short GIF of Bullet Sudoku gameplay](https://i.imgur.com/W5812oP.gif?raw=true "Short GIF of Bullet Sudoku gameplay")

The source code is currently not open-source, but I plan on releasing a condensed open-source version of the game engine in the near future.

### Game jam submissions

In 2023 I published multiple game jam submissions, with open source code, to try out new technology and new ideas:

[**Unicast Network Sim**](https://github.com/rbaltrusch/unicast_network_sim): a Python game where you deliver network packets. Placed 16th out of 500 for innovation due to the creative input system.

<img width="384" height="256" src="/media/unicast_network_sim.gif" alt="Unicast network simulator gameplay">

[**Myrkur**](https://github.com/rbaltrusch/myrkur): a dungeon exploration game written with Love2D in Lua.

<img width="384" height="256" src="/media/myrkur.gif" alt="Myrkur gameplay">

[**Uncaved**](https://github.com/rbaltrusch/uncaved-gmtk): a reverse cave-exploring game where you control a cave full of traps, written in Java with libGDX.

<img width="384" height="256" src="/media/uncaved.gif" alt="Uncaved gameplay">

### Pygame examples

I have a number of small / medium size pygame examples that illustrate a certain technique or explore game concepts, such as particle effects, lighting, events and networking, in more detail.

![Gif of the particle effects](https://github.com/rbaltrusch/pygame_examples/blob/master/media/particle_effects.gif?raw=true "Gif of the particle effects")
![Gif of the lighting system](https://github.com/rbaltrusch/pygame_examples/blob/master/media/lighting_system.gif?raw=true "Gif of the lighting system")
![Gif of the hexagonal tile map](https://github.com/rbaltrusch/pygame_examples/blob/master/media/hexagons.gif?raw=true "Gif of the hexagonal tile map")
![Gif of a red light source](https://github.com/rbaltrusch/pygame_examples/blob/master/media/red_light.gif?raw=true "Gif of a red light source")

### Chess engine(s)

I have developed a semi-complete [chess-engine in Python](https://github.com/rbaltrusch/chess_ng) from scratch and done a fair amount of optimization, until realizing a fully optimized chess engine likely would require more speed than Python can offer, so I started work on an [implementation in C](https://github.com/rbaltrusch/thcc_engine). The C-code looks less beautiful, but already runs around 70 times faster :)

Here is an AI playing chess against itself using a minimax algorithm (depth 4) using the Python version:

![Chess artificial intelligence playing a game](https://github.com/rbaltrusch/chess_ng/blob/master/media/chess_ai.gif?raw=true "Chess artificial intelligence playing a game")

## Music

### Music analysis

Here's my [music analysis tool](https://github.com/rbaltrusch/music_mood_analysis), which I started building in 2018 and recently built a fancy user interface for:

![Screenshot of the analysis GUI](https://github.com/rbaltrusch/music_mood_analysis/blob/master/music_mood_analysis/gui/media/screenshot2.png?raw=true "Screenshot of the analysis GUI")

### Music generators

Over the years, I have worked on multiple procedural music generators, two of which are open-sourced on Github and available on pypi:
- My [Bach generator](https://github.com/rbaltrusch/bach_generator) generates a transformed version of music input (via midi files) using a machine-learning algorithm optimizing for correlation of the output with the input. This ensures the produced musical transformations are internally consistent.
- [Continuo](https://github.com/rbaltrusch/continuo) is a pypi package that procedurally generates music based on a provided set of input parameters.

## Tools

### Batest

[Batest](https://github.com/rbaltrusch/batest) is a lightweight unit testing framework for Windows batchfile scripts. As no testing framework existed when I was learning [Batch](https://github.com/rbaltrusch/batch), I wrote my own :+1:.

It generates simple HTML test reports like this:

![Screenshots of the test reports](https://github.com/rbaltrusch/batest/blob/master/batest/media/screenshot.png?raw=true)

## Meta-programming

### Natscript

[Natscript](https://github.com/rbaltrusch/natscript) is an interpreted programming language with a natural syntax resembling English:

```powershell
define function main as {
    set squares to []
    for each number in range from 0 to 5 not equal to 3 {
        multiply it by itself, then append it to squares
    }
    return squares
}

# This will output [0, 1, 4, 16] to the console
print result of call main
```

Although a bit slow, due to its current main implementation being in Python, it is a fully functional language that support procedural and functional programming. Performance issues may be addressed in the future with the [C++ version](https://github.com/rbaltrusch/cpp-natscript) (currently still WIP), or by implementing a LLVM JIT-compiler for the language.

### Object oriented batch

For people unfortunate enough to come to Batch with an object oriented background, I wrote an [object oriented framework for Batch](https://github.com/rbaltrusch/objectbatch/wiki), including classes and instances, methods and attributes, inheritance, encapsulation, polymorphism and object composition.

As can be seen in the code examples below, the batch OOP syntax is surprisingly clean (for batch):

Simple use of a class instance:
```batch
::instantiate new object obj of type MyClass
call new MyClass obj construct

::calling method myMethod of instance obj
call # obj myMethod

::reading obj attribute myAttr
echo !%obj%.myAttr!

::writing obj attribute myAttr
set %obj%.myAttr=1
```

Simple class definition:
```batch
::boilerplate
call class %*
%class%

::this is the constructor, adding one custom attribute attr
:public-construct
    call super %*
    set %self%.attr=0
exit /b
```

<sub>It's probably not very useful, but at least it was fun to make :100::100:</sub>

## Apps

- I wrote a small [shop application](https://github.com/rbaltrusch/desktop_shop) to solidify my understanding of SQL and handling confidential data securely in databases.
- I also made a small [chat application](https://github.com/rbaltrusch/pychatter) to get a good grasp of networking using websockets. The application can be run on a local network.

![Gif of the application GUI](https://github.com/rbaltrusch/pychatter/blob/master/pychatter/gui/media/gif1.gif?raw=true "Gif of the application GUI")
