# mirocard-postprocessing

Sample Jupyter notebook (`MiroCard_App_Characterization.ipynb`) that post-processes MiroCard
power measurements recorded with the [RocketLogger](https://rocketlogger.ethz.ch/)
(ETH Zurich): it trims the recording, extracts application executions and low-power-mode
periods from the current trace and digital inputs, and plots/quantifies them.
A sample measurement is included in `data/mirocard_triggered_data_app.rld` (about 30 MB).

## Prerequisites

Python 3 with Jupyter, NumPy, pandas and Matplotlib, plus the
[RocketLogger Python library](https://pypi.org/project/rocketlogger/):

```
pip3 install rocketlogger
```

## Usage

```
jupyter notebook MiroCard_App_Characterization.ipynb
```

## MiroCard project

The MiroCard is a batteryless, light-powered BLE smart card, designed by Andres Gomez
(Miromico AG) and inspired by the
[Transient BLE Node](https://gitlab.ethz.ch/tec/public/employees/sigristl/transient_ble_node)
project developed at ETH Zurich. It was presented in:

> Andres Gomez. 2020. *Demo Abstract: On-Demand Communication with the Batteryless MiroCard.*
> In The 18th ACM Conference on Embedded Networked Sensor Systems (SenSys '20).
> [doi:10.1145/3384419.3430440](https://doi.org/10.1145/3384419.3430440)

Related repositories:

| Repository | Contents |
| --- | --- |
| [mirocard-hardware](https://github.com/ansgomez/mirocard-hardware) | Hardware: datasheet, schematics and Altium PCB project (MiroCard V2.0) |
| [mirocard-contiki-ng](https://github.com/ansgomez/mirocard-contiki-ng) | Firmware: Contiki-NG fork with the MiroCard platform and example applications |
| [miroreader-app](https://github.com/ansgomez/miroreader-app) | Android app to receive and display MiroCard beacons |
| [mirocard-scanner-python](https://github.com/ansgomez/mirocard-scanner-python) | Python scripts to scan for and decode MiroCard beacons (bluepy) and discover devices (gattlib) |
| [mirocard-scanner-mqtt](https://github.com/ansgomez/mirocard-scanner-mqtt) | Node.js bridge forwarding MiroCard beacons to an MQTT broker |
| [mirocard-scanner-influx](https://github.com/ansgomez/mirocard-scanner-influx) | Node.js bridge storing MiroCard beacons in InfluxDB |
| [mirocard-webid](https://github.com/ansgomez/mirocard-webid) | Web Bluetooth demo page for identification and sensor readout |
| **mirocard-postprocessing** (this repository) | Jupyter notebook to post-process RocketLogger power measurements |
| [mirocard-plotly](https://github.com/ansgomez/mirocard-plotly) | Plotly Dash web app visualizing a RocketLogger measurement |

## License

BSD-3-Clause. Copyright (c) 2022, Andres Gomez. See [LICENSE](LICENSE).
