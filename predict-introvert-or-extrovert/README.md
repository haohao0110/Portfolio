# Predicting Introverts vs. Extroverts 🧠

It was the weekend right before I moved out of my Rutgers dorm—a quiet Saturday where I stayed home all day, aside from a quick gym session. While browsing Kaggle for fun, I stumbled upon a quirky little competition: **“Predict the Introverts from the Extroverts.”** The topic instantly caught my eye, so I downloaded the dataset just to play around with it.

Two years ago, when I first arrived in the U.S., I was a full-on “E” — my MBTI result showed I was 56% Extroverted. Fast forward to today, I’ve flipped into 63% Introverted. That shift alone made me curious: what kind of features could actually help predict whether someone leans introvert or extrovert?

## 🔍 Dataset Features & Intuition

MBTI doesn’t define E/I based on how social you are, but rather on **how you recharge**. That’s why I found three columns especially meaningful:
- `drained_after_socializing`
- `social_event_attendance`
- `time_spent_alone`

Other features like `friends_circle_size`, `going_outside`, and `stage_fear` seemed less crucial.

> For example, I might go out to dinner with friends four nights a week — does that make me an extrovert? Not really. I don’t *recharge* from these interactions. I often need more alone time afterward to regain energy.

## ⚙️ Feature Engineering

To capture this concept, I created a new feature: **social_energy_score**.  
Weights:
- `drained_after_socializing`: -0.35
- `time_spent_alone`: -0.20
- `social_event_attendance`: +0.25

This score helped determine which users were more likely to be introverted vs. extroverted — based on how they gain or lose energy.

## 📊 Results

- Submitted to Kaggle’s leaderboard
- Achieved **97.4% accuracy**
- Fun and insightful weekend project!

## 📁 Files
- `train.csv` and `test.csv`: From Kaggle Playground S5E7
- `social_energy_score.ipynb`: Main notebook
- `submission.csv`: Final result

---

## ✨ Future Ideas
- Try SHAP to interpret model decisions
- Deploy as a mini MBTI quiz app
- Compare results with real-world MBTI tests

---

### Created by [@haohao0110](https://github.com/haohao0110)
