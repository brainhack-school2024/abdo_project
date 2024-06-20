# abdo_project
<h5> About me: </h5>
<a href="https://github.com/janeabdo">
   <img src="https://avatars.githubusercontent.com/u/160653193?v=4" width="100px;" alt=""/>
   <br /><sub><b>Jane Abdo</b></sub>
</a>

Hey! I'm Jane. I have a background in neuroscience and I'm now completing my professional master's in biomedical engineering at Polytechnique Montréal. In an effort to blend both, here's my project on computational neuroscience:) 

<h1> Controlling machines with imagination  </h1>
<img src="https://github.com/brainhack-school2024/abdo_project/blob/iss1/images/Project%20intro.gif?raw=true" >
<h3> <strong>Introduction:</strong> </h3>
A variety of movement types can be decoded from brain signals during movement execution, ex: wrist flexion and extension, grabbing, finger moving… (<a href= "https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6901702/ "> Volkova et al, 2019</a>). These decoded signals can then be used to control external devices, such as a screen cursor, a mouse or a prosthetic limb. Certain handicapped populations, like paralyzed and amputated people, could largely benefit from the control of external devices. As they do not have brain signals associated with the execution of movement, other ways of controlling the external device are needed. Fortunately, studies have shown that motor imagery (imagining executing movement) and motor control (executing movement) share neural mechanisms, by activating similar brain regions (<a href= "https://pubmed.ncbi.nlm.nih.gov/18819106/ "> Guillot et al, 2009</a>).
<br> Hence, the question is: Can we decode movement types based on brain signals from imagined movement?
<br> There are many ways of extracting brain signals, the least invasive of which (which is actually not invasive at all) is EEG (electro<strong>encephalo</strong>graphy). However, because of the location of the electrodes on the scalp, the signal is distorted by the scalp and skull. Other more invasive techniques include EcoG (electro<strong>cortico</strong>graphy), in which the electrodes are placed on the surface of the cortex. This technique has been shown to yield better signal quality.
<br> The question becomes: Can we decode movement types based on EcoG brain signals from imagined movement?
<br> A group of students have laid the foundations for answering this question during an online computational neuroscience course called <a href= "https://compneuro.neuromatch.io/"> Neuromatch</a>. Amongst other creations, they have developed a classifier to decode movement types from imagined as well as executed movement EcoG signals. This classifier will be the foundation of my project.
<h3> <strong>Main Objectives:</strong> </h3>
<ul>
<li>Demonstrate better classifier accuracy through improved data processing </li>
<li>Implement other classifiers and compare performances </li>
<li>Apply acquired data visualization concepts on electrophysiological data </li>
</ul>
<h3> <strong>Personal Objectives:</strong> </h3>
<ul>
<li>Develop an understanding of EcoG data (features, filtering, processing…)</li>
<li>Get familiar with Github/Git</li>
<li>Gain an understanding of open science notions</li>
</ul>
<h3> <strong>Training Modules:</strong> </h3>
Introduction to Deep Learning, Deep Learning for neuroimaging, Working with MNE-Python and EEG-BIDS, Data visualization.
<br> These modules can all be found  <a href="https://school-brainhack.github.io/modules/">here</a>.
<h3> <strong>Data:</strong> </h3>
The raw data comes from a public source (<a href= "https://pubmed.ncbi.nlm.nih.gov/31451738/ "> Miller et al, 2019</a>). The data used for my project has been downloaded from a preprocessed source coming from the <a  href = "https://osf.io/ksqv8"> Neuromatch Academy website for computational neuroscience</a>.
<h3> <strong>Deliverables:</strong> </h3>
Two jupyter notebooks: one for the 3d plotting of brains, and one for the preprocessing, classification and data visualization of classifier performance.
<h3> <strong> Tools :</strong> </h3> 
Click <a href="https://github.com/brainhack-school2024/abdo_project/blob/iss1/requirements.txt">here</a> for the requirements.txt file.
<h3> <strong> Methods & Results:</strong> </h3>
The starting point was examining the data. Upon doing so, I realized the electrode placement was different depending on the subject. Since the study was realized in the context of an presurgerical epileptic monitoring, the location of the electrodes depended on the approximate source of the epilepsy. The 3D brains with the electrodes of each individual were plotted. Only the electrodes present in the precentral and postcentral gyruses were selected, as these regions are involved in the execution and imagination of movement.  
<img src="https://github.com/brainhack-school2024/abdo_project/blob/iss1/images/brains.png?raw=true">
Click <a href="https://brainhack-school2024.github.io/abdo_project/images/3dbrain_electrodes.html">here</a> for the interactive version: 
After that, the performance of the classifier on each individual was plotted. 

The following steps were about getting a better classification. Three classifiers were compared. 
<br>The first one, called SVM original, is a support vector machine that came from the original NeuroMatch project. 
<br> The second one, called SVM RFE, is a modified version of the first SVM, with an additional data standardization and a feature selection (using RFE).
<br> The third one, called Random Forest, is a random forest classifier with a data standardization and an RFE feature selection.

The three classifiers were compared on both the actual and the imagined movement conditions. 
<br>For the actual movement: 
<img src="https://github.com/brainhack-school2024/abdo_project/blob/iss1/images/classifier_actual_movement.png?raw=true" >
Click <a href="https://brainhack-school2024.github.io/abdo_project/images/Actual_Movement_Condition.html">here</a> for the interactive version:
<br> For the imagined movement:
<img src="https://github.com/brainhack-school2024/abdo_project/blob/iss1/images/classifier_imagined_movement.png?raw=true" >
Click <a href="https://brainhack-school2024.github.io/abdo_project/images/Imagined_Movement_Condition.html">here</a> for the interactive version
<h3> <strong> Conclusion :</strong> </h3>
Contrary to my beliefs, it seemed that no single classifier excels for everyone; each individual's data requires a tailored approach for optimal performance.
<br> Fortunately, each individual had at least one classifier with an accuracy > 50%. 
<br> Going back to the initial question: Can we decode movement types using imagined movement EcoG signals?
<br> The results from this project are somehow inconclusive. Some individuals show pretty good classifier accuracy, but how much accuracy is needed to be able to confirm that movement types are decodable is unclear. 
<br> Possible causes of this unreliable conclusion are that the EcoG data is too noisy to be correctly classified, that there's not eneough data, and/or that movement imagination was not reliable enough in some individuals. Future projects should try data augmenttaion techniques and different classifier approaches. 
<br> Lastly, I can confidently say I have attained my personal and academic objectives throughout this project, despite a quasi-unsure demonstration of better classifier accuracy. I'd like to thank the TAs as well as Dr Alonso Ortiz for this great opportunity! 
<h3> <strong> References :</strong> </h3>
<ol>
<li> Volkova K, Lebedev MA, Kaplan A, Ossadtchi A. Decoding Movement From Electrocorticographic Activity: A Review. Front Neuroinform. 2019 Dec 3;13:74. doi: 10.3389/fninf.2019.00074. PMID: 31849632; PMCID: PMC6901702.</li>
<li>Miller KJ. A library of human electrocorticographic data and analyses. Nat Hum Behav. 2019 Nov;3(11):1225-1235. doi: 10.1038/s41562-019-0678-3. Epub 2019 Aug 26. PMID: 31451738.</li>
<li>Guillot A, Collet C, Nguyen VA, Malouin F, Richards C, Doyon J. Brain activity during visual versus kinesthetic imagery: an fMRI study. Hum Brain Mapp. 2009 Jul;30(7):2157-72. doi: 10.1002/hbm.20658. PMID: 18819106; PMCID: PMC6870928.</li>


