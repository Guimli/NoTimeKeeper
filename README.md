# NoTimeKeeper

![Photo-01](https://github.com/Guimli/NoTimeKeeper/blob/main/Images/OnKonamiBoard.jpg)

During one of our evenings at the Arcade Club, a Konami Silent Scope cabinet displayed the dreaded error message: P1!
This error is known to indicate that the TimeKeeper, a NVRAM used to store the cabinet's settings and scores is running low on battery power and needs replacing.
The M48T58Y, which is the name of this NVRAM in Konami cabinet of this generation, has two functions: non-volatile RAM and internal clock. And the battery life is given as 10 years. So this component has to be replaced every 10 years.
25 years after the creation of this terminal, I thought that there was probably a better component to replace this expensive perishable component. So I naturally turned my attention to F-RAM. F-RAM is non-volatile RAM, but does not require a battery. And it has a data retention time of 120 years. Much longer than NAND or NOR memory. We still have to manage the internal clock. But while browsing the forums, I discovered that the only game that really needs the clock is Battle Tryst. Last but not least, the M48T58Y has two ChipEnable pins. One is active high and the other is active low. Although SilentScope doesn't use the ChipEnable in its high state, as I couldn't check that it was the same on all Konami terminals of this generation, and to facilitate compatibility in my universal programmer, I added a bit of combinatorial logic to recreate the missing ChipEnable on the F-RAM.
After conventional reprogramming of the first 16 bits so that the terminal recognises this new TimeKeeper, the game went from P1 error to Backup Memory Error. You then press the test button on the terminal and set the various essential parameters (calibration of the rifle in my case on SilentScope).
The result is perfect. The game now behaves exactly as if the TimeKeeper were an original M48T58Y. But I don't have to worry about replacing this component again in my lifetime.

Approximate cost for one NoTimeKeeper (costs can reduced if you build several modules) :

- FM16W08-SG : 7 €
- 74LVC2G00DP : 0.50 €
- Capacitor 100nF 0805 : 0.15 €
- PCB (with Shipping cost) : 23 €

Total : 30.65€

I can sell you this module if you don't want to assemble it yourself. Contact me on guimli@free.fr
