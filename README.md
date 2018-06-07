[`analysis.ipynb`](https://github.com/AdamStelmaszczyk/retro-leaderboard/blob/master/analysis.ipynb) is the most important file with all the plots.

Leaderboard data from every day* of the contest is in the [`json`](https://github.com/AdamStelmaszczyk/retro-leaderboard/tree/master/json) directory.

To get it, `14 19 * * * ./download.sh` cron job was set invoking `download.sh` script every day:

```
wget https://contest.openai.com/rest/leaderboard --output-document `date +%m-%d`.json -o `date +%m-%d`.out
```

<sup>* Except first 5 days, i.e. 5-9 April, because the idea for `retro-leaderboard` came to my mind on 10 April.</sup>
