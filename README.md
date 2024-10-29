# Georgia Tech Woodruff Research Projects Classification Analysis

This README provides an overview of the project classification analysis we're working on, including the development and categorization of research themes for the dataset.

## Overview
The main goal of this project is to classify research projects based on their titles, using themes that better reflect the type of work being undertaken. The dataset we're working with contains research project titles, which will be categorized into different themes using a machine learning model and an extended list of themes that we defined.

### Main Dataframe (`award_data`)
- The main dataframe, `award_data`, contains research project details, including project titles and other metadata.
- After generating the classifications, the results will be merged back into the `award_data` dataframe.

## Project Workflow
### 1. Initial Themes and Research Areas
- Originally, the project titles were to be classified into one Research Area Group (RAG) and multiple applicable themes.
- A list of Research Area Groups (RAGs) was provided by Georgia Tech, and themes included categories like 'Sustainability & Energy', 'Health, Water & Agriculture', etc.
```
 Research Area Groups (choose ONLY ONE):
        - Acoustics/Dynamics
        - AI and Informatics for ME (AI2ME)
        - Automation, Robotics, and Control
        - Bioengineering
        - CAE and Design
        - Engineering Education
        - Fluid Mechanics
        - Heat Transfer, Combustion, & Energy Systems
        - Manufacturing
        - Mechanics of Materials
        - Medical Physics
        - Micro and Nano Engineering
        - Nuclear & Radiological Engineering
        - Tribology
        
    Themes (choose 1-3 from this list ONLY):
        - Sustainability & Energy
        - Health, Water & Agriculture
        - Ocean, Space, Aerospace
        - Design, Materials, Manufacturing
        - Mobility/Automotive/Robotics
```
### 2. Classification Approach
- The approach involves analyzing the project titles, professor names, and departments to classify each one into one or more of the themes listed above.
- Used `GPT-4o-mini` API calls as a LLM classifier
- Once classifications are generated, they will be merged back into the main `award_data` dataframe.

### 3. Implementation Tools
- **ChatGPT API**: Utilized to classify project titles by making API calls for each row in a dataframe containing project titles and associated professor information.


## Potential Next Steps
1. **Run Analysis on Expanded Themes**: Proceed with running the classification analysis using expanded themes to evaluate if they effectively categorize the project titles.
    The 10 expanded themes are:
    1. **Sustainable Energy & Environmental Impact**: Covers energy generation, storage, sustainability, and environmental-focused research.
    2. **Advanced Materials & Manufacturing**: Involves new material development, additive/hybrid manufacturing, and materials testing.
    3. **Biomedical Engineering & Health Technologies**: Projects on medical devices, drug delivery, healthcare improvements, and wearable health monitoring.
    4. **Robotics & Automation**: Projects focused on robotics, control systems, automation, and human-machine interactions.
    5. **Data Science & Machine Learning Applications**: Projects leveraging AI, machine learning, and data analytics for modeling, anomaly detection, and optimization.
    6. **Fluid Dynamics & Thermal Management**: Includes research on fluid mechanics, heat transfer, thermal solutions, and thermophysical studies.
    7. **Electronic & Nano-Scale Devices**: Research focused on electronic devices, nanomembrane sensors, and micro/nanofluidics.
    8. **Cybersecurity & Digital Systems**: Covers cybersecurity, protection of digital systems, digital twins, and simulation-based research.
    9. **Aerospace & Space Technologies**: Projects related to hypersonics, space systems, satellite technology, and aerospace testing.
    10. **Biomaterials & Tissue Engineering**: Focuses on biomaterials, tissue engineering, regenerative medicine, and cell biology innovations.
2. **Google Search Integration**: Planned to leverage the GPT-4 model (`gpt-4o`) to conduct Google searches for gathering contextual information to enhance classification accuracy.
3. **Validate Results**: Review the classifications for consistency and accuracy, and make any necessary adjustments.