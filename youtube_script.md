# YouTube Script: I Built an AI to Predict the World Cup and It's Unhinged
### Style: Michael Reeves | Target: Gen Z | Runtime: ~10–12 min

---

## METADATA

**Title options:**
- *I Made an AI Predict the Entire World Cup and It's Completely Delusional*
- *I Trained a Neural Network on Football and It Chose Violence*
- *This AI Predicted the 2026 World Cup and I Kind of Hate It*

**Thumbnail:** You looking confused/horrified next to a bracket showing England
winning, with "ENGLAND??" in big red text and a brain exploding emoji

**Hook for algorithm:** "I built an AI that simulated every single World Cup match.
72 group games. 31 knockout matches. One champion. It's England. I'm as upset
as you are."

---

## SCRIPT

---

### [COLD OPEN — 0:00]

*[You, standing in front of a whiteboard covered in incomprehensible math]*

**YOU:** So I built an AI to predict the 2026 World Cup.

*[Beat.]*

**YOU:** And England won.

*[Long pause. You stare into the camera with dead eyes.]*

**YOU:** I know. I know. I'm going to explain why this happened and why none of
it is my fault. Roll the intro.

*[INTRO — chaotic montage of code, football clips, loading bars, and your face
looking progressively more unhinged at 3am]*

---

### [PART 1: THE BIT — 0:45]

**YOU:** Okay so here's the thing. The 2026 World Cup has 48 teams. 48.
They just kept adding teams. At some point FIFA looked at the tournament and
said "you know what this needs? More." And now we have Curacao. We have
DR Congo. We have — I checked — **Haiti**. I love Haiti but come on.

And I thought, you know what, instead of watching people on Twitter argue about
who's going to win for the next six months, what if I just... made a computer
do it. And then I could be wrong *efficiently*.

So I built a neural network. From scratch. At an unreasonable hour. Like a
normal person.

---

### [PART 2: WHAT IS A NEURAL NETWORK — 2:00]

**YOU:** Okay so real quick — for the people in the back who just watch my
videos for the chaos and don't actually care about the code, which is valid,
here's neural networks in like 45 seconds.

*[Cut to: extremely bad MS Paint diagram of a brain]*

**YOU:** Your brain has neurons. Neurons talk to each other. When lots of
neurons agree on something, you have a thought. Like "I should not eat that"
or "I should definitely eat that" or "what if England won the World Cup."

A neural network does the same thing but with math. You have an input layer —
that's where the data goes in. You have hidden layers — that's where the
"thinking" happens, and also where all my bugs live. And you have an output
layer — that's where the answer comes out.

*[Cut to: actual code briefly]*

**YOU:** See this? This is 128 neurons, then 64, then 32. It looks like a
funnel. It is a funnel. Information goes in wide and comes out narrow. Like a
brain, but worse and also I made it.

The key thing is the network doesn't start smart. It starts completely stupid.
It's basically a newborn. You have to *train* it by showing it thousands of
examples until it figures out the pattern. Like when you teach a puppy not to
bite — except the puppy is math and you can't yell at it.

---

### [PART 3: THE DATA — 3:30]

**YOU:** So to train the network, I needed data. Historical football match data.
Tens of thousands of games.

I also needed to actually represent each team as *numbers* because computers
don't understand "Brazil is vibing right now" or "Argentina is built different."
They understand arrays. Cold, dead arrays.

So for every team I tracked:
- Their FIFA ranking — which is basically the official "how good are you" number
- How many goals they score on average per game
- How many goals they *let in* on average
- Their win rate over the last two years

*[Show the team database briefly]*

**YOU:** This is all 48 teams. Look at this. Curacao has a 32% win rate and
averages 0.95 goals per game. That's not a football statistic, that's a cry
for help.

And then there's the hosts — USA, Canada, Mexico — who get a little home
advantage boost because, scientifically, playing in front of your own fans
makes you slightly less bad.

---

### [PART 4: HOW IT PREDICTS SCORES — 4:45]

**YOU:** Now here's where it gets actually kind of insane. Most prediction
models just do win/draw/loss. That's boring. I wanted *scores*. I wanted to
know it's a 3-1, not just "team A wins."

So instead of classifying outcomes, my neural network outputs two numbers:
*expected goals* for each team. Statisticians call this xG. It's basically
"how many goals should this team have scored based on the quality of their
chances."

*[Draw a quick diagram]*

**YOU:** So the model says, okay, based on the ranking difference, goal
averages, win rates, home advantage — Team A should score about 1.8 goals.
Team B should score about 0.9.

But then — and this is the fun part — I don't just round those. I pull from
a **Poisson distribution**.

Poisson is this statistical distribution that's literally designed for
modelling random events that happen at a certain rate. Goals in football.
Buses arriving. Emails from your boss at 11pm. It captures the randomness.

