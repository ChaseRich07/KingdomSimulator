import time
import random
from random import shuffle
print('Welcome')
time.sleep(1)
print("")
name = input("Enter your name: ")
print("")
kingdom_name = input("What would you like to name your kingdom?: ")
print("")
print("GENERATING KINGDOM")
time.sleep(1)
print("")

#GLOBAL VARIABLES
return_merchant = 0
global productivity
productivity = 0
global riches
riches = 1000
global day_tracker
day_tracker = 0
global pop_amount
pop_amount = random.randint(100, 250)
global research
research = 0
global mindeath
mindeath = 20
global maxdeath
maxdeath = 60
global infected
infected = random.randint(30,60)

plague_wlist = ["rats", "water", "infected citizens"]
land_list = ["Tundra","Grassland","Swamp",]
pop_list =["Farmer", "Guard", "Builder"]

#GENERATES THE KINGDOM

class Kingdom():
    
    def __init__(self, land, people):
        self.land = land
        self.people = people
        self.final_land = []
        self.final_pop = []
        self.generate_land()
        self.final_att = []
        
    def generate_land(self):
        for num in range(2):
            create_land = random.choice(land_list)
            self.final_land.append(create_land)
            create_pop = random.choice(pop_list)
            self.final_pop.append(create_pop)
        
        if "Tundra" in self.final_land:
            landad1 = "frigid"
        else:
            landad1 = "grassy"
        
        if "Swamp" in self.final_land:
            landad2 = "muddy"
        else:
            landad2 = "grassy"
            
        if landad1 == landad2:
            landad1 = "dark"
            
        
        print(f"""Hello, King {name}. Welcome to {kingdom_name}. A {landad1}, {landad2}
kingdom of {pop_amount} lowly peasants, where a terrible plague runs rampant. Will you rule with an iron fist? 
Or perhaps be the kindly ruler who takes pity on the weak? {kingdom_name}'s success is up to you...""")
        time.sleep(3)
        print("")
        
    def generate_pop():
        farmer = 3
        guard = 2
        builder = 1
    
Kingdom(kingdom_name, pop_amount)
day_tracker = 0
#CREATES NEW DAY AND NEW DAY'S EVENTS



def new_day():
    global day_tracker
    global productivity
    
    daily_riches()
    
    print(f"Your riches are at {riches}")
    print("")
    resist_list= ["washing their hands", "hiding in their homes", "praying to their Gods"]
    plague_wlist = ["rats", "water", "infected citizens"]
    spread = random.choice(plague_wlist)
    resist = random.choice(resist_list)
    plague_worse = (f"Gods have mercy! The plague has further spread through the {spread}! Citizen productivity is now at {productivity - 1}...")
    plague_better = (f"Hoorah! The plague has taken a hit as citizens have begun {resist}! Citizen productivity is now at {productivity + 1}...")
    no_event = (f"A blessedly uneventful day. Citizen productivity is at {productivity}" )
    
    
    plague_num = [0,0,0,1,2]
    plague_event = random.choice(plague_num)
    if plague_event == 0:
        day_plague = no_event
    elif plague_event == 1:
        productivity = productivity + 1
        day_plague = plague_better
    else:
        productivity = productivity - 1
        day_plague = plague_worse
        
    ##################################################################
    
    if day_plague == no_event:
        print("DAY" , day_tracker + 1)
        time.sleep(2)
        day_tracker = day_tracker + 1
        game_enders()
        mornings()
        random_events()
        time.sleep(2)
        print(no_event)
        response_neutral()
    elif day_plague == plague_better:
        print("DAY" , day_tracker + 1)
        time.sleep(2)
        day_tracker = day_tracker + 1
        game_enders()
        mornings()
        random_events()
        time.sleep(2)
        print(plague_better)
        response_resist()
    else:
        print("DAY" , day_tracker + 1)
        time.sleep(2)
        day_tracker = day_tracker + 1
        game_enders()
        mornings()
        random_events()
        time.sleep(2)
        print(plague_worse)
        response_spread()
        
        
        
