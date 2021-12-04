#Library
pacman::p_load(tidyverse, car)


#Recoding NA to 0 to identify patients without diagnostic and/or medication
CatVar <- c("AFDx", "STROKEDx", "DemDx", "DEMSUBDx", "CHADDx", #Disease
            "WARMed", "APIXMed", "DABMed", "RIVARMed", "EDOXMed", "ACENMed", "PHENMed", #AC
            "ASPMed", "PRASMed", "CLOPMed", "TICAGMed", "DIPYRMed", #AP
            "MEMMed", "RIVASMed", "DONEMed", "GALANMed", #AD
            "RISPMed", #APsy
            "SERTMed", "CITMed", "MIRTMed", "TRAZMed") #ADep

myDT <- as_tibble(myDT) %>% #from datatable to tibble
  mutate_at(all_of(CatVar), recode, "NA = 0; 1 = 1")
