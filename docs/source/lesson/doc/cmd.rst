cmd Module Basics
=========
The cmd module contains a public class, Cmd, designed to be used as a base class for command processors such as interactive shells and other command interpreters. 



Example Program
------------------------
In order to demonstrate commands provided by cmd, an example have been provided: 

.. code:: python
    import cmd

    class BankAccountTransaction(cmd.Cmd):
    
        def do_deposit(self, line):
            print "The total deposited is " + line
    
	def help_deposit():
            print "This functionality determines the deposit balance"

        def do_withdraw(self, line):
            print "The total withdrawal " + line
        
	def do_balance(self, line )
            print "The total balance is " + line 
        
        def main():
            BankAccountTransaction().cmdloop()

if __name__ == '__main__':
    main()

To execute the program, simply:

Example::
    $ python bankAccountCMD.py

    (Cmd)


The CMD class can be used to customize a subclass and become a user-defined command prompt. After you have executed your program, commands, which were defined in your class can be used.  A few features, which would help understand the module cmd include: 

* The methods of the subclass, which begins with do_xxx are the prompt commands. For example, in the BankAccountTranscation class, the function do_withdraw maps to withdraw on the commandline.

Example::
    (Cmd) withdraw 23   

* The methods of the subclass, which beings with help_xxx provide descriptive messages. For example, in the BankAccountTranscation class, the function help_deposit suggests the utility of the command.

Example::
    (Cmd) help deposit 
 

* For more information on the use of cmd, please refer to: https://pymotw.com/2/cmd/
