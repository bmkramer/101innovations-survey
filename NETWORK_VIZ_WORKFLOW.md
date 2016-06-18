# Description of workflow used to create network visualization of tools used together
- taking on [issue #11] (https://github.com/bmkramer/101innovations-survey-data/issues/11)
- using [Gephi] (https://gephi.org/) as visualization tool
- for preset answer options only

## Source files
- co-occurrence matrix (created with [frequencies_of_bivariate_tool_use.R] (https://github.com/bmkramer/101innovations-survey-data/blob/network_viz/frequencies_of_bivariate_tool_use.R)): [survey_presets_frequencies.csv] (https://github.com/bmkramer/101innovations-survey-data/blob/network_viz/survey_presets_frequencies.csv)
- tool variables coupled with GEO and TMIE classification (to be used as modularities in network viz): [coupling_variables_toolID_TMIE_GEO.csv] (https://github.com/bmkramer/101innovations-survey-data/blob/network_viz/coupling_variables_toolID_TMIE_GEO.csv)

## Step 1: Convert co-occurrence matrix for import in Gephi
Clean co-occurrence matrix for import in Gephi as described here: https://github.com/gephi/gephi/issues/1143.

This will require some permutations that would be great if coded into R (but I'll probably do them in Calc for now):

1) Replace column names in first row with sequential numbers (as in first column), remove last column (with names)
This will create a csv that can be imported in Gephi and will be automatically processed into an edge table

2) Create separate csv with sequential numbers, names (e.g. current first and last column). Add columns for research activity, research phase, TMIE en GEO classification
This csv can be imported into Gephi as node table. 
