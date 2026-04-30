# TemperateMOI

This repo contains two small projects.

1 ) MOI:
- Determines if temperate phages can entrap spores & explores the relationship with MOI

2) PlvGe (Plaques vs. Germination):
- Compares the ratios of plaques vs. the number of countable germinated spores from the same mixture.


## MOI

### Code:
- 202511133_1301_moicleaning.Rmd 
normalization of all plaque count MOI data of lytic vs. wt phi3t across trials

- 20251113_1215_allMOIS.Rmd
plotting regression relationship between MOI & phage lifestyle (lytic, wt phi3t) 

- 20251113_1444_PilotFig.Rmd
PFU comparison across MOI of 1 for lytic and wt phi3t -- (note that MOI is listed as 0 in dataset because it is in logform. MOI log = 0 is MOI =1)

### data/:
- .csv files of plaque counts of phi3t lytic and WT across multiple MOIs and dilutions
- data from is repeated iterations (different mois) between 08/2025-11/2025. 
- briefly: d6 was treated with equivalent mois of lytic and wt phi3t, allowed to incubate overnight,
treated with heat to isolate spores, and counted.


### archive/ folder 
- can be safely ignored (it includes reference code that was used to inform SporeMOI and/or old code drafts)

## PlvGe (Plaques vs. Germinated Spores)

### PlvGe_data/ 
- plaque and germinated spore counts from both spbeta and phi3t (lytic & wt phenotypes) at various MOIs (mostly 1)
- note that spore counts and plaques are paired (i.e. came from the same samples but were plated differently to count either # of entrapped virospores or # of uninfected germinating spores)
- datasets with _nocount at the end are the same as the datasets lacking the _nocount suffix, just have had all 0 data removed for easier datacleaning -- the ones with zero counts are kept only for posterity/reference

- most data is from 08-09 2025 pilot to see if entrapment was even possible in temperate phage,  but later, 20251113_1204_MOI6_4 was added (from spore MOI) since methods were equivalent & plaque/spore count is known.


### Code:
- 20250924_LyticVsWt_Collated.Rmd combines all data/ and analysis related to plaque count vs. germinated count
- Important to note what the three types of treatments referenced in this dataset mean:

1) Lytic infection:  d6 cells exposed to the dSrof lytic mutant, incubated ON and isolated for spores.

2) WT infection: d6 cells exposed to WT temperate phage, incubated ON and isolated for spores.

3) Prophage (lysogen) infection: d6 cells with integrated prophage (so all cells already carry the temperate phage prior to the experiment, and are therefore 100% pre-infected with the WT strain)

- the purpose of including prophage was to see if phage plaques was equivalent to total infected "virospores" (i.e. spores w/ prophages). data suggests that implies are always more spores able to germinate then plaques are counted, suggesting that counting may not be perfectly efficient (possibly we only visibly see ~x% plaques out of 100 virospores) 



- 20250919_sporevveglawns.Rmd looks at the difference between countable plaques of phi3T lysogens when plated on vegetative d6 lawns vs. spore d6 lawns.

### archive_PlvGe
- original drafts of the code that resulted in 20250924_LyticVsWt_Collated.Rmd
- was initally in multiple parts/analysis, so LyticVsWt_Collated combines these efforts
- can be safely ignored and may be nonfunctional, but are kept for posterity/reference