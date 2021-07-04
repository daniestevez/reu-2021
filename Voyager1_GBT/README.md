# Voyager-1 Green Bank Telescope recording and GNU Radio

This activity shows how to use GNU Radio to process a raw recording of Voyager-1
made with Green Bank Telescope on 2015, in order to obtain spectrum and
waterfall data.

The recording to be used in this activity can is
[blc3_guppi_57386_VOYAGER1_0004.0000.raw](https://storage.googleapis.com/gbt_guppi/blc3_guppi_57386_VOYAGER1_0004.0000.raw).
This recording uses
[GUPPI
format](https://github.com/UCBerkeleySETI/breakthrough/blob/master/doc/RAW-File-Format.md). More
recordings can be downloaded from the [Breakthrough Listen Open Data
Archive](https://breakthroughinitiatives.org/opendatasearch).

The size of the recording is 16 GB. A much smaller file of 127 MB that only
contains the channel in which the Voyager-1 signal appears is
[blc3_guppi_57386_VOYAGER1_0004.0000_only_vgr1_chan.ci8](https://drive.google.com/file/d/1z6MKabxUX7SaojL4ouVf2WBTWeGCr7t-/view?usp=sharing)
(this is hosted in Google Drive, so it might disappear at some point).

This activity contains the following files:

* `voyager_integrator.grc` shows how to use the
  [FFT](https://wiki.gnuradio.org/index.php/FFT),
  [Integrate](https://wiki.gnuradio.org/index.php/Integrate) and
  [QT GUI Vector Sink](https://wiki.gnuradio.org/index.php/QT_GUI_Vector_Sink)
  blocks to compute and plot the spectrum of the channel of the GUPPI file that
  contains the Voyager-1 signal.

* `voyager_spectrum.grc` shows how to use the
  [Frequency Xlating FIR
  filter](https://wiki.gnuradio.org/index.php/Frequency_Xlating_FIR_Filter) to
  select and downsample the portions of the spectrum containing the carrier and
  data sideband of the Voyager-1 signal. It also shows how to record waterfall
  data to a file.

* `Voyager-1 waterfall.ipynb` is a Jupyter notebook that shows how to plot the
  waterfall data files with Matplotlib.

The GUPPI file is read with a custom embedded Python block that re-uses code
from
[this
notebook](https://github.com/daniestevez/jupyter_notebooks/blob/master/VoyagerGBT.ipynb).
