# Getting Started: Laboratory Assignment #0

Welcome to CIT 384/L: Web Development and Hosting



# Overview:

### From the CIT160 Syllabus:

Today, very few have not heard of or have not used "The Internet." For the vast majority of users, they access network-based applications via the web. I.e., these users utilize a web-browser to access these applications. Some common examples include: social networks, communication tools, search tools, commerce sites, information sites, etc.

### From the CIT384 Syllabus:	

In this course, we will learn the fundamentals of developing a web site and web applications. This will provide us with a better understanding of the needs of our users and of our software developers that we serve. We then turn our attention to developing the necessary tool set to configure, to deploy, and to maintain IT systems that hosts such web applications. We also examine other tools and techniques to ensure seamless and continuous delivery of the associated services to users. Knowledge and expertise in both pieces will prepare us to be effective members of a [DevOps](https://en.wikipedia.org/wiki/DevOps) team.

While the best-practices and the technology tool-sets _de jour_ are constantly changing and evolving (and you will be expected to learn these new practices and technologies, again, again, and again _throughout_ your career), there are some widely accepted concepts and universally adopted technologies. 

As such, this class is designed to reinforce your knowledge of these prevalent technologies, but with an emphasis on the core concepts and best-practices:

  - effective team-based communication --- using https://www.slack.com
  - source and version control --- using https://git-scm.com/
  - containers, containerization --- using https://docker.com
  - automation, automation, automation --- it's a mindset, not a tool!


# Required Background Knowledge:
For CIT384, we presume that each student already posses certain knowledge of various technologies, or has the ability to learn these technologies on their own. This information includes:

  - the bash shell environment: as introduced in CIT160
  - ssh, scp, and other file transfer protocols: as introduced in CIT160 and reinforced in other CIT courses.
  - basic programming: as introduced in COMP110, CIT160, CIT270, etc., etc., 
  - elementary knowledge of docker: as introduced in CIT160

This assignment presume this knowledge. If you don't know how to perform a particular step:
  - ask!
  - ask your teammates!
  - ask in slack!
  - the professors look up to those that _work towards success and are not afraid to ask for help along the way_!


# Assignment Summary:
In this assignment, you will taking steps to setup your personal computer and various campus-provided resources. You will also need to establish accounts with various online services. These resources and services will be used throughout this course. Moreover, the professors will take every effort to utilize such services throughout the course. 

For example, 
   * all class material will be delivered via git using a GitHub repository.
   * all class assignments will be submitted via GitHub Classroom
   * all deployed software may be purged at anytime
      - the only thing that is assured to be stable is your GitHub repository
      - this will force you to automate the deployment of all your deliverables


# Assignment
Complete the following steps, and submit your <user-id>.env via GitHub Classroom.

## Steps:
  1. Read these instructions in total before you begin!

  1. Send an email to my "steven.fitzgerald@csun.edu" account to provide me with your @my.csun.edu address.

  1. On your personal computer, create a working directory for this class
     - the canonical name for this directory is: \~/classes/cit384
     - as such, all class related documents will refer to this location

  1. Validate that your campus resources are correctly configured!
     1. Log into the following shell servers using your campus user-id, and create a working directory for this class.
        ```
        ssh.csun.edu 
        ssh.sandbox.csun.edu
        k200.ecs.csun.edu
        ```
	
        Note that to access k200.ecs.csun.edu, you must first use the VPN or ssh into one of the other servers first.
	
        This step will validated that your campus account is configured correctly. If you run into any problems, contact the [heldesk@csun.edu](mailto:helpdesk@csun.edu) immediately so that any problems can be fixed quickly.

        If you don't know your user id, you can look it up via the [Forgot User ID web page](https://auth.csun.edu/idm/forgot_uid).

     1. Log into the VM (virtual machine) that has been provisioned specifically for you, and create a working directory.
        ```
        <user-id>.csun.edu
        ```
        - Note that the hostname for your VM is your campus user-id
        - Also note that you need to first ssh into one of the three aforementioned shell servers first (or be on the VPN), and then ssh into your VM.
        - If you run into any problems with this step, contact ["Barrett, Yolanda"](mailto:yolanda.barrett@csun.edu) immediately so that any problems can be fixed quickly.

  1. Establish accounts with the following online resources. In many cases, you might have already establish such accounts.
     - https://slack.com : The communication tool for this class is Slack.
     - https://github.com : All assignments and projects will be submitted via GitHub Classrooms, which requires a GitHub account.
     - https://docker.com : You will be using docker containers on you personal computer and on the CIT384 VM for all of your web hosting assignments.

  1. Setup your personal computer for CIT384:
     1. Install various software packages on your personal computer. In many cases, you might have already have these packages installed.
        - https://slack.com  <br />   You also consider install the mobile slack application on your personal digital lifeline, aka your smart-phone.
        - https://github.com <br />   I recommend that you configure your account to authenticate using [SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
        - https://docker.com
 
     1. Join the Slack CIT384 work space
        1. Accept the automatic invitation via https://join.slack.com/t/cit-384/signup using your @my.csun.edu address.
        1. Add the 'fitzgerald-f21' channel, this is wherel all online-discussions will be conducted.
        1. Respond to the 'Hello Class' via the 'reply to thread' option (do NOT "Also send to #fitzgerald-f21").
 
     1. On your personal computer clone the CIT384 repository
        1. git clone git@github.com:CIT384/class-material.git \~/classes/cit384/class-material/
        - Note that during the semester you will need to periodically perform a 'git pull' to obtain new material, updates, corrections, etc. 

  1. Complete this first laboratory assignment
     1. Accept this assignment via GitHub Classroom: https://classroom.github.com/a/ze2eta3b
     1. Clone the assignment into the directory \~/classes/cit384/labs/getting-start
     1. Create a file called "\<user-id\>".env that contains the following information associated with you!
     	```
     	name: Steven Fitzgerald
     	user-id: steve
     	email: steven.fitzgerald@csun.edu
     	githandle: smf-steve
     	```
        1. add this file to the repo (git add \<user-id\>.env)
        1. commit this change to the repo (git commit -m 'Some message' \<user-id\>.env)
        1. push to submit this assignment (git push)

     1. Using the github GUI
        1. validate that you repo has your assignment upload correctly
        1. link you github account to the class rooster

  1. Now that you have read the instruction, in total:
     - You can no complete all the steps enumerated above.
     - Except: Do not seen me email to provide me with your @my.csun.edu email address,
     - this information is contained with the \<user-id\>.env file that you submit via GitHub Classroom

## Optional (but highly recommended):
  * Setup your SSH environment to make sure you can easily log into your servers.
     1. Create a public-private key pair
     2. Add you your public key to all the releveant ~/.ssh/authorized-keys file
     3. Create a ~/.ssh/config file that allows you to JUMP into the servers behind the firewall
	```
	HOST steve.csun.edu k200.ecs.csun.edu
	   ProxyJump ssh.csun.edu
	```

