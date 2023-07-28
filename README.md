# manage-LS-Errors

This is a proposal to manage Lotusscript errors. The base idea came from Ben Poole blog, that seems no to be anymore available
http://benpoole.com/weblog/200812121152

I will wait that Ben Poole return to develop wonderfull piece of lotusScript or VoltScript code!

This error managing model allow to store all the calling stack between function, subfunction, class methods, and return to the caller.

The point is to have only one point in charge to display or log the error (the root calling agent or event), while the other nodes reports to it what is the problem.

To adapt it to every situation you just need to decide Which are the functions that can consider the error as part of normal operation and perform a simple skip and which instead are the blocking errors that must be reported with their entire stack.

The example shown here is a series of functions that if an error occurs at any point everything must stop reporting it to the user in a MessageBox che conterrà questa stringa:
"Error: 11, call stack: Division by zero (at row 6 of FUNC2) (at row 5 of FUNC1) (at row 6 of INITIALIZE)"



