# ADS1-Assignment-3
C02 Emission by Electricity Production
from scipy.optimize import curve_fit
#!pip install lmfit
from lmfit import Model
def gaussian(x, amp, cen, wid):
    return (amp / (np.sqrt(2*np.pi) * wid)) * np.exp(-(x-cen)**2 / (2*wid**2))
