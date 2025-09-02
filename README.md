# RAIK 183H/184H VS Code/Cursor Setup

Hello! The following information explains the setup process for Checkstyle in Visual Studio Code (VSCode) or Cursor. The following tutorial will work for either code editor because Cursor is a fork of VSCode! **We will refer to VSCode in this tutorial, but you can think of them interchangebly.**

## Prerequisites:

1. Ensure you have the Java Extension Pack installed in VSCode

## Step 1: Install Extensions for Record-keeping

1. Find the Extensions icon at the top of the left sidebar of VSCode (should be very near the Git branch icon). The Extensions icon looks like a pile of squares, with one square balancing on its corner. Click on that to reveal the Extensions panel.
2. Search for `Local History` in the search bar. You should see a plugin published by `xyz`. That's the one. Install it. This plugin will capture snapshots of your code as you develop and store them in the `.history` folder of your repositories so Git can bundle them up for you.
3. Search for `SpecStory` in the search bar. You should see a plugin published by `SpecStory`. Install that one, too. This plugin will save your chat history to the `.specstory` folder of your repositories, so those can be bundled up by Git, too.
   - Once SpecStory is installed, click the gear icon to get to its settings page.
      <img width="1363" height="627" alt="Screenshot 2025-09-02 at 4 11 12 PM" src="https://github.com/user-attachments/assets/642250d2-e4a1-40c5-8705-f5644c147b01" />
   - Make sure your Autosave and Timezone settings are set like the screenshot below:
     <img width="1035" height="630" alt="Screenshot 2025-09-02 at 4 41 16 PM" src="https://github.com/user-attachments/assets/a538ade6-f63b-4b8d-9cce-dca2b84a4d3c" />

## Step 2: VSCode editor settings

1. Navigate to VSCode settings via the user interface or by pressing Control + Comma (Command + Comma on MacOS)
2. In the search bar, search for `editor.insertSpaces`. Check the box if it isn't already.
3. In the search bar, search for `editor.tabSize`. Enter "4" in the text box.

## Step 3: Import the `Checkstyle for Java` Extension

### If you are using VSCode:

1. Search the "Checkstyle for Java" extension and install it.

### If you are using Cursor:

1. In the files of this repository, look for the `CheckstyleForJava.vsix`.
2. Open Cursor and open the Extensions panel.
3. Drag and drop the `CheckstyleForJava.vsix` file into the Extensions panel and install the extension.

- Although Cursor is a fork of VSCode, it does not automatically expose all of the extensions that are available on VSCode. Thus, we must manually import the extension as we just did!

## Step 4: Configure the `Checkstyle for Java` Extension

1. Go back to the VSCode settings we opened earlier.
2. In the search bar, search for `checkstyle.configuration`. Enter this link into the text box:

```
https://raw.githubusercontent.com/raik183h-master/RAIK-Style-Guide/refs/heads/main/raik-style.xml
```

- Checkstyle will now automatically grab the raw XML file from that link and use it for linting your Java code!

## Step 5: Configure Java Formatting

1. In the settings search bar, search for `java.format.settings.url`. Enter this link into the text box:

```
https://raw.githubusercontent.com/raik183h-master/RAIK-Style-Guide/refs/heads/main/raik-style-formatter.xml
```

2. Now, when you save your Java code, it should automatically format according to the rules defined in that raw file.

## Using Checkstyle to find your linter errors

Checkstyle errors should automatically appear in your editor with a squiggly line under offending code, but you can also view a list of all the Checkstyle issues with your code by navigating to the Problems panel. You can either press Control + Shift + M (Command + Shift + M on Mac) or click the "Toggle Panel" button in the top right of VSCode and navigate to the "Problems" tab in the panel.

## General Troubleshooting

- If your code doesn't reformat, you can manually reformat by pressing Control + Shift + P (Command + Shift + P on MacOS) and type "Format Document With". You can click the option that pops up and click "Language support for Java"
