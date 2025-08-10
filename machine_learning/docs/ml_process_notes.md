# Financial Stock ML Process

* Known observations
* Historical data reveals when to buy, sell, or hold based on known performance
* Training the model needs the highest quality data to provide the best predictions
* Features:
  * Price
  * Target
  * Beta
  * Sector

## How to use color in a bar plot

* Ie: `sns.countplot(y='Sector', hue='Sector', palette='tab10', legend=False, data=stock_data_v2)`
  * y = series
  * hue = series
  * palette = 'tab10' (there are other identifiers to be used, but 'tab10' provides different colors for each)
  * legend = False is because this is a bar chart, having a legend is redundant

## How to drop NaN values

* NaN cannot be masked out as it is not recognized as a value
* Must use the `isnull` syntax
* Ie: `pd.isnull(dataframe_name['series name])` or `pd.isnull(dataframe_name.series_name)
  * Execute using as a Boolean Mask: `dataframe_name[pd.isnull(dataframe_name[series_name])]`
* To drop a null value, use: `dataframe_name = dataframe_name.dropna()`

## Increase/Decrease the font size
* Ie: `plt.rcParams.update({'font.size': 20})`

