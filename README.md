# ModeController
A shape optimized mode y-splitter designed using the adjoint method and used as a mode controller. 

We here provide datasets for a mode modulator/controller built using an optimized mode Y-Junction (mode converter). The mode converter transforms the $TE_0$ and $TE_1$ inputs into an in-phase and off-phase $TE_0$ outputs respectively, or vice-versa. An active Mach-Zhender interferometer is then used to control the phase in one of its branches to enabled the device to be used as a mode controller. This type of systems are useful for mode-filtering, advance communication systems using mode enconding, mode based otical computing and more. 

In this workbook, we provide data for two different design of controllers using MZIs with different phase controls. Both have the same branch length difference, but:
- One circuit design has a 400 um long heated section in the shorter branch,
- The other circuit has a 200 um long heated section in the longer branch.

To drive the controller, a voltage is applied to the heaters. The datasets include 5 different voltage levels for each ciruit and the use of either $TE_0$ or $TE_1$ as an input to the system. An evanescent field based coupler is used to extract the TE1 power in a separte waveguide for tests. The available circuits are:

| Circuit Label      | Input       |  Output 1   |   Output 2  |   Voltage   |
| -----------        | ----------- | ----------- | ----------- | ----------- |
| TE0_topo_DEV03     | TE_0        | TE_1        | TE_0        | [-2, 0.0] V |
| TE0_topo_DEV04     | TE_0        | TE_1        | TE_0        | [-2, 0.0] V |
| TE1_topo_DEV03     | TE_1        | TE_1        | TE_0        | [-2, 0.0] V |
| TE1_topo_DEV04     | TE_1        | TE_1        | TE_0        | [-2, 0.0] V |

## In this notebook

Select a wavelength and the circuit you want to use to query the behaviour of the mode controller. We do so by first finding the resonance shift per power in the electrical circuit, this effect is normally linear to the power so we can extrapolate to any value of power in the heaters. We may use said extrapolation to numerically shift the response at 0 W for any other value in the drive power. Note that even though the thermo-optic effect is linear, the temeperature change in the device is not necessarily depending on the environment conditions and the device temperature. The resulting extrapolated response is consequently only a good approximate in the same range as the data measured.

# Using the notebook
The easier way to interact with this notebook is openning a new google colab space (https://colab.research.google.com/) and cloning this reposiry by running

```
git clone https://github.com/jevillegasd/ModeController
```
