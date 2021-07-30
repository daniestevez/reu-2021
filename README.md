# SETI / Breakthrough Listen REU 2021 materials

This repository contains miscellanous materials used with the SETI and
Breakthrough Listen Research Experience for Undergraduates summer programs. The
material was elaborated in the context of the collaboration between GNU Radio
and SETI Institute.

## Outline

* `ata-control` contains a Jupyter notebook that teaches how to control the ATA
  using the `ata_control` Python module from
  [ATA-Utils](https://github.com/SETIatHCRO/ATA-Utils). This was used together
  with `Hydrogen_line_ZMQ` to set up an activity where the students could freely
  observe different parts of the Hydrogen line of the Milky Way.

* `gr-ata` contains a simple flowgraph done as a demo of how the
  [gr-ata](https://github.com/SETIatHCRO/gr-ata) block can be used to control
  the ATA.

* `Hydrogen_line_ZMQ` contains a ZMQ server that streams IQ data from the USRPs
  of the [ATA GNU Radio
  backend](https://wiki.gnuradio.org/index.php/GR-ATA_Testbed) and a client that
  plots the Hydrogen line spectrum.

* `interferometry` contains a demostration of two-antenna interferometry, including
  concepts such as lag domain and fringe rate. There is a simulation flowgraph and
  a live demo with the ATA.

* `live-spectrum.py` is used to send a real time spectrum from the USRPs over ZMQ.
  This contains the client and the server flowgraphs.

* `Tianwen-1` uses [this recording](https://zenodo.org/record/4568100#.YQAskPaxVhG)
  done with Allen Telescope Array of the Chinese Mars orbiter Tianwen-1 and shows how
  to decode the digital information transmitted by the spacecraft. This needs
  [gr-satellites](https://github.com/daniestevez/gr-satellites) installed.

* `Voyager1_GBT` uses a Voyager-1 recording from Green Bank Telescope to show
  how to compute spectrum and waterfall data with GNU Radio
