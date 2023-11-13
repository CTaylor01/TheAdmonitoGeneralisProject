# Introduction
This is a new digital edition of the first seven _capitula_ of the Admonito Generalis as prepared by Cole Taylor, a History Ph.D. Student at Fordham University. This github serves as a repository of the .xml and .odd files necessary for deployment to TEIPublisher as well as the code and files that constructed the .xml edition. As I learn more coding, I plan on having a full display of the text using TEIPublisher embedded within a website which can accurately display the text as intended. This project serves as the final assignment for Dr. Brian Reilly's course _Editing Medieval Texts_ at Fordham University. What follows is how to use the files, my research methods, the historical context of the text, and the scholarly tradition of the text. For these subsections, full bibliographic information is provided for corresponding references in the bibliography subsection.

# Using the Files
If you would like a more visual representation of the text, outside of reading .xml code, follow the steps below:
  1. Navigate to https://teipublisher.com/exist/apps/tei-publisher/index.html
  2. Log in with the username: "tei-demo" and password: "demo" (Do not include the quotations when signing in)
  3. Scroll down to the bottom of the page and enter a file name and title for display (these can be anything you wish) then click create. You will now see your .odd at the bottom of the long list, click the pencil/pen icon which will take you to the .xml of the .odd.
  4. CTRL+A and delete the text, then copy the text from the style sheet provided by this repo and paste all of it into the file, be sure to click save at the top.
  5. Navigate back to the TEI Publisher tab and click on 'Playground' and click the Upload button on the right, select the Admonito Generalis.xml file to upload
  6. You should now see the edition on the screen, click the title of the edition to access the digital edition.
  7. Click on the three lines to the far right (below where it says logged-in as tei-demo) and under 'select ODD' select the .odd you created and then click out to return to the edition.
  8. You should now have a visual representation of the edition that represents what I will (eventually) have hosted on a website, removing all these steps to access a visual version of the edition.
  9. Do note that the tei-demo account is a **public** account, meaning that other people can view and access the .odd and .xml that you upload as part of these steps. In order to keep the tei-demo account clean, I recommend you remove the uploaded .xml and .odd files after you have finished viewing the text.

The python file provided can also be used to run your own calculations of Euclidean distance, simply change the Matrix and MatrixNames to your preference as well as the matrices themselves with their corresponding points. For example, change V = [0,1,1....] to the corresponding point and sigla, and change the matrix = [V, M3, P3G] to the sigla you use to identify the point. Then, change matrixNames = ['M3', 'V', 'P3G'] to the corresponding sigla. Be sure to keep the apostrophes and commas that define the sigla.
## Research Methods
This edition is first and foremost eclectic and genealogical. My reasons for pursuing this method are two fold. Firstly, given the intense variance present within a text as legalistic as the _Admonito_, I could not logically prefer a Bédier best-text edition. This logical necessity to praise the variant itself derives from my focus on capturing the whole 'text' of the abstract 'work'. In this case, there is an idea of the 'work', i.e. the _Admonito Generalis_, and the actual text of the 'work' and in works with more than one manuscript, the text is invariably going to vary. Secondly, the current standard edition of the _Admonito_ is the _Monumenta Germaniae Historica_'s edition as prepared by Hubert Mordek, Klaus Zechiel-Eckes and Michael Glatthaar, contain elements that do not translate easily to a clean page along with stylistic representation choices that leads to a 'noisy' text. For example, the current digital _MGH_ edition contains italicization elements which are not represented within the manuscripts and instead derive from editorial intervention. As for the apparatus and it's connection to a 'clean' page, within the actual text of the _Admonito_ nearly half of each page is covered by extensive footnotes denoting variants and connections among other information.[^1] Therefore, with my presentation of the text, both of these issues are rectified. I do not present elements within the edition that are themselves not represented in the manuscripts, therefore extensive punctuation and italicizaiton are absent from this edition. Furthermore, because of the .xml coding, I am able to present all the information present within the footnotes within the text through tooltips. Therefore, this allows for those who are not wholly interested in the manuscript variation to have a more fluid reading experience while still containing all the information for those who are interested in the variations. 

The earlier discussion of 'work' and 'text' deserve further clarification. 

Regarding my edition itself, I have referred to it as both eclectic and genealogical. Translating this to actual editing is as follows: I do not rely on one single manuscript as the 'base' manuscript in order to reconstruct the text and I have, as will be explored, relied on the stemma tree as the main indicator for which word or variant is more representative. For those of you who are interested, you can click on this link: () to see the actual process of how I constructed the stemma tree, with the sheets at the bottom corresponding to the order of operations as it were. Firstly, I began with transcribing the text of the manuscripts from in the order from left to right, beginning with Munich, Clm. 14468 and ending with Paris, Lat. 10758. To streamline the tracking of variations, I color-coded the instances of variations based on their type. For example, misspellings received a light blue where as actual word variations received a light yellow or orange, and when omissions occured I darkened the corresponding boxes. With the manuscripts fully transcribed, I then began on recension. For most instances, depending on the variations and their proximity, the variations either received a 1 or 0 depending on whether or not they possesed a specific variation. In other cases, I combined variations together that were similar enough. Finally, after each manuscript received a one or zero for its variations, I had to calculate the distance between these manuscripts. The string of 1's and 0's correspond to the manuscript's vector in an abstract literary space and to calculate the distance between manuscripts, I relied on euclidean distance. While it would be interesting to see how the stemma tree would have been constructed had I chosen a different distance formula, the euclidean distance is the simplest and most straight forward. From here, according to the distance, I paired the closest manuscripts together in which the first pairing was M1 and M2, followed by P1 and P2, then P(1+2) and G, and finally P(1+2)G with V. In combining the manuscripts for the purposes of the distance calculation, I found the average points between the two manuscripts. For example, if P1 had a variation but P2 did not, then the corresponding number for the combined manuscript would be 0.5.

With the process established, it is ever prudent to turn towards disparities between digital and traditional editions and their defining characteristics. While I largely contrast this edition with the _MGH_'s, it is worth noting that the current edition of the _Admonito_ is available digitally through the _MGH_. But there are several extant issues with denoting an edition as 'digital' and one as 'traditional' which largely rests on how a person defines the two. For the digital editions, one could define them simply as whether or not they are available on the computer. Taking this definition and applying it to the _MGH_ holds true, it is in fact a digital edition of the _Admonito_. Yet this leaves several unresolved issues, namely that there exists little user interaction, outside of a search function, within the page and rather the digital edition is itself similar to a photo of the page as it appears in the print copy and presented online. 

[^1]: _Die Admonitio Generalis Karls Des Grossen_, _Fontes Iuris Germanici Antiqui in Usum Scholarum Separatim Editi_, _Monumenta Germaniae Historica_, edited by Hubert Mordeck, Klaus Zechiel-Eckes, and Michael Glatthaar. (Hannover: Hahnsche Buchhandlung, 2012). 

# Historical Context

# Scholarly Tradition

# Bibliography

# Credits
I am grateful for Frances Eshleman, History Ph.D. Student at Fordham, for providing the documentation on creating .odd files and the various ways to reconfigure the display of text. I also must give credit to the Siege of Antioch Project Team at Fordham University for teaching me the basic formatting of an .xml file, and I largely follow the code guidelines established by this project to recreate the Admonito Generalis. The python code for calculating Euclidean distance between points comes from 2LT Dylan Taylor, MSECE at Purdue University.

