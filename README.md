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
This edition is first and foremost eclectic and genealogical. My reasons for pursuing this method are two fold. Firstly, given the intense variance present within a text as legalistic as the _Admonito_, I could not logically prefer a Bédier best-text edition. This logical necessity to praise the variant itself derives from my focus on capturing the whole 'text' of the abstract 'work'. In this case, there is an idea of the 'work', i.e. the _Admonito Generalis_, and the actual text of the 'work' and in works with more than one manuscript, the text is invariably going to vary. Secondly, the current standard edition of the _Admonito_ is the _Monumenta Germaniae Historica_'s edition as prepared by Hubert Mordek, Klaus Zechiel-Eckes and Michael Glatthaar, contain elements that do not translate easily to a clean page along with stylistic representation choices that leads to a 'noisy' text. For example, the current digital _MGH_ edition contains italicization elements which are not represented within the manuscripts and instead derive from editorial intervention. As for the apparatus and it's connection to a 'clean' page, within the actual text of the _Admonito_ nearly half of each page is covered by extensive footnotes denoting variants and connections among other information.[^1] Therefore, with my presentation of the text, both of these issues are rectified. I do not present elements within the edition that are themselves not represented in the manuscripts, therefore extensive punctuation and italicizaiton are absent from this edition. Furthermore, because of the .xml coding, I am able to present all the information present within the footnotes within the text through tooltips. Therefore, this allows for those who are not wholly interested in the manuscript variation to have a more fluid reading experience while still containing all the information for those who are interested in the variations. This is not to say that there has not been extensive effort on the _MGH_'s part to include new digital tools in the representation of the text. For example, the openMGH project seeks to encode the various editions into TEI .xml documents. Yet it remains to be seen the progress of this project and which editions they started with, as at the time of writing this readme, the .xml repository is down or at the very least inaccessible on my end. 

The _MGH_'s edition concerns itself with many more manuscripts than this edition's six manuscripts. In choosing the manuscripts for this edition I had several qualifications. Firstly, the manuscript had to be available digitally. Secondly, based on the stemma constructed by the _MGH_, I decided not to choose any manuscripts which were completely unrepresentative of the text or those which most 'accurately' represented the text, thereby affording me a middle slice of information. In selecting the manuscripts, I did not rely on any random selection principle but rather went through the list of manuscripts that pertain to the _Admonito_ and chose them by hand. While this does invite tremendous bias into the presentation of the text, I only claim to offer a slice of information rather than the whole pie. Thirdly, the manuscripts each had to start in the same place. In practice, this means the manuscripts had to beging with _capitulum_ one and continue for enough length to satisfy the word count requirements. There are presently over fifty manuscripts and manuscript fragments which in some way relay the text of the _Admonito_. This could be as little as a table of contents to an actual copy of the text. The reason so many manuscripts and fragments exist for this one particular text will be explored in the Historical Context section. For the future, I do wish to expand this project beyond the confines of a final assignment, and in turn include more manuscripts, yet this test project still laid the groundwork in terms of structure and method. 

The earlier discussion of 'work' and 'text' deserve further clarification as it pertains to this edition. A guiding principle behind the construction of this edition was the separation between work and text as it is a fundamental truth of editorial scholarship that in the presence of more than one manuscript of the same 'work', there will be variation. My approach to texts therefore is necessarily informed by a Tansellian framework that establishes texts as artifacts and work as abstract.[^2] This approach however has broad implications. Namely, I do not seek to present an authoritative and critical edition of the _Admonito_. Rather, it is my aim to present the information present within the manuscripts in a detailed, readable, and usable manner while minimizing my role as editor as stated earlier with the lack of punctuation and other forms of intervening representations. All of the manuscripts were treated in some way as pertaining to the idea of the 'work' of the _Admonito_ whereas the actual 'text' inevitably has, at times, substantial variations. Therefore, when considering the production of legalistic texts, much in the same way of literary texts, scribes transcribed variations whether willingly or unknowingly which forms the center of this edition. 

Regarding my edition itself, I have referred to it as both eclectic and genealogical. Translating this to actual editing is as follows: I do not rely on one single manuscript as the 'base' manuscript in order to reconstruct the text and I have, as will be explored, relied on the stemma tree as the main indicator for which word or variant is more representative. For those of you who are interested, you can click on this link: () to see the actual process of how I constructed the stemma tree, with the sheets at the bottom corresponding to the order of operations as it were. Firstly, I began with transcribing the text of the manuscripts from in the order from left to right, beginning with Munich, Clm. 14468 and ending with Paris, Lat. 10758. To streamline the tracking of variations, I color-coded the instances of variations based on their type. For example, misspellings received a light blue where as actual word variations received a light yellow or orange, and when omissions occured I darkened the corresponding boxes. With the manuscripts fully transcribed, I then began on recension. For most instances, depending on the variations and their proximity, the variations either received a 1 or 0 depending on whether or not they possesed a specific variation. It is important to note that I drew no distinction between genealogically relevant and genealogically irrelevatn information, therefore misspellings were counted as genealogically relevant variations in contrast to Schøsler's conceptions.[^3] In other cases, I combined variations together that were similar enough. Finally, after each manuscript received a one or zero for its variations, I had to calculate the distance between these manuscripts. The string of 1's and 0's correspond to the manuscript's vector in an abstract literary space and to calculate the distance between manuscripts, I relied on euclidean distance. While it would be interesting to see how the stemma tree would have been constructed had I chosen a different distance formula, the euclidean distance is the simplest and most straight forward. From here, according to the distance, I paired the closest manuscripts together in which the first pairing was P1 and P2, followed by M1 and M2, then P(1+2) and G, and finally P(1+2)G with V. In combining the manuscripts for the purposes of the distance calculation, I found the average points between the two manuscripts. For example, if P1 had a variation but P2 did not, then the corresponding number for the combined manuscript would be 0.5. This entire process led to the creation of the stemma tree shown here:

