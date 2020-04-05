DataWarrior(abbr. DW) is "A Free Cheminformatics Program for Data Visualization and Analysis".
- DW's website: http://www.openmolecules.org/datawarrior/index.html
- DW's forum: http://openmolecules.org/forum/index.php?t=index
  - DW is actively maintained. You can raise questions to the developers. I posted several questions, and they were either answered or fixed quickly, much appreciated.

After some practices of DW, I feel it is a very good tool to MedChem research. And I'd like to share my experiences here.


## Practice
    Case study
        ChEMBL data analysis
            DW = DataWarrior
            Search target
                FXR
            Download data from ChEMBL
                Binding data
                Efficacy data
            Preprocess the download data
                replace '";"' by ‘","’
            Load data into DW
                Binding data
                Append
                    Efficacy data
                Create new from> pivoting
                    o
                    Group rows sharing
                        CHEMBL ID
                        Structure of smiles
                    Split columns by
                        Standard Type
                    Data columns(s)
                        Standard Value
                    o
            Set columns
                Data>Treat Logarithmically
                    o
    SAR analysis
        Correlation analysis of 2D plot
            2D plot
                right click at a 2D plot
                    Set Statistical View Option
                        o
        Calculate chemoinformatics parameters
            logP
                o
            logS
            PSA
            number of 
                Hbond
        Core based SAR analysis
        Not yet available
            Matched molecular pair
    Select columns
        hide columns
    Data operations
        Copy rows(contains 2D, 3D and reaction) and paste to table
            Ref
                openmolecules.org > Forum > Index ? ... <http://openmolecules.org/forum/index.php?t=msg&th=255&start=0&>
            Update
                3/19/2020
                Available only after v5.2.1
            How-to
                Select some rows you want to copy, right click on one of the selected rows, then click "Copy Selection Without Header"
                    o
                    o
                Add a new empty row
                    o
                    o
                Disable all filter to show the added empty row
                    o
                Right click on the 1st cell of the added empty row, click "Paste Into Table"
                    o
                Done
        Add a calculated column
            concatenate string
                "20200304_"+str(Index)
                    str(Index)
                        Index is a integer, it must be converted to a string before operation
            log10()
                log(Activity)
    Visualization
        Align 2D structures
            Chemistry>Generate 2D Atom Coordinates
                Draw one or more scaffolds, click "OK"
            o
        Form view
            o
        Add label to structure grid
            o
        Histogram
            add "Bin" column
                o
            switch to "Bar chart"
        Jump to selected row in table view
            double click the structure in grid view or dot in 2D scatter plot
            o
    Input / output
        Pivot data <#ID_744569315>
        Update data
            Method 1
                Maintain a CSV file as data source, update the CSV file, then load the updated CSV file into DataWarrior
            Method 2
                Open dwar file
                File>Merge File
                Disable all filters
                Delete properties calculated by DataWarrior
                Calculate the properties
        Export images
            o
                o
            default
                Copy image to clipboard
                    Use transparent background
