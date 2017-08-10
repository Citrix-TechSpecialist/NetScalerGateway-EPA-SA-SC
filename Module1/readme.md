# Module 1: Setting up a Pre-Auth EPA scan policy

#Introduction

~8 min to complete and to test end user experience

We can set up a simple preAuthentication scan, which is checked before allowing the client to even see the login page. For my test here, I used NetScaler 12, and tested off a Mac, and a RDS for Windows. It is easy to manipulate a file on the desktop for an example and here we used the file test.txt in either /Library for the Mac, or C:/Users/user1/Desktop for the pc.

Here are the policies used:
CLIENT.FILE(/Library/test.txt) EXISTS
CLIENT.FILE('C:\\\\Users\\\\user1\\\\Desktop\\\\test.txt') EXISTS

To do the file on my mac, I used the following commands in a terminal window:

	sudo touch /Library/test.txt

	sudo mv /Library/test.txt /Library/test-ish.txt

	sudo mv /Library/test-ish.txt /Library/test.txt

	sudo rm -rf /Library/test.txt

	or sudo rm -rf /Library/test-ish.txt

Doing the file on the PC is simple foe sure. C:/Users/user1/Desktop.....

## Exercises 

# Reset the Sandbox Environment 

### Shortcuts
1. [Module 1: Setting up a Pre-Auth EPA scan policy](../Module1)
2. [Module 2: Setting up a Smart Control Policy](../Module2)
3. [Module 3: Setting up Smart Access](../Module3)