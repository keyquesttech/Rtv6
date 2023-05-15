
<p align="center" style="margin-bottom: 0px !important;">
 <a href="https://github.com/keyquesttech">
  <img width="150" src="https://github.com/keyquesttech/Rtv6/blob/main/Imgs/nbgicon.png?raw=true" alt="Keyquest logo" align="center">
   <a href="https://www.behance.net/matiasms">
    <img width="80" src="https://github.com/keyquesttech/Rtv6/blob/main/Imgs/behance.png?raw=true" align="center">
</p>

<p align="center" style="margin-bottom: 0px !important;">
  <a href="https://igg.me/at/rtv6/x/33605500#/">
    <img width="300" src="https://github.com/keyquesttech/Rtv6/blob/main/Imgs/gogo.png?raw=true" align="center">
</p>
 
 <p align="center" style="margin-top: 200px !important;">
  <h2 align="center" style="margin-bottom: 100px;">For info and sales PM via discord at: TC#4730 or click the indiegogo image above</h2>
</p>
 
</div>
<p align="center" >RtV6 (Revo to V6)</p>
<p align="center" >A revo nozzle adapter to make any V6 nozzle a quick change nozzle</p>
<p align="center" >Revo CHT? Revo Diamond? Revo Emerald?</p>
<p align="center" >All possible now.</p>
</div>

<div align="center" >
  
  ![GitHub Repo stars](https://img.shields.io/github/stars/keyquesttech/Rtv6?color=%23ff8672)
  ![GitHub forks](https://img.shields.io/github/forks/keyquesttech/Rtv6?color=%238ce2d0)
  ![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/w/keyquesttech/Rtv6?)

<p align="center" style="margin-top: 100px !important;">
  <h2 align="center" style="margin-bottom: 0px;">RtV6 V1:</h2>
</p>

</div>

 - Brass Body.
 - Titanium alloy inner tube.
 - Adds 6mm from heater base to tip of nozzle.

<p align="center" style="margin-bottom: 0px !important;">
  <img width="900" src="https://github.com/keyquesttech/Rtv6/blob/main/Imgs/1.PNG?raw=true" alt="Keyquest logo" align="center">
</p>

<p align="center" style="margin-top: 100px !important;">
  <h2 align="center" style="margin-bottom: 0px;">Tips and tricks:</h2>
</p>

**Nozzle soak:**
In general it's always a good idea to wait a bit to start printing to let the nozzle zoak and stabilize at the desired temperature, however for for the RtV6 nozzle adapter it's even more important.

As a starting point 1 minute is a good value. To do it add the following g-code to your print start right at the end of the code block:

    G4 S60

An improperly soaked/heated nozzle may result in poor print quality, bad bed adhesion, reduced flow or in the worst case 
a broken adapter, where the top and bottom pieces get separated due to the pressure inside the titanium tube pushing both ends apart.

**Print hotter:**
Due to the extra size of the adapter and the increase in mass you may need to print hotter. A good starting point is 10c hotter.

Start with +10c and do a temperature calibration print. You may automate this with a macro:

    [gcode_macro _PRINT_START]
	gcode:
    {% set hotendtemp = params.HOTEND|string %} #Extruder temp parameter
    M109 S{hotendtemp+10} #Set & wait for hotend temp

 Or do it manually
 
**Adjust Z offset:**
Since the adapter is 6mm taller than the standard revo nozzle you will need to re-set you home offset, to do this there's many ways and some depend on your printer/setup. I'm sure you can figure this point out.

**Cooling solution:**
As mentioned above the nozzle is 6mm taller, so the standard Revo cooling solution won't work. You will need to create your own, add stronger fans to your toolhead or add external cooling, just make sure it points to the part, otherwise you will reduce the performance of the adapter.
