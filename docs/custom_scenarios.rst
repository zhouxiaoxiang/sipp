Custom SIPp scenarios
================================

Of course embedded scenarios will not be enough. So it's time to create your own scenarios. A SIPp scenario is written in XML (a DTD that may help you write SIPp scenarios does exist and has been tested with jEdit - this is described in a later section). A scenario will always start with:

<?xml version="1.0" encoding="ISO-8859-1" ?>
<scenario name="Basic Sipstone UAC">

And end with:

</scenario>

Easy, huh? Ok, now let's see what can be put inside. You are not obliged to read the whole table now! Just go in the next section for an example.

There are many common attributes used for flow control and statistics, that can be used for all of the message commands (i.e., <send>, <recv>, <nop>, <pause>, <sendCmd>, and <recvCmd>).
