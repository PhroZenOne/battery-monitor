# Battery Monitor

This is the documentation for a device that monitors a car battery.

Things we still need to start with:

* Database for storage of customer and device data
* Server that handles all communication between devices, users and db
* Android App
* Ios App
* Webpage
* Hardware Devices
    * Workflow, design etc

Work in progress

* Hardware gsm-devices
    * Figure out parts needed

## Device docs

Plan is to find parts so that we can design and order assemble the PCB in china
and then program and assemble the rest of the parts (case, cables etc) at home.

### PCB components

The total list of things needed to be populated on the PCB

We might skip the battery!

#### Battery charger

We need a something that can take 12v+ to charge the lipo battery. 

##### BQ24040DSQR

[Mousers listing](https://www.ti.com/lit/ds/symlink/bq24045.pdf?HQS=dis-mous-null-mousermode-dsf-pf-null-wwe&ts=1698692613899&ref_url=https%253A%252F%252Feu.mouser.com%252F)


#### Voltage reg

AP1501-33K5G-13 | IC: PMIC; DC/DC converter; Uin: 4.5÷40VDC; Uout: 3.3VDC; 3A; TO263-5
AP1501-33K5G-13

[ljcpcb] https://jlcpcb.com/partdetail/DiodesIncorporated-AP1501_33K5G13/C9982

#### Voltage sensing

INA226 as power or on board adc?

##### INA226

[specs](https://www.ti.com/product/INA226?utm_source=google&utm_medium=cpc&utm_campaign=asc-null-null-GPN_EN-cpc-pf-google-wwe&utm_content=INA226&ds_k=INA226&DCM=yes&gclsrc=ds&gclsrc=ds)

[jlcpcb](https://jlcpcb.com/partdetail/TexasInstruments-INA226AIDGSR/C49851)

$1.1713 - 1
$0.84 -> 100

#### Processor

I think we want to stay at 3.3v to use same v as gsm-devices and
kan use the 3.7v lipo

Options:

##### Some 3.3v arduino 

Not sure if available

##### ESP32

Lots of IO and power, probably to much for this project.

##### ESP8226

Smaller but enough for wifi + connectivity

Need to investigate ports needed for gsm-device + power sens

##### AtTiny

Skipping wifi and other stuff, smallest possiblility

##### STM32

The smallest low powered versions "L" seems capable and cheap

#### Gsm-device

We need a LTE-M device (optionally also NB-IoT)

##### Sim7080g

[SimCom Overview](https://www.tme.eu/Document/6d3e53b0fa4b72dd4e7fd1bddf920252/Product%C2%A0Catalogue%C2%A0202301%C2%A0V1.pdf
)

[Dev Board](https://github.com/techstudio-design/sim7080_dev_board)

##### GMO2S 

[Datasheet](https://eu.mouser.com/datasheet/2/1047/PI_GM02S_1_20200910_WEB-2905882.pdf)

[TME listing](https://www.tme.eu/Document/6d3e53b0fa4b72dd4e7fd1bddf920252/Product%C2%A0Catalogue%C2%A0202301%C2%A0V1.pdf)


### Cable and other external

### Case

### Antenna

### Lipo battery



