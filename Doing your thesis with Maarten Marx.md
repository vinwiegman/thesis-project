# Doing your thesis with Maarten Marx

Hi, happy to supervise your thesis. I supervise quite a number of students and created a system to do this smoothly and with high chance of success. Here we go:

2. Create a **private** github repo for your thesis and invite me (`maartenmarx`) and, if you have , your other supervisors.
3.  Register yourself at <https://forms.gle/XNhBL3nLdswZ7jTG7>



## Your Github repo

THis contains **everything related to your thesis**, nicely organized in folders.


1. This document as a markdown file, in a prominent place.
1. A folder for the Latex files of your thesis, including the pdf.
    2. If you work on Overleaf, you can link that account to your repo
    3. If you work on Overleaf, put the URL large in your README.md
3. A folder with notebooks containing experiments, etc
4. Maybe a literature folder
5. A personal folder with information about yourself, like e.g., your CV and your gradelist and whatever more you want to share with me.  
    * This helps me to personalize your thesisproject to your background and interests, and to create a projectplan with highest chance for success and grade. 
    * **Sharing this personal information is by no means an obligation. Only share those things that you are comfortable with.**
6.  [Great github repo template at the Gemeente Amsterdam](https://github.com/Amsterdam-Internships/InternshipAmsterdamGeneral)


### Overleaf

* New in 2022: [Templates for the master IS](https://www.overleaf.com/read/bctyrsjktnrx) (for thesis design, reports and the final thesis). This is a read only link. Download the source and start a new project with it.
* Other studies have their own thesis templates, and templates for other documents. Get to know them at once and get familiar with them.

Many of you prefer overleaf for their thesis. I am fine with that, but please stick to these guidelines to keep you orgamized and me sane

1. Put the URL to your main overleaf file (the one that complies to your thesis) LARGE in your github readme.
2. Organize your overleaf project well, as follows:
3. Create directories for 
    4. images
    5. preamble and style files
    6. sections
        7. For each section you create a seperate file which you include in `main.tex` at the top level.
        8. I suggest to use [the subfiles package](https://www.overleaf.com/learn/latex/Multi-file_LaTeX_projects), which is really nice and easy, and saves a lot of hassle.
    9. bib stuff
8. Top level contains `main.tex`  and the folders, and I guess that is it.


# How to make and keep everyone happy 
* Read, read, reread and use it daily in everything you do, but first of all in all you comunicate, [this advice by Eamonn Keogh ](https://www.cs.ucr.edu/~eamonn/public/SDM_How_to_do_Research_Keogh.pdf):

> If you can save the reviewer one minute of their time, by spending one extra hour of your time, then you have an obligation to do so. [page 75]



#### Thesis itself

1. Follow provided templates of your study.  
2. Use `\tableofcomntents`, `\hyperref` and **number lines and pages** with `\usepackage{lineno} \linenumbers`.
3. Make seperate files for each section and clean folders and include the files in a `main` tex document
4. If you use Overleaf, set the url to the main tex file large in your `readme.md` on github (then I can find it back).





## Weekly updates

Every week before Friday 09:00 you post a new issue entitled *update `the date of today`* , where you @-mention me and in which you describe 

* what you have achieved,
    *   with hyperlinks to the notebooks or pdf (indicate exactly where) in which this is reported
*   what did **not** work out
*   what you plan to achieve next week
*   if you want to ask me something/discuss something
    *   clearly stated questions/discussion points
    *   preferably with hyperlinks to material/notebooks

## Communication and meetings

* **All communication is via github issues in which you mention or assign me.**
    * I tend to react quickly, and try to help your continue your work.
    * If you have a question or want me to help you (eg get feedback on a section), make an issue, @mention me, and make it very clear what you want from me. 
        * *I like to have feedback on section 4.* is not a good issue or question. Make your problem precise and direct me exactly to that paragraph or line numbers you want advice on. Really state a clear question for which you want an answer. All this ensures better and faster feedback from my side.
* Biweekly zoom or in person meetings on either a fixed timeslot or we vary, depending how it goes. 
    * If needed we can always meet more or less often

## Snellius/super computing

This is taken from <https://canvas.uva.nl/courses/6056/pages/gpu-slash-cpu-access>

<p>It is possible to get a maximum of around 30000 SBU's. For internal projects, the university pays for computing time. You need to complete the following steps to be able to make use of the Snellius computer:</p>
<ol style="list-style-type: decimal;">
    <li>Student gives supervisor a small summary of how GPU will be used (e.g., the model name, the training goal, the dataset size, the duration of using the GPU on how many days, if CPU is needed etc.)</li>
    <li>After approval of the supervisor, the student goes <a href="https://servicedesk.surf.nl/jira/plugins/servlet/samlsso?redirectTo=%2Fservicedesk%2Fcustomer%2Fplugins%2Fservlet%2Fdesk%2Fportal%2F13%2Fcreate%2F51">here</a></li>
    <li>Click Direct Institute Contract</li>
    <li>Then select UvA and tick the box &ldquo;Yes&rdquo; under the question of this is the project for the GSI. See below!</li>
    <li>The approval will be sent to the programme.&nbsp;</li>
    <li>Within one week, an approval should be sent to supervisor and student, along with the login information. Please be aware that you may also use <a style="font-family: inherit; font-size: 1rem;" href="https://canvas.uva.nl/courses/6056/discussion_topics/362770" data-api-endpoint="https://canvas.uva.nl/api/v1/courses/6056/discussion_topics/362770" data-api-returntype="Discussion">Machine Learning Machines</a><span style="font-family: inherit; font-size: 1rem;"> at Lab42 or</span>&nbsp;<a class="inline_disabled" href="https://colab.google/" target="_blank" rel="noopener">Google Colab</a>.</li>
</ol>


### Nog meer over Snellius

Computational power
When you need additional computational power for your BSc thesis project you can make request to get access to the GPU's at the RoboLab:

https://github.com/IntelligentRoboticsLab/robolabws/blob/master/README.md

Information on requesting access to the DAS-6 cluster:

https://www.cs.vu.nl/das6/accounts.shtml

Information on requesting access to Snellius cluster:

De docenten kunnen in hun onderwijsmodule gebruik maken van een speciaal hiervoor gereserveerd deel van het zogenaamde Snellius GPU cluster. Er is gpu ruimte beschikbaar gesteld zonder dat er sprake is van wachtrijen. Het is daarmee uitstekend geschikt voor gebruik in het onderwijs. 

Begeleiders van afstudeerprojecten  die gebruik van willen maken van Snellius GPU dienen een e-mail te sturen naar: helpdesk@surfsara.nl

met een cc naar:  B.N.J.Menist@uva.nl

Bij Bachelor project/stage/scriptie  (kosten komen tlv onderzoek) moeten de volgende punten benoemd worden:
-naam begeleider (=de aanvrager)
-naam van de student
-naam van het vak (dus Afstudeerproject BSc Informatiekunde)
-naam van het onderzoeksinstituut (b.v. IVI / ILLC)

De begeleider kan meer informatie vinden op: 

https://medewerker.uva.nl/fnwi/content-secured/nieuws/2019/08/lisa-gpu-cluster-beschikbaar-voor-docenten.html 

## Group supervision

During Corona I started with group supervsion, which worked out very well. Groups of 3-4 persons, working on similar projects. Benefits:

* you can learn a lot from each other
* you see that others have the same problems/troubles/frustrations/... as you
* you are not alone
* you can do peer reviewing/helping
    *   eg, read each others introduction and criticize/help

Depending on my students I might do that as well. Then usually we all open up our github repos to each other.    

## Grades and passing

I like good quality. If you want to aim for a high grade ("good" or higher ($\geq 8$), and I think your work is worth it I will fight for you and your grade. Many of my students won awards with their thesis or could present it at a workshop or conference (in this case, your study subsidizes a (large) part of the travel costs). Also many who did an internship at a company got an offer to stay there after their thesis. 

Almost all of my thesis students pass in the time which is given for the thesis project (so for an 18EC thesis, this is 3 months full time). I like that and I will help you  meet this "deadline".

My mean and median grade is in line with the mean and median of the study: "satisfactory" (in Dutch *bevredigend*), which is a 7 or 7.5. 


### How to "satisfy" the independent examiner


Nog even een tip. Probeer toch die onafhankelijke examinator die ik niet ken, en met wie ik ook niet praat in gedachten te nemen en te kijken hoe je die kunt **behagen**. Geweldige tips staan in [this advice by Eamonn Keogh ](https://www.cs.ucr.edu/~eamonn/public/SDM_How_to_do_Research_Keogh.pdf). 
Hier geef ik een heel veel gebruikte volgorde van lezen van een artikel. **Gebruik dit als je weinig tijd hebt, om te zorgen dat die delen allemaal perfect zijn.** 

1. Die andere examinator heeft maar heel weinig tijd, en dit moet even tussendoor.
2. Die leest je scriptie als volgt:
   * abstract
   * zoekt de onderzoeksvragen op, als ze die niet in een paar tellen gevonden heeft wordt ze al kribbig
   * leest die heel nauwkeurig, en probeert zich het antwoord voor te stellen
      * is dat rottig , een gedoe of onmogelijk, dan zit je al op een 7-7.5 maximaal
   * gaat dan op zoek naar de antwoorden in de conclusie en in tabelletjes/grafiekjes in je resultaten
      * is dat te vinden en gebeurt er iets spannends, dan gaat ze verder lezen of hier allicht ook een 8 of hoger in zit
      * anders is het of een default 7 of 7.5, of als er gekke dingen in zitten, lager, en dan gaat ze verder kijken of dat nou aan haar ligt of dat er echt gekke dingen gebeuren/ommissies zijn.

      
## Publication

I strongly encourage this.
Your study as well. Different studies have different reimbursement strategies. Often publications can also be made without having to pay anything. 

### support Master IS
The master IS program (financially) supports students whose thesis work gets accepted for conference or publication. Students can reimburse costs up to 500 Euro’s via: <https://expenseclaims.uva.nl/?language=en>. They need to  upload copy of receipts and enter the following information: 
 
reference number (wbs): R.2318.0040.01
contact person:Dr. Sennay Ghebreab
phone number: 020-5252270

### Support BSc KI and IK

* Also 500 Euro
* Contact Sophie Krakers, `s.a.krakers@uva.nl`
