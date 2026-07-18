1. Dataset Title

Dataset on student engagement in teaching evaluations at a private university in Vietnam.

2. Dataset Description

This dataset contains survey responses examining students’ perceptions and behaviors related to Student Evaluation of Teaching (SET) in a higher education context.

The dataset was collected to investigate the institutional and psychological factors associated with students’ willingness to provide constructive feedback in course evaluations.

The conceptual model includes the following constructs:

- Organizational Identification

- Institutional Trust

- Perceived Usefulness of Student Evaluations

- Constructive Evaluation Behavior

- Self-Perceived Evaluation Bias

The dataset supports research examining student participation in teaching evaluation systems and can be used for statistical analysis, structural equation modeling (SEM), or replication studies.

3. Data Collection

- Population: Undergraduate students

- Institution: A private university in Vietnam

- Fields of study: Software Engineering and Business

- Data collection method: Online questionnaire (Google Forms)

- Collection period: Late February – early March 2026

- Sample size: 362 respondents

- Response format: Five-point Likert scale

Participation in the survey was voluntary and anonymous, and no personally identifiable information was collected.

4. Dataset Structure

The dataset file: dataset_SET_student_evaluation.xlsx

Each row represents one respondent.

Dataset Variables

Variable            Description
--------------------------------------------------------------
ID                  Anonymous respondent identifier
gender              Respondent gender
year_of_study       Academic year (1–4)
program             Field of study
OI1–OI5             Organizational Identification items
TR1–TR5             Institutional Trust items
PU1–PU5             Perceived Usefulness of SET items
CB1–CB5             Constructive Evaluation Behavior items
PB1–PB5             Self-Perceived Evaluation Bias items
PC1–PC5             Process Clarity items

All survey items were measured using a five-point Likert scale:

1 = Strongly disagree
2 = Disagree
3 = Neutral
4 = Agree
5 = Strongly agree

5. Survey Instrument

The original questionnaire contained 30 survey items across six conceptual domains.

The complete instrument is provided in the file: questionnaire_30items.pdf

6. Analysis Code and Reproducibility

The file analysis_reproducibility.R contains the R code used for data
preparation, measurement validation, statistical analysis, robustness
assessment, and output generation. The script includes procedures for:

-   Data import and preprocessing
-   Screening for missing values and possible straight-line responses
-   Descriptive statistics for observed indicators and construct scores
-   Cronbach’s alpha reliability assessment
-   Confirmatory factor analysis (CFA)
-   Composite reliability and average variance extracted
-   Fornell–Larcker and HTMT discriminant validity assessment
-   Structural equation modeling (SEM)
-   Bootstrap estimation of indirect effects
-   Alternative factor-model assessment
-   Common method bias assessment using a single-factor CFA
-   Sensitivity analysis excluding potential straight-line responses
-   Generation of the respondent demographic figure
-   Export of statistical results to Microsoft Excel

The original dataset contains 30 survey items across six conceptual
domains. The main validated measurement analysis retains 15 indicators
representing five constructs: organizational identification,
institutional trust, perceived usefulness of student evaluations,
constructive evaluation behavior, and self-perceived evaluation bias.

File paths

The R script uses a relative file path:

    path <- "dataset_SET_student_evaluation.xlsx"

Therefore, analysis_reproducibility.R and
dataset_SET_student_evaluation.xlsx should be stored in the same
directory. The script does not require a user-specific or hard-coded
local file path.

Execution instructions

1.  Download or clone all files in the repository.
2.  Store analysis_reproducibility.R and
    dataset_SET_student_evaluation.xlsx in the same directory.
3.  Open R or RStudio.
4.  Set the repository folder as the working directory.
5.  Run:

    source("analysis_reproducibility.R")

The script checks whether the required R packages are installed and
installs any missing packages before loading them.

Required R packages

-   readxl
-   dplyr
-   psych
-   lavaan
-   semTools
-   writexl
-   tidyr
-   stringr
-   ggplot2
-   patchwork

Generated outputs

After successful execution, the script generates:

-   SEM_5factor_results.xlsx
-   Figure_1_sample_profile.png
-   sessionInfo.txt (if enabled)

The script reproduces the numerical results underlying the descriptive
statistics, reliability and validity assessments, standardized factor
loadings, model-fit statistics, robustness checks, and demographic
figure reported in the accompanying Data in Brief article. It also
includes additional SEM, mediation, and diagnostic analyses to support
secondary analysis and methodological replication.

Computational environment

The analyses were conducted using the R statistical environment. The
exact R version, operating system, and package versions used for the
archived analysis are documented in sessionInfo.txt.

To generate this file, include:

    session_info <- capture.output(sessionInfo())
    writeLines(session_info, "sessionInfo.txt")

This information facilitates reproducibility across different systems.


7. Ethical Considerations

Participation in the survey was voluntary and based on informed consent.
All responses were collected anonymously, and no personally identifiable information was recorded.

The dataset shared in this repository has been fully anonymized.

8. Data Reuse

The dataset is provided to support research on:

- Student engagement in higher education

- Student evaluation of teaching (SET)

- Institutional trust and organizational identification

- Educational survey data analysis

- Structural equation modeling applications in education research

Researchers are encouraged to reuse the dataset for replication studies, methodological research, or comparative studies across higher education systems.

9. Related Research Article

At the time of this release, no related research article has been formally published. The dataset is intended to support future research on student engagement in Student Evaluation of Teaching.

10. Contact

For questions regarding the dataset or research, please contact:

Tran Trong Huynh
Department of Mathematics, FPT University, Ho Chi Minh City, Vietnam 
E-mail: huynhtt4@fe.edu.vn
