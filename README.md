<h1>Firefox 57+ full dark theme with dark scrollbars and multirow tabs/bookmarks</h1>

<p>This repository includes the files requires to (almost) fully dark theme firefox quantum to dark-gray colors 
(with #222-#444 colors mostly). </p>
<p><b>Of course... you could as well use these files to color your firefox any way you wanted</b>, the only thing you'd have to do is change the correct values (what each class or id does is commented above each) in the .css files (as far as you know some 
basic css or <a href="https://www.w3schools.com/colors/colors_picker.asp">color coding</a>, it shouldn't be too hard)</p>
<p>What this "theme" will not affect will be your persona, the text color used by it, and the accent color (line above active tab). To change those settings, you can change them manually through the <code>about:config</code> page, searching 
<b>lightweightThemes.usedThemes</b> there, and changing the textcolor or accentcolor codes of your used persona respectively as seen on the image below:</p>
<img src="https://i.imgur.com/3lzN95E.png">
<p>To change these you will have to use the right hex codes. You can find a color picker to hex code in <a href="https://www.w3schools.com/colors/colors_picker.asp">this page</a>.

<h3>Last update: <b>03/01/2017</b></h3>
<p>Files updated:</p>
<ul>
  <li><b>Usercontent</b> -> Added the <code>about:profiles</code> page.</li>
  <li><b>UserChrome.js</b> -> Added a new way to change the scrollbars, which should be permanent (at least until Mozilla decides to disallow the use of UserChrome.js completelly) using the method designed by <a href="http://mozilla.zeniko.ch/userchrome.js.html">Zeniko</a>, <a href="https://github.com/Endor8/userChrome.js">Endor8</a>, and <b>RAZR_96</b> <a href="https://www.reddit.com/r/firefox/comments/7dtcpm/restyle_an_userstyle_manager_that_can_edit/">in this reddit comment</a>.</li>
  <li><b>scrollbars*.uc.js</b> -> Added a few variations of the default scrollbar that was being used for this dark theme (such as a slim, a squared, or a better gradient version).</li>
</ul>
<h3>Last update: <b>30/12/2017</b></h3>
<p>Files updated:</p>
<ul>
  <li><b>Usercontent</b> -> Added the <code>about:healthreport</code> page (it is actually an external page hidden as an about: page... so it could be styled with a userstyle.</li>
</ul>

<h2>FAQ:</h2>

<h3>The scrollbars go back to the default ones after a firefox update when using the old method!</h3>
<p>You should be using the new method (inside the scrollbars dark theme folder) for the permanent fix for them. I'm only keeping this folder for legacy reasons (or just in case Mozilla disallows the user of UserChrome.js in the future)
<p>If you still want to use the old method because the userChrome.js method somehow doesn't work for you, you will have to re-patch the <code>chrome.manifest</code> file after each firefox update either following the manual steps found in here, <b>or applying the right re-patcher found on the "Scrollbar patchers(Old method)" folder</b> (which should at least give you one or two months before having to re-patch it until the next firefox update).</p>
<p>This problem happens because firefox overwrites the omni.ja and the <code>chrome.manifest</code> file with each firefox update to "clear" any possible problem with the old version, making our change only temporary without re-patching it after each update.</p>

<h3>Why use this method instead of using <a href="https://addons.mozilla.org/es/firefox/addon/styl-us/">Stylus</a>?</h3>
<p>The main reason is that you can't style firefox about: pages nor the scrollbar with just stylus.</p>

<h3>What features does this theme have?</h3>
<p>The main features (apart from the theming) are:</p>
<ul>
  <li>Multiple row tabs.</li>
  <li>Multiple row bookmarks toolbar (2 usable rows by default, but it is NOT enabled by default. You can add more rows editing userchrome).</li>
  <li>Hides some rarely used commands on the context menu such as "Set image as desktop background".</li>
  <li>Changes the tab close button to always be visible.</li>
  <li>You can hide the sidebar completelly resizing it instead of having to click the sidebar button.</li>
  <li>Can change the URL bar font (You have to change the commented line on userchrome to use it).</li>
  <li>Can change the tabs position under the URL bar (You have to change the commented line on userchrome to use it).</li>
  <li>Change the Ublock Origin blocking/control panel/popup page to a dark version (You need to change the commented lines and update the dynamic url of the extension on usercontent).</li>
</ul>
<p>You can turn these features on or off changing the commented lines on the CSS file (To change them you just have to open the userchrome.css with notepad or any code editor, and encase between "/*" and "*/" (without the quotation marks) the lines you don't want to take effect). Of course, if you think that you are NEVER going to use certain feature, you can always delete the specific lines you don't want without any other side-effect.</p>

<h2>Installation</h2>

<p>There is a short steps version (TL;DR version) after the description of the installing method</p>

<h3>Main browser UI</h3>

<img src="https://i.imgur.com/dmIuudb.png" title="Dark firefox overall UI" />

<p>Most of the job is already done with the userContent.css and userChrome.css files that you have to place in the 
chrome folder of your firefox profile (Look below for "the chrome folder" section if you don't know where that is). For this to work as intended, you should be using a persona (aka lightweight theme) or the default dark theme (The persona used on the screenshot is "<a href="https://addons.mozilla.org/en-US/firefox/addon/deep-dark-blue-forest/">Deek Dark Blue forest</a>" by <b>Sondergaard</b>).</p>
<p>If you are only looking for how to change the default scrollbars, you can apply just that without the need
of using the usercontent or userchrome files provided here.</p>

<h4>Short version:</h4>
<ul>
  <li>Type <code>about:support</code> in your URL bar, then go to that page.</li>
  <li>Click the "open folder" button inside the "profile folder" section.</li>
  <li>Create a folder named "chrome" in your profile folder if it doesn't exist yet.</li>
  <li>Place "usercontent.css" and "userchrome.css" inside the "chrome" folder.</li>
  <li>(Optional) Edit userchrome.css to disable or re-enable features typing "/*" before the lines you don't want to apply, and "/*" after them (If you want some line to apply that is within those slashes, just delete the starting "/*".</li>
  <li>(Optional) If you have Ublock Origin and want the blocked page to be dark as well, edit usercontent.css (the url line explained in there) to have the dynamic url of your ublock extension.
</ul>

<h3>The scrollbars</h3>
<img src="https://i.imgur.com/qe6tGJW.png" title="Dark blue scrollbar" />

<p>To install the custom scrollbars to match the dark theme, you will have to use one of the 2 methods found on the "Scrollbars dark theme" or "Scrollbars patchers(Old method)" folders inside this repository. You should be using the "Scrollbars dark theme" folder method, since it's the most permanent, but if you find some bug or if the scrollbars lag for you, you could try using the old method one instead. The problem with the old method is that you will have to re-patch the scrollbars with each firefox update, but it's a mainly CSS method with no JavaScript involved, so the scrollbars shouldn't lag at all.</b>

<h3>The chrome folder</h3>
<p>If you don't know where that is, just type <code>about:support</code> on the URL bar of your firefox, and in the page
you will be redirected to, on the section labed as "profile folder" click the <b>open folder</b> button.</p>
<p>After this, your profile folder will be open. You may or may not see the chrome folder. If you don't see it, just create it and place inside the usercontent.css and userchrome.css files.</p>

<p>If you want to know the exact location for profile folders (information taken from <a href="http://kb.mozillazine.org/Profile_folder_-_Firefox">here</a>):</p>

<h4>On Windows 7 and above, profile folders are in this location, by default:</h4>

<pre>C:\Users\(Windows login/user name)\AppData\Roaming\Mozilla\Firefox\Profiles\(profile folder)</pre>
  
<p>The AppData folder is a hidden folder; to show hidden folders, open a Windows Explorer window and choose "Tools → Folder Options → View (tab) → Show hidden files and folders".</p>

<p>You can also use this path to find the profile folder, even when it is hidden:</p>

<pre>%APPDATA%\Mozilla\Firefox\Profiles\(profile folder)</pre>

<h4>On Linux, profile folders are located in this other location:</h4>

<pre>/home/(Your-username)/.mozilla/firefox/(profile folder)</pre>

<p>The ".mozilla" folder is a hidden folder. To show hidden files in Nautilus (Gnome desktop's default file browser), choose "View -> Show Hidden Files". On others such as Dolphin (Kubuntu's default file browser), you'd have to choose "Control -> Hidden files"</p>

<h4>On Mac, profile folders are in one of these locations:</h4>

<pre>~/Library/Application Support/Firefox/Profiles/(profile folder)
~/Library/Mozilla/Firefox/Profiles/(profile folder)</pre>

<p>The tilde character (~) refers to the current user's Home folder, so ~/Library is the /Macintosh HD/Users/(username)/Library folder. For OS X 10.7 Lion and above, the ~/Library folder is hidden by default.</p>

<p>You can make them visible by typing the following in a terminal window.</p>
<pre>defaults write com.apple.finder AppleShowAllFiles TRUE
killall Finder</pre>
<br /><p>This will also cause any file icons to take on a hazy, 50% alpha look. To restore the old settings (hide the files and make the icons look normal) issue the same commands again, but enter FALSE instead of TRUE.<p>

<h2>The userChrome.css file</h2>

<p>The userchrome file turns dark all context menus, bookmarks, the url bar, the search bar, the main menu, and the toolbar. 
It will, although, not turn dark the extension popups you may have. <p>
<img src="https://i.imgur.com/wWjBcqz.png" title="Dark search menu (spanish)" />
<img src="https://i.imgur.com/7zj3SSq.png" title="Dark context menu (spanish)" />
<p>It will also turn dark the autocomplete popups (mostly a side-effect)</p>
<br />

<p>This userchrome will also make the close button on tabs always show, as well as adding multiple row tabs support thanks to <a href="https://github.com/andreicristianpetcu/UserChrome-Tweaks/blob/09fa38a304af88b685f4086bc8ea9997dd7db0fd/tabs/multi_row_tabs_firefox_v57.css">the code</a> of <b>Andreicristianpetcu</b>. It will also hide some (at least to me) useless options of the main context menu, such as "send image", 
"set as desktop background", "bookmark page", "send page", "bookmark this link", "send link" and "send tab/page/link to device".</p>
<p>If for some reason you wanted to keep any of those, you can still recover them deleting the css entries for the ones you are 
interested on (or commenting them between /* and */)</p>

<h2>The userContent.css file</h2>

<p>The usercontent file will turn dark the most commonly used <code>about</code> pages.</p>
<img src="https://i.imgur.com/e4zVTC7.png" title="Dark preferences page" /></a>
<p>These include:</p>
<ul>
  <li>About</li>
  <li>Addons</li>
  <li>Cache</li>
  <li>Config</li>
  <li>Debugging</li>
  <li>Downloads</li>
  <li>Error</li>
  <li>Healthreport</li>
  <li>Home</li>
  <li>Memory</li>
  <li>Plugins</li>
  <li>Preferences</li>
  <li>Profiles</li>
  <li>Support</li>
</ul>
<p>It will also turn dark the <a href="https://addons.mozilla.org">Mozilla addons page</a>, both the old and the new.</p>

<h2>The scrollbars.uc.js file</h2>
<img src="https://i.imgur.com/qe6tGJW.png" title="Dark blue scrollbar" />

<p>Same as with the other files, you can edit the scrollbars appearance using the scrollbars.uc.js, editing only past the 
`s you will find there (which are the CSS code).</p>

<h2>Credits</h2>
<p>The original code for the custom scrollbars belongs to <b>Arty2</b>, and you can find it <a href="https://gist.github.com/Arty2/fdf19aea2c601032410516f059d58eb1">here</a>.
<p>The original code for the multirow tabs was written by <b>Andreicristianpetcu</b>, and you can find it <a href="https://discourse.mozilla.org/t/tabs-in-two-or-more-rows-like-tabmixpro-in-quantum/21657/2">here</a>, or for just the code, <a href="https://github.com/andreicristianpetcu/UserChrome-Tweaks/blob/09fa38a304af88b685f4086bc8ea9997dd7db0fd/tabs/multi_row_tabs_firefox_v57.css">here</a>.
<p>The original code for the multirow bookmarks toolbar belongs to the original creator mentioned in <a href="https://www.reddit.com/r/firefox/comments/75wya9/multiple_row_bookmark_toolbar_for_firefox_5758/">this reddit thread</a>, whose code was fixed by <b>jscher2000</b> to use in our current firefox.
<p>Thanks to <b>BelladonnavGF</b>, <b>Hakerdefo</b> and <b>YiannisNi</b> for noting some issues with the theme, and <b>BelladonnavGF</b> for the addition of the url font and and tabs below url bar suggestions.</p>
<p>Also thanks to <a href="http://mozilla.zeniko.ch/userchrome.js.html">Zeniko</a>, <a href="https://github.com/Endor8/userChrome.js">Endor8</a>, and <b>RAZR_96</b> <a href="https://www.reddit.com/r/firefox/comments/7dtcpm/restyle_an_userstyle_manager_that_can_edit/">in this reddit comment</a> for the userChrome.js way of editing the scrollbars.</p>
