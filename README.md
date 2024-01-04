# Home Assistant Cards
Welcome to my github and some explanations about the interface and cards I build in Home Assistant. For every card i'll explain a bit about the contents and what features are in it. The room cards I use, are custom, but i re-use them throughout the whole interface, you can just place them in Grids or other cards to arrange them. The base for every room is the same card.  
The interface you see in the overview is our mobile dashboard, which is also usable for desktop. Every room has a Subview in where you can see all the detailed information or extended features for the entities in that room. I use the subviews, because they also contain a 'back' button by default.  
Down here you can see the overview and screenshots of the card, also mentioned which yaml configuration corresponds to that card in this repository.  
I will also include a short Guide later, on howto setup your first room card from the basic.

# Overview
![total_room_cards](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/c373e5c2-f11b-46e0-8a9e-df0729510afc)

Custom made mostly using Mushroom cards and Card Mod  
blinking rings: Automations for that entity/area are enabled, no ring means disabled. Double click to toggle.  
Animated Icons  
Colors and text changing from entities and attributes   

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
Temperature graph in top of card, containing last 24 hours.  
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
Temperature and Humidity graph in top of card, containing last 24 hours.  
Current Temperature and Humidity statusses.  
Blinking ring around the light, to show if automations for that entity/room are enbled. Double click on icon to toggle automations (on/off).  
Chips icon and color changing based on value: fan, toothbrushes charging, shower status, window.
Navigation to subview from click on card.
#### devices in room
Aqara Zigbee Temperature and Humidity sensor  
Zigbee Wall socket for controlling charging electric toothbrushes  
Shelly 1L for controlling the Fan (based on humidity level)  
Toon integration for reading shower/warm water status
#### filename
badkamer_room_card.yaml

## Kinderkamer Sophie Room Card
Room card for daughters room. Offcourse including princesses, controlls for the led-lighting (desk and unicorn), motion status, controlls for the airconditiong/heating, and temp/humidity/illumination status.  
![sophie_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/110e952c-5979-4731-8029-3b6d862b0966)
#### features
Temperature and Humidity graph in top of card, containing last 24 hours.  
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
#### filename
kinderkamer_sophie_room_card.yaml

## Kinderkamer Lucas Room Card
Room card for sons room. Offcourse including babyicons, controlls for the led-lighting (commode), motion status, controlls for the airconditiong/heating, and temp/humidity/illumination status.  
![lucas_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/c3ace65b-76e9-4c74-b12e-f5beb4321e57)
#### features
Temperature and Humidity graph in top of card, containing last 24 hours. 
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
#### filename
kinderkamer_lucas_room_card.yaml

## Woonkamer Room Card
![woonkamer_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/ccd2267c-a1d9-47f0-b373-a23409d9ea9d)

woonkamer_room_card.yaml

# Subview Energy (navigation from Top Button card)
## Current Devices status
Visualised with Mushroom Chips. Which devices are on and using power. Visualised with colored/animated icons. 
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/f095f9dd-80d9-4008-926f-d76976c91073)
#### filename
energy_current_devices_status_card.yaml

## Netto Electricity per day 
Visualised in Apexcharts. Import electricity from net - exported electricity to net  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/54edec09-d756-4430-a497-c117ce7f7e0c)
#### filename
energy_electricity_netto_card.yaml

## Electricity In per day, last week
Visualised in Apexcharts. Total Electricity import per day from last week  
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/54edec09-d756-4430-a497-c117ce7f7e0c)
#### filename
energy_electricity_in_card.yaml

## Electricity Out per day, last week
Visualised in Apexcharts.  Total Electricity export per day from last week 
![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/54edec09-d756-4430-a497-c117ce7f7e0c)
#### filename
energy_electricity_out_card.yaml

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


![image](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/2e8f5b40-0f4a-4fba-aef7-c57988b2761c)

