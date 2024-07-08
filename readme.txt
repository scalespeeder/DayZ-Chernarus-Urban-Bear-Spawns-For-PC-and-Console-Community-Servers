DayZ Bears Also Spawn In Chernarus Urban Areas XML Mod For Consoles & PC XML Snippets Instructions & Terms Of Use

These snippets add additional Chernarus urban spawns (villages, towns & citis) for the Bears. 

Limited Testing on PC Chernarus Local Server DAYZ Version 1.25 JULY 2024.

XML Snippets Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

WARNING! THESE BEARS CAN BE DIFFICULT TO KILL, SO THIS CAN MAKE SURVIVAL ON YOUR SERVER MUCHER HARDER!

Instructions:

THESE MODS DO NOT INCREASE THE FREQUENCY OF ANIMAL SPAWNS, SO ANIMALS WILL REMAIN RARE. 

TO INCREASE BEAR SPWN RATE, EDIT THE EVENT IN events.xml eg:

  <event name="AnimalBear">
        <nominal>0</nominal>
        <min>2</min>
        <max>2</max>
        <lifetime>180</lifetime>
        <restock>0</restock>
        <saferadius>200</saferadius><!--was 200-->
        <distanceradius>0</distanceradius>
        <cleanupradius>0</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>custom</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="1" min="1" type="Animal_UrsusArctos"/>
        </children>
    </event>
	
change to:

  <event name="AnimalBear">
        <nominal>0</nominal>
        <min>15</min><!--was 2-->
        <max>15</max><!--was 2-->
        <lifetime>180</lifetime>
        <restock>0</restock>
        <saferadius>200</saferadius>
        <distanceradius>0</distanceradius>
        <cleanupradius>0</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>custom</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="1" min="1" type="Animal_UrsusArctos"/>
        </children>
    </event>

 (Then save & re-upload as necessary)

These new spawn points are based on the locations of the water wells on Chernarus.

Simply upload the supplied territory files into your DayZ Chernarus Mission env directory (over the top of the existing ones) and restart your server.

OR

Use the supplied  "basic urban list of graze locations" file to add the coordinates to the bear territory files, save and restart your server.

PLEASE NOTE: To increase the chance of animal urban spawns you could also decrease the  <saferadius>200</saferadius> of
each relevant animal event to  <saferadius>100</saferadius> in the events.xml .

Thanks, Rob.