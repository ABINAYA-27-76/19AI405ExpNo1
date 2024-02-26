<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Abinaya A</h3>
<h3>Register Number:212223040005</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>VacuumCleanerAgent:</h3>
<p>Such this agent description for vacuum cleaner agent (to clener rooms) which we consider here as dirtyy, by the user cleaner, and another by cleaning tha rooms . This agent has to consider two factors one is room location and an dirty in a random rooms, the agent has to move from one place to another to check whelther there is any kind of dirty. The performance of the agent is calculated by performance of the vacuum cleaner and each time not to clean the rooms again and again .It has to check another room so that the movement causes the agent to reduce its performance. Hence, agents perrform for clean the rooms easily.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>VacuumCleaner agent</strong></td>
    <td><strong>dirty, suck</strong></td>
     <td><strong>Right, left</strong></td>
    <td><strong>suck, no_action</strong></td>
    <td><strong>Rooms, Dirty</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>dirty of the room, sucks the dirty.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>to clean the room in kind manner.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Dirty in each room. And check for the dirty and suck or mno action</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each cleaning inside the room, for each movement of dirty in rooms</p>
<h3>STEP 6:</h3>
# CODE:

class VacuumCleanerAgent:
    def __init__(self):
        # Initialize the agent's state (location and dirt status)
        self.location = "A"  # Initial location (can be "A" or "B")
        self.dirt_status = {"A": False, "B": False}  # Initial dirt status (False means no dirt)

    def move_left(self):
        # Move the agent to the left if possible
        if self.location == "B":
            self.location = "A"

    def move_right(self):
        # Move the agent to the right if possible
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self):
        # Suck dirt in the current location if there is dirt
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")

    def do_nothing(self):
        # Do nothing
        pass

    def perform_action(self, action):
        # Perform the specified action
        if action == "left":
            self.move_left()
        elif action == "right":
            self.move_right()
        elif action == "suck":
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):
        # Print the current status of the agent
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")

# Example usage:
agent = VacuumCleanerAgent()

# Move the agent, suck dirt, and do nothing

agent.perform_action("left")
agent.print_status()
agent.perform_action("suck")
agent.print_status()
agent.perform_action("nothing")
agent.print_status()

# OUTPUTS:
![funAI](https://github.com/23002776/19AI405ExpNo1/assets/145742657/c5169936-e586-4ff5-a28d-92a5feacee9c)


# result
The cleaning agent as vacuum cleaner as cleaned the without any kind of inside the rooms.

