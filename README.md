# Chessn-tutorials-
Below is a structured 5-part beginner-to-intermediate chess curriculum suitable for a chess website.

# Lesson 1: How the Pieces Move

### Introduction

Every chess game begins with understanding how each piece moves. The rook moves in straight lines, the bishop moves diagonally, the queen combines both movements, and the king moves one square in any direction. Two pieces deserve special attention: the knight, which jumps over other pieces in an "L" shape, and the pawn, which has unique movement and capture rules, including the special *en passant* capture.

**Key Concepts**

* Knight moves in an L-shape: two squares in one direction, then one square perpendicular.
* Knights can jump over pieces.
* Pawns move forward but capture diagonally.
* *En passant* allows a pawn to capture an opposing pawn that has just advanced two squares.

**Illustrative FEN (En Passant Example)**
`8/8/8/3pP3/8/8/8/8 w - d6 0 1`

*In this position, White can play exd6 en passant.*

---

# Lesson 2: Opening Principles

### Introduction

Strong openings are built on simple principles rather than memorizing long variations. The goal is to control important central squares, develop your pieces efficiently, and protect your king through castling. Following these principles will help you reach solid positions regardless of the opening you choose.

**Key Concepts**

* Control the center (e4, d4, e5, d5).
* Develop knights and bishops early.
* Avoid moving the same piece repeatedly.
* Castle early for king safety.

**Illustrative FEN**
`r1bqkb1r/pppp1ppp/2n2n2/4p3/3PP3/2N2N2/PPP2PPP/R1BQKB1R w KQkq - 4 4`

*Both sides have developed pieces and are preparing to castle.*

---

# Lesson 3: Basic Tactics

### Introduction

Tactics are short combinations that win material or deliver checkmate. Learning to recognize common tactical patterns will dramatically improve your results. Three of the most important tactical motifs are forks, pins, and skewers.

### Fork

A single piece attacks two or more targets simultaneously.

**FEN (Knight Fork)**
`r3k2r/pppp1ppp/8/3N4/8/8/PPPP1PPP/R3K2R w KQkq - 0 1`

*The knight attacks multiple valuable targets at once.*

### Pin

A piece cannot move because a more valuable piece behind it would be exposed.

**FEN (Pin Example)**
`r3k2r/pppp1ppp/8/8/2b5/5N2/PPPP1PPP/RNBQK2R w KQkq - 0 1`

*The bishop pins the knight to the king.*

### Skewer

A valuable piece is attacked and forced to move, exposing a less valuable piece behind it.

**FEN (Skewer Example)**
`4k3/8/8/8/8/8/4r3/4KQ2 b - - 0 1`

*The rook attacks the queen, exposing the king behind it.*

---

# Lesson 4: Essential Checkmate Patterns

### Introduction

Recognizing common mating patterns helps you convert winning positions and defend against threats. Some checkmates appear repeatedly in practical games, making them essential for every improving player.

### Two Rooks Checkmate

Two rooks can work together to trap the enemy king along the edge of the board.

**FEN**
`6k1/8/8/8/8/8/5RR1/6K1 w - - 0 1`

*White can coordinate the rooks to force mate.*

### Defending Against Scholar's Mate

Beginners often fall for the quick attack on f7. Knowing how to defend it prevents early losses.

**FEN**
`r1bqkb1r/pppp1ppp/2n5/4p2Q/2B5/8/PPPP1PPP/RNB1K1NR b KQkq - 2 3`

*Black must respond accurately to White's queen-and-bishop attack on f7.*

---

# Lesson 5: Basic Endgame Fundamentals

### Introduction

Many games are decided in the endgame. Even a small advantage can become a win if you understand fundamental endgame principles. Learning how to activate your king and promote pawns is crucial for converting advantages.

**Key Concepts**

* Activate your king in the endgame.
* Push passed pawns.
* Support pawn promotion with your king.
* Understand opposition and king positioning.

**Illustrative FEN**
`8/8/8/3k4/8/3K4/4P3/8 w - - 0 1`

*White's goal is to escort the pawn toward promotion while using the king actively.*

---

### Curriculum Summary

1. **How the Pieces Move** — Master movement rules, including knights and *en passant*.
2. **Opening Principles** — Control the center, develop pieces, and castle early.
3. **Basic Tactics** — Learn forks, pins, and skewers.
4. **Essential Checkmate Patterns** — Execute common mates and defend against Scholar's Mate.
5. **Basic Endgame Fundamentals** — Use king activity and pawn promotion techniques to win endgames.
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Chess Academy</title>

<script src="https://cdn.tailwindcss.com"></script>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/chessboard.js/1.0.0/chessboard-1.0.0.min.css"/>

<style>
body {
    background: #0f172a;
}

