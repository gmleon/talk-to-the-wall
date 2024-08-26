# Talk to the Wall: The Role of Speech Interaction in Collaborative Visual Analytics

This repository contains the data and scripts necessary to reproduce the figures and results of the paper **Talk to the Wall: The Role of Speech Interaction in Collaborative Visual Analytics** by Gabriela Molina León, Anastasia Bezerianos, Olivier Gladin, and Petra Isenberg. The full paper was accepted at the [IEEE VIS 2024 conference](https://ieeevis.org/year/2024/welcome) and will be published in the journal [IEEE Transactions on Visualization and Computer Graphics](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=2945).

Here is the [preprint](https://doi.org/10.48550/arXiv.2408.03813) 📄. 

[This video](https://osf.io/8gpv2/files/osfstorage/66a2c40f0a0507907d80e38d) 🎥 gives an overview of how the exploratory study worked and our findings.

For running **TouchTalkInteractive**, our technology probe, the source code is in [this GitLab repository](https://gitlab.inria.fr/aviz/TouchTalkInteractive) 🛠️. 

This GitHub repository is based on the [OSF project](https://osf.io/8gpv2) 🌐 that accompanied the paper submission.

## Files 📁

The **Questionnaires** folder contains the following PDF files:
- `pre-questionnaire.pdf`: The questionnaire participants filled out before solving the task.
- `post-questionnaire.pdf`: The questionnaire participants filled out after solving the task.

The **Data** folder contains the following CSV files:
- `all_interactions_all_participants.csv`: The interactions logged during the study.

In the **Pre-questionnaire** sub-folder:
- `pre-demographics.csv`: The answers to the pre-questionnaire questions about demographics.
- `pre-interaction-experience.csv`: The answers to the pre-questionnaire questions about previous experience with input modalities and interactive systems.
- `pre-collaboration-experience.csv`: The answers to the pre-questionnaire questions about previous experience collaborating with others.
- `pre-personal-traits-*.csv`: The answers to the pre-questionnaire questions corresponding to the IPIP-NEO-60 personality assessment instrument.

In the **Post-questionnaire** sub-folder:
- `post-modality-preferences.csv`: The answers to the post-questionnaire questions about preferences of input modality.
- `post-collaboration.csv`: The answers to the post-questionnaire questions related to the collaboration experience.
- `post-time-distribution.csv`: The answers to the post-questionnaire questions related to the distribution of time among multiple activities.
  
In the **Figures** sub-folder:
- `modalities_per_action.csv`: The actions executed by each participant with the used input modality.
- `speech_count_with_personality_scores.csv`: The total count of speech commands executed per participant, combined with their scores per personality trait.
- `wall-positions.csv`: The positions of the participants in front of the wall, when they executed a speech command or a touch gesture.
- `avg_distance_to_wall_with_collab_style.csv`: The average distance between each participant and the wall display, during loose or close collaboration.
- `avg_distance_between_participants_with_collab_style.csv`: The average distance between the two participants of each pair, during loose or close collaboration.
The answers are anonymized and participants are identified by the IDs going from P1 to P20 (excluding the participants of the pilot studies). They are organized in groups G1 to G10.

The **Scripts** folder contains the following Jupyter notebooks:
- `fig3-modality-use-and-preferences.ipynb`: Code to generate Figures 3(a) and 3(b).
- `fig4-personality-traits.ipynb`: Code to generate Figure 4.
- `fig5-wall-positions.ipynb`: Code to generate Figure 5.

## Software requirements 💻
The Jupyter notebooks run with Python 3.11.7 and Jupyter Notebook 7.0.8. In the first cell of each notebook, you can find the list of Python libraries required. Therefore, in addition to a normal Python3 installation, you will require the Python packages:
- `pandas`
- `plotly.express`
- `numpy`

Install them using `pip3 install [package]` or the respective alternative for your installation of Python 3 (e.g., Anaconda). 

The scripts run on Windows 10 Pro (64-bit, x64-based processor), but you can also execute them on any other operating system where Python and Jupyter distributions are available.

### How to run the scripts 📊
The Jupyter notebooks recreate Figures 3, 4, and 5 of the paper. 

1. Download the CSV files in the `Data/Figures` subfolder to a folder called `data`.
2. Download the CSV file `post-modality-preferences.csv` from the `Data/Post-questionnaire` folder to the `data` folder.
3. In the parent folder, run each Jupyter Notebook as follows:
     - Start the notebook server from the command line: `jupyter notebook`.
     - You should see the notebook open in your browser.

You can learn more about Jupyter notebooks in their [documentation](https://docs.jupyter.org/en/latest/running.html).

The PDF versions of the figures will be generated in the parent folder. We finalized Figures 3 and 5 in [Figma](https://www.figma.com/) for minor fixes (e.g., adding the gray arrows in Figure 3). 

Figure 6 was created with the drag-and-drop tools [RAWGraphs](https://www.rawgraphs.io/about) and [Figma](https://www.figma.com/), using the files `avg_distance_to_wall_with_collab_style.csv` and `avg_distance_between_participants_with_collab_style.csv`, so we could not script it.
