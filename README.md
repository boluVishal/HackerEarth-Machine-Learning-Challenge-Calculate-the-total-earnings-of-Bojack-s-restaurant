Readme for Total Amount Extraction from Bills
This project aims to extract the total amount from various types of bills using Optical Character Recognition (OCR) techniques. The process involves converting the PDF files into images, extracting text from the images using Google Vision API, and then finding the total amount from the extracted text.

Step 1: Convert PDF to Image
In the first step, I used the Wand library to convert the PDF files into images. This step is necessary because Google Vision API requires an image as input. I converted all the PDF files in the test set into JPEG images.

Step 2: Extract Text from Images
In the second step, I used Google Vision API to extract text from the images. I saved all the extracted text to text files. This step is crucial because I need to find the total amount from the text.

Step 3: Find Total Amount
In the third step, I found the total amount from the extracted text. Initially, I observed that all the total variables are floating numbers. Hence, I listed all the digits in the text file and took the maximum from each list. This approach gave me an accuracy of 99.8.

However, I analyzed the errors and found out that some bills had an option to provide change, resulting in errors in the extraction process. To overcome this, I added all the digits in the text and checked if that was present in the list or not. This approach gave me an accuracy of 99.92.

Conclusion
In conclusion, this project demonstrates how OCR techniques can be used to extract the total amount from various types of bills. The approach involves converting PDF files to images, extracting text from images using Google Vision API, and finding the total amount from the extracted text. The accuracy of the approach can be improved further by considering various scenarios like change, discount, and taxes.
