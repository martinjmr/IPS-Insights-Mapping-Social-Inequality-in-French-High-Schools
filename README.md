IPS Insights: Mapping Social Inequality in French High Schools

A data analysis project studying how a French high school's Indice de Position Sociale (IPS) — an official measure of its students' socio-economic background — relates to academic success, social reproduction, and geography. The title nods to Bourdieu and Passeron's Les Héritiers (The Heirs), whose central question — does school reward merit, or does it simply reproduce social position? — frames the analysis.

Context

The IPS is computed from the occupation and education level of students' parents, averaged at the school level. Created in 2016 by the French Ministry of Education and made public in 2022, it serves as a proxy for a school's socio-economic environment. This project asks: does a student's future depend on their social origin, or on their own school path? Are geography, access to culture, and family income determining factors in academic and professional success?

Structure
Social position and parental income — the primary drivers of educational inequality and family orientation strategies, illustrated with an interactive world map of every French high school's IPS
Case study: Sciences Po Paris — social composition of admitted students across the three admission tracks (standard exam, international, CEP)
Access to culture as a determinant of success — cultural practice data by parental occupation and education level; case study on École Polytechnique's candidate demographics
Case study: Overseas territories (Outre-Mer) — schooling rates and diploma levels in Mayotte, Réunion, and Guyane
IPS and the public/private divide — distribution, mean, and median IPS by sector, with a Paris case study
Case study: the Dauphine IASO dual-degree cohort — the author's own class, compared against the national IPS average
General/technological vs. vocational tracks — IPS gaps and their link to family orientation strategies
Evolution of IPS over the last five years
Data
Variable	Source
general_data	Annuaire de l'éducation — school directory, incl. GPS coordinates
ival_data	Indicateurs de résultat des lycées — pass/distinction rates
ips_data	IPS lycées (ap2022) — social position index per school
ips_data_full	IPS lycées, multi-year — for the 5-year evolution analysis
eloignement_data	Indice d'éloignement — distance from infrastructure
department boundaries	france-geojson.gregoiredavid.fr
Polytechnique, Sciences Po, INSEE culture figures	Manually collected from published reports (cited inline in the notebook)
dl_data	The author's own class roster — not included

All government sources are official open data (Licence Ouverte / Etalab) with stable export URLs, so they aren't bundled in this repo — the notebook downloads them directly.

Tech stack

pandas · matplotlib · seaborn · geopandas · folium / mapclassify (interactive maps)

Project structure
.
├── Analyse_IPS.ipynb   # Main notebook (full analysis, executed with outputs)
├── data/               # Only non-sensitive, non-redistributable inputs (see Data section)
└── README.md
Usage
bash
pip install pandas matplotlib seaborn geopandas folium mapclassify
jupyter notebook Analyse_IPS.ipynb

The notebook is committed with its outputs already run — the charts, correlation matrices, and interactive maps render directly on GitHub without needing to re-execute anything.

Key findings
Parental income and CSP (socio-professional category) strongly shape family orientation strategies and investment in children's education
IPS correlates positively with baccalauréat distinction rates, further-study rates, and access to culture
Elite institutions (École Polytechnique, Sciences Po) draw disproportionately from higher-CSP, higher-IPS backgrounds
Overseas territories (Mayotte, Réunion, Guyane) show markedly lower IPS and higher rates of early school-leaving, alongside a preference for shorter studies
Private schools have a consistently higher IPS than public schools, correlated with a mostly urban geographic footprint — with the North of France a notable exception
Vocational-track schools have lower and less dispersed IPS than general/technological schools
National average IPS rose modestly, from about 102.7 in 2016 to 104 in 2021
