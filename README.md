# backtrader_plus_pyfolio

由于作者对 backtrader 和 pyfolio 都分别做了更新，所以分别起了  [backtrader](https://github.com/NoraGithub/test_backtraderr) 和  [pyfolio](https://github.com/NoraGithub/test_pyfolio)
对修改进行跟踪，然后在本项目中以文件夹形式引入，方便debug和对比。

##  安装
由于backtrader和pyfolio都是子模块。需要用`git submodule`更新
```
git clone https://github.com/NoraGithub/backtrader_plus_pyfolio.git
cd backtrader_plus_pyfolio
git submodule init
git submodule update
```
## 
创建新的本地新的环境并激活。

## 依赖
```
pip install  -r requirements.txt
```

## 运行

PS:  未使用Jupiter。
命令行执行：
```
python run.py
```

## 现象
```
./pyfolio/pyfolio/pos.py:27: UserWarning: Module "zipline.assets" not found; multipliers will not be applied to position notionals.
  'Module "zipline.assets" not found; multipliers will not be applied'
<IPython.core.display.HTML object>
<IPython.core.display.HTML object>
/Volumes/code/quant/test/env/lib/python3.7/site-packages/seaborn/categorical.py:1296: UserWarning: 90.2% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
  warnings.warn(msg, UserWarning)
/Volumes/code/quant/test/env/lib/python3.7/site-packages/seaborn/categorical.py:1296: UserWarning: 53.2% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
  warnings.warn(msg, UserWarning)
/Volumes/code/quant/test/env/lib/python3.7/site-packages/pandas/core/indexes/base.py:5277: FutureWarning: Indexing a timezone-aware DatetimeIndex with a timezone-naive datetime is deprecated and will raise KeyError in a future version.  Use a timezone-aware object instead.
  start_slice, end_slice = self.slice_locs(start, end, step=step, kind=kind)
<IPython.core.display.HTML object>
<IPython.core.display.HTML object>
<IPython.core.display.HTML object>
<IPython.core.display.HTML object>
/Volumes/code/quant/test/env/lib/python3.7/site-packages/seaborn/distributions.py:2557: FutureWarning: `distplot` is a deprecated function and will be removed in a future version. Please adapt your code to use either `displot` (a figure-level function with similar flexibility) or `histplot` (an axes-level function for histograms).
  warnings.warn(msg, FutureWarning)
Traceback (most recent call last):
  File "run.py", line 168, in <module>
    round_trips=True)
  File "./pyfolio/pyfolio/tears.py", line 208, in create_full_tear_sheet
    set_context=set_context)
  File "./pyfolio/pyfolio/plotting.py", line 52, in call_w_context
    return func(*args, **kwargs)
  File "./pyfolio/pyfolio/tears.py", line 759, in create_txn_tear_sheet
    plotting.plot_txn_time_hist(transactions, ax=ax_txn_timings)
  File "./pyfolio/pyfolio/plotting.py", line 1631, in plot_txn_time_hist
    txn_time.index = txn_time.index.tz_localize(pytz.timezone('Asia/Shanghai'))
  File "/Volumes/code/quant/test/env/lib/python3.7/site-packages/pandas/core/indexes/datetimes.py", line 250, in tz_localize
    arr = self._data.tz_localize(tz, ambiguous, nonexistent)
  File "/Volumes/code/quant/test/env/lib/python3.7/site-packages/pandas/core/arrays/datetimes.py", line 978, in tz_localize
    raise TypeError("Already tz-aware, use tz_convert to convert.")
TypeError: Already tz-aware, use tz_convert to convert.
```
