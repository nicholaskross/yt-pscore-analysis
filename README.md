# YouTube P-Score Analysis
The following are some thoughts I had while analyzing the YouTube P-Score dataset compiled by Bowblax, Nicholars DeOrio, Optimus, and Pescatore.

Original dataset: https://docs.google.com/spreadsheets/d/130CDsPSjg2BzzlA476AxjZQDdGiHGejhwV_F1H99RMs/edit
Original writeup of the dataset: https://docs.google.com/document/d/1xyxDZIGztWDqGQGae4Oakkt0VAYB21-OcXgNKYrPzcw/edit

My cleaned-up, extended, and modified version of the dataset: In this repo, as "modded P-ScoreList.xlsx".
**All data cited in the below analysis is present in "modded P-ScoreList.xlsx".**

# First Analysis
I went in with some initial hypotheses, based on my existing knowledge and guesses as to how YouTube recommendations work. This knowledge was based on public information, such as "YouTube uses machine learning" and "YouTube publicly encourages creators to make 'engaging' content" and "watch time and viewer retention generally help a video get recommended in the sidebar".

To test my hypotheses, I hand-added (and cleaned) several extra pieces of data per channel, including channel id (for automated addition of data later, if needed), and total views (see the spreadsheet for some collection details).

My first hypothesis was that P-score would be a good predictor of views-per-video. Turns out, P-score seems more related to sub counts instead.
My second hypothesis: people who made fewer vids (implying quality > quantity, or new channels > backlog) would have more views-per-video. Turns out, there's not much correlation, possibly an inverse correlation (so the more vids you make, the more views each one gets, but not much mattering either way).

So basically, p-scores seem to correlate well with subcount, a little bit with views, and not much else.

# Further Analysis
The this tells me youtube uses "channelPScore" to promote videos by channel. Like how you get recommended multiple videos from the same channel, sometimes.

# Conclusions for Creators
1. 
