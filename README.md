# Zomato KPT Optimization – Improving ETA Accuracy

## 🚨 Problem
Zomato’s ETA predictions are inaccurate due to unreliable kitchen prep time (KPT) signals, caused by biased merchant inputs and lack of real-time system visibility.

## 🔍 Key Insights
- ~75% of orders had biased prep-time signals due to incorrect merchant marking
- High variation in prep times (~±12 mins), reducing prediction reliability
- No visibility into external kitchen load (Swiggy, dine-in, takeaway orders)

## 💡 Solution
Designed a multi-signal KPT prediction system that improves ETA accuracy by combining:
- Rider wait-time feedback loop
- Merchant reliability scoring
- Kitchen congestion estimation

## ⚙️ Approach
- Identified root causes behind ETA inaccuracies
- Built correction logic using rider wait signals
- Segmented merchants based on behavioral reliability
- Modeled hidden kitchen congestion using proxy signals

## 📈 Impact
- Improved ETA prediction accuracy
- Reduced rider idle time at restaurants
- Scalable across 300K+ merchants

## 🧠 Product Thinking
Instead of relying on a single input (merchant marking), I designed a system combining:
- Behavioral signals (merchant reliability)
- Real-time signals (rider wait time)
- Environmental signals (kitchen congestion)

This makes ETA prediction more robust and scalable.

## 📎 Case Study
[zomato-kpt-case-study.pdf](./zomato-kpt-case-study.pdf)

## 📊 Datasets
1) Zomato Orders Dataset (https://docs.google.com/spreadsheets/d/1qC1GQ606XoGxHjob17DloTxdiXXABtP3/edit?
usp=sharing&ouid=104015938540875365368&rtpof=true&sd=true)
2) Rider Activity Dataset (https://docs.google.com/spreadsheets/d/1Q-6CgcgKVVziZnz7iRQ9EJBV9NTeseOV/edit?
usp=sharing&ouid=104015938540875365368&rtpof=true&sd=true)
3) Merchant Performance Dataset (https://docs.google.com/spreadsheets/d/1sbhNaCrCOxxvmu9clEUtR1LVlmFeqmcT/edit?
usp=sharing&ouid=104015938540875365368&rtpof=true&sd=true)
