## List of datasets

1. `train_ziji_feb27.csv`: fill in missing value except `built_year`
2. `train_ziji_mar26.csv`: fill in `built_year` on top of `train_ziji_feb27.csv`
3. `ronghua_mar_26.csv`: remove unused columns, bucketize `tenure`
4. `ziji_mar27.csv`: correct `np.nan` treatment in `ronghua_mar_26`, drop original columns that have a converted counterpart.
5. `train_yutong.csv`[(here)](https://github.com/StevenShi-23/CS5228-Data-Mining/blob/yutong/train_yutong.csv): merge `train_ziji_mar27.csv` and new distance-related attributes (i.e.,`train_distance_attributes.csv`)

> Note: meaning of new attributes in `ziji_mar27.csv`
> `tenure_remains`: number of years left in the tenure (contains very large number and 0)
> `tenure_years`: number of years in the tenure. If not avaialble, set to 99. Only has two buckets (99, 999)
> Also, ziji removed `lat, lng, index, bedrooms, tenure`, and renamed `bedrooms_1` to `bedrooms`

6. `test_ziji_mar27.csv`: raw test.csv converted using the same method as training set