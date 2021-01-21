# GWE: easy monitoring and overclocking

GWE - aka GreenWithEnvy - is a very useful tool for monitoring and overclocking Nvidia GPUs. Even if you don't intend to overclock, it is still recommended to install it due to useful information it provides.

For installation instructions see [GWE's official website](https://gitlab.com/leinardi/gwe). I recommend to avoid using flatpak for variety of reasons including driver versions desync and lack of auto startup support, but you still can try it out if you will.

## Suggested GWE settings

Once you have installed GWE, launch it and open its settings window. Here are the settings I suggest to use:

### Launch on login - on
### Check for new App version on launch - on (especially for source code installations)
### Load last fan and overclocking profile - off

I really, *really* recommend to have this one turned off, especially if using "launch on login" as well, unless you love getting stuck out of desktop.

### Minimixe to tray on close - on
### Refresh interval - 1 second

1 second wors perfectly fine, but you may want to use other value for some reason, I guess.

### Show App indicator - on

### Show GPU Temperature - on

## Data to look at

Outside of obvious usage and temperature indicators, there is one output field you're interested in: PCIe. If it says "Gen3" in it, your PC supports PCIe3 (which it very likely does if you intend to use it for gaming to begin with), meaning that you can get an extra boost for data transfer speed between system and GPU. Check out next article to learn how.

TODO: write about overclocking
