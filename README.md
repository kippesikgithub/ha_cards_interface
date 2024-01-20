# Home Assistant Cards
Welcome to my github and some explanations about the interface and cards I build in Home Assistant. For every card i'll explain a bit about the contents and what features are in it. The room cards I use, are custom, but i re-use them throughout the whole interface, you can just place them in Grids or other cards to arrange them. The base for every room is the same card. Just use them in grids, horizontal/vertical stacks, stack-in cards, whatever floats your boat.  
The interface you see in the overview is our mobile dashboard, which is also usable for desktop. Every room has a Subview in where you can see all the detailed information or extended features for the entities in that room. I use the subviews, because they also contain a 'back' button by default.  
Down here you can see the overview and screenshots of the card, also mentioned which yaml configuration corresponds to that card in this repository.  
I will also include a short Guide later, on howto setup your first room card from the basic.

# Overview
![total_room_cards](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/c373e5c2-f11b-46e0-8a9e-df0729510afc)
![mobile_overview_front](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/b91ef952-08ee-494a-a057-ce32c8d9003d)

Custom made mostly using Mushroom cards and Card Mod  
blinking rings: Automations for that entity/area are enabled, no ring means disabled. Double click to toggle.  
Animated Icons  
Colors and text changing from entities and attributes   

# Wall Tablet Overview
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/7a58060c-08d9-4722-9c6f-4b4439ec1e30)
#### repository link
[https://github.com/kippesikgithub/hass_detailed_power_monitoring](https://github.com/kippesikgithub/hass_walltablet)  
Documentation still has to be updated

# Screenshot per card
## Top Chips Current card  
Build with custom Mushroom chips, card to show the current situation, most important things. Shows the current outside temperature, the main entrance/exit doors status, current power usage, current solar production, and conditional chip for garbage collection icon.
![top_chips_current_overview](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/4fe34500-c97d-4ba1-a8ba-9042f930419c)
#### features 
chips icon and color changing based on value: Outside Temperature, Doors, Current power usage, Solar, Garbage Bin notification  
chips animated based on value: Solar
#### filename
top_chips_card_current_overview.yaml 

## Top Persons card  
Build with custom Mushroom chips and custom Mushroom person cards. Simple overview for persons and car, containing location status, status of ble transmitters on phone (for espresense thoughout the home, will be disbaled when you leave the house, enabled when entering the house), status of charging and battery. Double click on the Tesla to pre-heat the car, will show with blinking red when heating.
![person_cards](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/435e8671-1b7b-47e0-a1b5-02728fb614df)
#### features
chips icon and color changing based on value: ble transmitter, charging and battery percentage
#### filename
top_persons_card.yaml


## Top Button card
Build with custom Mushroom template cards. Just some simple buttons to navigate to subviews with summaries and statistics about Energy, Temperatures, Mediaplayers incl volumes and sources, 3d printing and outside screens. every button navigates to a subview.
![top_button_navigation](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/f1ade95c-a77d-4a4b-b31f-af099f8c1018)
#### features
nothing special, just some color changing and animated icons
#### filename
top_button_card.yaml

## Top Chips Today card  
Build with custom Mushroom chips, card to show the today statistics, most important things. Shows todays energy total (import-export), todays total usage of gas and water and todays total produced sun-energy.  
![top_chips_today_overview](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/8da5b64d-24ae-4ee5-98d4-780b8c6922a5)  
  
top_chips_today_overview.yaml  
chips icon and color changing based on value: Total power usage, gas, water and solar    
chips animated based on value: Solar 

## Trapkast Room Card
Room card for the Trapkast. Contains a pretty basic version of the roomcard, only displaying the temperature, temperature trend, controlls for the light, and some chips for statusses.  
![trapkast_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/9de6b181-02ae-4656-8920-c9d77cc54fa2)
#### features
Color changing Temperature graph in top of card, containing last 24 hours.  
Current Temperature status.  
Blinking ring around the light, to show if automations for that entity/room are enbled. Double click on icon to toggle automations (on/off).  
Chips icon and color changing based on value: motion, main water usage, floor heating pump, rc wifi car (project: https://github.com/kippesikgithub/esp_rc_car)
#### devices in room
Hue light  
Wemos D1 + 3 Dallas DS18B20 sensors (measure floor heating pipes)  
Wemos D1 + proximity sensor (measure watermeter)  
Esp32 + LD2410 (mmwave) + BMP180 (temp and baro)  
Zigbee Wall socket for controlling floor heating pump
#### filename
trapkast_room_card.yaml

## Badkamer Room Card
Room card for the Badkamer.  
![badkamer_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/637caac6-3d99-4ecf-80e3-45628e5833d1)
#### features
Color changing Temperature and Humidity graph in top of card, containing last 24 hours.  
Current Temperature and Humidity statusses.  
Blinking ring around the light, to show if automations for that entity/room are enbled. Double click on icon to toggle automations (on/off).  
Chips icon and color changing based on value: fan, toothbrushes charging, shower status, window.
Navigation to subview from click on card.
#### devices in room
Aqara Zigbee Temperature and Humidity sensor  
Zigbee Wall socket for controlling charging electric toothbrushes  
Shelly 1L for controlling the Fan (based on humidity level)  
Toon integration for reading shower/warm water status  
Aqara Zigbee window sensor
#### filename
badkamer_room_card.yaml

## Kinderkamer Sophie Room Card
Room card for daughters room. Offcourse including princesses, controlls for the led-lighting (desk and unicorn), motion status, controlls for the airconditiong/heating, and temp/humidity/illumination status.  
![sophie_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/110e952c-5979-4731-8029-3b6d862b0966)
#### features
Color changing Temperature and Humidity graph in top of card, containing last 24 hours.  
Current Temperature, Humidity, Illumination and Power usage of room statusses.  
Chips icon and color changing based on value: motion, window, airco.  
Navigation to subview from click on card.
#### devices in room
Hue Light  
Hue remote dimmer  
Esp32 + LD2410 (mmwave) + DHT22 (temp and humidity + WDR (illumination)  
Zigbee Wall socket(s) measuring power usage  
Mitsubishi Heavy Industries Airco (cooling/heating)  
Esp32 WLED Desk ledstrip  
Wemos D1 mini WLED Unicorn light  
Esp32 Somfy RTS for controlling screens  
Aqara Zigbee window sensor
#### filename
kinderkamer_sophie_room_card.yaml

## Kinderkamer Lucas Room Card
Room card for sons room. Offcourse including babyicons, controlls for the led-lighting (commode), motion status, controlls for the airconditiong/heating, and temp/humidity/illumination status.  
![lucas_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/c3ace65b-76e9-4c74-b12e-f5beb4321e57)
#### features
Color changing Temperature and Humidity graph in top of card, containing last 24 hours. 
Current Temperature, Humidity, Illumination and Power usage of room statusses.  
chips icon and color changing based on value: motion, window, airco.  
Navigation to subview from click on card.
#### devices in room
Hue Light  
Hue remote dimmer  
Esp32 + LD2410 (mmwave) + DHT22 (temp and humidity + WDR (illumination)  
Zigbee Wall socket(s) measuring power usage  
Mitsubishi Heavy Industries Airco (cooling/heating)  
Esp32 WLED Commode ledstrip  
Aqara Zigbee window sensor
#### filename
kinderkamer_lucas_room_card.yaml

## Woonkamer Room Card
Room card for the Woonkamer.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/5e0b8316-9594-4ca2-b19b-a743cc76de51)
#### features
Color changing Temperature graph in top of card, containing last 24 hours. 
Current Temperature, Humidity, Illumination of room statusses.  
chips icon and color changing based on value: television, motion, particulate matter, robot vacuum.  
Navigation to subview from click on card.
#### devices in room
Hue Lights  
Hue remote dimmers  
Hue Motion sensors  
Esp32 + LD2410 (mmwave) + DHT22 (temp and humidity + WDR (illumination)  
Esp32 + IR transmitter + IR receiver
Esp32 + espresense  
WLED Esp vuilniswagen (garbage collection light/notifier) https://github.com/kippesikgithub/wled_garbagetruck  
Zigbee Wall socket(s) measuring power usage  
IRobot Roomba  
Lenovo Wall Tablet  
#### filename
woonkamer_room_card.yaml

## Washok Room Card
Room card for the Washok.  
![washok_cards](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/a68dad4d-edd4-4f24-843a-7d860de0f9b5)
#### features
Color changing Temperature graph in top of card, containing last 24 hours. 
Current Temperature, Illumination of room statusses.  
Blinking ring around the light, to show if automations for that entity/room are enbled. Double click on icon to toggle automations (on/off).  
chips icon and color changing based on value: motion, washing machine, dryer, window.  
Navigation to subview from click on card.
#### devices in room
Hue Light  
Hue Motion sensors  
Esp32 + LD2410 (mmwave) + DHT22 (temp and humidity + WDR (illumination)  
Shelly 1PM Power measuring (washing machine, dryer)  
Zigbee Wall socket(s) measuring power usage  
Aqara Zigbee window sensor
#### filename
washok_room_card.yaml


# Subview Energy (navigation from Top Button card)
## Overview Electricity per room
Visualised with Sankey Diagram.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/3e555eb7-0633-4f20-84ac-a111361c6b4b)
#### repository link
https://github.com/kippesikgithub/hass_detailed_power_monitoring

## Current Devices status
Visualised with Mushroom Chips. Which devices are on and using power. Visualised with colored/animated icons. 
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/f095f9dd-80d9-4008-926f-d76976c91073)
#### filename
energy_current_devices_status_card.yaml

## Netto Electricity per day, last3 days
Visualised in Apexcharts. Import electricity from net - exported electricity to net, per day-start, start at 0 (utility meter helper).    
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/8f56a9e7-ecc4-43c2-b348-c82a4d4667cd)

#### filename
energy_electricity_netto_last_week_card.yaml

## Electricity In per day, last week
Visualised in Apexcharts. Total Electricity import per day from last week  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/3c281470-6239-44c6-b875-1a447d4afcc2)
#### filename
energy_electricity_in_last_week_card.yaml

## Electricity Out per day, last week
Visualised in Apexcharts.  Total Electricity export per day from last week  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/d08a4f3b-125f-4293-8cb0-2b64562da124)
#### filename
energy_electricity_out_last_week_card.yaml