![alt text](https://github.com/CTaylor01/TheAdmonitoGeneralisProject/blob/main/Stemma%20Tree.png?raw=true)

Finally, it was time to reconstruct the ideal version of the work. Using the stenna tree, I went through word by word choosing the word that is most representative of the work according to its place on the tree. Starting with 1 at the omega symbol, I divided by two for each branch of the stemma tree which formed the likelihood that the specific word was the 'original' or 'ideal' word for a given spot. This thus formed the lemma of the text or the base representation of the text, with the variations which were found not to be the 'right' fit, I encoded them as readings of the lemma. Therefore, there is a usable and visual text that readers can interact with, but if they want more information on why a particular word was chosen over others, they can hover over the red words to show variations. What is left then at the end is a relatively clean text in which all the manuscript evidence is encoded into the text itself. 

With the process established, it is ever prudent to turn towards disparities between digital and traditional editions and their defining characteristics. While I largely contrast this edition with the _MGH_'s, it is worth noting that the current edition of the _Admonito_ is available digitally through the _MGH_. But there are several extant issues with denoting an edition as 'digital' and one as 'traditional' which largely rests on how a person defines the two. For the digital editions, one could define them simply as whether or not they are available on the computer. Taking this definition and applying it to the _MGH_ holds true, it is in fact a digital edition of the _Admonito_. This is directly involving the current 'standard', or at least what the _MGH_ considers to be the official, and in no way referencing the work of the openMGH project. Yet this definition leaves several unresolved issues, namely that there exists little user interaction, outside of a search function, within the page and rather the digital edition is itself similar to a photo of the page as it appears in the print copy and presented online. Yet this matter of definitions cannot be resolved so easily. If we change the definition of a digital edition to say that it must include x or y element then we necessarily engage in exclusionary scholarship which seeks more to discredit than collaborate. One possible solution to this conundrum is to instead present the nature of digital editions on a scale rather than as binaries. Therefore, we can comfortably place the _MGH_ edition on the more conservative side of the scale regarding the possibilities of digital editions and then place this current edition more so towards the exploratory side regarding the use of technology. I am by no means the first person to present this issue of digital and traditional editions, as Appolon and Bélisle present the "explosion" of traditional editorial scholarship in the wake of the digital edition.[^4] While this process of digitization will undoubtedly uproot some, if not most, of the longstanding pillars of editorial and textual scholarship, it also opens up a plethora of pathways that can only add to the relationship between text, editor, and reader. 

[^1]: _Die Admonitio Generalis Karls Des Grossen_, _Fontes Iuris Germanici Antiqui in Usum Scholarum Separatim Editi_, _Monumenta Germaniae Historica_, eds. Hubert Mordeck, Klaus Zechiel-Eckes, and Michael Glatthaar. (Hannover: Hahnsche Buchhandlung, 2012). 
[^2]: G. Thomas Tanselle, "The Varieties of Scholarly Editing," in _Scholarly Editing: A Guide to Research_, ed. D. C. Greetham (New York: MLA, 1995): 10.
[^3]: L. Schøsler, "Scribal Variations: When are they Genealogically Relevant-and when are they to be considered as instances of 'mouvance'?" in _Studies in Stemmatology 2_, eds. Pieter van Reenen, August den Hollander and Margot van Mulken (Philadelphia: J. Benjamins, 2004): 207.
[^4]: D. Appolon & C. Bélisle, "The Digital Fate of the Critical Apparatus" in _Digital Critical Editions: Topics in the Digital Humanities_, eds. Daniel Apollon, Claire Bélisle, and Philippe Régnier (Champaign, IL: University of Illinois Press, 2014), 106.
# Historical Context

# Scholarly Tradition

# Bibliography

# Credits
I am grateful for Frances Eshleman, History Ph.D. Student at Fordham, for providing the documentation on creating .odd files and the various ways to reconfigure the display of text. I also must give credit to the Siege of Antioch Project Team at Fordham University for teaching me the basic formatting of an .xml file, and I largely follow the code guidelines established by this project to recreate the Admonito Generalis. The python code for calculating Euclidean distance between points comes from 2LT Dylan Taylor, MSECE at Purdue University.

