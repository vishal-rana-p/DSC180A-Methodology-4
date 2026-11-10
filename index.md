**Name:** Vishal Rana Paidi
**Email:** vpaidi@ucds.edu

**Section:** D06
**Mentor:** Duncan Watson-Parris

---

**What is the most interesting topic covered in your domain this quarter?**

The most interesting topic was differentiable climate modeling. Because JCM is written in JAX, it can compute the exact derivative of any model output with respect to any input directly from the model code. One reverse-mode pass gives the sensitivity of a quantity like global outgoing radiation to every grid point's sea-surface temperature at once, which would otherwise take thousands of separate model runs. This allows us to record the response to different scenarios much faster than with a full GCM model like NorESM2.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to investigate how greenhouse gases and aerosols separately drive changes in extreme rainfall and daily temperature range over South Asia, a region with some of the world's largest sulfur dioxide and black carbon emissions. Using ClimateBench's single-forcing NorESM2 experiments, I would separate the greenhouse-gas and aerosol contributions, then build a regional emulator in JAX and use its gradients to map which emission sources, local or remote, most affect South Asian extremes. I would also bring in Indian Ocean sea-surface temperature data from NorESM2 and observations to test whether aerosols act on rainfall partly by cooling the ocean and weakening the monsoon.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would validate the simplified model's regional behavior before relying on its global numbers. In Quarter 1, SPEEDY's equilibrium climate sensitivity closely matched NorESM2's, but its Gregory regression failed because the top-of-atmosphere imbalance never decreased. A likely cause is that the land surface was held at its climatology every day. I would test how that setting and other configuration choices affect the results, and use monthly rather than annual means so that the regression has more points during the fast warming phase.

**What other techniques would you be interested in using in your project?**

I'd like to use gradient-based optimization to search for emissions pathways that limit regional warming or extreme rainfall under constraints. I'm also interested in regridding ocean data with and accessing CMIP6 data to compare NorESM2's aerosol response with other models.
