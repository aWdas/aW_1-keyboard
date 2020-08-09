# aW_1 Keyboard

This repository contais the firmware and pcb for the aW_1 split (semi-)wireless keyboard.
The aW_1 layout is a modification of the ErgoDox layout with straightened rows and removed thumb clusters. It is therefore fully compatible with ErgoDox keysets. 

**The PCB design is finished, has been delivered and validated (bugs and enhancements have been created as GitHub issues)**  
**The firmware has been validated with the delivered PCB, but still lacks some features (please refer to the GitHub issues)**

![PCB Preview](pcb/aW_1/pcb_preview.png)

The aW_1 is based on the Nordic NRF52832 that provides both the CPU and bluetooth module in a single chip, which allows for lower power consumption. It can be operated from a standard JST-connected battery, or plugged in via USB-C, which will simultaneously charge the battery. The two keyboard halves are connected with a USB-C cable, hence the "semi"-wireless, with the right half containing most of the circuitry and the left only containing an IO expander. A different approach would be the one pursued by the Mitosis (https://www.reddit.com/r/MechanicalKeyboards/comments/66588f/wireless_split_qmk_mitosis/), which does require a dongle that both halves communicate to. I prioritized the ability to quickly connect the keyboard to laptops, mobile devices, etc. and potential pairing of multiple devices at the same time over cutting the last remaining wire. The connection between the halves is USB-C instead of TRRS because TRRS is not hot-pluggable. Like with an ErgoDox, the there is only a single reversible PCB design for both halves, which makes it cheaper to order. 

The firmware is implemented with the Zephyr RTOS (https://www.zephyrproject.org/) and will allow for layout configuration, although not to the extent that QMK offers. I may decide to make the keyboard QMK compatible later on, but building the firmware from the ground up serves as an educational effort to me. 
