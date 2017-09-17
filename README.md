# SmartThings-IKEA-Tradfri-RGB
SmartThings Device Handler for IKEA Tradfri RGB Bulbs


Copyright 2017 Pedro Garcia

     Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except
     in compliance with the License. You may obtain a copy of the License at:
     
     http://www.apache.org/licenses/LICENSE-2.0
     
     Unless required by applicable law or agreed to in writing, software distributed under the License is distributed
     on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License
     for the specific language governing permissions and limitations under the License.

IKEA Trådfri RGB Bulb

Color management is not trivial. IKEA bulbs are using CIE XY color scheme instead of Hue/Saturation. Also the 
bulbs do not seem to be able to output "light cyan" color. Maybe it is my fault for not having being able to
identify the correct color scheme (currently assuming sRGB with gamma correction), but cannot either with the 
IKEA remote pairing...

This handler is written so that it reports any change in the bulb state (on/off, brightness, color) as an event 
immediately to be processed by other apps.

Author: Pedro Garcia
Date: 2017-09-17
Version: 1.1

TO DO:
 * Color presets
 * Enable debug logging on app settings
 * Remove custom code when ST correctly parses both all color attributes and multiple reporting in one message
 * Color event should send string with hue and saturation values instead of hex, as per API reference, but when
   doing so, the color picker does not get updated 

Please refer to the SmartThings community forum post about this Device Handler for any comments, bux fixes. etc:
 https://community.smartthings.com/t/ikea-tradfri-rgb-bulbs-zigbee-with-cie-xy-color-scheme/98503
