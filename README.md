# INTRO TO INHERITANCE
## The first version

The program defines a class *Computer* and its two suclasses: *Server* and *Graphicssystem*

using System;
using System.Collections.Generic;

namespace OOP_in_Csharp
{
    //--------------------------------
    public class Computer
	{
		public Computer (string ip, string make, string osystem, bool switched)
		{
			this.Ipaddress = ip;
			this.Make = make;
			this.OperatingSystem = osystem;
			this.SwitchedOn = switched;

			compCounter++;
		}

		public Computer ()
		{
			compCounter++;
		}

		// private member variables
		private string _ipadress;
		private bool _switchedOn;
		private string _make;
		private string _operatingSystem;

		private static int compCounter = 0; //counts comps in the network
		private static int switchedCounter = 0; //counts comps that are switched

		public static int CountComps ()
		{
			return compCounter;
		}

		public static int CountSwitched ()
		{
			return switchedCounter;
		}

		public void StartComputer() 
		{
			this.SwitchedOn = true; 
			switchedCounter++;
			Console.WriteLine("The comp {0} is starting ...", this.Ipaddress);
		}
````