So even if the model says "Brazil should score 1.8 goals," they might score 0.
They might score 4. Because football is stupid and that's kind of the point.

*[Show Poisson distribution graph briefly]*

**YOU:** This is what makes the predictions interesting. The model isn't
deterministic. Run it twice, you get different scores. Run it a hundred times,
you get a distribution of outcomes. That's actually how professional sports
models work. Monte Carlo simulation. They run it like 10,000 times and take
the average.

I ran it once. For content.

---

### [PART 5: THE LEARNING CURVE — 6:15]

**YOU:** Before we get to the actual predictions — and oh, they are something —
let me show you the learning curve because I think this part is genuinely cool
and nobody ever shows this.

*[Show the learning curve graph]*

**YOU:** This green line is the training error. This is how wrong the model
is on data it's *already seen*. The red dashed line is the cross-validation
error — how wrong it is on data it's *never seen*. 

When you start with almost no training data, over here on the left, both lines
are all over the place. The model is basically guessing. It's me at a pub quiz
at round one.

As you add more data, both lines go down. The model gets smarter. By the end,
the training error and the validation error are basically touching, which means
the model is *generalising* — it's actually learned the pattern, not just
memorised the training data.

The gap between those two lines? That's the generalisation gap. Ours is 0.003
expected goals. That is extremely good. I did not expect that. I was prepared
to be embarrassed.

Also the loss goes to basically zero in under 100 epochs of training. The thing
learned fast. Suspiciously fast. I'm choosing to take credit for that.

---

### [PART 6: THE GROUP STAGE — 7:15]

*[Dramatic music. Pull up the group tables.]*

**YOU:** Okay. Let's talk about what actually happened.

72 matches. Every group, every game. And immediately the AI chose violence.

*[Highlight Group B]*

**YOU:** Switzerland. *Switzerland.* Won every single group game. Flawless.
9 points, 6 goals scored, zero conceded. Perfect record. Switzerland!
The country famous for cheese, watches, and *being neutral in everything*
just absolutely cooked Italy, Canada, and Qatar.

*[Highlight Group G]*

**YOU:** Group G. Belgium, Iran, Egypt, New Zealand. The AI decided **Iran
tops the group**. With 7 points. Iran! Ahead of Belgium! Belgium, who's been
in the top 10 in the world for like a decade, got knocked out in the group
stage. I looked at this output and I said "okay, what are you doing" and it
just stared at me.

*[Highlight Group E]*

**YOU:** Germany wins Group E with a perfect record. 9 points, 8 goals, zero
conceded. That I believe. Germany in a World Cup group stage is just Germany
doing normal Germany things.

*[Highlight biggest upsets]*

**YOU:** The craziest group result though? Japan. Japan tops their group,
beats Netherlands, beats Poland. And then in the Round of 32 — I'm not joking —
Japan beats Mexico. Japan eliminates the host nation. In round one. Mexico,
playing in front of their own fans, at the Azteca, and they lose to Japan 1-0.

The AI has decided Mexico's home advantage is not enough. The AI does not care
about the Azteca. The AI grew up watching anime.

---

### [PART 7: THE KNOCKOUT BRACKET — 8:30]

*[Show the bracket PNG]*

**YOU:** Okay so this is the bracket. This is what it looks like when you let
a neural network run a sports tournament. Look at it. It's beautiful. It's
cursed. It's both.

The big ones:

**Ecuador.** Ecuador made the *Final*. They come in as a 21st-ranked team,
they beat South Korea, they beat Netherlands — Netherlands, people — they beat
Brazil in the semi-finals in extra time. Gooooone. Brazil, 5-time World
Cup champions, out in the semis, 1-0 after extra time, because Ecuador
apparently read a different script than everyone else.

*[Zoom in on the semi-final bracket]*

**YOU:** And the other semi-final. Senegal. Senegal gets out of the group stage
as a second-place team, and then just starts sending people home. They beat
Portugal 1-0. They beat Argentina 1-0 in the quarters. They beat France — wait
sorry — no, England beat France, then England beat Senegal in the semis 2-0.
The AI is respecting Senegal a lot more than your bracket does.

Actually let me be real with you. Senegal reaching the semi-finals of the World
Cup is not that crazy. They were in the quarters in Qatar. The AI might
actually be onto something here.

---

### [PART 8: THE FINAL — 9:30]

*[Dramatic pause. Long stare into camera.]*

**YOU:** So. The Final.

Ecuador. Versus England.

Two nations with very different relationships to winning the World Cup.
Ecuador has never won it. England won it in 1966, which was 60 years ago, and
has been emotionally recovering since.

The AI says: England. 3-1. In 90 minutes. No extra time, no penalties.
Just England scoring three goals and walking away.

*[Beat.]*

