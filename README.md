# Impede IE

## Warning, this software assumes that you have Windows sysadmin knowledge, this is not for noobs

Just a quick thing I put together to Impede the functioning of Internet Explorer as much as possible for situations where it is not possible to remove it completely from **appwiz.cpl > Turn Windows features on or off > Internet Explorer 11** due to app compatibility issues but you still want to prevent the user from actually using Internet Explorer as much as possible.

In case the user somehow finds their way back into Internet Explorer (perhaps there is a wayward shortcut, or a misbehaving app which doesn't respect the default browser choice), this will make the actual using of Internet Explorer practically useless so that the user will be forced back onto the right path of using Chrome or Firefox (or Edge, etc.) instead.

All websites in IE will render as a blank page, and there is a button available for the Command Bar to open the URL they are on directly in Chrome or Firefox instead (useful for Wayward apps trying to direct the user to a particular URL, assuming that URL is compatibile with Chrome or Firefox)

It's won't stop a determined user with technical knowledge on how to disable it, but it should be enough of a barrier for most users.

To install, 

* Download from GitHub using **[Clone or Download] -> Download ZIP**
* Right-click on the ZIP file in explorer and **Unblock** it (or you'll get security warnings every time you run any of the files inside  it) and then **Extract** it
* Copy all the files to **C:\Program Files\Impede IE** (not PFx86, and don't remove  any spaces - some of the encoded reg entries is hardcoded to this path) 
* Run **install-block_ie-PerMachine.reg** as an Admin
* Run **install-block_ie-PerUser.reg** for each user that you wish for Impede IE to apply to.
* Open Internet Explorer for each user to  confirm change of homepage to about:blank (not necessary but speeds things up) and confirm it's working 

To disable the blank page rendering, go to **inetcpl.cpl > Accessibility > Turn off the Style Sheet**

I have only tested on Windows 10 1903 x64 but should work on x86 and other versions of Windows too. This is very much a "use at your own risk" thing. 

You'll probably want to customise it to your organisation requirements rather than run it straight, as well as it needing more testing, so I did not bother packaging it up, but if you want to contribute then feel free.

Credit goes to Ramesh Srinivasan from Winhelponline.com, for the IE extension to open in Chrome or Firefox (some components have copyright retained by him). Also thanks to Vishal Gupta of AskVG.com.

TODO: Make an "Open with Chromium Edge" option (PS: Chromium Edge has a built-in "IE mode" which works similar to "IE Tab", which you might find useful) - I probably won't get around to this bit any time soon even though it would be easy so feel free to do it yourself and contribute it back.
