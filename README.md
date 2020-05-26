# time-series-analysis

Repository for self study on Jonathan, D. Cryer, and Chan Kung-Sik. "Time series analysis with applications in R." SpringerLink, Springer eBooks (2008).

Exercises are conducted on both R and Python for language practice purposes. 

### Notable packages used
- R: TSA (functions mostly extracted / used as reference), ggplot, zoo, tseries
- Python: matplotlib, statsmodels, scipy, arch

### Implementation notes
- Regression diagnostic graphs, in the same style as R, are implemented in `Python/utils.py`.
- `eacf`, from the TSA library, is reimplemented in Python in `Python/eacf.py`.  Note that it uses statsmodels' ACF, rather than R, which may lead to small numerical computation differences.
- `armasubsets`, from the TSA library, is reimplemented in Python in `Python/armasubsets.py`.  It uses its own subset search code, rather than relying on R's `regsubsets` library.
- `gBox`, the generalized portmanteu test from the TSA library, is reimplemented in Python in `Python/gBox.py`.  It expects a fitted model from Python's `arch` library, and it uses Numpy for linear filters and linear algebra calculations, statsmodels for ACF, and matplotlib for plotting.
- Spectral density utilities from R are partially reimplemented in `Python/spectrum.py`, providing support for tapering, convolution with arbitrary kernels, and plotting, ensuring compatibility with R's `state::spec.pgram`.