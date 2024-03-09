
1.	Objective:
The objective of this automation process is to read medical text from an Excel file, extract drug names using the Hugging Face API, and update the extracted drug names in the Drugs column of the same Excel file.
2.	 Process Steps:
   
a.	Input Data Acquisition:
	Input: Excel file containing medical text.
	Output: Drugs name found in the text to be extracted.

b.	Reading Medical Text from Excel:
	Activity: Excel Scope
	Description: Utilize the Excel Scope activity to read the medical text from the Excel file one by one.
	Input: Path of the Excel file containing medical text.
	Output: Medical text read from the Excel file.


c.	Extracting Drug Names using Hugging Face API:
	Activity: HTTP Request
	Description: Use the Hugging Face model (d4data/biomedical-ner-all) to extract drug names from the medical text.
	Input: Medical text. Hugging Face API
	Authentication: OAuth2 (Passing Hugging face token)
	Output: Extracted drug names.


d.	Updating Extracted Drug Names in Excel:
	Activity: Write Excel Activity
	Description: Update the extracted drug names in the Drugs column of the Excel file.
	Input: Extracted drug names and corresponding rows in the Excel file.
	Output: Updated Excel file with drug names.

