# Juneau Empire Index

In a facebook group recently an archive of a local paper was published.  Using the front page of the first page I have put together an OCR tool to see how easy it would be to pull string data from the .pdfs. I used an online tool to convert the first page from .pdf to .png.  I also fooled around with the image settings to see how much the results of text extraction would change. 

Nearly the entire implementation comes from small modifications suggested by this post:

https://stackoverflow.com/questions/10947399/how-to-implement-and-do-ocr-in-a-c-sharp-project

I believe in order to improve the extraction of text the following could be performed:

1. Image processing
2. Improving training data (let it know what fonts are used, tell it what the results are, I don't know Tesseract...)

If fairly reliable text were able to be extracted it would be trivial to tokenize and index with something like Solr or Elastic and make a searchable archive. 

Feel free to try for yourself.  You'll need to put the english training data (all files in screenshot) in the tessdata directory in the project. 

![Training Data](https://github.com/craigmillard/Juneau-Empire-Index/blob/master/Ocr/Ocr/Required%20Tesseract%20Files.PNG)

# Attribution for Tesseract
```
Name: Tesseract OCR engine
Source: https://github.com/tesseract-ocr/tesseract
License: Apache license 2.0 (below)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
# Results: 

## First Attempt
![Front Page Original](https://github.com/craigmillard/Juneau-Empire-Index/blob/master/Ocr/Ocr/Newspaper/pngs/front-page-original.png)
![Console Output](https://github.com/craigmillard/Juneau-Empire-Index/blob/master/Ocr/Ocr/Newspaper/pngs/First%20OCR.PNG)

## Second Attempt
![Front Page Edited](https://github.com/craigmillard/Juneau-Empire-Index/blob/master/Ocr/Ocr/Newspaper/pngs/front-page-updated.jpg)
![Console Output](https://github.com/craigmillard/Juneau-Empire-Index/blob/master/Ocr/Ocr/Newspaper/pngs/Second%20OCR.PNG)

