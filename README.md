# vice-metro-game
Vice metro text-based game in Bash script 
```
#!/bin/bash
echo "Welcome to Vice Metro!"
echo "You are Carl 'CJ' Johnson, a criminal mastermind."
PLAYER_HEALTH=100
PLAYER_MONEY=500
PLAYER_LOCATION="Little Havana"
while true; do
  clear
  echo "Vice Metro Game"
  echo "----------------"
  echo "Player Status:"
  echo "Health: $PLAYER_HEALTH"
  echo "Money: $PLAYER_MONEY"
  echo "Location: $PLAYER_LOCATION"
  echo "----------------"
  echo "Choose Action:"
  echo "1. Explore City"
  echo "2. Start Mission"
  echo "3. Buy Weapons"
  echo "4. Visit Hospital"
  echo "5. Exit Game"
  read -p "Enter choice: " CHOICE
  case $CHOICE in
    1) PLAYER_LOCATION="Random Location"; echo "You explored the city!"; sleep 2;;
    2) 
      echo "Mission Briefing:"
      echo "Meet Tommy Vercetti at the Malibu Club."
      read -p "Accept mission? (y/n): " MISSION_CHOICE
      if [ $MISSION_CHOICE = "y" ]; then
        PLAYER_MONEY=$((PLAYER_MONEY+1000))
        echo "Mission completed! Earned $1000."
      fi
      ;;
    3) echo "Weapon Shop Menu:"; echo "1. Pistol ($500)"; echo "2. Shotgun ($1000)";;
    4) PLAYER_HEALTH=100; echo "You visited the hospital. Health restored!";;
    5) exit;;
  esac
done
```
