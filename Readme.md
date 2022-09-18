### Definitions

- `Healthcare workers (HCW)`: refer to those who work in healthcare settings who may come into contact with patients, including clinical administration staff, and home care staff.

относится к тем кто работает в "healthcare settings" (медицинских учереждениях), кто может контактировать с пациентами включая персонал администрации, и персонал по уходу на дому

- `Doses of vaccines`: refers to the total number of vaccine doses, considering that an additional close may be obtained from each vial (e.g. six doses for Pfizer BioNTech Comirnaty).

относится к общему количеству доз вакциин, включая дополнительзую дозу которую можно получить из флакона


- `Number of doses distributed`: refers to the doses distributed by the manufactures to the country.

- `Number of doses administered`: refers to any individual receiving any dose of the vaccine.

- `Additional dose and boosters`: refer to doses administered after a complete primary course, being them admninistered respectively as an extension of the primary course (e.g. in moderately to severely immunocompromised individuals) or as boosters in individuals who already received a standard primary course (e.g. see footnote with WHO definitions).

- `Weekly data` refer to:
    - Week of vaccine distribution by the manufactures to the country

    - Week of vaccine dose administration to individuals receiving any of the first, second, addtional or unspecified dose


### Data dictionary
_______________________________________________________________________________________________________________________
| Variable      | Definition                                                                                  | Code  |
| ---------     | ---------                                                                                   | ----- |
| YearWeekISO   | Date when the vaccine was received administered. Only weeks are allowed (e.g. “2021-W01”).  | yyyy-Www |
| ---------         | ---------           | -----           |
| ReportingCountry  | ISO 3166-1-alpha-2  | two-letter code |
| ---------     | ---------  | ----- |
|  Denominator  | Population denominators for target groups (total population and agespecific population obtained from Eurostat/UN). Denominators reported by countries for TargetGroup = “HCW” and TargetGroup = “LTCF”. | Numeric |
| ---------           | ---------                                                                                          | -----   |
| NumberDosesReceived | Number of vaccine doses distributed by the manufacturers to the country during the reporting week. | Numeric |
| ---------           | ---------                                                                              | ----- |
| NumberDosesExported | Number of vaccine doses donated or sold by the country during the reporting week.      | Numeric |
| ---------           |                                                                           --------     | ----- |
| FirstDose           | Number of first dose vaccine administered to individuals during the reporting week.    | Numeric |
| ---------           | ---------                                                                              | -----   |
| FirstDoseRefused    | Number of individuals refusing the first vaccine dose.                                 | Numeric |
| ---------           | ---------                                                                              | -----   |
| SecondDose          | Number of second dose vaccine administered to individuals during the reporting week.   | Numeric |
| ---------           | ---------                                                                              | -----   |
| DoseAdditional1     | Number of first additional vaccine doses administered after a complete standard primary course to individuals during the reporting week. | Numeric |
| ---------           | ---------                                                                              | -----   |
| DoseAdditional2     | Number of second additional vaccine doses administered after a complete standard primary course to individuals during the reporting week. | Numeric |
| ---------           | ---------                                                                              | -----   |
| UnknownDose   | Number of doses administered during the reporting week where the type of dose was not specified (i.e. it is not known whether it was a first or second dose). | Numeric |
| ---------           | ---------                                                                              | -----   |
| Region        | As a minimum data should be reported at national level (Region = country code). |  Country/NUTS1 or 2/GAUL1/Country specific |
| ---------           | ---------                                                                              | -----   |
| TargetGroup | Target group for vaccination.  | ALL = Overall adults (18+) Age<18 = Overall adolescents and children HCW = Healthcare workers, LTCF = Residents in long term care facilities, Age0_4 = 0-4 years old, Age5_9 = 5-9 years old, Age10_14 = 10-14 years old, Age15_17 = 15-17 years old, Age18_24 = 18-24 years old, Age25_49 = 25-49 years old, Age50_59 = 50-59 years old, Age60_69 = 60-69 years old, Age70_79 = 70-79 years old, Age80+ = 80 years and over, AgeUnk = Unknown age 1_Age<60 = adults below 60 years of age, 1_Age60+ = adults 60 years and over |
| ---------           | ---------                                                                              | -----   |
| Vaccine | Name of vaccine. Additional vaccines will be added on approval or as requested. | AZ = Vaxzevria – AstraZeneca, BECNBG (previously CN) = Inactivated – Beijing CNBG, BHACOV = Covaxin – Bharat, CHU = Chumakov - Covi-Vac, COM = Comirnaty – Pfizer/BioNTech, CVAC = Curevac-CVnCOV, JANSS = Ad26.COV 2.5 – Janssen, HAYATVAC = Hayat VAC, MOD = mRNA-1273 – Moderna, NVX = Novavax – Covovax, NVXD = Novavax – Nuvaxovid, QAZVAQ = QazCovid-In, SGSK = Sanofi GSK - Subunit, SIICOV = Covishield – SII, SIN = CoronaVac – Sinovac, SPU = Sputnik V – Gamaleya, SPUL = Gamaleya - Sputnik-Light, SRCVB = EpiVacCorona – SRCVB, WUCNBG = Inactivated – Wuhan, CNBG, UNK = UNKNOWN, ZFUZ = Sino-Uzbek - ZF-UZ, VAC |
| ---------           | ---------                                                                              | -----   |
| Population | Age-specific population for the country | Numeric |