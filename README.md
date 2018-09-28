A simple interface providing simplified MultiProcessing for Jupyter notebooks.

This class is a Context Manager that makes a command line call to start a 
cluster of python processes on entry, and shuts them down again on exit.

As a context manager, the exit actions take place even if the contextualised
code throws an error or the user hits the KeyboardInterrupt. Restarting the
Kernel however, may leave orphaned python processes running. To close them 
down, open a Command Line Interface and run the following command:
        ipcluster stop