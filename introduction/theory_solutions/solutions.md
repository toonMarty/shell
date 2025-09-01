# 1. Login incorrect

From a security point of view, this functionality (displaying just **Login incorrect**) helps in making the system a bit more secure because of the vague nature of the message. For instance, if an attacker guesses the username correctly and not the password, an attacker can carry out a user enumeration attack.

Making the incorrect login message more descriptive (by stating what credential is invalid) makes brute-force attacks easier to carry out given the attacker has one credential, say the username. Just displaying Login incorrect makes it harder for the attacker to access the system because the number of combinations required to carry out the brute-force attack goes up. The attacker will have to find a username and password combination that works, unlike finding just one given the other credential was provided.

**TL;DR**: It helps to mitiagate unauthorized access in the event a bad actor is involved, or an unintented access attempt is carried out. For example misspelling a username or missing a character in a password

# 2. There are no wrong answers...only "wrong" passwords

* password - too obvious. Simple string
* scooby - too simple
* 5c00by - l33t-speak variation of scooby (clearly a pet name).
* qwerty- a predictable string sequence. Along with 12345
* abc - too short.

**Sorry, try again**

# 3. Streets ahead...Fido(ed) and minted
Fido is not an acceptable password. Reasons as to why it's not an acceptable password include:

* The length of the password is too short
* The sequence of characters is too simple. It contains only alphabetic lowercase characters. No uppercase characters, no special characters like $£!, no numbers

# 4. You shall not pass, unless ...

* Make sure the **```CapsLock```** key is off
and enter username and password exactly as specified or as I had set them up

* Ensure I'm set up as a user

* If login prompt re-appears after logging in and the credentials are correct, boot the system in recovery mode and delete some files then try to login.

* Check if I'm on the right machine. If on a larger, networked system, I'd specify the machine I intend to connect to before login

# 5. Doggone it
BAD PASSWORD: it is too short

# 6. What do you call a lady computer? A COMPRESS
Use apropos with a keyword when you don't know the name of a command used to carry out a particular task. All utilities related to the keyword will then be displayed by apropos.

    apropos compress

# 7. Those who fail to learn from a command line  are doomed to repeat it

#### Method 1

* Press the **```UP ARROW```** key to display an earlier command line
* Use the **```RIGHT ARROW```** and **```LEFT ARROW```** keys to move the cursor back and forth along the command line where at any point you can edit the command line
* Press the **```RETURN KEY```** execute the modified command

#### Method 2
* Type !! on a command line prompt

    $ !!
* Edit the command line using the **```RIGHT ARROW```** and **```LEFT ARROW```** keys
* You can also edit using **^old^new^**
* Press the **```RETURN KEY```** execute the modified command

Method 2 comes in handy when we forget to precede a command that requires sudo privileges to be executed with sudo. For example

    $ apt update

    $ sudo !!

    $ sudo apt update

# 8. Help wanted
Information (options) displayed by the --help option of the tar utility

* Main operation mode
* Operation Modifiers
* Local file name selection
* Overwrite control
* File name transformations
* Compression
* Device blocking
* Device selection and switching
* Handling of file attributes
* Handling of extended file attributes 
* Informative output

To display the --help option of the tar utiliy one screen at a time


    tar --help | less

# 9. Shadow Hunter

    man 5 shadow

# 10. Transformers: Shells in disguise
Changing login shell to tcsh without using root privileges.

If unsure about what command to use, use apropos

    apropos shell

This will output several utilities involving shells. Checking the output of ```apropos shell``` we find a utility:

    chsh (1)             - change login shell

To find more information about chsh, type

    man chsh

There's an option:

    -s, --shell SHELL
        The name of the user's new login shell. Setting this field to blank causes the system to select the default login shell.

Exit the man pages after finding the appropriate option to use

To check valid login shells on the system run:

    $ cat /etc/shells

The output might look like this:

    # /etc/shells: valid login shells
    /bin/sh
    /usr/bin/sh
    /bin/bash
    /bin/tcsh
    /usr/bin/bash
    /bin/rbash
    /usr/bin/rbash
    /usr/bin/dash
    /usr/bin/pwsh
    /usr/bin/tmux
    /usr/bin/screen
    /bin/zsh
    /usr/bin/zsh

On the terminal prompt enter the following command and then press the **```RETURN```** key to execute it.

    $ chsh -s /bin/tcsh



# 11. 

    man -k devices | wc -l

# 12. Where's passwd

    man -f passwd

    man --whatis passwd

or

    man -k passwd


# 13. Archive 81

    apropos archive
    
