#Total Amount Extraction from Bills using OCR
This project aims to extract the total amount from various types of bills using Optical Character Recognition (OCR) techniques. The process involves converting the PDF files into images, extracting text from the images using Google Vision API, and then finding the total amount from the extracted text.

#Table of Contents
-Installation
-Usage
-Methodology
-Conclusion
-Installation

#To use this project, you need to install the following dependencies:

-Wand
-Google Cloud Vision

#You can install these dependencies by running the following commands:

python
Copy code
!pip install Wand
!pip install google-cloud-vision

#You also need to set up a Google Cloud Vision API account and obtain the API key. You can follow the instructions here to set up your account.

#Usage
To use this project, you need to follow the following steps:

-Place the PDF files in the "input" folder.
-Run the "ConvertPDFToImage.ipynb" notebook to convert the PDF files to JPEG images.
-Run the "ExtractText.ipynb" notebook to extract the text from the images using Google Vision API.
-Run the "FindTotalAmount.ipynb" notebook to find the total amount from the extracted text.
-The total amount will be displayed on the screen and saved to a text file in the "output" folder.

#Methodology
-In the first step, the Wand library is used to convert the PDF files into images. This step is necessary because Google Vision API requires an image as input. The PDF files in the input folder are converted to JPEG images and saved in the output folder.

-In the second step, Google Vision API is used to extract text from the images. The extracted text is saved to a text file in the output folder.

-In the third step, the total amount is found from the extracted text. Initially, all the digits in the text file were listed, and the maximum was taken from each list. This approach gave an accuracy of 99.8%. However, some bills had an option to provide change, resulting in errors in the extraction process. To overcome this, all the digits in the text were added, and the sum was checked if it was present in the list or not. This approach gave an accuracy of 99.92%.

#Conclusion
In conclusion, this project demonstrates how OCR techniques can be used to extract the total amount from various types of bills. The approach involves converting PDF files to images, extracting text from images using Google Vision API, and finding the total amount from the extracted text. The accuracy of the approach can be improved further by considering various scenarios like change, discount, and taxes.
