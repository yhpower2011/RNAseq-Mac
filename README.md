# RNAseq-Mac
step1: 
This will install FastQC, Trimmomatic, STAR, Samtools, Subread (which provides featureCounts), and R. The Bioconductor installation will fetch DESeq2, tximport, rhdf5, clusterProfiler, and the mouse GO annotation database org.Mm.eg.db. Make sure Homebrew’s bin (e.g. /usr/local/bin or /opt/homebrew/bin) is in your $PATH. After this step, all required software is installed.

Step 2: 
Integrate the Script into an Automator App
You can now create an Automator Application to run this script with one click.
Open Automator:
Go to your Applications folder and launch Automator.
Choose "Application" when prompted for a new document type.
Add a “Run Shell Script” Action:
In the search box at the top left, type “Run Shell Script.”
Drag the Run Shell Script action into the workflow area on the right.
In the Run Shell Script panel, set:
Shell: /bin/bash
Pass input: “to stdin” (or “Ignore” since no input is used).
Embed the Script:
Copy the entire Bash script from above (from #!/bin/bash to the final echo) and paste it into the text area of the Run Shell Script action.
(Optionally, if you want to specify a custom base directory, you can modify the first line of the script or pass an argument. By default, it will use $HOME/Desktop.)
Save the Automator Application:
Go to File > Save…
Name your application (e.g., "Pre-Create RNAseq Project Folders").
Save it to a location that’s convenient (for example, your Desktop or Applications folder).
Run the App:
To generate the folder structure, simply double-click your new Automator application.
A Terminal window will briefly open (showing the log messages), and it will create the three project folders with all the necessary subdirectories.
You should see messages like “Created folder structure for RNAseq-a at /Users/yourname/Desktop/RNAseq-a” in the Terminal.

Step3: 