#HERE IS WHERE THE PLAYER RESPONDS TO THE DAY'S EVENTS
def response_spread():
    global pop_amount
    global research
    global mindeath
    global maxdeath
    global riches
    global productivity
    global return_merchant
    time.sleep(4)
    print("What are you going to do?: ")
    if return_merchant == 0 :
        print("1:Slaughter the infected | 2:Study the disease(-100 Riches) | 3:Study plague cure(-150 Riches) | 4:Nothing")
        action_spread = input("")
        
        print("")
        if action_spread == "1":
            pop_killed = random.randint(mindeath,maxdeath)
            pop_amount = pop_amount - pop_killed
            productivity = productivity + 1
            print(f"You have betrayed some for the good of all. {kingdom_name}'s total population is now {pop_amount}")
            time.sleep(3)
            print("+1 Productivity")
            time.sleep(2)
            print("")
    
        elif action_spread == "2":
            riches = riches - 100
            maxdeath = maxdeath - 5
            if maxdeath <= 0:
                print("Due to your noble efforts, no more citizens are dying! ...from the plague at least...")
                print("")
            else:
                print("Maximum infections per day has been lowered!")
            time.sleep(2)
            print("")
        
        elif action_spread == "3":
            riches = riches - 150
            mindeath = mindeath - 4
            print("Potential for curing the afflicted has been raised!")
            time.sleep(2)
            print("")
        
        else:
            print("Sometimes it is wise to let fate decide...")
            time.sleep(2)
            print("")
            
        game_enders()
        new_day()
        #################################WITH MERCHANT####################
    elif return_merchant == 3:
        print("1:Slaughter the infected | 2:Study the disease(-100 Riches) | 3:Study plague cure(-150 Riches) | 4:Send the Merchant(-200 Riches) | 5:Nothing")
        action_spread = input("")
        print("")
        if action_spread == "1":
            pop_killed = random.randint(mindeath,maxdeath)
            pop_amount = pop_amount - pop_killed
            productivity = productivity + 1
            print(f"You have betrayed some for the good of all. {kingdom_name}'s total population is now {pop_amount}")
            time.sleep(3)
            print("+1 Productivity")
            time.sleep(2)
            print("")
    
        elif action_spread == "2":
            riches = riches - 100
            maxdeath = maxdeath - 5
            if maxdeath <= 0:
                print("Due to your noble efforts, no more citizens are dying! ...from the plague at least...")
                print("")
            else:
                print("Maximum infections per day has been lowered!")
            time.sleep(2)
            print("")
        
        elif action_spread == "3":
            riches = riches - 150
            mindeath = mindeath - 4
            print("Potential for curing the afflicted has been raised!")
            time.sleep(2)
            
        elif action_spread =="4":
            return_merchant = 0
            print("The merchant has been sent off in search of trades...")
        
        else:
            print("Sometimes it is wise to let fate decide...")
            time.sleep(2)
        
        game_enders()
        new_day()
    
    
################################################################################
def response_resist():
    global riches
    global pop_amount
    global research
    global mindeath
    global maxdeath
    time.sleep(4)
    recruit_tactic_list = ["Through needless violence","By promising glory", "Thanks to a population boom"]
    recruit_tactic = random.choice(recruit_tactic_list)
    print("What are you going to do?: ")
    print("1:Recruit more citizens | 2:Study plague prevention(-100 Riches) | 3:Study plague cure(-150 Riches) | 4:Nothing")
    action_resist = input("")
    
    if action_resist == "1":
        pop_growth = random.randint(5,20)
        pop_amount = pop_amount + pop_growth
        print(f"{recruit_tactic}, {kingdom_name}'s population has grown by {pop_growth}!")
        print(f"Total population is now at {pop_amount}")
        time.sleep(3)
        print("")
        
    elif action_resist == "2":
        riches = riches - 100
        maxdeath = maxdeath - 5
        print("Maximum infections per day has been lowered!")
        time.sleep(2)
        
    elif action_resist =="3":
        riches = riches -150
        mindeath = mindeath -4
        print("Potential for curing the afflicted has been raised!")
        time.sleep(2)
        
    else:
        print("Sometimes it is wise to let fate decide...")
        time.sleep(2)
    
    game_enders()    
    new_day()
    
