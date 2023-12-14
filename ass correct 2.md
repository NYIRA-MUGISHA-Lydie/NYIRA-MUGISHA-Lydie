(1) Write a Shell Scripts that takes three numbers on the command line and does the following
       - Checks that the number of command line arguments is correct (3). If not write an error message in a file called error.txt and exit
       - If the number of command line arguments is correct write the numbers in a file called numbers, in ascending order.

Solution

#!/bin/bash

# Check if the number of arguments is not equal to 3
if [ $# -ne 3 ]; then
    echo "Error: The script requires exactly three arguments." > error.txt
    exit 1
fi

# If the number of arguments is correct, sort the numbers in ascending order and write them to a file
echo -e "$1\n$2\n$3" | sort -n > numbers.txt
