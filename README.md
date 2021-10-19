# DATA51000 - Data Mining and Analytics
Lewis University Summer 1, 2021

<br />

### Week 3 Assignment - Clustering: 
#### MGolf_DATA51000A3.ipynb 
##### (requires 77_cancer_proteomes_CPTAC_itraq.csv; clinical_data_breast_cancer.csv; PAM50_proteins.csv)
PAM50 proteomic breast cancer data clustered using K-means and FC-means to discover subcluster structures.

<br />

Tumor profiling tests like PAM50 (tumor profiling test) help to identify breast cancer through the use of 43 protein markers. Identifying patients with cancer and the subsequent subtypes of expression of these proteins may be helpful for predicting likelihood of cancer given a patient sample. Therefore, to discover the underlying structure of cancer subtypes clustering is performed on clinical proteome data indexed by the known PAM50 proteins responsible for most breast cancers. K-means was used by the researchers and they found that optimal clustering was produced from a K-value of 3[1]. Therefore, we seek to validate their conclusion and determine if K-means is the best fit clustering method.

<br />

Proteomic data was obtained through Kaggle, in particular the data was iTRAQ Mass Spectrometry proteome profiles of 80 patients breast cancer samples provided by the Clinical Proteomic Tumor Analysis Consortium (NCI/NIH). This dataset is three parts and contains ~12,000 protein samples. Once the dataset is processed and transformed using the PAM50 identifiers specific for breast cancer, clustering can be performed to discover any underlying subtypes of breast cancer in the patient samples.

<br />

Researchers used hard clustering techniques which do not represent expression data well as expression data is best represented through possibilistic or soft clustering techniques. This distinction is important as expression data from biological samples are best represented as members of multiple distinct subtypes, pathways, or phenotypes. Having multiple memberships is important as no gene, transcript, or protein servers a single function without influencing others. Functions are dynamic overtime, throughout development, and change with respect to the environment. Therefore, if we represent protein expression values as possibilistic then we may be able to uncover subtypes previously missed by the hard partition membership of ‘yes or no’ generated by K-means clustering. In order to do so, fuzzy c-means (FC-means) was implemented as a possibilistic or fuzzy clustering technique.

<br />

For this analysis three datasets were used, two of the raw datasets (Cancer Proteomes & Clinical Data) contained too many columns to represent in a table or in the appendix. As mentioned, these were the raw datasets and once processed we generated an array of 80 patients with 43 proteins pulled from the PAM50 identifiers. These 43 proteins are known to be related to breast cancer, therefore isolating them from the whole sample allows clustering of cancer subtypes. The Cancer Proteome and Clinical Data were combined for reference if needed, but the Cancer Proteome dataset contained all the expression values that were indexed using the PAM50 identifiers found in the third dataset. Any missing values were filled with the median expression value.

<br />

### Week 4 Assignment - Association Rule Mining: 
#### SmokerVNon_Smoker_DATA51000A4.ows and DATA_51000_Assignment4_MGolf-converted.pdf
Identification of candidate gene targets for therapeutic intervention to rescue gene expression in B cells from smoker to non-smoker levels. Smoking continues across multiple cultures and generations despite the known consequences and risks associated with it. In particular B cell changes are known to be directly associated to the onset of smoking-related diseases. Therefore, we sought to identify association rules of gene expression data for female smokers compared to female non-smokers (control). In doing so, we hope to uncover differential gene associations between groups which may identify candidate gene targets for intervention to reverse the effects of smoking observed in B cells. Since we are identifying candidate gene targets for intervention, we will mainly consider associations between a single gene and a set of genes. Data was accessed through the in-built dataset feature of Orange. The attached document is the report resultant from the analysis of B cells from smoker and non-smoker populations.

<br />

### Week 5 Assignment - Supervised Learning: 
#### DATA51000_Assignment5_MGolf.ows and DATA51000_Assignment5_MGolf-converted.pdf
Predicting transplant success based on gene expression values in kidney tissue and peripheral blood lymphocytes. Understanding the likelihood of rejection or acceptance and the degree of either is important in determining which patient may be best suited for transplant priority. Current intervention methods are based around the use of immunosuppressants to ensure the host immune system does not reject the transplanted organ. Additional intervention may be possible through targeted therapeutic administration that changes the gene expression landscape from all states (acute rejection, dysfunction, etc.) to the well-functioning transplant gene expression landscape, thus ensuring transplant viability and patient health. Data was obtained through the in-built GEO dataset feature of Orange using their bioinformatics add-on package. Data was visualized using manifold learning to reduce the dimensionality of the data and to visualize the inherent transplant status subgroups within, while also preserving any non-linear relationships. Splitting the data into training and testing sets was done by randomly sampling 90% of the data for the training set and 10% of the data for the testing set. Next, we ran the training data through multiple different techniques such as: tree, random forest, gradient boosting, kNN, and adaBoost tuning the parameters with cross-validation.


<br />

### Week 6 Assignment - Link Analysis: 
#### DiseasomeA6.gephi and DATA51000_Assignment6_MGolf-converted.pdf
Uncovering community structures of disease classes within the human disease network. Finding communities within the human disease network will enable the identification of associative disease phenotypes as well as the genes involved. The human disease network was created by researchers through the use of the Morbid Map accessed through the Online Mendelian Inheritance in Man (OMIM). The OMIM consists of human disease genes and phenotypes for thousands of disorders and genes. Therefore, the human disease network was created by further classifying the data from the OMIM into 22 disorder classes based on the physiological system affected. Nodes represent disorders and disorders are connected if they share at least one gene where mutations are involved in both disorders. Data for the human disease network was obtained through the Gephi wiki and analyzed using Gephi.
