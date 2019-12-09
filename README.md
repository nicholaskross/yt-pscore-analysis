# YouTube P-Score Analysis
The following are some thoughts I had while analyzing the YouTube P-Score dataset compiled by Bowblax, Nicholars DeOrio, Optimus, and Pescatore. (Mirrored at https://www.thinkingmuchbetter.com/main/youtube-p-score-analysis/)

Original dataset: https://docs.google.com/spreadsheets/d/130CDsPSjg2BzzlA476AxjZQDdGiHGejhwV_F1H99RMs/edit
Original writeup of the dataset: https://docs.google.com/document/d/1xyxDZIGztWDqGQGae4Oakkt0VAYB21-OcXgNKYrPzcw/edit

Any extra analysis or things you notice, please share as pull requests or forks!

My cleaned-up, extended, and modified version of the dataset: In this repo, as "modded P-ScoreList.xlsx".
**All data cited in the below analysis is present in "modded P-ScoreList.xlsx".**

# First Analysis
I went in with some initial hypotheses, based on my existing knowledge and guesses as to how YouTube recommendations work. This knowledge was based on public information, such as "YouTube uses machine learning" and "YouTube publicly encourages creators to make 'engaging' content" and "watch time and viewer retention generally help a video get recommended in the sidebar".

To test my hypotheses, I hand-added (and cleaned) several extra pieces of data per channel, including channel id (for automated addition of data later, if needed), and total views (see the spreadsheet for some collection details).

My first hypothesis was that P-score would be a good predictor of views-per-video. Turns out, P-score seems more related to sub counts instead.
My second hypothesis: people who made fewer vids (implying quality > quantity, or new channels > backlog) would have more views-per-video. Turns out, there's not much correlation, possibly an inverse correlation (so the more vids you make, the more views each one gets, but not much mattering either way).

So basically, p-scores seem to correlate well with subcount, a little bit with views, and not much else.

# Further Analysis
The (US) P-Score didn't correlate much with any of the per-upload metrics I tried (e.g., views per upload). This tells me youtube uses "channelPScore" to promote videos by channel. Like how you get recommended multiple videos from the same channel, sometimes.

The algorithm seems to weight heavily towards creators who upload frequently and currently (HolaSoyGerman, one of the top creators ever, is low on the list, due to not having uploaded anything in years).

Pre-existing popularity matters, just not by more than a few dozen points: many podcasts (JRE and SFTP) have sorta-higher scores than their own second channels/clips channels, even though the content is the same. This could, however, be due to watch time differences: the clips/second channels may have shorter content, which reduces watchtime.

The only "homegrown" YouTuber with a US p-score > 1000, was Linus Tech Tips. The highest-P-score channel in the dataset with < 1M subs, is Scrubs, which appears to be a type of "drama"/commentary channel.

The metrics most correlated with US P-Score seem to be Total Subscribers (r=0.383) and Average Views Per Subscriber (r=0.362).

Still, channels with wildly-varying sub- and view-counts could get high or low P-Scores.

# Conclusions for Creators
1. Higher P-Scores seem to either cause, or be caused by, higher fan devotion. Many creators don't need to be told this twice, but creating a subscriber base around *you* and *your specific brand* (as opposed to random personality-less videos around a popular topic) is important.
2. Watch-Time matters for P-Score, but not too much. The same content in shorter forms loses in the dozens of points, not the hundreds. (This may make a large difference though; identical content seems to get fewer views and subscribers in shorter form).


Again, if this dataset helps you, or you want to add to the analysis, fork this repo or submit a pull request!
