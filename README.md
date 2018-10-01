# LASER_seq_2018
Exact code, with explanatory Jupyter Notebook, used for Zinshteyn et al. 2018 LASER-seq paper

to run the pipeline:
1)compress all of your fastq files with gzip and place them in one folder
2)fill out a settings file, pay attention to the output location, or you risk overwriting previous runs
3)from the pipeline folder run:
    python mod_seq_main.py my_experiment.settings.json

optional parameters (add after settings file):
    --threads : max number of parrallel processes to use. Default is 8.

Python dependencies (install with pip):
    simplejson
    bokeh (optional, but very helpful)
    statsmodels
    matplotlib
    numpy
    scipy

This package requires installation of the ShapeMapper package from Kevin Weeks' lab.
Download ShapeMapper 2 from http://www.chem.unc.edu/rna/software.html compile it, and add it to your PATH.

skewer is required: https://github.com/relipmoc/skewer

seqtk is required: https://github.com/lh3/seqtk

pigz is required: https://zlib.net/pigz/

STAR is required, add to PATH: https://github.com/alexdobin/STAR

the bokeh interactive plotting package is optionally required:
http://bokeh.pydata.org/en/latest/docs/user_guide/quickstart.html#userguide-quickstart


explanation of settings files:
I've included modified versions the settings files used in the paper. They will need to be further modified to match the names and locations of the files on your system.

The included Jupyter notebooks include an explanation of a settings file and example running anhd use of the pipeline. The notebook does not produce useful error output from the pipeline, so if it isn't working, run in the command line as described above and/or check the log files.