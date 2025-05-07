Overview of the Scenario files and what they do

Scen_A_Annual8760_CF-DEM: Defines the demand as hourly percentages. So a demand of 10 PJ in my demand process will be split evenly across these percentages.
Scen_A_SubAnnual8760_AF-RE: Large file. Defining hourly capacity factors for several milestone years. There are a lot of solar arks. The original one is the one simply titled 'Solar' and encompasses the regular tilted solar panels. However, due to persistent errors when defining years 2030 and above in the same excel 'ark', there are separate arks for each year (Solar 2030, Solar 2040, Solar 2050). There are then a few Solar tech2 arks. These are used for the vertical bifical solar panels.
Scen_A_SubAnnual8760_EXP: Import and export electricity price definitions for milestone years, based on climate year 2008. Interpolation of electricity prices. TimeSeries contains price checks for all hours. I have highlighted prices in red that were above a certain threshold, in order to try to assess outliers for analysis. 
Scen_A_SubAnnual8760_YRFR: Breaking the year down into equal sized timeslices. 
Scen_B_NCAP_UP_SPINES_Model4: Large file! Stochastic file, using the SPINES approach, only capacity factor uncertainty. Base 2030, 2040 and 2050 are old and do not do anything here. Scenario tree ark defines the branching possibilities in the future, more explanation in the file itself. Uncertainty 2030, 2040, 2050 provide the values associated with the different sows for each technology (vertical bifacial values not defined in this file), categorized by years. Database contains the calculations for the normalized version of the capacity factors used (they would otherwise sometimes exceed 1). It does not contain vertical bifacial calculations.
Scen_B_NCAP_UP_Stoch_Model4: Same as above but with the Stochastic approach.
Scen_CO2_TAXES: As stated, defining tax on CO2 emissions base on year. More details in file.
Scen_COST_Det: Future cost trajectories defined for deterministic cases. 
Scen_ELC_CO2BND: Scenario with slow reduction in CO2 emissions allowed. Based on CO2 emissions from base run.
Scen_NCAP_UP_SPINES_Model4: Large file! Stochastic file, using SPINES, capacity factor and cost reduction uncertainty both included. Scenario tree is now extended. However, SPINES is unable to actually handle cost uncertainties, and so this file is a bit redundant.
Scen_NCAP_UP_Stoch_Model4: Large file! Stochastic file, using Stoch approach, capacity factor and cost reduction uncertainty. The 'Uncertainty Cost' ark shows the relative percentage decreases per milestone year. Interpolation was considered by adds an unfeasable amount of calculation time. New database that shows how the costs calculations where achieved. Otherwise same as the other stochastic files above.
Scen_SUN_NCAP_UP_SPINES_Model4: Same as just above, but with the vertical bifacial as well (ELERNWSUN02).
Scen_SUN_NCAP_UP_Stoch_Model4: Same as just above, but with vertical bifacial solar panels as well (ELERNWSUN02). The actual calculations for the vertical bifacial solar panels are not found in these files.

Scen_UC_SOLCAP & Scen_UC_WINDCAP: Unused but meant to introduce capacity constraints on tech installations.

The last two files are from EML	
 
