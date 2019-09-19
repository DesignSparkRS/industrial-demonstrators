# RS Industrial Demonstrators

![DIN rail detail](/images/featured.jpg)

The code in this repository is for a pair of demonstrator units constructed to
showcase RS Components industrial products, that are each driven by a Brainboxes
BB-400 Neuron Edge Industrial Controller, plus ED-538 (Ethernet to 8 x Digital In
and 4 x Relay out I/O module).

## Contents

The directory structure is as follows:

      conveyor/              - Conveyor demonstrator
      rotlin/                - Rotary and linear actuator demonstrator

## Usage

Since this project is not intended to be used as-is, it has not been packaged
for installation. However, the steps to install are quite simple:

1. Create the directory `/opt/rsid/bin`
2. Copy [brainboxes.py][1] and the appropriate PLC script (`plc-conveyor` or
`plc-rotlin`) to the new directory
3. Copy the associated `.service` file to `/lib/systemd/system`
4. Enable at boot with `sudo systemctl enable plc-UNIT`

## Licence

Copyright (C) 2019 RS Components Ltd.

This software is published under the Apache License Version 2.0.

[1]: http://www.brainboxes.com/files/pages/support/faqs/sample_code/Brainboxes.IO.Python.zip
