# mysensors-watermeter

/*
 * Sketch to read pulses from pulse meter;
 * Only accepts a pulse change if the signal has been stable for more than x seconds;
 * Only sends message to gateway after more than x seconds have passed since sending last message;
 * Pulses are assumed to equal 1 liter of water
 *
 * Author  Sandor Incze & Michel Schilthuizen
 * Created 2016-05-29
 * Version 1.0
 *
 * Based on the flow reader sketch "WaterMeterPulseSensor" by
 * Henrik Ekblad <henrik.ekblad@mysensors.org>
 * Copyright (C) 2013-2015 Sensnology AB
 * Full contributor list: https://github.com/mysensors/Arduino/graphs/contributors
 *
 * During testing in can be handy to be able to set the values in domoticz; You can do this by using the REST request below:
 * (replace x.x.x.x and deviceid by relevant numbers
 * http://x.x.x.x:8080/json.htm?type=command&param=udevice&idx=deviceid&nvalue=0&svalue=0

 * This sketch was designed because of the enormous amount of false interrupts we received from the TCRT-5000
 * And is a modified version of the isrcounter.c we found for the same radio module used with a raspberry.

 * https://www.mysensors.org/build/pulse_water
 * Follow wiring instructions here:     https://www.mysensors.org/temp/APM_D3.png
                                        https://www.mysensors.org/water/doao.png
 */
