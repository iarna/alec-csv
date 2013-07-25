SourceWatch's ALEC Corporations as CSV
--------------------------------------

These tools read the sourcewatch.org ALEC Corporations page and generate a CSV file suitable for use elsewhere.

This documentation assumes basic Unix skills.

Usage
-----

To generate a CSV file from the current live version of the website (requires that you have curl installed):

    ./alec-live-web > alec.csv

Or with wget:

    wget -q -O- http://www.sourcewatch.org/index.php/ALEC_Corporations | ./alec-from-html > alec.csv

If you have a copy of the website locally, like the one included with the source, you can generate CSV from that with:

    ./alec-from-html < ALEC_Corporations.html > alec.csv

And finally, if you have a plain-text copy of the website that you got by, for instance, copying and pasting the page into a text file and then editing out the lines that aren't corporation names:

    ./alec-from-txt < ALEC_Corporations.txt > alec.csv

