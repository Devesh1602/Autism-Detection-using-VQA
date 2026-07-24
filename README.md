# Leveraging-VQA-to-Analyse-Autism-Spectrum-Disorder

The purpose of this project is to create a goal-oriented Visual Question Answering (VQA) system that helps assist in the diagnosis of Autism Spectrum Disorder (ASD) that could be used in the early stages of diagnosis.  Using a unique VQA architecture, the system analyses the video of patients with a specific disorder, extracts characteristics, and correctly predicts the extent of, the existence of the disorder.

## Research Outcomes
* In collaboration with Bangalore Medical College and Research Institute (BMCRI) and Academy for Severe Handicaps and Autism (ASHA).
* Book Chapter “Advancements in AI for Mental Health: Exploring ASD, ADHD  & Schizophrenia, Video Datasets and Future Directions” ACCEPTED in the book titled “Computational Intelligence for Oncology and Neurological Disorders: Current Practices and Future Directions” by Taylor and Francis.
* Journal Publication in progress.

## Extracting Features
Extraction of individual frames. The frames were passed through a facial features extraction library called open-face and other tools. The acquired features include Action units (AUs), facial coordinates and emotions. 

## Dataset
Video Dataset
* BMCRI x ASHA : 12 videos of ASD and TD children each, in the age group 5-7 years. The video length is 6-7 mins. ( not publically available )
* YouTube Dataset : 18 videos of ASD and TD children each, in the age group 5-10 years. (Open-Source)

Questions for VQA dataset:
1. Does the child have reduced eye contact?
2. Are cheeks puffed or raised with happiness?
3. Are the inner portions of the brows furrowed horizontally?
4. Are their lips parted?
5. Are there any noticeable lip movements, (such as lip pursing, biting, or smacking, exhibited by the child in the video) ?
6. Are there signs of Unusual/ excessive smiling?
7. Are there signs of jaw clenching or teeth grinding?
8. Does the child have atypical gaze patterns?
9. Does the lip corner depressor show discomfort or stress?
10. Is the face asymmetric(FA)?
11. Is there absence of the inner brow raiser?

VQA Dataset
* Manual Threshold: to generate the answers for the questions.
* Mean: to generate answers for the questions.
* Mode: to generate answers for the questions.


## Directory Structure
### YOUTUBE
	
* TD
  
	```Videos```: videos of Neurotypical collected from YouTube

	```Features```: CSV files of extracted features of the above videos

* ASD

	```Videos```: videos of ASD collected from YouTube

	```Features```: CSV files of extracted features of the above videos
   
### CLINICAL SOURCE (Note: Cannot upload videos due to ethical concerns)
	
* TD

	```Features```: CSV files of extracted features of the above videos of Neurotypical children collected by the authors

* ASD

	```Features```: CSV files of extracted features of the above videos of ASD children collected by the authors
### DATASET
* YOUTUBE

	``` Threshold  - Final Dataset```: Final QA dataset where answers were generated using a manual threshold

	``` Mean  - Final Dataset```: Final QA dataset where answers were generated using a mean as a threshold

	``` Mode - Final Dataset```: Final QA dataset where answers were generated using a mode as a threshold

* CLINICAL

	``` Threshold  - Final Dataset```: Final QA dataset where answers were generated using a manual threshold

	``` Mean  - Final Dataset```: Final QA dataset where answers were generated using a mean as a threshold

	``` Mode - Final Dataset```: Final QA dataset where answers were generated using a mode as a threshold

### FEATURE EXTRACTIONS

 ```Action Units.ipynb```: Notebook to extract features trial.
 
 ```Extraction of Action Units From Video.ipynb```: Notebook to extract features from frames of a video.
   
### GENERATING QAs
   
```Threshold``` : Notebook to calculate manual threshold.

```Mean```: Notebook to calculate mean as a threshold.

```Mode```: Notebook to calculate mode as a threshold.
  
### MODELS
   
* ANN

	```ANN.ipynb```: Notebook to train the model.

	```question_answering_model.h5``` : Trained model.

 	```tokenizer```: tokenizer used in the model.
   
* LSTM
  
	```LSTM.ipynb```: Notebook to train the model.

	```question_answering_model.h5``` : Trained model.

	```tokenizer```: tokenizer used in the model.
  
* Transformers
  
	```Transformers.ipynb``` : Notebook to train the model.
   
* VQAutism
  
	```VQAutism.ipynb``` : Notebook to train the model.
	
	 ```question_answering_model.h5``` : Trained model.
	
 	```tokenizer```: tokenizer used in the model.
  
### OVERALL PIPELINE

* ```Final Capstone Pipeline.ipynb```: Final pipeline
  
* ```Weights and Entropy```: CSV file with weights for facial features and questions.

### REPORTS AND RESULTS
* ```Capstone Poster```: Poster for our final year thesis.
 
* ```Final Report```: Final Report for our final year thesis.
 
* ```Graphs.ipynb```: Notebook to generate graphs for results.
