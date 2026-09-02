# The Marble Machine

A tiny hands-on training game about chance and expected value. You pull
marbles from a weighted bag and watch the math show up on its own.

**The bag:** 10 marbles — 6 green (win 1 point), 3 blue (win 5), 1 gold
(win 20). A pull costs 5 points, and the marble always goes back in.

Pull once and anything can happen. Pull a thousand times and the color bars
settle on 60% / 30% / 10%, and the "give-back" number settles near **82%** —
because a pull costs 5 but is only *worth*

```
(0.6 × 1) + (0.3 × 5) + (0.1 × 20) = 4.1 points
```

That gap — price just above expected value — is the entire business model of
every slot machine, roulette wheel, and prize box ever built. This little
machine just lets you *feel* it instead of taking anyone's word for it.

## Run it

No installs, no build, no dependencies — it's one HTML file.

```
git clone https://github.com/marianna718/marble-machine.git
cd marble-machine
```

Then open `index.html` in any browser (double-click it), or serve it if you
prefer:

```
python -m http.server 8000
# then visit http://localhost:8000
```

## What it demonstrates

- **Probability is counting** — 6 out of 10 marbles are green, so green is 60%.
- **Expected value** — each prize times its chance, added up: what one pull
  is worth *on average*, even though no single pull ever pays that amount.
- **The law of large numbers** — the average is invisible in 5 pulls and
  unmissable in 1,000. The tick marks on the bars show where the counting
  says the bars must end up; the bars obey, every time.
- **The house edge** — the machine charges 5 for something worth 4.1 and
  keeps the 0.9 difference. One player can beat it; a crowd of players
  cannot.

## Tinker with it

Everything lives in one `<script>` block at the bottom of `index.html`.
Change the prizes, the cost, or the bag mix and watch the give-back number
move — if you make the expected value bigger than the cost, congratulations,
your machine now loses money.

## License

MIT — see [LICENSE](LICENSE).
