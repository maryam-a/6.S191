# Setting up Deep Learning Environment on Windows using Anaconda
## Ensure that you have Python 3.5 installed. 
To check, open Command Prompt/ PowerShell/ you favourite CLI and enter `python --version`. You should see something like `Python 3.5.x :: Anaconda 4.x.x (64-bit)`.
- If you know you have Python 3.5 installed but `python --version` returns `Python 2.7.x :: Anaconda 4.x.x (64-bit)`, you can switch your **Environment Variables** by:
  * Open `Control Panel`.
  * `System and Security > System > Advanced System Settings`.
  * A window entitled `System Properties` should open. Ensure that you're on the `Advanced` tab. 
  * Click the `Environment Variables...` button.
  * A new window entitled `Environment Variables` should open. Select `PATH` and click `Edit`.
  * Another window should open up. Ensure that each of the Anaconda3 paths are above all the Anaconda2 paths.
  * Once completed, click `Ok` on each of the three windows.
- Don't have it installed? Download it from [Anaconda's website](https://www.continuum.io/downloads).

## Copy the instructions below into your favorite CLI
```
conda create -n intro_dl;
activate intro_dl;
pip install --upgrade --ignore-installed https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.0rc0-cp35-cp35m-win_amd64.whl;
pip install gensim;
conda install jupyter;
echo 'done'
```

## Testing the Installation
```
git clone https://github.com/nicholaslocascio/intro-deeplearning-setup
cd intro-deeplearning-setup
jupyter notebook
```

Open `test_script.ipynb` in the jupyter notebook. Then run the top block in the jupyter notebook (you can run with the little right-arrow button).

Chances are you're going to get the following error.
```
C:\Anaconda3\lib\site-packages\gensim\utils.py:855: UserWarning: detected Windows; aliasing chunkize to chunkize_serial
  warnings.warn("detected Windows; aliasing chunkize to chunkize_serial")
```

That's okay. It's a Windows thing. If you don't get any errors other than this warning, you're all setup!