## Gas per day, last week 
Visualised in Apexcharts. Gas usage last week, per day. Color changing bars based on values.
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/6dc65b24-abde-4783-8dea-cef5466c610c)
#### filename
energy_gas_last_week_card.yaml

## Water per day, last week 
Visualised in Apexcharts. Water usage last week, per day. Color changing bars based on values.
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/3a08d52e-e6e9-4b57-97d1-1cbb7b803ef2)
#### filename
energy_water_last_week_card.yaml

## Gas vs Outside temperature per day, last week 
Visualised in Apexcharts. Gas usage vs outside temperature last week, per day. Color changing bars based on values.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/da36e4cd-287c-4dc6-a68b-c16b57d73c4a)
#### filename
energy_gas_vs_temp_last_week_card.yaml

## Solar Production today vs yesterday vs prediction
Visualised in Apexcharts. Solar production today's current vs yesterday's current same time vs prediction last week, per day. Color changing bars based on values,  including upcoming sunset, sunrise lines.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/ae78dde2-987b-40c6-aa6c-5b8e11e93cd7)
#### filename
energy_solar_today_vs_yesterday_vs_prediction_card.yaml

## Solar Production today vs predicction
Visualised in Apexcharts. Solar production today vs prediction. Color changing bars based on values,  including upcoming sunset, sunrise lines.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/80ab676b-27f8-4602-be79-947c86fc0923)
#### filename
energy_solar_today_vs_prediction_card.yaml

# Subview Audio (navigation from Top Button card)
## TV and Audio Card
Visualised using Mushroom template and Mushroom chips cards. Current status of tv/audio related devices, buttons for controll and color changing icons based on TV/Audio sources and power usage.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/708ec9fb-37dd-4daa-af4f-6f6bb319109f)
#### filename
multimedia_tv_audio_controll_card.yaml

## Mediaplayer Card
Visualised using Mushroom Mediaplayer and Mushroom chips cards.  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/d54e982d-ee71-4a7d-9590-878de173fa25)
#### filename
multimedia_mediaplayer_card.yaml

# Subview Temperatures (navigation from Top Button card)
## Airco Card
Visualised using Mushroom climate card. Color changing and animated icons.  
![airco_lucas](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/1d4067cb-63e0-40e7-8782-1e111b1644a9)
#### filename
temperatures_climate_card.yaml
