# Arma-3-TDM By Blaq G-Sus


Servers:

Extract .rar file and add the pbo files to your "mpmissions" folder on your server. 
Open the "AddToConfig" text file and copy the text to your serverconfig.

Local:

Extract .rar file and add the pbo files to your "mpmissions" folder in Documents -> Arma3 -> mpmissions.
Open the Arma 3 editor, open the mission you want to play and select "Play in multiplayer".



///////////////////////////
Server.cfg template for TDM 
///////////////////////////

//
// server.cfg
//
// STEAM
steamport=2312;
steamqueryport=2303;

// GLOBAL SETTINGS
hostname= "Team Deathmatch - Hardcore - PvE/PvP ";

password = "";						// Password for joining, eg connecting to the server
passwordAdmin = "AddAdminPassword";					// Password to become server admin. When you're in Arma MP and connected to the server, type '#login xyz'
reportingIP = "master.gamespy.com";
logFile = "server_console.log";				// Tells ArmA-server where the logfile should go and what it should be called
allowedFilePatching = 2;

motd[] = {"TDM by Blaq G-Sus"};
motdInterval = 5;					// Time interval (in seconds) between each message


// JOINING RULES
checkfiles[] = {};					// Outdated.
maxPlayers     = 15;					// Maximum amount of players. Civilians and watchers, beholder, bystanders and so on also count as player.
kickDuplicate = 0;					// Each ArmA version has its own ID. If kickDuplicate is set to 1, a player will be kicked when he joins a server where another player with the same ID is playing.
verifySignatures = 2;					// Verifies .pbos against .bisign files. Valid values 0 (disabled), 1 (prefer v2 sigs but accept v1 too) and 2 (only v2 sigs are allowed). 
equalModRequired = 0;					// Outdated. If set to 1, player has to use exactly the same -mod= startup parameter as the server.


// VOTING
autoSelectMission = true;
voteMissionPlayers = 0;					// Tells the server how many people must connect so that it displays the mission selection screen.
voteThreshold = 0.33;					// 33% or more players need to vote for something, for example an admin or a new map, to become effective
allowedVoteCmds[] = {};
randomMissionOrder = true;
// INGAME SETTINGS
disableVoN = 0;						// If set to 1, Voice over Net will not be available
vonCodecQuality = 10;					// since 1.62.95417 supports range 1-20 //since 1.63.x will supports range 1-30 //8kHz is 0-10, 16kHz is 11-20, 32kHz is 21-30
persistent = 0;						// If 1, missions still run on even after the last player disconnected.
timeStampFormat = "short";				// Set the timestamp format used on each report line in server-side RPT file. Possible values are "none" (default),"short","full".
BattlEye = 0;                                           // Server to use BattlEye system


// SCRIPTING ISSUES
onUserConnected = "";					//
onUserDisconnected = "";				//
doubleIdDetected = "";					//
//regularCheck = "{}";                                  //  Server checks files from time to time by hashing them and comparing the hash to the hash values of the clients. Causes heavy I/O, uncomment to disable feature - READ WARNING ABOVE - makes cheating possible!


// SIGNATURE VERIFICATION
onUnsignedData = "kick (_this select 0)";		// unsigned data detected
onHackedData = "ban (_this select 0)";			// tampering of the signature detected
onDifferentData = "";					// data with a valid signature, but different version than the one present on server detected



class Missions
{
	class TestMission01
	{
		template = AGM.stratis;
		difficulty = "custom";
		class Params {};
	};
	class TestMission02
	{
		template = Airbase.stratis;
		difficulty = "custom";
		class Params {};
	};
	class TestMission03
	{
		template = Arudy.malden;
		difficulty = "custom";
		class Params {};
	};
	class TestMission04
	{
		template = CampMaxwell.stratis;
		difficulty = "custom";
		class Params {};
	};	
		class TestMission05
	{
		template = SainteMarie.Malden;
		difficulty = "custom";
		class Params {};
	};
	class TestMission06
	{
		template = Lolisse.Malden;
		difficulty = "custom";
		class Params {};
	};
	
	class TestMission07
	{
		template = Leroy.Malden;
		difficulty = "custom";
		class Params {};
	};

	class TestMission08
	{
		template = Girna.Stratis;
		difficulty = "custom";
		class Params {};
	};

	class TestMission09
	{
		template = LaPessagne.malden;
		difficulty = "custom";
		class Params {};
	};
	class TestMission10
	{
		template = LaRiviere.malden;
		difficulty = "custom";
		class Params {};
	};

//	class TestMission11
//	{
//		template = Linjhaven.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission12
//	{
//		template = Tanouka.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission13
//	{
//		template = Tavu.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission14
//	{
//		template = Dock.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission15
//	{
//		template = Harcourt.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission16
//	{
//		template = IslandBoys.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};
//	class TestMission17
//	{
//		template = Jungle.Tanoa;
//		difficulty = "custom";
//		class Params {};
//	};

};


// FYI The missions that are disabled with "//" is part of the Apex pack and should be disabled if you don't own Apex.
