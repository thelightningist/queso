# queso
Queso is a suite of shell scripts inspired by real world interactive scripts I have developed for work.

When working at ACME, Support Engineers were instructed that account changes to a user's ACME account email address must be made using the company's proprietary internal `Achilles` tool and one of it's plugins, `bow`.

This manual process involved going to several different company pages, installing a script for Achilles, running `achilles plugin -name bow` command to install the required dependency plugin. Once that was all done, support engineers had to run an `achilles bow --acmeid=am:bb:c96540 --emailupdate=email@address.com` command every time by hand.

Enter Queso! With one single command, you can pull and download a setup script that will install 3 aliases into the ~/.zshrc file, and mark queso.sh, queso-update.sh, and queso-uninstall.sh.as executables (so that the aliases work).

Now support engineers can simply type `queso` into their terminal and will be prompted with an interactive script for entering in the user's ACME UDID and the new email address the support engineer is updating the account to. This script will halt if either prompts are given empty values and instruct the support enginner that both an ACME UDID and new email address are required to make the change.

Additionally, support engineers can run `queso update` and `queso remove` to update the suite or remove it respectively. 
