# jupyter_stuff

It was embarrassingly painful to get to this point, but here's the deal.

Jupyter at this point apparently needs an old version of matplotlib to work if you plan on plotting anything with it.  Here's what is working for me now (2023-10-11):


$ pip list|grep -P "numpy|matplotlib|jupyter"
jupyter                   1.0.0
jupyter_client            8.3.1
jupyter-console           6.6.3
jupyter_core              5.3.2
jupyter-events            0.7.0
jupyter-lsp               2.2.0
jupyter_server            2.7.3
jupyter_server_terminals  0.4.4
jupyterlab                4.0.6
jupyterlab-pygments       0.2.2
jupyterlab_server         2.25.0
jupyterlab-widgets        3.0.9
matplotlib                3.5.1
matplotlib-inline         0.1.6
numpy                     1.26.0

Before this I was running matplotlib 3.8.0 and things were failing miserably with an error about "cannot import name "\_docstring' from 'matplotlib'"

Notebook enclosed, and thanks to https://www.youtube.com/watch?v=yR0wtOxjx-U .

USAGE:
jupyter notebook matplotlib_example.ipynb


If you have trouble, try "pip remove matplotlib" and then "pip install matplotlib", at least that is what worked for the broken state of things I was initially trying...

also finance tools (covered in video):
pip install mpl_finance

mpl_finance 0.10.1 is what worked for me