**YOU:** I want to be upset about this. I want to sit here and say "the AI is
wrong, this is obviously wrong." But here's the thing. England are ranked 4th
in the world. They have a 71% win rate. They score 1.9 goals a game and
concede less than 1. On paper, England winning a World Cup is not insane.
It's statistically reasonable.

It's just *England*.

*[Stare at camera]*

**YOU:** The AI doesn't know about 1966. The AI doesn't know about penalty
shootouts. The AI doesn't have trauma. The AI has never watched England play
in a tournament and felt that specific feeling of hope being slowly excavated
from your chest. The AI just sees numbers, and the numbers say England.

*[Sigh]*

**YOU:** Brazil gets third place, by the way. Brazil beats Senegal 2-1 in the
third place match. So at least they get a trophy. Sort of.

---

### [PART 9: LIMITATIONS AND REAL TALK — 10:30]

**YOU:** Now look. Is this going to be right? Probably not exactly. A neural
network trained on stats and rankings can't predict injuries, can't predict
the referee being cooked, can't predict Kylian Mbappé waking up and deciding
it's his World Cup today.

Sports prediction is genuinely one of the hardest problems in machine learning.
The best models in the world — used by actual betting companies with millions
of dollars on the line — get football predictions right maybe 50% of the time.
My model, trained on synthetic data in a Jupyter notebook at whatever time it
was, is not beating the betting companies.

But here's the thing — and I mean this genuinely — the *process* is what's
interesting. Building a system that can take 48 teams' worth of data, simulate
72 group matches, rank the best third-place finishers, seed a 32-team bracket
without same-group rematches, and spit out a full tournament in 12 seconds?
That's actually kind of insane that a relatively small piece of code can do
that.

The neural network trained in under 100 epochs. The learning curve showed
genuine generalisation — the model wasn't just memorising, it was learning
patterns. The Poisson sampling adds realistic randomness that pure win/loss
models miss.

It's not going to be right. But it's going to be *interesting* to watch.

---

### [OUTRO — 11:30]

**YOU:** So. England wins the 2026 World Cup. Ecuador is the dark horse.
Senegal breaks your bracket. Germany is boringly good. Switzerland is
inexplicably perfect. Iran beats Belgium. Japan beats Mexico. Brazil gets
third place.

Screenshot your bracket now. When England lifts the trophy and you had them
winning, you're welcome. When Ecuador reaches the final and your friends are
losing their minds, you're welcome. When literally none of this happens and
France wins in three weeks? That's on the AI. I'm just the messenger.

The code is on GitHub, link in the description. You can run it yourself.
Change the random seed, get completely different results. That's kind of
the point — there's a range of plausible outcomes, and this is one of them.

If you want to see me do something equally unhinged with a different sport,
or if you want to see me improve this model with actual real historical data
instead of synthetically generated stuff — subscribe. Like. Leave a comment
telling me which team you think the AI is most wrong about.

My money's on the AI being completely delusional about Iran. We'll see in
June.

*[Walk off camera. Come back.]*

**YOU:** Also Curacao is going 0-3 in the group stage with zero goals scored
and ten conceded. That part I believe 100%. That part the AI got right.

*[Walk off again.]*

---

## PRODUCTION NOTES

**Pacing:**
- This runs 10–12 minutes at a conversational pace — don't rush the comedic
  beats, let the pauses land
- The "I know. I know." cold open pause should be at least 3 full seconds

**B-Roll suggestions:**
- The notebook running in the terminal (real-time simulation output scrolling)
- The bracket PNG being generated (screen record + zoom to champion box)
- The learning curve graph with a slow zoom from the chaos on the left to the
  convergence on the right
- Quick cuts between team flags when mentioning upsets
- The Poisson distribution animation (a few frames of the distribution shifting)

**On-screen text moments:**
- "0.003 xG generalisation gap" — flash on screen when you mention it
- "SWITZERLAND PERFECT RECORD" — big text overlay
- "IRAN TOPS GROUP G" — red text, horror music sting
- "JAPAN BEATS MEXICO 1-0" — same energy
- The Final scoreline: **ECUADOR 1 – 3 ENGLAND** in massive text

**Tone calibration:**
- You're not angry, you're *bewildered*. The AI is a force of nature. You built
  it and now you have to live with what it decided.
- The England reveal in the cold open should feel like a confession, not a
  celebration
- When you explain the technical stuff, you're explaining it *to yourself* as
  much as to the audience — you're figuring it out out loud

**Thumbnail A/B test ideas:**
1. Your face + "ENGLAND WON??" in red over the bracket
2. Bracket image alone with "The AI Broke Football"
3. Side-by-side of you looking confident vs you looking horrified with
   "Before training" / "After training" labels

---

*Generated to accompany: `world_cup_2026_predictor.ipynb`*
*Predictions based on seed 2026, run May 2026*
*Champion: England | Runner-up: Ecuador | 3rd: Brazil*
