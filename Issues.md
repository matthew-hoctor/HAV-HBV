Issues:

 * Missing values to impute
   * Gender # 96, 105
   * race
   * ethnicity
   * FIB-4
 
 * Outstanding Issues
   * how was the original vaccine administration dataset derived?  

 * To Do
   * Incorporate cirrhosis into FIB-4
   * validate HBV variable against 'HBV Vaccination Status' variable from STI chart review
   
 * Questions
   * lab costs of HBV E antigen?
   * what's going on with blank rows in the ICU dataset?
   * are the vaccines administered in 'UHS 5C FAMILY MEDICINE' considered to be in hospital?
   
   
 * Answers   
   * Values of HBV DNA to determine HBV status: 10
   * Chart review variable for prior HBV exposure?  I.e. is there a HBV status prior to admission variable I'm missing somewhere
     * look in 'HBV screening recommended' variable from the main dataset; validate against this dataset
   * should anything be done with the comments? e.g. 'declined HBV vaccine?", "left AMA", etc
     * nah
   * HAV: no prior immunity?  
     * Look at 'HAV vaccination status' and 'HAV IgG screening recommended' variables in the main dataset
   * Definitions of eligibility for the vaccines?
     * HBV: No prior immunity, no prior documentation of vaccination, no prior documentation of resolved HBV , no active hepatitis
   
 * For next week:
   * lab costs?
   * improper labs
     * IgM HAV
     * HBV DNA
     * HBV E antigen/antibody
     * HDV 
     * Looking at just Surface AB alone
     * HBV core antibody/antigen without HBV surface antigen
   * other exploratory labs
 * For next week   
   * Look at retesting for immunity for HBV 6 months after the series; no need to test for HAV completeness
   * validate HBV variable against chart review HBV prior to admission
   * Look at completion rates before Heplisav-B vs after
   * Send list of study IDs for confirmed HBV; we can look at HCC screening for these patients
   
 * Resolved Issues
   * test named 'HEB P DNA QUANT'
     * The HEB P DNA QUANT is definitely a typo and is listed as Hepatitis B by PCR in the chart with matching results
   * Discordant HCV data: updated HCV +/- definition to include any evidence of past HCV exposure
   * Discordant HIV data: apparent discordance is mostly due to lack of indication for HIV test in some patients; the HIV+ patient who tested negative could be due to viral suppression, but this is unclear, as there is no info in the dataset on HIV status on admission.
   * Updated HAV screening variable to not include HAV IGM measurement; 8 observations had only HAV IgM measurements without HAV IGG or HAV AB total measurements
   * Lack of temporality info in labs: unclear which labs to use (e.g. to calculate FIB-4)
   * issues with date info on vaccine administration: Vaccines without an administration date were ordered but not given
   * other out of range liver biomarkers (ALT > 200, total bilirubin levels ≥ 3.0 mg/dL)
   * double check on the FIB-4 timeframe; and double check how other studies have looked at FIB-4
   * cleanup null to na conversions