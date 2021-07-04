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

* `Hydrogen_line_ZMQ` contains a ZMQ server that streams IQ data from the USRPs
  of the [ATA GNU Radio
  backend](https://wiki.gnuradio.org/index.php/GR-ATA_Testbed) and a client that
  plots the Hydrogen line spectrum.

* `Voyager1_GBT` uses a Voyager-1 recording from Green Bank Telescope to show
  how to compute spectrum and waterfall data with GNU Radio
