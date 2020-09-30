# AnotherIFTTTWebhook Trigger

After I discovered the IFTTT webhook library in Arduino has been depriciated, I found some great code by Neil Webber that can be used to send a webhook to IFTTT.

His original code is here: https://gist.github.com/outofmbufs/d6ced37b49a484c495f0

# How to use:
1. Place AnotherIFTTTWebhook.h in the same directory as your Arduino .ino project file.
2. Add #include "AnotherIFTTTWebhook.h" to your main project file
3. Send webhook by adding the function send_webhook(EVENT, KEY, Value1, Value2, Value3) to your main project file.

This version is again modified to enable detection of errors when trying to reach IFTTT, it now returns a "false" or "true", depending on whenever the client.connect()
function is successful in reaching IFTTT or not. Needed this for my little (snail)mail notification project to ensure we got our notification to IFTTT out or not.
Based on www.siytek.com's mod of this lib.  