.board-container {
    max-width: 700px;
    margin: auto;
}

.white-1e1d7 {
    background-color: #e2e8f0 !important;
}

.black-3c85d {
    background-color: #475569 !important;
}

.lesson-active {
    background: linear-gradient(135deg,#2563eb,#7c3aed);
}

#board {
    width: 100%;
}

::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-thumb {
    background: #475569;
    border-radius: 20px;
}
</style>
</head>

<body class="text-white min-h-screen">

<div class="flex flex-col lg:flex-row min-h-screen">

    <!-- Sidebar -->
    <aside class="w-full lg:w-80 bg-slate-900 border-r border-slate-800 p-6">

        <h1 class="text-3xl font-bold mb-2">
            ♟ Chess Academy
        </h1>

        <p class="text-slate-400 mb-8">
            Beginner to Intermediate Interactive Lessons
        </p>

        <nav class="space-y-3">

            <button
                class="lesson-btn lesson-active w-full text-left p-4 rounded-xl transition"
                data-lesson="0">
                Lesson 1<br>
                <span class="text-sm opacity-80">
                    How the Pieces Move
                </span>
            </button>

            <button
                class="lesson-btn w-full text-left p-4 rounded-xl bg-slate-800 hover:bg-slate-700 transition"
                data-lesson="1">
                Lesson 2<br>
                <span class="text-sm opacity-80">
                    Opening Principles
                </span>
            </button>

            <button
                class="lesson-btn w-full text-left p-4 rounded-xl bg-slate-800 hover:bg-slate-700 transition"
                data-lesson="2">
                Lesson 3<br>
                <span class="text-sm opacity-80">
                    Basic Tactics
                </span>
            </button>

            <button
                class="lesson-btn w-full text-left p-4 rounded-xl bg-slate-800 hover:bg-slate-700 transition"
                data-lesson="3">
                Lesson 4<br>
                <span class="text-sm opacity-80">
                    Essential Checkmate Patterns
                </span>
            </button>

        </nav>

    </aside>

    <!-- Main Content -->
    <main class="flex-1 p-4 md:p-8">

        <div class="max-w-6xl mx-auto">

            <!-- Header -->
            <div class="mb-6">
                <h2 id="lessonTitle"
                    class="text-3xl font-bold mb-2">
                    Lesson 1: How the Pieces Move
                </h2>

                <p class="text-slate-400">
                    Experiment freely with the board and learn visually.
                </p>
            </div>

            <!-- Chessboard Card -->
            <div class="bg-slate-900 rounded-2xl p-4 md:p-6 shadow-2xl">

                <div class="board-container">
                    <div id="board"></div>
                </div>

                <div class="flex justify-center mt-6">
                    <button
                        id="resetBtn"
                        class="px-6 py-3 bg-blue-600 hover:bg-blue-700 rounded-xl font-semibold transition">
                        Reset Position
                    </button>
                </div>

            </div>

            <!-- Lesson Description -->
            <div class="bg-slate-900 rounded-2xl p-6 mt-6">

                <h3 class="text-xl font-semibold mb-4">
                    Lesson Overview
                </h3>

                <div id="lessonContent"
                     class="text-slate-300 leading-relaxed">
                </div>

                <div class="mt-6 p-4 bg-slate-800 rounded-xl">
                    <div class="text-sm text-slate-400 mb-2">
                        FEN Position
                    </div>

                    <code id="fenDisplay"
                          class="break-all text-blue-400">
                    </code>
                </div>

            </div>

        </div>

    </main>

</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/chess.js/0.10.3/chess.min.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/chessboard.js/1.0.0/chessboard-1.0.0.min.js"></script>

<script>

