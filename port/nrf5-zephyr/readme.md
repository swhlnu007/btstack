# Experimental port of BTstack to Zephyr running on Nordic nRF5 Series

## Overview

This port targets the bare Nordic nRF5-Series chipsets with the BLE Link Layer provided by the Zephyr project.

## Status

Working with nRF52 pca10040 dev board. BD ADDR is set to 11:22:33:44:55:66

## Getting Started

To integrate BTstack into Zephyr, please move the BTstack project into the Zephyr root folder 'zephyr'.

Then integrate BTstack:

	./integrate_btstack.sh

Now, the BTstack examples can be build from the Zephyr examples folder in the same way as other examples, e.g.:

	cd samples/btstack/le_counter
	make

to build the le_counter example for the pca10040 dev kit using the ARM GCC compiler.

See nRF5 SDK documentation about how to install it.

All examples that rovide a GATT Server use the GATT DB in the .gatt file. Therefore you need to run ./update_gatt_db.sh in the example folder after modifying the .gatt file.