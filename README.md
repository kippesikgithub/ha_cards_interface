# Home Assistant Cards
Welcome to my github and some explanations about the interface and cards I build in Home Assistant. For every card i'll explain a bit about the contents and what features are in it. The room cards I use, are custom, but i re-use them throughout the whole interface, you can just place them in Grids or other cards to arrange them. The base for every room is the same card.  
The interface you see in the overview is our mobile dashboard, which is also usable for desktop. Every room has a Subview in where you can see all the detailed information or extended features for the entities in that room.  
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
# features
top_chips_card_current_overview.yaml  
chips icon and color changing based on value: Outside Temperature, Doors, Current power usage, Solar, Garbage Bin notification  
chips animated based on value: Solar   


#### Top Persons card  
Build with custom Mushroom chips and custom Mushroom person cards. Simple overview for persons and car, containing location status, status of ble transmitters on phone (for espresense thoughout the home, will be disbaled when you leave the house, enabled when entering the house), status of charging and battery. Double click on the Tesla to pre-heat the car, will show with blinking red when heating.
![person_cards](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/435e8671-1b7b-47e0-a1b5-02728fb614df)
  
chips icon and color changing based on value: ble transmitter, charging and battery percentage
top_persons_card.yaml


#### Top Button card
![top_button_navigation](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/f1ade95c-a77d-4a4b-b31f-af099f8c1018)

top_button_card.yaml


#### Top Chips Today card  
Build with custom Mushroom chips, card to show the today statistics, most important things. Shows todays energy total (import-export), todays total usage of gas and water and todays total produced sun-energy.  
![top_chips_today_overview](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/8da5b64d-24ae-4ee5-98d4-780b8c6922a5)  
  
top_chips_today_overview.yaml  
chips icon and color changing based on value: Total power usage, gas, water and solar    
chips animated based on value: Solar 

#### Trapkast Room Card
![trapkast_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/9de6b181-02ae-4656-8920-c9d77cc54fa2)
  
trapkast_room_card.yaml

#### Badkamer Room Card
![badkamer_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/637caac6-3d99-4ecf-80e3-45628e5833d1)

badkamer_room_card.yaml

#### Kinderkamer Sophie Room Card
![sophie_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/110e952c-5979-4731-8029-3b6d862b0966)

kinderkamer_sophie_room_card.yaml

#### Kinderkamer Lucas Room Card
![lucas_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/c3ace65b-76e9-4c74-b12e-f5beb4321e57)

kinderkamer_lucas_room_card.yaml

#### Woonkamer Room Card
![woonkamer_room_card](https://github.com/kippesikgithub/ha_cards_interface/assets/100353268/ccd2267c-a1d9-47f0-b373-a23409d9ea9d)

woonkamer_room_card.yaml