def response_neutral():
    #FUNCTION GLOBALS
    global riches
    global productivity
    global pop_amount
    global research
    global mindeath
    global maxdeath
    time.sleep(2)
    
    print("What are you going to do?: ")
    print("1:Slaughter the infected | 2:Study plague prevention(-100 Riches) | 3:Study plague cure(-150 Riches) | 4:Nothing")
    action_neutral = input("")
    
    #NEUTRAL CHOICE CONSEQUENCES
    
    if action_neutral =="1":
        pop_killed = random.randint(mindeath,maxdeath)
        pop_amount = pop_amount - pop_killed
        productivity = productivity + 1
        print(f"You have betrayed some for the good of all. {kingdom_name}'s total population is now {pop_amount}")
        time.sleep(3)
        print("+1 Productivity")
        print("")
    
    elif action_neutral == "2":
        riches = riches - 100
        maxdeath = maxdeath - 5
        print("Maximum infections per day has been lowered!")
        time.sleep(2)
    
    elif action_neutral == "3":
        riches = riches -150
        mindeath = mindeath -4
        print("Potential for curing the afflicted has been raised!")
        time.sleep(2)
        
    else:
        print("Sometimes it is wise to let fate decide...")
        time.sleep(2)
        
    game_enders()        
    new_day()
    
def game_enders():
    global productivity
    global riches
    global day_tracker
    global pop_amount
    if productivity <= -10:
        print("DEATH BY PLAGUE")
        print(f"You failed on day {day_tracker} ")
        quit()
    if productivity >= 10:
        print("YOU HAVE BECOME A GOD AMONGST MEN")
        print(f"You achieved total victory over all on {day_tracker}")
        quit()
        
    if riches <= 0:
        print("DEATH BY FAMINE")
        print(f"You failed on day {day_tracker} ")
        quit()
    if riches >= 5000:
        print("YOU HAVE BECOME A GOD AMONST MEN")
        print(f"You achieved total victory over all on {day_tracker}")
        quit()
        
    if pop_amount <= 0:
        print("YOU ARE RULER OVER NOTHING")
        print(f"You failed on day {day_tracker}")
        quit()
    if pop_amount >= 1000:
        print("YOU HAVE BECOME A GOD AMONGST MEN")
        print(f"You achieved total victory over all on {day_tracker}")
        quit()
    
def daily_riches():
    global productivity
    global pop_amount
    global riches
    
    #NEUTRAL PRODUCTIVITY RICHES FLOW
    if productivity == 0:
        print("Citizens are just barely making end's meet. No more riches today.")
        time.sleep(2)
        
    #NEGATIVE PRODUCTIVITY RICHES FLOW
    elif productivity < 0 and productivity > -6:
        print("Your citizens are suffering! Purchase resources for 50 Riches or watch them Perish!")
        print("1: Provide Riches for the poor | 2: Greed...")
        save_them = input("")
        if save_them == "1":
            riches = riches - 50
            print("You are noble... for today...")
        elif save_them == "2":
            pop_loss = random.randint(3,8)
            pop_amount = pop_amount - pop_loss
            print(f"You did what you had to do, but {pop_loss} citizens have perished...")
            time.sleep(2)
        else:
            print("invalid selection")
            daily_riches()
    
    elif productivity >= -6 and productivity < -9:
        print("Your citizens are suffering massively! Purchase resources for 100 Riches or watch them Perish!")
        print("1: Provide Riches for the poor | 2: Greed...")
        save_them = input("")
        if save_them == "1":
            riches = riches - 100
            print("You are noble... for today...")
            time.sleep(2)
        elif save_them == "2":
            pop_loss = random.randint(6,16)
            pop_amount = pop_amount - pop_loss
            print(f"You did what you had to do, but {pop_loss} citizens have perished...")
            time.sleep(2)
        else:
            print("invalid selection")
            time.sleep(2)
            daily_riches()
            
    #POSITIVE PRODUCTIVITY RICHES FLOW
    elif productivity > 0 and productivity <= 5:
        production_list = ["Agricultural breakthroughs", "An industrial revolution", "A blessing from the Gods","a population boom","the grit of the men","unrivaled nationalism"]
        rand_production = random.choice(production_list)
        riches_gain = random.randrange(50,100,50)
        riches = riches + riches_gain
        print("Your citizens are thriving! You are rewarded by their amazing productivity!")
        time.sleep(2)
        print("")
        print(f"Thanks to {rand_production}, your Riches have increased by {riches_gain}! ")
        time.sleep(2)
        print("")
    
    elif productivity >= 9 and productivity > 5:
        production_list = ["agricultural breakthroughs", "an industrial revolution", "a blessing from the Gods","a population boom","the grit of the men","unrivaled nationalism"]
        rand_production = random.choice(production_list)
        riches_gain = random.randrange(50,150,50)
        riches = riches + riches_gain
        print("Your citizens are thriving spectacularly! You are rewarded by their fantastic productivity!")
        time.sleep(2)
        print(f"Thanks to {rand_production}, your Riches have increased by {riches_gain}! ")
        time.sleep(2)
        
