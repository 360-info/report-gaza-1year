# `/data`

## `daily-killed-cumulative.csv`

A daily timeseries of casualties across Israel, Lebanon and Gaza since October 7, 2023. Where possible, casualties are broken down into adults and children.

Adult and child casualties in Gaza are estimated twice: once using the daily numbers provided by the Gaza Ministry of Health directly from Tech for Palestine, and again by multiplying the total casualty count by the fraction of children in the named list of casualties also published by TFP. The "adjusted" columns therefore divide casualties into those confidently believed to be adults, those confidently believed to be children, and those where the age is not known due to differing estimates.

Palestinians killed in the West Bank are not included in these estimates.

Columns include:

- `date`: YYYY-MM-DD
- `killed_in_lebanon`: cumulative number of people killed in Lebanon (both children and adults)
- `palestine_children_tfp`: cumulative number of children killed in Gaza according to TFP's daily estimates
- `palestine_adults_tfp`: cumulative number of adults killed in Gaza according to TFP's daily estimates
- `israel_children`: the number of Israeli or foreign national children killed in Israel on October 7
- `israel_adults`: the number of Israel or foreign nationals killed in Israel on October 7, plus the number of Israeli soldiers killed in or near Gaza
- `palestine_total`: 
- `palestine_children_adj`: cumulative number of children killed in Gaza estimated using the named lists (as described above)
- `palestine_unknown`: the cumulative number of casualties in Gaza where the age is not known due to differing estimates
- `palestine_adults_adj`: cumulative number of adults killed in Gaza estimated using the named lists (as described above)

# `/data/raw`

## `gaza-casualties-daily.csv`

The ["Daily casualties - Gaza"](https://data.techforpalestine.org/docs/casualties-daily) dataset from TFP, current as of September 26.

## `tfp-named-killed.csv`

The ["Killed in Gaza"](https://data.techforpalestine.org/docs/killed-in-gaza/) dataset from TFP, current as of September 26.

## `israel-killed.csv`

A timeseries of Israeli soldiers killed in or near Gaza since October 7, manually transcribed from OCHA Flash Updates. (`analysis/casualties/index.qmd` extracts the text of these updates, but the actual figures were manually transcribed from them.) Columns include:

- `date`: YYYY-MM-DD
- `killed_soldiers_gaza`: number of soldiers killed
