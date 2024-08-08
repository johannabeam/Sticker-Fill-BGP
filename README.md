## Automatically filling sticker templates for sample tubes
This is code made to automatically fill [LabTag](https://www.labtag.com/resources/templates/letter-us-8-5-x-11/) sticker templates for extracted DNA sample tubes and tissue/blood sample tubes. The format used for the stickers is the standard way that the [Bird Genoscape Project](https://www.birdgenoscape.org/) makes their stickers for storage. Lab Tag makes sticker paper templates that can be used safely around chemicals and freezers, making sure that your sample information will never be lost or erased from the tube.

### Before Running
Make sure your input datasheet is saved as a UTF-8 encoded csv so that spaces are properly encoded. Also, if the templates you download from LabTag are doc files, re-save them as docx files so they can be properly read by the python package.

### First code section
The first section of code makes stickers for the side of the tubes, which inlcude specific information that the BGP uses to identify their tubes. These are the alpha code for the species of bird, sample type, band number of the bird, date of extraction, and location from which the sample came. The template used is the US-12 from LabTag. 
### Second code section
The second section of code makes stickers for the top of the tubes, which can only fit the species and the BGP ID, but the BGP must be split onto two lines based on the position of the 'N' in the ID. The template used is the US-5. 
### Third code section
Finally, the last section of code makes stickers just for the top of the tissue/blood tubes, which have smaller lids than the final extraction tubes. These can just fit the BGP ID, once again split onto two lines. You can of course change what the code prints to the template if you need it to print something else. The template used is the US-10 from LabTag. 
**IMPORTANT TO NOTE** This template (at least the one I am using) is a bit funky. You only fill every other cell (the large squares) and every other row. This code will do that for you. Just be sure that your template fits this format!

Eventually, I will make the code run so that you input variables and it will run, but that's not something that I have time to do at the moment. 
Another thing that I will want to code in is skipping a certain # of rows when filling the sheet. That way partially used sticker sheets can be used just by specifing the number of rows to skip before starting to fill.
