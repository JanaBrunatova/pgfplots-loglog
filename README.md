Create a goupplot of loglog plots using the [PGFPlots](https://ctan.org/pkg/pgfplots?lang=en) package.

The data in this example are in the code itself, where `pgfplotstableread` function is used. The first column contains data for the x-asix, the second and third column contain y-data. Different datasets are used for each subfigure.

To compute the slope and intercept for each data, you can use `linregress` function as follows:
```python
from scipy import stats
slope, intercept, _, _, _ = stats.linregress(log_x, log_y)
```
Note that since we create a loglog plot in LaTeX, we actually need to store `np.exp(intercept)` instead of `intercept`!

The output should look like this:
[standalone_loglog.pdf](https://github.com/user-attachments/files/18789216/standalone_loglog.pdf)
![standalone_loglog](https://github.com/user-attachments/assets/d620c859-4ca1-4354-8672-1d79fe86e341)
