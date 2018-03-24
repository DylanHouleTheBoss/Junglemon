# Junglemon
Junglemon is a project made by people just starting out.
from time import sleep
import random
CPU = 500
USER = 500
poison = 0
CPUpoison = 0
print('Hello, new challenger, what is your name?')
junglemons = ["charring","froggitir","treehoot"]
name = input(">")
print(f"Welcome to my jungle, {name}, I'm trainer Anserh")
sleep(1)
print("Choose your junglemon")
print("charring: fire type. abilitys: flamethrower, lava spout, blaze, erupt \n froggitir: water type, abilitys: bubble, water gun, splash \n treehoot: plant type, abilitys: leaf blade, vine whip,  venom bite")
user_choice = input(">")
if user_choice not in ['froggitir', 'charring', 'treehoot']:
  print('thats not one silly')
  user_choice = junglemons[random.randint(0,2)]
CPUa = random.randint(0,2)
print("I chose " + junglemons[CPUa] )
sleep(1)
print(f"LET THE BATTLE BEGIN!\n {user_choice} vs " + junglemons[CPUa])
while True:
  print("It is your turn")
  sleep(1)
  chance = random.randint(1, 5)
  if user_choice == 'froggitir':
    print("bubble\n water gun\n splash")
    choice = input(">")
    if chance == 4:
      print("Your junglemon refuses")
    else:  
      if 'bubble' in choice:
        print("FROGGITIR, USE BUBBLE!")
        CPU -= random.randint(60, 65)
      if 'water gun' in choice:  
        print("FROGGITIR, USE WATER GUN")
        CPU -= random.randint(70, 90)
      if 'splash' in choice:
        print("FROGGITIR, SPASH!")
        CPU -= random.randint(50, 90)
  if user_choice == 'charring':
    print("Flamethrower\n Lava spout \n Blaze \n Erupt")
    choice = input(">")
    if chance == 4:
      print("Your junglemon refuses")
    else:  
      if 'flamethrower' in choice:
        print("CHARRING, USE FLAMETHROWER!")
        CPU -= random.randint(80, 90)
      if 'lava spout' in choice:  
        print("CHARRING, USE LAVA SPOUT")
        CPU -= random.randint(50, 90)
      if 'blaze' in choice:
        print("CHARRING, BLAZE IT UP!")
        CPU -= random.randint(50, 75)  
      if 'erupt' in choice:
        print('CHARRING, ERUPT')
        CPU -= random.randint(20, 100)
  if user_choice == 'treehoot':
    print("Leaf blade\n Vine whip \n Venom bite")
    choice = input(">")
    if chance == 4:
      print("Your junglemon refuses")
    else:  
      if 'leaf blade' in choice:
        print("TREEHOOT, USE LEAF BLADE!")
        CPU -= random.randint(50, 85)
      if 'vine whip' in choice:  
        print("TREEHOOT, USE VINE WHIP")
        CPU -= random.randint(60, 90)
      if 'venom bite' in choice:
        print("TREEHOOT, VENOM BITE!")
        CPU -= 40
        CPUpoison += 2
  if poison > 0:
    print('You took poison damage')
    poison -= 1
    USER -= 10
  print(f"Anserh's junglemon is at {CPU} hp!")
  if USER < 1:
    print("LOL, U DIED")
    exit()
  if CPU < 1:
    print("LOL, Anserh's JUNGLMON DIED")  
    exit()
  sleep(3)
  CPUchoice = random.randint(1, 4)
  if CPUa == 1:
    if CPUchoice == 1:
      print("FROGGITIR, USE BUBBLE")
      USER -= random.randint(80, 90)
    if CPUchoice == 2:
      print("FROGGITIR, USE WATER GUN")
      USER -= random.randint(70, 90)      
    if CPUchoice == 3:
      print("FROGGITIR, SPLASH")
      USER -= random.randint(50, 80)  
    if CPUchoice == 4:
      print("Ha! Anserh's junglemon missed!")
  if CPUa == 2:
    if CPUchoice == 1:
      print("TREEHOOT, USE LEAF BLADE")
      USER -= random.randint(50, 90)
    if CPUchoice == 2:
      print("TREEHOOT, USE VINE WHIP")
      USER -= random.randint(60, 85)      
    if CPUchoice == 3:
      print("TREEHOOT, BITE WITH YOUR VENOM TEETH")
      USER -= 40
    if CPUchoice == 4:
      print("Ha! Anserh's junglemon missed!")      
  if CPUpoison > 1:
    print("Anserh's junglemon took poison damage")
    CPUpoison -= 1
    CPU -= 10
  print(f"Your junglemon is at {USER} hp")  
  if USER < 1:
    print("LOL, U DIED")
    exit()
  if CPU < 1:
    print("LOL, Anserh's JUNGLMON DIED")
    exit()
