---
title: "Malmodin's Simple Power Model"
---

This power model offers a more accurate reflection of the instantaneous and short-term effect of video streaming on network energy consumption compared to the [Conventional Approach](energy/approaches/Conventional%20Approach.md).

This power model uses a baseload and dynamic component power model in accounting, and calculates the internet transmission-related energy of networks.
This approach more closely represents the always on state of network equipment and energy consumption compared to the conventional average that is measured in $kWh/GB$.

This is because the power draw is driven by the baseload (or idle power) consumption to operate the equipment, and a function of computational load or data traffic. The separation between baseload and computational load is closer to the actual workflow, since network equipment usually operates nonstop at a constant power consumption baseline, i.e. idle or minimal load/data demand. The constant baseline operation of network devices is required to be able to listen and respond instantly to incoming requests. 