def random_events():
    global return_merchant        
    global riches
    global productivity
    global pop_amount
    global research
    global mindeath
    global maxdeath
    global day_tracker
    global randeventlist
    global tempevent
    randeventlist = [1,2,3,4,5,6,7,8,9,10,11]
    tempevent = random.choice(randeventlist)
    
    if tempevent == 1:
        print("")
        print("Gods have mercy, the plague has evolved... ...those are not human...")
        for num in range(2):
            if new_day():
                pop_amount = pop_amount - 20
                time.sleep(2)
                print("They are eating eachother!")
                print("")
                time.sleep(2)
                print("-20 citizens.")
    
    elif tempevent == 2:
        print("")
        print("Another kingdom requests an alliance. Do you accept?")
        print("1:Accept offer | 2:Reject offer")
        acceptoff = input("")
        if acceptoff == '1':
            pop_amount = pop_amount + 100
            kingdomnames = ["Thalin","Grorpta","Kligdot","Smead","Tungselot","Waltawite","Beak","Pewter"]
            ally_kingdom = random.choice(kingdomnames)
            print(f"The kingdom of {ally_kingdom} joins your ranks! Put its citizens to good use...")
            print(f"Total population is now {pop_amount}.")
        else:
            print("You can't trust anyone in these lands...")
    
    ############################MERCHANT###################################        
    elif tempevent == 3:
        print("")
        print("A lone merchant in a shredded white coat wanders to the castle...")
        time.sleep(3)
        print("")
        return_merchant = randeventlist.pop(2)
        print("The option to trade has now been unlocked!")
        
    elif tempevent == 4:
        print("")
        print("The miners in the mountains have struck gold!")
        print("")
        time.sleep(2)
        riches = riches + 300
        print("+300 Riches")
    
    elif tempevent == 5:
        print("")
        print("No... NO! This can't be happening!!!")
    else:
        print("")
        
def mornings():
    morning_list = ["The dim sun peaks above the freezing mountains", "The icicles are beginning to form...",
    "The cattle are loud this morning. The infection is getting to them...", "The orange sky is undeniably beautiful today.",
    "Another day closer to death... or, perhaps, redemption?", "The aroma of baked goods flood the kingdom this morning",
    "The sun didn't rise today, but the moon is still a sight to behold.", "You awake feeling a sense of vigor!",
    "dont give up hope, sir"]
    temp_morning = random.choice(morning_list)
    
    randnumchoice = random.randint(0,10)
    if randnumchoice % 2 == 0:
        print("")
        print(temp_morning)
        time.sleep(4)
        print("")
    else:
        print("")
    
begin = input("Shall we begin? 'Y' or 'N': ")
begin = begin.upper()
if begin == 'Y':
    new_day()
else:
    print("bye")
