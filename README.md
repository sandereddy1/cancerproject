Please use the Anaconda Navigator and open the IPYNB file in the Jupyter Notebook.
Ensure that the DataSet and the IPYNB file that you are opening are both in the same folder.
Hope this helps!

Here is the LINK TO THE DATASET:

https://drive.google.com/file/d/1MRGBfX3TBmzoMdHzQSjgDSO4AQp3uM0U/view?usp=sharing
https://drive.google.com/file/d/1ixuMCHxKHhUAFOYy9lUL8kiKfYc4KtOx/view?usp=drive_link

import subprocess
import sys

def install(package):
    subprocess.check_call([sys.executable, "-m", "pip", "install", package])

# List of packages to install
packages = ['pandas', 'numpy', 'matplotlib', 'scikit-learn', 'seaborn', 'scipy', 'tensorflow']

for package in packages:
    try:
        dist = __import__(package)
        print("{} ({}) is installed".format(dist.__name__, dist.__version__))
    except ImportError:
        print('{} is NOT installed'.format(package))
        print('Installing...')
        install(package)
        print('{} has been installed'.format(package))

