### What I got
- A table, with the victim as the unit
- Scraped PDFs arranged by working progress
- 4 out of 5 regions are annotated

### Expectation
- To establish the relation between table records and saved PDFs (done)
- Cleaned text for fine-tuning (not done)

### Current Status
- Rearranged the table to be victim-source, for better linkage between records and files
- Populated the last region and merged with the final table ([victims_sources_reorganized.csv](victims_sources_reorganized.csv)) 
- Rearranged the PDFs in region/victim structure rather than working progress ([GitHub repository](https://github.com/xingyuanzhao-project/UMN-ODIM-Data-Cleaning))
- Rescraped lost files, so that 3422 out of 4267 (80%) victim-source pairs are restored, having correct files linking to the records 
- Preliminary cleaning of the PDFs using Docling and OlmOCR


### Issues
- Original table unit is not suitable for building record-file relation (solved)
- Files are not structured in a way that can be easily tracked (solved)
- PDFs cannot be traced back to records (solved)
- Lost files (recovered partially)
- One region (Veracruz) is not annotated (not solved)
- PDFs contain content that is not related to the topic, such as ads, comments, placeholders, i.e. links and descriptions for other articles (Coahuila\Bertha Alicia Z P), comment section (Coahuila\Abel M H), or contact information (Coahuila\Bernando A) (not solved. Docling and OlmOCR can only identify some of them with no 100% guarantee. **Even if these elements are solved, there will be more problems identified in the future**)

### What Could Have Been Done Differently
- Rescraping everything at the beginning would have saved massive time. Reverse engineering is more costly than having a clean start

### Steps and Options for Future Researchers

1. Getting Clean Text Files
- Option 1: select the "cleaner" PDFs
    - Pro: 
        - Files are readily available
    - Con: 
        - Only a very small fraction of the files will be used. 
        - Picking out "cleaner" files may take an unknown amount of time and may require manual labor.
- Option 2: rescrape all available links and save them as HTML files.
    - Pro: 
        - A clean start
        - More files compared to selecting cleaner PDFs
        - Timeline is more predictable and controllable
    - Con: 
        - Some links might be broken

2. Cleaning 
   - If using only the "cleaner" PDFs, Docling should do the job IF these PDFs are truely "cleaner". 
   - If taking the total rescraping route, select the correct elements from the HTML files.

3. Fine-Tuning Using Shreya's Framework



