
 This Folder contains example of projects which can be easily used to start working with Bluegiga modules.
 There are three main folders:
    dkble        - Examples for DKBLE development board
    dkble112     - Examples for Bluegiga DKBLE112 development board
    dkble113     - Examples for bluegiga DKBLE113 development board
 Below short description of each example:

 
    Project:        Bluegiga Battery 
    Folder name:    battery
    Puropse:        Provide battery voltage readout.
    Dercription:    This project base on Battery Service which is part of BLE GATT specification. 
                    Project configuration contains a BG script - battery.bgs - which handles mater battery readout request, 
                    scale read ADC value for percentage notation and send it back  to the master.

    Project:        BG Demo
    Folder name:    bgdemo
    Puropse:        Provide periodic VDD readout.
    Dercription:    This project starts 12-bits VDD readout every 1 second. 
                    VDD value is finally written to "xgatt_battery"  characteristic and notify to the master.
                    Data can be notified by "xgatt_battery" characteristic if Client Configuration characteristic flag is set 1.

    Project:        Bluegiga CR Demo
    Folder name:    cable_replacement
    Puropse:        Provide bi-derecional communication between USART1 and "xgatt_data" characteristic.
    Dercription:    This project provides communication between USART1 and 128-bit uuid "xgatt_data" characteristic. 
                    Data can be send by USART1 and write to "xgatt_data" characteristic and vice versa. 
                    Data can be indicated by "xgatt_data" characteristic if Client Configuration characteristic flag is set 2.

    Project:        BLExxx-xxx thermometer
    Folder name:    dkble
    Puropse:        Provide Thermometer readout for all BG modules.
    Dercription:    This is example of periodic temperture measurement for all BG modules. 
                    Temperature is displayed on development kit and also can be indicated by Temperature service if indication is enabled.

    Project:        BG Demo
    Folder name:    evkit_accelerometer
    Puropse:        Provide example of ADXL350 accelerometer readout for all BG modules.
    Dercription:    This project shows how to use periodic acceloremeter readout. 
                    BG script configures SPI and accelometer and starts 1 sec periodic timer.
                    Accelerometer value can be notify by "acc_value" if indication is enabled.

    Project:        BG Demo
    Folder name:    evkit_altimeter
    Puropse:        Provide example of MPL3115A2 atlimeter readout for BLE121LR-m256k, BLE113 and BLE113-m256k
    Dercription:    This is example how to use periodic altimeter readout and notify values on characteristics.
                    MPL3115A2 and BLE module use I2C to communicate with each other.  
                    The temperature and altitude are notify on "alt_value" and "temp_value" characteristic if notification flag is set.

    Project:        BG Demo
    Folder name:    evkit_display
    Puropse:        Provide example of display usage for BLE121, BLE113 and BLE113-m256k
    Dercription:    This is example how to configure display on development kit and display "Hello World!" string. 
                    Note: BLE module does not enter in advertising mode.

    Project:        Bluegiga Heart Rate Demo
    Folder name:    hr
    Puropse:        Provide example of Heart Rate readout for all BLE modules				
    Dercription:    This is example how to use periodic heart rate readout and notify values on "xgatt_hr" characteristics.
                    GATT configuration use Heart Rate service for indication. 
                    BG script read 9 effective bits from AIN6, convert it and write to "xgatt_hr" characteristic.

    Project:        Bluegiga HTM demo
    Folder name:    htm
    Puropse:        Provide example of periodic Health Thermometer readout for all BLE modules.
    Dercription:    This is example shows how to use periodic health thermometer readout and notify values on "xgatt_temperature_celsius" characteristics.
                    Periodic readout is started/stopped by enabling/disabling characteristic "xgatt_temperature_celsius" indication. 
                    Temperature is periodically read from Temperature sensor, converted to Celsius scale and wrote to "xgatt_temperature_celsius" characteristic.

    Project:        Bluegiga Keyboard Demo
    Folder name:    keyboard
    Puropse:        Provide example of HID keyboard for all BLE modules.
    Dercription:    This example base on HID Service oparating as keyboard.
                    BG script start 1 second timer on every connection event and stop it after disconnection. 
                    Soft timer handler fills data buffer with the pattern and write it to "hid_keyboard_in" characteristic. 
                    Next clear data buffer and againt write is to "hid_keyboard_in" characteristic. 
                    Those patterns are indicated when "hid_keyboard_in" characteristic indication is enabled.
	
    Project:        Bluegiga OTA Demo
    Folder name:    ota
    Puropse:        Provide example of flashing images to internal and external flash via OTA.
    Dercription:    After booting into DFU mode bootloader reads flash contents and flashes contents to module.
                    More detail can be found in "ota256.bgs" and "ota.bgs" files for external and internal flash respectively.

    Project:        Bluegiga UART Demo
    Folder name:    uartdemo
    Puropse:        Use UART1 as default interface for all BLE modules.
    Dercription:    Provide example of UART configuration. UART is configured as USART1 interface with 57600 b/s baud rate.
                    After reseting BLE module sends initialization string over the USART1. BLE module can be also managed by UART interface.
                    Note: BLE module is in sleep mode by default. Configuration of "wake up" pin allows to wake it up after pressing button P0_0.
                    Setting up <sleep enable="false" /> in hardware file disable sleep of BLE module.

    Project:        Bluegiga BLED112
    Folder name:    usbcdc
    Puropse:        Use USB as default interface for BLE112
    Dercription:    Provide example of USB configuration. USB usage on development kit requires also switching "USB to UART converter" on.
                    BLE module is recognized by system as "Bluegiga Low Energy Dongle".

    Project:        Bluegiga Find Me
    Folder name:    find_me
    Puropse:        This project base on Immediate Alert Service which is part of BLE GATT specification.
    Dercription:    Provide example of indication Immediate Alert. There is possible to indicate three level on alert: No Alert, Mild Alert and High Alert.
                    Alert level is displayed on developmen kit display after sending write command w/o response to Alert Level characteristic.

    Project:        Bluegiga Mouse Demo
    Folder name:    mouse
    Puropse:        Provide example of HID mouse for BLE113 module.
    Dercription:    This example base on HID Service oparating as mouse.
                    20 ms soft timer is started when Client Configuration characteristic is enabled for "hid_mouse" or "hid_boot_mouse" characteristic respectively. 
                    After reset BLE module operates as "report mode". This can be changed for "boot mode" when "hid_protocol_mode" characteristic value is set to 2.
					Current buttons status (pressed/release) and accelorometer value are written to the "hid_mouse" or "hid_boot_mouse"  depengind on the value of "hid_protocol_mode" characteristic.

    Project:        DKBLE112 thermometer
    Folder name:    dkble112
    Puropse:        Provide example of periodic Health Thermometer readout for  DKBLE112 module. 
    Dercription:	This is example shows how to use periodic health thermometer readout, indicate values on "xgatt_temperature_celsius" characteristics
	                and write temperature to the display. Periodic readout is started after module boot up. Temperature is periodically read from Temperature sensor, 
                    converted to Celsius scale and wrote to "xgatt_temperature_celsius" characteristic and display.

    Project:        DKBLE112 thermometer
    Folder name:    dkble113
    Puropse:        Provide example of periodic Health Thermometer readout for  DKBLE113 module.
    Dercription:    This is example shows how to use periodic health thermometer readout, indicate values on "xgatt_temperature_celsius" characteristics
	                and write temperature to the display. Periodic readout is started after module boot up. Temperature is periodically read from Temperature sensor, 
                    converted to Celsius scale and wrote to "xgatt_temperature_celsius" characteristic and display.
