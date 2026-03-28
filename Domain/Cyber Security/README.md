# CYBERSECURITY

## Task: Your First Lab & Recon Mission Welcome

This task is your first step into the world of **practical cybersecurity**. It's designed to test your enthusiasm, your ability to follow technical instructions, and your problem-solving skills.

Don't worry if you don't know everything; the goal is to **learn, explore, and have fun**. We are looking for **effort and curiosity, not perfection**.

---

# PHASE 1: BUILDING YOUR DIGITAL WORKSPACE (THE KALI LINUX SETUP)

Every security professional needs a **safe, isolated environment** to practice their craft. Your first mission is to build your own.

---

## OBJECTIVE

Install and run **Kali Linux inside a Virtual Machine** on your computer.

---

## INSTRUCTIONS

### 1. Download & Install VirtualBox

- Go to the official Oracle VirtualBox website:  
  https://www.virtualbox.org/wiki/Downloads

- Download and install **VirtualBox** for your host operating system  
  *(Windows, macOS, or Linux)*.

---

### 2. Download the Kali Linux Image

- For beginners, the easiest method is to use a **pre-built virtual machine image**.

- Go to the official Kali Linux downloads page:  
  https://www.kali.org/get-kali/#kali-virtual-machines

- Download the **"VirtualBox" image** for Kali Linux.  
  It will be a **large file (several GB)**.

---

### 3. Import and Run Kali

- Open **VirtualBox**.

- Go to **File → Import Appliance**

- Select the **Kali Linux image file** you just downloaded.

- Follow the **import wizard**. You can usually accept the default settings.

- Once imported:
  - Select the **Kali VM** from the list in VirtualBox
  - Click **Start**

- The default login credentials are typically:
  - Username: kali
  - Password: kali

---

### 4. Update Your System

Once you are at the **Kali desktop**:

1. Open a **Terminal**  
2. Run the following commands to ensure your system is **up-to-date**
  - sudo apt update
  - sudo apt upgrade -y

This is a **critical first step in any secure environment**.

---

## PRO-TIP

If you get stuck, search for a tutorial on YouTube. Searching for:

**"How to install Kali Linux on VirtualBox"**

will give you many visual guides.

Reference tutorial:  
https://youtu.be/ZJFu0AoAY_g?si=GFqI9ka786WHO-78


# PHASE 2: DOCUMENTING YOUR JOURNEY (THE PORTFOLIO)

A good security professional documents their work. You will now create your portfolio file to record your progress.

---

## OBJECTIVE:

Create a text file in your Kali environment to document this task.

---

## ABOUT GEDIT:

gedit is a simple, easy-to-use graphical text editor that comes pre-installed on Kali Linux. It's like Notepad on Windows or TextEdit on macOS. It's perfect for beginners because you can use your mouse and menus, but it can also be launched from the command line.

---

## INSTRUCTIONS:

1. Open a Terminal in Kali.

2. Launch the gedit text editor by simply typing the command:

**Bash:**
  - apt install gedit
  - gedit

3. A new window will pop up. This is your text editor.

4. Save the file immediately. Go to **File -> Save** and name it **YourName_CyberPortfolio.txt** (replace YourName with your actual name). Save it in your home directory.

5. In this file, write the following sections:

- **Phase 1 Completion:** A brief sentence confirming you have successfully installed and updated Kali Linux.

- **Tool Installation:** You will fill this section in the next phase.

- **Tool Usage:** You will fill this section in the next phase.

- **Challenges Faced:** As you work through this task, write down any problems you ran into and how you tried to solve them.

# PHASE 3: YOUR FIRST RECON MISSION (USING GOBUSTER)

Now it's time to install a real security tool and use it to gather information. This process, known as reconnaissance, is one of the first steps in any security assessment.

---

## OBJECTIVE:

Install GoBuster, learn its functions, and run a basic scan.

---

## ABOUT GOBUSTER:

GoBuster is a popular command-line tool used for brute-forcing directories and files on web servers. In simple terms, it takes a list of common directory names (like /admin, /login, /images) and checks if a website has them. It's an excellent tool for finding hidden or forgotten parts of a website.

---

## INSTRUCTIONS:

### 1. Install GoBuster:

- GoBuster is not installed by default. You will install it using the command line.

- Open a Terminal and run the following command:

**Bash:**
  - sudo apt install gobuster

---

### 2. Learn How to Use GoBuster:

- Professional tools don't come with a user manual. Instead, they have built-in help files.

- Hint: You can learn the commands and options for almost any tool by using the -- help flag. Try running this command:

**Bash:**
 - gobuster --help

- Read through the output. Pay attention to the dir command and the flags for - u (URL) and -w (wordlist).

---

### 3. Run a Scan:

- GoBuster needs a wordlist to work. Kali comes with many pre-installed wordlists. A common one is located at  
`/usr/share/wordlists/dirbuster/directory-list-2.3- medium.txt`.

- Your mission is to run GoBuster against a safe, legal target. We will use `http://10.0.2.15`, which is the local IP address of your own Kali VM's web server (if it's running). If it's not running, you can use a public practice site like `http://testphp.vulnweb.com`.

- The command will look something like this:

**Bash:**
  - gobuster dir -u http://10.0.2.15 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

- Let the scan run for a few minutes.

---

### 4. Update Your Portfolio:

- Go back to your `YourName_CyberPortfolio.txt` file.

- In the **"Tool Installation"** section, write down the command you used to install GoBuster.

- In the **"Tool Usage"** section, paste the GoBuster command you ran for your scan and copy one or two interesting lines from the scan's output.

  