const lessons = [
{
title: "Lesson 1: How the Pieces Move",
fen: "8/8/8/3pP3/8/8/8/8 w - d6 0 1",
description: `
<p class="mb-3">
Every chess game begins with understanding how each piece moves.
The knight is unique because it jumps over pieces in an L-shape.
Pawns move forward but capture diagonally.
</p>

<p>
This position demonstrates the special pawn capture called
<strong>en passant</strong>.
White may capture the black pawn on d5 by playing exd6 en passant.
Try moving the pieces around and explore the position.
</p>
`
},
{
title: "Lesson 2: Opening Principles",
fen: "r1bqkb1r/pppp1ppp/2n2n2/4p3/3PP3/2N2N2/PPP2PPP/R1BQKB1R w KQkq - 4 4",
description: `
<p class="mb-3">
Good openings are built on principles rather than memorization.
</p>

<ul class="list-disc ml-6 space-y-2">
<li>Control the center.</li>
<li>Develop knights and bishops early.</li>
<li>Castle quickly for king safety.</li>
<li>Avoid moving the same piece repeatedly.</li>
</ul>
`
},
{
title: "Lesson 3: Basic Tactics",
fen: "r3k2r/pppp1ppp/8/3N4/8/8/PPPP1PPP/R3K2R w KQkq - 0 1",
description: `
<p class="mb-3">
Tactics win games.
</p>

<ul class="list-disc ml-6 space-y-2">
<li><strong>Fork:</strong> One piece attacks multiple targets.</li>
<li><strong>Pin:</strong> A piece cannot move because something valuable is behind it.</li>
<li><strong>Skewer:</strong> A valuable piece moves away exposing another piece.</li>
</ul>

<p class="mt-3">
The knight in this position demonstrates the idea behind a fork.
</p>
`
},
{
title: "Lesson 4: Essential Checkmate Patterns",
fen: "6k1/8/8/8/8/8/5RR1/6K1 w - - 0 1",
description: `
<p class="mb-3">
Checkmate patterns are essential for finishing games.
</p>

<ul class="list-disc ml-6 space-y-2">
<li>Two rooks can force mate by cutting off escape squares.</li>
<li>Learn how to defend against Scholar's Mate attacks.</li>
<li>Coordinate pieces to trap the king.</li>
</ul>

<p class="mt-3">
This position demonstrates the famous Two-Rook mating technique.
</p>
`
}
];

let currentLesson = 0;
let game = new Chess();

const board = Chessboard('board', {
position: lessons[0].fen,
draggable: true,
dropOffBoard: 'snapback',
sparePieces: false,

onDrop: function(source, target) {

    const move = game.move({
        from: source,
        to: target,
        promotion: 'q'
    });

    if (move === null) {
        return 'snapback';
    }
}
});

function loadLesson(index) {

    currentLesson = index;

    document.querySelectorAll('.lesson-btn').forEach(btn => {
        btn.classList.remove('lesson-active');
        btn.classList.add('bg-slate-800');
    });

    document
      .querySelector(`[data-lesson="${index}"]`)
      .classList.add('lesson-active');

    const lesson = lessons[index];

    game.load(lesson.fen);
    board.position(lesson.fen);

    document.getElementById('lessonTitle').textContent =
        lesson.title;

    document.getElementById('lessonContent').innerHTML =
        lesson.description;

    document.getElementById('fenDisplay').textContent =
        lesson.fen;
}

document.querySelectorAll('.lesson-btn')
.forEach(btn => {

    btn.addEventListener('click', () => {
        loadLesson(Number(btn.dataset.lesson));
    });

});

document.getElementById('resetBtn')
.addEventListener('click', () => {

    const lesson = lessons[currentLesson];

    game.load(lesson.fen);
    board.position(lesson.fen);

});

loadLesson(0);

window.addEventListener('resize', () => {
    board.resize();
});

</script>

</body>
</html>
```
const lessonPuzzles = {
    0: {
        correctMove: "e5d6",
        success: "Correct! You found the en passant capture.",
        fail: "Try again. Look for the special en passant rule."
    },

    1: {
        correctMove: "e4e5",
        success: "Excellent! Advancing into the center gains space.",
        fail: "Look for a move that increases central control."
    },

    2: {
        correctMove: "d5c7",
        success: "Great! The knight fork attacks multiple targets.",
        fail: "Search for a tactical fork with the knight."
    },

    3: {
        correctMove: "f2f8",
        success: "Checkmate! The rooks coordinate perfectly.",
        fail: "Look for a forcing mating move."
    }
};const board = Chessboard('board', {
    position: lessons[0].fen,
    draggable: true,
    dropOffBoard: 'snapback',

    onDrop: function(source, target) {

        const puzzle = lessonPuzzles[currentLesson];
        const attemptedMove = source + target;

        if (puzzle) {

            if (attemptedMove === puzzle.correctMove) {

                const move = game.move({
                    from: source,
                    to: target,
                    promotion: 'q'
                });

                if (move === null) {
                    return 'snapback';
                }

                setTimeout(() => {
                    alert(puzzle.success);
                }, 100);

                return;
            }

            alert(puzzle.fail);
            return 'snapback';
        }

        const move = game.move({
            from: source,
            to: target,
            promotion: 'q'
        });

        if (move === null) {
            return 'snapback';
        }
    }
});<div id="feedback"
     class="hidden mt-4 p-4 rounded-xl text-center font-semibold">
</div>function showFeedback(message, success) {

    const box = document.getElementById("feedback");

    box.textContent = message;

    box.className =
        success
        ? "mt-4 p-4 rounded-xl bg-green-600 text-white text-center font-semibold"
        : "mt-4 p-4 rounded-xl bg-red-600 text-white text-center font-semibold";
}showFeedback(puzzle.fail, false);
