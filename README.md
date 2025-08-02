# EECE 5554 LAB 0: Getting familiar with Linux, Git, and ROS
Welcome to Robotics Sensing and Navigation! 
These GitHub repositories will serve as the primary place for lab assignment handouts, although we may also post some materials on Piazza.

At the start of each lab, you should clone each repository to get the files. 
You can also read the instructions here. 

## After completing this lab, a well-prepared student should be able to: 
       <li> Use basic functions of Ubuntu from the command line (make directories and files) </li>
        <li> Push files to a Git repository </li>
        <li> Modify ROS nodes in Python </li>
   
  ## ROS Basics you will learn about in this assignment
     <li> The ROS core systems: Packaging, Buildsystems, Messaging, CLI and GUI tools, creating packages, nodes, topics, services, and parameters. </li>
   <li> Writing a Simple Publisher and Subscriber (Python)</li> 
    <li> Examining the Simple Publisher and Subscriber </li>
   <li> Writing a Simple Service and Client (Python) </li>
    <li> Examining the Simple Service and Client </li>
  
  ### Collaboration statement: 
    You should complete this assignment without collaboration with other students in the course or elsewhere. Please ask for help from the TAs or course instructors if you are getting stuck!
    ### Step 1: Install Ubuntu 24.04 LTS ("Noble Numbat") on your laptop. Please make sure you install this version of Linux.
    You can dual-boot, use a Docker container, or use virtualization software (Oracle Virtualbox, UTM, VMWare Fusion, Parallels). Please make sure that your USB port and network connection are working. VM instructions are at the end of this document. If you are making changes to your machine, it would be a good idea to back up your entire hard drive beforehand! 
    
    ### Step 2: Set up your GitHub account
    <li>If you need a refresher or have not used Git before, do “good for beginners” starred tutorials on GitHub. https://docs.github.com/en/get-started/quickstart/hello-world   </li>
    <li> Once you are comfortable with basic Git use through the command line/terminal, open an account on GitHub using your Northeastern email ([name]@northeastern.edu) email (please!). Make sure you are signing up for a free account. </li>   
    <li>Make your username the same as your Northeastern username if possible, and if not, make it a few more letters. Example: dorsey-k (if available) or dorsey-kri  </li>
    <li>If your Github username differs from your Northeastern username, please post it to the Piazza thread.  </li>
    
    ### NOTICE! It is essential that you: 
    <li> Use your Northeastern email for your GitHub account </li>
    <li> Match spelling and capitalization (case) of subfolders with the instructions.  </li>
    <li> Set your repository to private</li>
    We cannot grade your assignments without these, which means you will not receive credit for your hard work!  
    
    ### Step 3: Set up your GitHub repository
    <li>On GitHub, create a repository called EECE5554 (Repository must be kept PRIVATE) </li>
    <li>On GitHub, make a subdirectory under EECE5554 called lab0  </li>
    <li>Install Git on your machine: https://GitHub.com/git-guides/install-git </li>
    <li>Under the lab0 subdirectory, use the command line interface to check in a text file named [yourNortheasternunsername.txt] that states that you have 1) a complete Ubuntu install or your plans to resolve any issues ASAP, and 2) you are ready to use Git and GitHub </li>
    If you can’t yet install Ubuntu, you can use the web interface to check this file in.  
    
    ### Step 4: Read about ROS
    <li> ROS Introduction https://wiki.ros.org/ROS/Introduction </li>
    <li> ROS Get Started Guide: Introduction, Concepts, Higher-Level Concepts, Client Libraries, Technical Overview https://wiki.ros.org/ROS/StartGuide </li>
    <li> ROS developer's guide https://wiki.ros.org/DevelopersGuide </li>
    <li> ROS Python Style Guide https://wiki.ros.org/PyStyleGuide </li>
    Useful Documentation on command line tools: https://wiki.ros.org/ROS/CommandLineTools 

    <li> rosnode </li>
    <li> rostopic </li>
 <li> rosparam </li>
  <li> rosmsg  </li>
    ### Step 5: Install ROS in Ubuntu  
    
    "Instructions are here: https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html. Make sure to install desktop and not bare
    "\n",
    "### Step 6: Complete the following tutorials\n",
    "(* indicates a component of the assignment turn in) \n",
    "**NOTE:**  we will exclusively use Ubuntu 22.04 LTS and the ROS 2 Humble Release \n",
    "Link to the first tutorial here: https://docs.ros.org/en/humble/Tutorials.html\n",
    "\n",
    "<ul> \n",
    "    <li> Configuring environment </li>\n",
    "    <li> Using turtlesim, ros2, and rqt </li>\n",
    "    <li> Understanding nodes </li>\n",
    "    <li> Understanding topics* </li>\n",
    "    <li> Understanding services </li>\n",
    "    <li> Using rqt_console to view logs </li>\n",
    "    <li> Creating a workspace (under client libraries) </li>\n",
    "    <li> Creating a package (under client libraries) </li>\n",
    "    <li> Writing a simple publisher and subscriber (Python)* </li>\n",
    "    <li> Creating custom msg and srv files </li>\n",
    "</ul>\n",
    "\n",
    "### What to submit for Lab 0:\n",
    "\n",
    "1. Post your username, if it differs from your Northeastern username, to the Piazza thread.\n",
    "\n",
    "2. Invite course staff to be developers on your GitHub using email ECERSN@Northeastern.edu \n",
    "\n",
    "3. Checked in .txt file to Github\n",
    "\n",
    "4. Understanding ROS Topics: submit a screenshot of your turtlesim window with the turtle having drawn a small doodle (your first initial, a star, etc.) You can use the keyboard to make this drawing, it does not need to be coded. Please name this LASTNAME_turtle.png \n",
    "\n",
    "5. Writing a Simple Publisher and Subscriber: Starting with the talker/listener example, write and test a publisher node that publishes a message containing a string (anything but hello world) to the topic chatter and a subscriber node that subscribes to the topic chatter with the callback “I heard” + the string message, where the string message is slightly modified in some way (two letters flipped, append a character to the string, etc. You will not receive full credit if the string is not modified). \n",
    "\n",
    "### Submission structure\n",
    "\n",
    "Your GitHub repository should be accessible through https: //github.com/ your username/ EECE5554 \n",
    "\n",
    "Your GitHub repository should look like this structure when cloned locally: EECE5554/lab0/src/other files\n",
    "\n",
    "|EECE5554| | | |\n",
    "|:------|:------|:------|:------|\n",
    "|     |lab0     |     |     |\n",
    "|     |     |Northeasternusername.txt     |     |\n",
    "|     |     |LASTNAME_turtle.png      |     |\n",
    "|     |     |src/     |     |\n",
    "|     |     |     | talker.py (which you have modified)    |\n",
    "|     |     |     | listener.py (which you have modified)     |\n",
    "\n",
    "You should attempt to use the command line to push to your GitHub repo. Please ask for help if you are unsure. If there are errors in your lab0 structure on GitHub, you may fix and resubmit for this assignment for full credit. However, for future assignments, you will need to use the command line, so we recommend you get used to it now!\n",
    "\n",
    "Please note: You should not push your build or devel directories to Git \n",
    "\n",
    "If you are having trouble with the Ubuntu install, you can use one of the course VMs, but you will not receive credit for this step.\n",
    "\n",
    "\n",
    "### Assessment \n",
    "\n",
    "<ul>\n",
    "    <li> Made GitHub account with your NU email, posted to Piazza thread if your GitHub username is not the same as your Northeastern username, and invited ECERSN@Northeastern.edu to be a developer (10 pts) </li> \n",
    "    <li> Correct GitHub repository structure (EECE5554/lab0/[Northeasternusername.txt]) (10 pts)  </li>\n",
    "    <li> Your text file says you installed Ubuntu (or states any challenges you are having and how you plan to fix them)  (20 pts) </li>\n",
    "    <li> Your text file states that you installed Git (10 pts)  </li>\n",
    "    <li> Screenshot of the turtle having drawn a fun doodle (10 pts)  </li>\n",
    "    <li> Modified talker node  (20 pts) </li>\n",
    "    <li> Modified listener node (20 pts) </li>\n",
    "</ul>\n",
    "\n",
    " \n",
    "\n",
    "### VirtualBox instructions for Ubuntu (Intel-based Macs and Windows):  \n",

