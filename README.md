
# Alt+Left on Firefox with Touchegg in GNOME
This project configures the Touchegg library to enable navigating to the previous page in Mozilla Firefox using 3 fingers across the system, should you choose to modify the code.
## Setup
Ensure that you have installed the following libraries:

    Touchegg Library
    X11 Gestures Extension for GNOME

Please note that this setup may only function properly in the GNOME environment, as it relies on the x11 gestures specific to GNOME, primarily for disabling desktop swipe functionality.


Keep in mind that you have the option to customize the browser on which this feature will take effect within the <command> tag and the <application> tag, specifically by adjusting the name, currently set as "Mozilla Firefox". This flexibility allows you to tailor the functionality to work seamlessly with your preferred browser. 

    <application name="firefox">
    <gesture type="SWIPE" fingers="3" direction="RIGHT">
      <action type="RUN_COMMAND">
        <command>xdotool search --name "Mozilla Firefox" windowactivate --sync key --clearmodifiers --delay 100 alt+Left</command>
        <repeat>false</repeat>
        <animation>NONE</animation>
        <on>begin</on>
      </action>
    </gesture>
    <gesture type="SWIPE" fingers="3" direction="LEFT">
      <action type="RUN_COMMAND">
        <command>xdotool search --name "Mozilla Firefox" windowactivate --sync key --clearmodifiers --delay 100 alt+Right</command>
        <repeat>false</repeat>
        <animation>NONE</animation>
        <on>begin</on>
      </action>
    </gesture>
    </application>


Feel free to personalize this setting to suit your specific browser preferences and requirements.

