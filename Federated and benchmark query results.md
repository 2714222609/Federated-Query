## Federated and benchmark query results

#### Q1 Which human gut microbes will change the expression of gene Nfkb1 and what diet will affect these gut microbes?

##### Datalog+ query statements

```
?(Gene,Microbiota,Alteration_gene,Food):-
relationship:has_expression_change_results_by_microbiotaQ1(<Nfkb1>,Microbiota_Gene_Index,Microbiota),
relationship:has_expression_change_results_by_microbiotaQ1(Gene,Microbiota_Gene_Index,Microbiota),
attribute:gene_expression_alteration_caused_by_microbiotaQ1(Microbiota_Gene_Index,Alteration_gene),
relationship:changes_the_abundance_of_by_foodQ1(Food,Microbiota,<changes_the_abundance_of_by_food>).
```

##### federated query results

```json
[
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "gluten-free diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "acidic pH water"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "dietary trans-10,cis-12-conjugated linoleic acid"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "high-fat diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "resistant starch"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "fasting mimicking diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "western diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "proanthocyanidin-rich grape seed extract"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "bamboo shoot fiber"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "lingonberry"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "heat-treated high-fat diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Food": "dietary flaxseed"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Eubacterium rectale",
        "Alteration_gene": "increase",
        "Food": "resistant starch"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Eubacterium rectale",
        "Alteration_gene": "increase",
        "Food": "soluble corn fiber"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_gene": "increase",
        "Food": "luten-free diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "probiotic fermented milk"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "gluten-free diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "dietary trans-10,cis-12-conjugated linoleic acid"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "polysaccharides from the ink of Ommastrephes bartrami"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "high-fat diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "resistant starch"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "western diet"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "proanthocyanidin-rich grape seed extract"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "bamboo shoot fiber"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "oligofructose-maltodextrin"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "lingonberry"
    },
    {
        "Gene": "Nfkb1",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Food": "heat-treated high-fat diet"
    },
    {
        "response count": 27,
        "response time": "0.617s"
    }
]
```

##### benchmark results

| food                                                  | microbiota          | gene  |
| :---------------------------------------------------- | :------------------ | :---- |
| resistant starch                                      | Eubacterium rectale | Nfkb1 |
| soluble corn fiber                                    | Eubacterium rectale | Nfkb1 |
| luten-free diet                                       | Ruminococcus bromii | Nfkb1 |
| probiotic fermented milk                              | Bacteroidetes       | Nfkb1 |
| gluten-free diet                                      | Firmicutes          | Nfkb1 |
| gluten-free diet                                      | Bacteroidetes       | Nfkb1 |
| acidic pH water                                       | Firmicutes          | Nfkb1 |
| dietary trans-10,cis-12-conjugated linoleic acid      | Firmicutes          | Nfkb1 |
| dietary trans-10,cis-12-conjugated linoleic acid      | Bacteroidetes       | Nfkb1 |
| polysaccharides from the ink of Ommastrephes bartrami | Bacteroidetes       | Nfkb1 |
| high-fat\_diet                                        | Firmicutes          | Nfkb1 |
| high-fat\_diet                                        | Bacteroidetes       | Nfkb1 |
| resistant starch                                      | Bacteroidetes       | Nfkb1 |
| resistant starch                                      | Firmicutes          | Nfkb1 |
| fasting mimicking diet                                | Firmicutes          | Nfkb1 |
| western diet                                          | Firmicutes          | Nfkb1 |
| western diet                                          | Bacteroidetes       | Nfkb1 |
| proanthocyanidin-rich grape seed extract              | Firmicutes          | Nfkb1 |
| proanthocyanidin-rich grape seed extract              | Bacteroidetes       | Nfkb1 |
| bamboo shoot fiber                                    | Firmicutes          | Nfkb1 |
| bamboo shoot fiber                                    | Bacteroidetes       | Nfkb1 |
| oligofructose-maltodextrin                            | Bacteroidetes       | Nfkb1 |
| lingonberry                                           | Firmicutes          | Nfkb1 |
| lingonberry                                           | Bacteroidetes       | Nfkb1 |
| heat-treated high-fat diet                            | Bacteroidetes       | Nfkb1 |
| heat-treated high-fat diet                            | Firmicutes          | Nfkb1 |
| dietary flaxseed                                      | Firmicutes          | Nfkb1 |



#### Q2 The abundance of which gut microbes will change when people suffer from colorectal cancer, which genes are affected by these gut microbes and which KEGG pathways are these genes involved in?

##### federated query results

```json
[
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "TNF",
        "Kegg_pathway": "hsa01523  Antifolate resistance, hsa04010  MAPK signaling pathway, hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04064  NF-kappa B signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04150  mTOR signaling pathway, hsa04210  Apoptosis, hsa04217  Necroptosis, hsa04350  TGF-beta signaling pathway, hsa04380  Osteoclast differentiation, hsa04612  Antigen processing and presentation, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04640  Hematopoietic cell lineage, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04660  T cell receptor signaling pathway, hsa04664  Fc epsilon RI signaling pathway, hsa04668  TNF signaling pathway, hsa04920  Adipocytokine signaling pathway, hsa04930  Type II diabetes mellitus, hsa04931  Insulin resistance, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa04940  Type I diabetes mellitus, hsa05010  Alzheimer disease, hsa05014  Amyotrophic lateral sclerosis, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05205  Proteoglycans in cancer, hsa05310  Asthma, hsa05321  Inflammatory bowel disease, hsa05322  Systemic lupus erythematosus, hsa05323  Rheumatoid arthritis, hsa05330  Allograft rejection, hsa05332  Graft-versus-host disease, hsa05410  Hypertrophic cardiomyopathy, hsa05414  Dilated cardiomyopathy, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "MAPK3",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04010  MAPK signaling pathway, hsa04012  ErbB signaling pathway, hsa04014  Ras signaling pathway, hsa04015  Rap1 signaling pathway, hsa04022  cGMP-PKG signaling pathway, hsa04024  cAMP signaling pathway, hsa04062  Chemokine signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04068  FoxO signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04072  Phospholipase D signaling pathway, hsa04114  Oocyte meiosis, hsa04140  Autophagy - animal, hsa04150  mTOR signaling pathway, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04218  Cellular senescence, hsa04261  Adrenergic signaling in cardiomyocytes, hsa04270  Vascular smooth muscle contraction, hsa04350  TGF-beta signaling pathway, hsa04360  Axon guidance, hsa04370  VEGF signaling pathway, hsa04371  Apelin signaling pathway, hsa04380  Osteoclast differentiation, hsa04510  Focal adhesion, hsa04520  Adherens junction, hsa04540  Gap junction, hsa04550  Signaling pathways regulating pluripotency of stem cells, hsa04611  Platelet activation, hsa04613  Neutrophil extracellular trap formation, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04664  Fc epsilon RI signaling pathway, hsa04666  Fc gamma R-mediated phagocytosis, hsa04668  TNF signaling pathway, hsa04713  Circadian entrainment, hsa04720  Long-term potentiation, hsa04722  Neurotrophin signaling pathway, hsa04723  Retrograde endocannabinoid signaling, hsa04724  Glutamatergic synapse, hsa04725  Cholinergic synapse, hsa04726  Serotonergic synapse, hsa04730  Long-term depression, hsa04810  Regulation of actin cytoskeleton, hsa04910  Insulin signaling pathway, hsa04912  GnRH signaling pathway, hsa04914  Progesterone-mediated oocyte maturation, hsa04915  Estrogen signaling pathway, hsa04916  Melanogenesis, hsa04917  Prolactin signaling pathway, hsa04919  Thyroid hormone signaling pathway, hsa04921  Oxytocin signaling pathway, hsa04926  Relaxin signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04929  GnRH secretion, hsa04930  Type II diabetes mellitus, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04934  Cushing syndrome, hsa04935  Growth hormone synthesis, secretion and action, hsa04960  Aldosterone-regulated sodium reabsorption, hsa05010  Alzheimer disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05034  Alcoholism, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05145  Toxoplasmosis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05205  Proteoglycans in cancer, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05210  Colorectal cancer, hsa05211  Renal cell carcinoma, hsa05212  Pancreatic cancer, hsa05213  Endometrial cancer, hsa05214  Glioma, hsa05215  Prostate cancer, hsa05216  Thyroid cancer, hsa05218  Melanoma, hsa05219  Bladder cancer, hsa05220  Chronic myeloid leukemia, hsa05221  Acute myeloid leukemia, hsa05223  Non-small cell lung cancer, hsa05224  Breast cancer, hsa05225  Hepatocellular carcinoma, hsa05226  Gastric cancer, hsa05230  Central carbon metabolism in cancer, hsa05231  Choline metabolism in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "MAPK1",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04010  MAPK signaling pathway, hsa04012  ErbB signaling pathway, hsa04014  Ras signaling pathway, hsa04015  Rap1 signaling pathway, hsa04022  cGMP-PKG signaling pathway, hsa04024  cAMP signaling pathway, hsa04062  Chemokine signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04068  FoxO signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04072  Phospholipase D signaling pathway, hsa04114  Oocyte meiosis, hsa04140  Autophagy - animal, hsa04150  mTOR signaling pathway, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04218  Cellular senescence, hsa04261  Adrenergic signaling in cardiomyocytes, hsa04270  Vascular smooth muscle contraction, hsa04350  TGF-beta signaling pathway, hsa04360  Axon guidance, hsa04370  VEGF signaling pathway, hsa04371  Apelin signaling pathway, hsa04380  Osteoclast differentiation, hsa04510  Focal adhesion, hsa04520  Adherens junction, hsa04540  Gap junction, hsa04550  Signaling pathways regulating pluripotency of stem cells, hsa04611  Platelet activation, hsa04613  Neutrophil extracellular trap formation, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04664  Fc epsilon RI signaling pathway, hsa04666  Fc gamma R-mediated phagocytosis, hsa04668  TNF signaling pathway, hsa04713  Circadian entrainment, hsa04720  Long-term potentiation, hsa04722  Neurotrophin signaling pathway, hsa04723  Retrograde endocannabinoid signaling, hsa04724  Glutamatergic synapse, hsa04725  Cholinergic synapse, hsa04726  Serotonergic synapse, hsa04730  Long-term depression, hsa04810  Regulation of actin cytoskeleton, hsa04910  Insulin signaling pathway, hsa04912  GnRH signaling pathway, hsa04914  Progesterone-mediated oocyte maturation, hsa04915  Estrogen signaling pathway, hsa04916  Melanogenesis, hsa04917  Prolactin signaling pathway, hsa04919  Thyroid hormone signaling pathway, hsa04921  Oxytocin signaling pathway, hsa04926  Relaxin signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04929  GnRH secretion, hsa04930  Type II diabetes mellitus, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04934  Cushing syndrome, hsa04935  Growth hormone synthesis, secretion and action, hsa04960  Aldosterone-regulated sodium reabsorption, hsa05010  Alzheimer disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05034  Alcoholism, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05145  Toxoplasmosis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05205  Proteoglycans in cancer, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05210  Colorectal cancer, hsa05211  Renal cell carcinoma, hsa05212  Pancreatic cancer, hsa05213  Endometrial cancer, hsa05214  Glioma, hsa05215  Prostate cancer, hsa05216  Thyroid cancer, hsa05218  Melanoma, hsa05219  Bladder cancer, hsa05220  Chronic myeloid leukemia, hsa05221  Acute myeloid leukemia, hsa05223  Non-small cell lung cancer, hsa05224  Breast cancer, hsa05225  Hepatocellular carcinoma, hsa05226  Gastric cancer, hsa05230  Central carbon metabolism in cancer, hsa05231  Choline metabolism in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "FOS",
        "Kegg_pathway": "hsa01522  Endocrine resistance, hsa04010  MAPK signaling pathway, hsa04024  cAMP signaling pathway, hsa04210  Apoptosis, hsa04380  Osteoclast differentiation, hsa04620  Toll-like receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04668  TNF signaling pathway, hsa04713  Circadian entrainment, hsa04725  Cholinergic synapse, hsa04728  Dopaminergic synapse, hsa04915  Estrogen signaling pathway, hsa04917  Prolactin signaling pathway, hsa04921  Oxytocin signaling pathway, hsa04926  Relaxin signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04932  Non-alcoholic fatty liver disease, hsa04935  Growth hormone synthesis, secretion and action, hsa05031  Amphetamine addiction, hsa05130  Pathogenic Escherichia coli infection, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05161  Hepatitis B, hsa05162  Measles, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05210  Colorectal cancer, hsa05224  Breast cancer, hsa05231  Choline metabolism in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "JUN",
        "Kegg_pathway": "hsa01522  Endocrine resistance, hsa04010  MAPK signaling pathway, hsa04012  ErbB signaling pathway, hsa04024  cAMP signaling pathway, hsa04137  Mitophagy - animal, hsa04210  Apoptosis, hsa04310  Wnt signaling pathway, hsa04380  Osteoclast differentiation, hsa04510  Focal adhesion, hsa04530  Tight junction, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04668  TNF signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04912  GnRH signaling pathway, hsa04915  Estrogen signaling pathway, hsa04921  Oxytocin signaling pathway, hsa04926  Relaxin signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05030  Cocaine addiction, hsa05031  Amphetamine addiction, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05161  Hepatitis B, hsa05162  Measles, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05210  Colorectal cancer, hsa05211  Renal cell carcinoma, hsa05224  Breast cancer, hsa05231  Choline metabolism in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "TLR2",
        "Kegg_pathway": "hsa04145  Phagosome, hsa04151  PI3K-Akt signaling pathway, hsa04613  Neutrophil extracellular trap formation, hsa04620  Toll-like receptor signaling pathway, hsa05132  Salmonella infection, hsa05134  Legionellosis, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05161  Hepatitis B, hsa05162  Measles, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05205  Proteoglycans in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "CXCR2",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04072  Phospholipase D signaling pathway, hsa04144  Endocytosis, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05163  Human cytomegalovirus infection"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Gene": "GLP1R",
        "Kegg_pathway": "hsa04024  cAMP signaling pathway, hsa04080  Neuroactive ligand-receptor interaction, hsa04911  Insulin secretion"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "decrease",
        "Microbiota": "Enterococcus",
        "Alteration_gene": "decrease",
        "Gene": "BCL2",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04064  NF-kappa B signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04140  Autophagy - animal, hsa04141  Protein processing in endoplasmic reticulum, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04261  Adrenergic signaling in cardiomyocytes, hsa04340  Hedgehog signaling pathway, hsa04510  Focal adhesion, hsa04621  NOD-like receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04725  Cholinergic synapse, hsa04915  Estrogen signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05014  Amyotrophic lateral sclerosis, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05145  Toxoplasmosis, hsa05152  Tuberculosis, hsa05161  Hepatitis B, hsa05162  Measles, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05210  Colorectal cancer, hsa05215  Prostate cancer, hsa05222  Small cell lung cancer, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "decrease",
        "Microbiota": "Enterococcus",
        "Alteration_gene": "increase",
        "Gene": "BAX",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04141  Protein processing in endoplasmic reticulum, hsa04210  Apoptosis, hsa04211  Longevity regulating pathway, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04722  Neurotrophin signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05203  Viral carcinogenesis, hsa05210  Colorectal cancer, hsa05212  Pancreatic cancer, hsa05213  Endometrial cancer, hsa05214  Glioma, hsa05216  Thyroid cancer, hsa05217  Basal cell carcinoma, hsa05218  Melanoma, hsa05220  Chronic myeloid leukemia, hsa05222  Small cell lung cancer, hsa05223  Non-small cell lung cancer, hsa05224  Breast cancer, hsa05225  Hepatocellular carcinoma, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "CCL3",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04620  Toll-like receptor signaling pathway, hsa05142  Chagas disease, hsa05163  Human cytomegalovirus infection, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "Il6",
        "Kegg_pathway": "mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu01523  Antifolate resistance, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04659  Th17 cell differentiation, mmu04668  TNF signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05321  Inflammatory bowel disease, mmu05323  Rheumatoid arthritis, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "decrease",
        "Gene": "Il6",
        "Kegg_pathway": "mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu01523  Antifolate resistance, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04659  Th17 cell differentiation, mmu04668  TNF signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05321  Inflammatory bowel disease, mmu05323  Rheumatoid arthritis, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Gene": "Ffar3",
        "Kegg_pathway": "null"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "Ffar3",
        "Kegg_pathway": "null"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "C5AR1",
        "Kegg_pathway": "hsa04080  Neuroactive ligand-receptor interaction, hsa04610  Complement and coagulation cascades, hsa04613  Neutrophil extracellular trap formation, hsa04936  Alcoholic liver disease, hsa05150  Staphylococcus aureus infection, hsa05171  Coronavirus disease - COVID-19"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "Il12b",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "decrease",
        "Gene": "Il12b",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "NR1H4",
        "Kegg_pathway": "hsa04976  Bile secretion"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "decrease",
        "Microbiota": "Enterococcus",
        "Alteration_gene": "increase",
        "Gene": "CASP3",
        "Kegg_pathway": "hsa01524  Platinum drug resistance, hsa04010  MAPK signaling pathway, hsa04115  p53 signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa04726  Serotonergic synapse, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05010  Alzheimer disease, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05205  Proteoglycans in cancer, hsa05206  MicroRNAs in cancer, hsa05210  Colorectal cancer, hsa05222  Small cell lung cancer, hsa05416  Viral myocarditis, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Gene": "Ffar2",
        "Kegg_pathway": "mmu04024  cAMP signaling pathway"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "Ffar2",
        "Kegg_pathway": "mmu04024  cAMP signaling pathway"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "Cd86",
        "Kegg_pathway": "mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04940  Type I diabetes mellitus, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05202  Transcriptional misregulation in cancer, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05416  Viral myocarditis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "decrease",
        "Gene": "Cd86",
        "Kegg_pathway": "mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04940  Type I diabetes mellitus, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05202  Transcriptional misregulation in cancer, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05416  Viral myocarditis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "Cd40",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04064  NF-kappa B signaling pathway, mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05330  Allograft rejection, mmu05340  Primary immunodeficiency, mmu05416  Viral myocarditis, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "decrease",
        "Gene": "Cd40",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04064  NF-kappa B signaling pathway, mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05330  Allograft rejection, mmu05340  Primary immunodeficiency, mmu05416  Viral myocarditis, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Gene": "Gcg",
        "Kegg_pathway": "mmu04024  cAMP signaling pathway, mmu04080  Neuroactive ligand-receptor interaction, mmu04714  Thermogenesis, mmu04911  Insulin secretion, mmu04922  Glucagon signaling pathway"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "increase",
        "Gene": "Nfkb1",
        "Kegg_pathway": "mmu01523  Antifolate resistance, mmu04010  MAPK signaling pathway, mmu04014  Ras signaling pathway, mmu04024  cAMP signaling pathway, mmu04062  Chemokine signaling pathway, mmu04064  NF-kappa B signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04071  Sphingolipid signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04210  Apoptosis, mmu04211  Longevity regulating pathway, mmu04218  Cellular senescence, mmu04380  Osteoclast differentiation, mmu04613  Neutrophil extracellular trap formation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04662  B cell receptor signaling pathway, mmu04668  TNF signaling pathway, mmu04722  Neurotrophin signaling pathway, mmu04917  Prolactin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04926  Relaxin signaling pathway, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05030  Cocaine addiction, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05203  Viral carcinogenesis, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05212  Pancreatic cancer, mmu05215  Prostate cancer, mmu05220  Chronic myeloid leukemia, mmu05221  Acute myeloid leukemia, mmu05222  Small cell lung cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "increase",
        "Gene": "Nfkb1",
        "Kegg_pathway": "mmu01523  Antifolate resistance, mmu04010  MAPK signaling pathway, mmu04014  Ras signaling pathway, mmu04024  cAMP signaling pathway, mmu04062  Chemokine signaling pathway, mmu04064  NF-kappa B signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04071  Sphingolipid signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04210  Apoptosis, mmu04211  Longevity regulating pathway, mmu04218  Cellular senescence, mmu04380  Osteoclast differentiation, mmu04613  Neutrophil extracellular trap formation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04662  B cell receptor signaling pathway, mmu04668  TNF signaling pathway, mmu04722  Neurotrophin signaling pathway, mmu04917  Prolactin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04926  Relaxin signaling pathway, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05030  Cocaine addiction, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05203  Viral carcinogenesis, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05212  Pancreatic cancer, mmu05215  Prostate cancer, mmu05220  Chronic myeloid leukemia, mmu05221  Acute myeloid leukemia, mmu05222  Small cell lung cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Bacteroidetes",
        "Alteration_gene": "decrease",
        "Gene": "Pdcd1lg2",
        "Kegg_pathway": "mmu04514  Cell adhesion molecules"
    },
    {
        "Disorder": "colorectal_carcinoma",
        "Alteration_microbiota": "increase",
        "Microbiota": "Firmicutes",
        "Alteration_gene": "decrease",
        "Gene": "Pdcd1lg2",
        "Kegg_pathway": "mmu04514  Cell adhesion molecules"
    },
    {
        "response count": 31,
        "response time": "3.371s"
    }
]
```

##### benchmark results

| Disorder             | Alteration\_Microbiota | Microbiota    | Alteration\_Gene | Gene     |
| :------------------- | :--------------------- | :------------ | :--------------- | :------- |
| colorectal carcinoma | increase               | Firmicutes    | increase         | FOS      |
| colorectal carcinoma | increase               | Firmicutes    | increase         | MAPK3    |
| colorectal carcinoma | increase               | Firmicutes    | increase         | MAPK1    |
| colorectal carcinoma | increase               | Firmicutes    | increase         | JUN      |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | NR1H4    |
| colorectal carcinoma | increase               | Bacteroidetes | increase         | GLP1R    |
| colorectal carcinoma | decrease               | Enterococcus  | decrease         | BCL2     |
| colorectal carcinoma | decrease               | Enterococcus  | increase         | BAX      |
| colorectal carcinoma | decrease               | Enterococcus  | increase         | CASP3    |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | C5AR1    |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | CXCR2    |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | TNF      |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | CCL3     |
| colorectal carcinoma | increase               | Firmicutes    | increase         | TLR2     |
| colorectal carcinoma | increase               | Firmicutes    | increase         | Ffar3    |
| colorectal carcinoma | increase               | Firmicutes    | increase         | Ffar2    |
| colorectal carcinoma | increase               | Firmicutes    | increase         | Nfkb1    |
| colorectal carcinoma | increase               | Firmicutes    | decrease         | Pdcd1lg2 |
| colorectal carcinoma | increase               | Firmicutes    | decrease         | Cd86     |
| colorectal carcinoma | increase               | Firmicutes    | decrease         | Cd40     |
| colorectal carcinoma | increase               | Firmicutes    | decrease         | Il6      |
| colorectal carcinoma | increase               | Firmicutes    | decrease         | Il12b    |
| colorectal carcinoma | increase               | Bacteroidetes | increase         | Ffar3    |
| colorectal carcinoma | increase               | Bacteroidetes | increase         | Ffar2    |
| colorectal carcinoma | increase               | Bacteroidetes | increase         | Nfkb1    |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | Pdcd1lg2 |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | Cd86     |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | Cd40     |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | Il6      |
| colorectal carcinoma | increase               | Bacteroidetes | decrease         | Il12b    |
| colorectal carcinoma | increase               | Bacteroidetes | increase         | Gcg      |



#### Q3 What kinds of bacteria in human intestinal tract will be increased by high-fat diet? What metabolites do these bacteria produce?

##### federated query results

```json
[
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Bile acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Bile acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Indoxyl sulfate"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "p-Cresol sulfate"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Phenylacetylglutamine"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Firmicutes",
        "Alteration": "decrease",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Akkermansia muciniphila",
        "Alteration": "increase",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Akkermansia muciniphila",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Prevotellaceae",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Veillonellaceae",
        "Alteration": "decrease",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Veillonellaceae",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Coprococcus",
        "Alteration": "decrease",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Eubacterium",
        "Alteration": "increase",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium",
        "Alteration": "decrease",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Caffeic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Caffeic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Dihydrocaffeic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Dihydrocaffeic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "3-(3-Hydroxyphenyl)propanoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "3-(3-Hydroxyphenyl)propanoic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Dehydroxychlorogenic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Dehydroxychlorogenic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Dihydrochlorogenic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Dihydrochlorogenic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "2,3-Dihydroxypropyl (E)-3-(3,4-dihydroxyphenyl)prop-2-enoate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "2,3-Dihydroxypropyl (E)-3-(3,4-dihydroxyphenyl)prop-2-enoate"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Dihydrocaffeoyl-glycerol"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Dihydrocaffeoyl-glycerol"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "3-Hydroxyphenethyl alcohol"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "3-Hydroxyphenethyl alcohol"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Phenylacetic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Phenylacetic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "red_wine",
        "Microbiota_name": "Veillonella",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Alanine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Alanine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Alanine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Glycine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Glycine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Glycine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "Alanine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "Glycine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Alanine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Glycine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Eubacterium",
        "Alteration": "increase",
        "Metabolite_name": "3-Hydroxybenzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium",
        "Alteration": "decrease",
        "Metabolite_name": "3-Hydroxybenzoic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Eubacterium",
        "Alteration": "increase",
        "Metabolite_name": "4-Hydroxybenzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium",
        "Alteration": "decrease",
        "Metabolite_name": "4-Hydroxybenzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Leucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Malic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Malic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dialister",
        "Alteration": "increase",
        "Metabolite_name": "Tartaric acid"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Ruminococcus bromii",
        "Alteration": "decrease",
        "Metabolite_name": "Tartaric acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium",
        "Alteration": "increase",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Enterococcus",
        "Alteration": "decrease",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Dorea",
        "Alteration": "decrease",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Paraprevotella",
        "Alteration": "decrease",
        "Metabolite_name": "Glycocholic acid"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Enterococcus",
        "Alteration": "decrease",
        "Metabolite_name": "3-Phenylpropionic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Roseburia",
        "Alteration": "increase",
        "Metabolite_name": "3-Phenylpropionic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Oscillospira",
        "Alteration": "increase",
        "Metabolite_name": "Citric acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Oscillospira",
        "Alteration": "decrease",
        "Metabolite_name": "Citric acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Oscillospira",
        "Alteration": "increase",
        "Metabolite_name": "4-Pyridoxic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Oscillospira",
        "Alteration": "decrease",
        "Metabolite_name": "4-Pyridoxic acid"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Ruminococcus bromii",
        "Alteration": "decrease",
        "Metabolite_name": "4-Pyridoxic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium hallii",
        "Alteration": "decrease",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Lactate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Lactate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Pyruvate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Pyruvate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Acetyl phosphate(2-)"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Acetyl phosphate(2-)"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Trimethylamine oxide"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Eubacterium",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Enterococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Hydroquinone"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Folic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Folic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Oxalacetic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Oxalacetic acid"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Oxalacetic acid"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Oxalacetic acid"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Oxalacetic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Succinate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium rectale",
        "Alteration": "decrease",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Eubacterium rectale",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Ruminococcus bromii",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Ruminococcus bromii",
        "Alteration": "decrease",
        "Metabolite_name": "Glycerol"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Indole-3-carboxaldehyde"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Indole-3-carboxaldehyde"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "decrease",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "probiotic fermented milk",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "increase",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Enterococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Dopamine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "2-Amino-1-methyl-6-phenylimidazo[4,5-b]pyridine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "2-Amino-1-methyl-6-phenylimidazo[4,5-b]pyridine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Ursodeoxycholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Ursodeoxycholic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Ursodeoxycholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Phascolarctobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Phenylalanine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Phascolarctobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Serine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Glycerophospholipids"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Glycerophospholipids"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Glycerophospholipids"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Phenylalanine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Glutamic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "3-Phenylpropionic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Cholic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Eicosapentaenoic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Chenodeoxycholic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Desoxycortone"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "7-Dehydrocholesterol"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Retinol"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Prevotella",
        "Alteration": "increase",
        "Metabolite_name": "Myristic acid"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Prevotella",
        "Alteration": "increase",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Prevotella",
        "Alteration": "increase",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Prevotella",
        "Alteration": "increase",
        "Metabolite_name": "Indole-3-acetic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Paraprevotella",
        "Alteration": "decrease",
        "Metabolite_name": "Myristic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Paraprevotella",
        "Alteration": "decrease",
        "Metabolite_name": "l-Isoleucine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Paraprevotella",
        "Alteration": "decrease",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Paraprevotella",
        "Alteration": "decrease",
        "Metabolite_name": "Indole-3-acetic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "3-Phenylpropionic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "3-Phenylpropionic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Benzoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "4-Hydroxybenzoic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "4-Hydroxybenzoic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "5-Hydroxyindole-3-acetic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "5-Hydroxyindole-3-acetic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "5-Hydroxyindole-3-acetic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Tyramine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Tyramine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Tyramine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Valine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Valine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Valine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Chenodeoxycholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Chenodeoxycholic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Chenodeoxycholic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "N-Acetylputrescine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "N-Acetylputrescine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "N-Acetylputrescine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Betonicine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Betonicine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Betonicine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Cholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Cholic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Cholic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "N-Acetyl-D-Mannosamine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "N-Acetyl-D-Mannosamine"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "N-Acetyl-D-Mannosamine"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "2-Formaminobenzoylacetate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "2-Formaminobenzoylacetate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "2-Formaminobenzoylacetate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "12-Ketolithocholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "12-Ketolithocholic acid"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "12-Ketolithocholic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Hyocholate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "decrease",
        "Metabolite_name": "Hyocholate"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Ruminococcus",
        "Alteration": "increase",
        "Metabolite_name": "Hyocholate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Hypoxanthine"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Hypoxanthine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Creatine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "4-Acetamidobutyric acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "N(6)-Methyllysine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "N-Acetyl-D-Mannosamine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "N-Isovaleroylglycine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "12-Ketolithocholic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo-"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Murideoxycholate"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Pentahomomethionine"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "7-Hydroxy-3-oxocholanoic acid"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "Nutriadeoxycholate vulpecholate"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Lachnospiraceae",
        "Alteration": "decrease",
        "Metabolite_name": "7a-hydroxy-3-oxo-5b-cholanoate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Proline"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Valyl-Hydroxyproline"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Parabacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Valyl-Hydroxyproline"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "1-Methoxypyrene"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Valyl-Hydroxyproline"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Ruminococcus sp.",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Eubacterium",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Eubacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "yogurt",
        "Microbiota_name": "Enterobacteriaceae",
        "Alteration": "decrease",
        "Metabolite_name": "Phenyl sulfate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Indole"
    },
    {
        "Food": "yogurt",
        "Microbiota_name": "Enterobacteriaceae",
        "Alteration": "decrease",
        "Metabolite_name": "Oxiglutatione"
    },
    {
        "Food": "yogurt",
        "Microbiota_name": "Enterobacteriaceae",
        "Alteration": "decrease",
        "Metabolite_name": "Cysteine-glutathione disulfide"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Blautia",
        "Alteration": "increase",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Methanol, (methyl-ONN-azoxy)-"
    },
    {
        "Food": "resistant starch",
        "Microbiota_name": "Faecalibacterium prausnitzii",
        "Alteration": "increase",
        "Metabolite_name": "Methanol, (methyl-ONN-azoxy)-"
    },
    {
        "Food": "fermented soymilk",
        "Microbiota_name": "Porphyromonadaceae",
        "Alteration": "increase",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Coriobacteriaceae",
        "Alteration": "increase",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Coriobacteriaceae",
        "Alteration": "decrease",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "decrease",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "probiotic fermented milk",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "increase",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Firmicutes",
        "Alteration": "decrease",
        "Metabolite_name": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "dietary resistant starch type 4",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "ketogenic low carbohydrate high fat diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroides",
        "Alteration": "decrease",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "ketogenic diet",
        "Microbiota_name": "Bacteroides",
        "Alteration": "increase",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "the recommended dietary intake of fibre and fat",
        "Microbiota_name": "Bacteroidaceae",
        "Alteration": "decrease",
        "Metabolite_name": "Deoxycholic acid"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Firmicutes",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "luten-free diet",
        "Microbiota_name": "Ruminococcus bromii",
        "Alteration": "decrease",
        "Metabolite_name": "Butyrate"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "probiotic fermented milk",
        "Microbiota_name": "Bacteroidetes",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "13-hydroxy-9(Z),15(Z)-octadecadienoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "13-hydroxy-9(Z),15(Z)-octadecadienoic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "13-oxo-9(Z),15(Z)-octadecadienoic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "13-oxo-9(Z),15(Z)-octadecadienoic acid"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Clostridium",
        "Alteration": "increase",
        "Metabolite_name": "3-Indolepropionic acid"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "carbohydrates",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Bifidobacterium",
        "Alteration": "decrease",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Acetate"
    },
    {
        "Food": "phenolic compounds from red wine and coffee",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "Food": "soluble corn fiber",
        "Microbiota_name": "Lactobacillus",
        "Alteration": "increase",
        "Metabolite_name": "Propionate"
    },
    {
        "response count": 300,
        "response time": "0.162s"
    }
]
```

##### benchmark results

| Food                                            | Microbiota\_name             | Alteration | Metabolite\_name                                             |
| :---------------------------------------------- | :--------------------------- | :--------- | :----------------------------------------------------------- |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Bile acid                                                    |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Bile acid                                                    |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Indoxyl sulfate                                              |
| fermented soymilk                               | Lachnospiraceae              | decrease   | p-Cresol sulfate                                             |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Phenylacetylglutamine                                        |
| gluten-free diet                                | Firmicutes                   | decrease   | Butyrate                                                     |
| resistant starch                                | Akkermansia muciniphila      | increase   | Acetate                                                      |
| resistant starch                                | Akkermansia muciniphila      | increase   | Propionate                                                   |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Trimethylamine oxide                                         |
| soluble corn fiber                              | Lactobacillus                | increase   | Trimethylamine oxide                                         |
| carbohydrates                                   | Bifidobacterium              | increase   | Trimethylamine oxide                                         |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Trimethylamine oxide                                         |
| dietary resistant starch type 4                 | Blautia                      | increase   | Trimethylamine oxide                                         |
| resistant starch                                | Prevotellaceae               | increase   | Succinate                                                    |
| luten-free diet                                 | Veillonellaceae              | decrease   | Succinate                                                    |
| soluble corn fiber                              | Veillonellaceae              | increase   | Succinate                                                    |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | 3-Indolepropionic acid                                       |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | 3-Indolepropionic acid                                       |
| soluble corn fiber                              | Coprococcus                  | decrease   | 3-Indolepropionic acid                                       |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 3-Indolepropionic acid                                       |
| dietary resistant starch type 4                 | Eubacterium                  | increase   | 3-Indolepropionic acid                                       |
| soluble corn fiber                              | Eubacterium                  | decrease   | 3-Indolepropionic acid                                       |
| carbohydrates                                   | Bifidobacterium              | increase   | Caffeic acid                                                 |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Caffeic acid                                                 |
| carbohydrates                                   | Bifidobacterium              | increase   | Dihydrocaffeic acid                                          |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Dihydrocaffeic acid                                          |
| carbohydrates                                   | Bifidobacterium              | increase   | 3-\(3-Hydroxyphenyl\)propanoic acid                          |
| soluble corn fiber                              | Bifidobacterium              | decrease   | 3-\(3-Hydroxyphenyl\)propanoic acid                          |
| carbohydrates                                   | Bifidobacterium              | increase   | Dehydroxychlorogenic acid                                    |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Dehydroxychlorogenic acid                                    |
| carbohydrates                                   | Bifidobacterium              | increase   | Dihydrochlorogenic acid                                      |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Dihydrochlorogenic acid                                      |
| carbohydrates                                   | Bifidobacterium              | increase   | 2,3-Dihydroxypropyl \(E\)-3-\(3,4-dihydroxyphenyl\)prop-2-enoate |
| soluble corn fiber                              | Bifidobacterium              | decrease   | 2,3-Dihydroxypropyl \(E\)-3-\(3,4-dihydroxyphenyl\)prop-2-enoate |
| carbohydrates                                   | Bifidobacterium              | increase   | Dihydrocaffeoyl-glycerol                                     |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Dihydrocaffeoyl-glycerol                                     |
| carbohydrates                                   | Bifidobacterium              | increase   | 3-Hydroxyphenethyl alcohol                                   |
| soluble corn fiber                              | Bifidobacterium              | decrease   | 3-Hydroxyphenethyl alcohol                                   |
| carbohydrates                                   | Bifidobacterium              | increase   | Phenylacetic acid                                            |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Phenylacetic acid                                            |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Butyrate                                                     |
| soluble corn fiber                              | Clostridium                  | increase   | Butyrate                                                     |
| red\_wine                                       | Veillonella                  | increase   | Propionate                                                   |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Alanine                                                      |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Alanine                                                      |
| resistant starch                                | Ruminococcus                 | increase   | Alanine                                                      |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Leucine                                                      |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Leucine                                                      |
| resistant starch                                | Ruminococcus                 | increase   | Leucine                                                      |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | l-Isoleucine                                                 |
| soluble corn fiber                              | Ruminococcus                 | decrease   | l-Isoleucine                                                 |
| resistant starch                                | Ruminococcus                 | increase   | l-Isoleucine                                                 |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Glycine                                                      |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Glycine                                                      |
| resistant starch                                | Ruminococcus                 | increase   | Glycine                                                      |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Proline                                                      |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Proline                                                      |
| resistant starch                                | Ruminococcus                 | increase   | Proline                                                      |
| soluble corn fiber                              | Dorea                        | decrease   | Alanine                                                      |
| soluble corn fiber                              | Dorea                        | decrease   | Leucine                                                      |
| soluble corn fiber                              | Dorea                        | decrease   | l-Isoleucine                                                 |
| soluble corn fiber                              | Dorea                        | decrease   | Glycine                                                      |
| soluble corn fiber                              | Dorea                        | decrease   | Proline                                                      |
| dietary resistant starch type 4                 | Blautia                      | increase   | Alanine                                                      |
| dietary resistant starch type 4                 | Blautia                      | increase   | Leucine                                                      |
| dietary resistant starch type 4                 | Blautia                      | increase   | l-Isoleucine                                                 |
| dietary resistant starch type 4                 | Blautia                      | increase   | Glycine                                                      |
| dietary resistant starch type 4                 | Blautia                      | increase   | Proline                                                      |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Serine                                                       |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Serine                                                       |
| resistant starch                                | Ruminococcus                 | increase   | Serine                                                       |
| soluble corn fiber                              | Dorea                        | decrease   | Serine                                                       |
| dietary resistant starch type 4                 | Blautia                      | increase   | Serine                                                       |
| dietary resistant starch type 4                 | Eubacterium                  | increase   | 3-Hydroxybenzoic acid                                        |
| soluble corn fiber                              | Eubacterium                  | decrease   | 3-Hydroxybenzoic acid                                        |
| dietary resistant starch type 4                 | Eubacterium                  | increase   | 4-Hydroxybenzoic acid                                        |
| soluble corn fiber                              | Eubacterium                  | decrease   | 4-Hydroxybenzoic acid                                        |
| soluble corn fiber                              | Faecalibacterium             | increase   | Leucine                                                      |
| soluble corn fiber                              | Faecalibacterium             | increase   | Serine                                                       |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Serine                                                       |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Serine                                                       |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Leucine                                                      |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Leucine                                                      |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Malic acid                                                   |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Malic acid                                                   |
| soluble corn fiber                              | Dialister                    | increase   | Tartaric acid                                                |
| luten-free diet                                 | Ruminococcus bromii          | decrease   | Tartaric acid                                                |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Creatine                                                     |
| soluble corn fiber                              | Lactobacillus                | increase   | Creatine                                                     |
| soluble corn fiber                              | Faecalibacterium             | increase   | 2-Imino-1-methylimidazolidin-4-one                           |
| ketogenic diet                                  | Enterococcus                 | decrease   | 2-Imino-1-methylimidazolidin-4-one                           |
| soluble corn fiber                              | Dorea                        | decrease   | 2-Imino-1-methylimidazolidin-4-one                           |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | 2-Imino-1-methylimidazolidin-4-one                           |
| soluble corn fiber                              | Clostridium                  | increase   | 2-Imino-1-methylimidazolidin-4-one                           |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | 2-Imino-1-methylimidazolidin-4-one                           |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | 2-Imino-1-methylimidazolidin-4-one                           |
| soluble corn fiber                              | Paraprevotella               | decrease   | Glycocholic acid                                             |
| ketogenic diet                                  | Enterococcus                 | decrease   | 3-Phenylpropionic acid                                       |
| resistant starch                                | Roseburia                    | increase   | 3-Phenylpropionic acid                                       |
| dietary resistant starch type 4                 | Oscillospira                 | increase   | Citric acid                                                  |
| soluble corn fiber                              | Oscillospira                 | decrease   | Citric acid                                                  |
| dietary resistant starch type 4                 | Oscillospira                 | increase   | 4-Pyridoxic acid                                             |
| soluble corn fiber                              | Oscillospira                 | decrease   | 4-Pyridoxic acid                                             |
| luten-free diet                                 | Ruminococcus bromii          | decrease   | 4-Pyridoxic acid                                             |
| soluble corn fiber                              | Eubacterium hallii           | decrease   | Butyrate                                                     |
| carbohydrates                                   | Bifidobacterium              | increase   | Lactate                                                      |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Lactate                                                      |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Pyruvate                                                     |
| soluble corn fiber                              | Clostridium                  | increase   | Pyruvate                                                     |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Acetyl phosphate\(2-\)                                       |
| soluble corn fiber                              | Clostridium                  | increase   | Acetyl phosphate\(2-\)                                       |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Trimethylamine oxide                                         |
| dietary resistant starch type 4                 | Eubacterium                  | increase   | Hydroquinone                                                 |
| soluble corn fiber                              | Eubacterium                  | decrease   | Hydroquinone                                                 |
| ketogenic diet                                  | Enterococcus                 | decrease   | Hydroquinone                                                 |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Hydroquinone                                                 |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Hydroquinone                                                 |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Hydroquinone                                                 |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Hydroquinone                                                 |
| ketogenic diet                                  | Bacteroides                  | increase   | Hydroquinone                                                 |
| carbohydrates                                   | Bifidobacterium              | increase   | Hydroquinone                                                 |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Hydroquinone                                                 |
| carbohydrates                                   | Bifidobacterium              | increase   | Folic acid                                                   |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Folic acid                                                   |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Oxalacetic acid                                              |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Oxalacetic acid                                              |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Oxalacetic acid                                              |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Oxalacetic acid                                              |
| ketogenic diet                                  | Bacteroides                  | increase   | Oxalacetic acid                                              |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Succinate                                                    |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Succinate                                                    |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Succinate                                                    |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Succinate                                                    |
| ketogenic diet                                  | Bacteroides                  | increase   | Succinate                                                    |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Propionate                                                   |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Propionate                                                   |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Propionate                                                   |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Propionate                                                   |
| ketogenic diet                                  | Bacteroides                  | increase   | Propionate                                                   |
| soluble corn fiber                              | Eubacterium rectale          | decrease   | Butyrate                                                     |
| resistant starch                                | Eubacterium rectale          | increase   | Butyrate                                                     |
| luten-free diet                                 | Ruminococcus bromii          | decrease   | Propionate                                                   |
| luten-free diet                                 | Ruminococcus bromii          | decrease   | Glycerol                                                     |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Indole-3-carboxaldehyde                                      |
| soluble corn fiber                              | Lactobacillus                | increase   | Indole-3-carboxaldehyde                                      |
| gluten-free diet                                | Bacteroidetes                | decrease   | Acetate                                                      |
| probiotic fermented milk                        | Bacteroidetes                | increase   | Acetate                                                      |
| ketogenic diet                                  | Enterococcus                 | decrease   | Dopamine                                                     |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | 2-Amino-1-methyl-6-phenylimidazo\[4,5-b\]pyridine            |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | 2-Amino-1-methyl-6-phenylimidazo\[4,5-b\]pyridine            |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Butyrate                                                     |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Butyrate                                                     |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Ursodeoxycholic acid                                         |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Ursodeoxycholic acid                                         |
| resistant starch                                | Ruminococcus                 | increase   | Ursodeoxycholic acid                                         |
| soluble corn fiber                              | Phascolarctobacterium        | increase   | Phenylalanine                                                |
| soluble corn fiber                              | Phascolarctobacterium        | increase   | Serine                                                       |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Glycerophospholipids                                         |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Glycerophospholipids                                         |
| resistant starch                                | Ruminococcus                 | increase   | Glycerophospholipids                                         |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Phenylalanine                                                |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Glutamic acid                                                |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 3-Phenylpropionic acid                                       |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Cholic acid                                                  |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Eicosapentaenoic acid                                        |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Chenodeoxycholic acid                                        |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Desoxycortone                                                |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 7-Dehydrocholesterol                                         |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Retinol                                                      |
| ketogenic diet                                  | Prevotella                   | increase   | Myristic acid                                                |
| ketogenic diet                                  | Prevotella                   | increase   | l-Isoleucine                                                 |
| ketogenic diet                                  | Prevotella                   | increase   | Benzoic acid                                                 |
| ketogenic diet                                  | Prevotella                   | increase   | Indole-3-acetic acid                                         |
| soluble corn fiber                              | Paraprevotella               | decrease   | Myristic acid                                                |
| soluble corn fiber                              | Paraprevotella               | decrease   | l-Isoleucine                                                 |
| soluble corn fiber                              | Paraprevotella               | decrease   | Benzoic acid                                                 |
| soluble corn fiber                              | Paraprevotella               | decrease   | Indole-3-acetic acid                                         |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | 3-Phenylpropionic acid                                       |
| soluble corn fiber                              | Clostridium                  | increase   | 3-Phenylpropionic acid                                       |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Benzoic acid                                                 |
| soluble corn fiber                              | Clostridium                  | increase   | Benzoic acid                                                 |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Benzoic acid                                                 |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Benzoic acid                                                 |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Benzoic acid                                                 |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | 4-Hydroxybenzoic acid                                        |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | 4-Hydroxybenzoic acid                                        |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Creatine                                                     |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Creatine                                                     |
| resistant starch                                | Ruminococcus                 | increase   | Creatine                                                     |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | 5-Hydroxyindole-3-acetic acid                                |
| soluble corn fiber                              | Ruminococcus                 | decrease   | 5-Hydroxyindole-3-acetic acid                                |
| resistant starch                                | Ruminococcus                 | increase   | 5-Hydroxyindole-3-acetic acid                                |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Tyramine                                                     |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Tyramine                                                     |
| resistant starch                                | Ruminococcus                 | increase   | Tyramine                                                     |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Valine                                                       |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Valine                                                       |
| resistant starch                                | Ruminococcus                 | increase   | Valine                                                       |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Chenodeoxycholic acid                                        |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Chenodeoxycholic acid                                        |
| resistant starch                                | Ruminococcus                 | increase   | Chenodeoxycholic acid                                        |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | 2-Hydroxy-2-methylbutanenitrile                              |
| soluble corn fiber                              | Ruminococcus                 | decrease   | 2-Hydroxy-2-methylbutanenitrile                              |
| resistant starch                                | Ruminococcus                 | increase   | 2-Hydroxy-2-methylbutanenitrile                              |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | N-Acetylputrescine                                           |
| soluble corn fiber                              | Ruminococcus                 | decrease   | N-Acetylputrescine                                           |
| resistant starch                                | Ruminococcus                 | increase   | N-Acetylputrescine                                           |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Betonicine                                                   |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Betonicine                                                   |
| resistant starch                                | Ruminococcus                 | increase   | Betonicine                                                   |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Cholic acid                                                  |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Cholic acid                                                  |
| resistant starch                                | Ruminococcus                 | increase   | Cholic acid                                                  |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Deoxycholic acid                                             |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Deoxycholic acid                                             |
| resistant starch                                | Ruminococcus                 | increase   | Deoxycholic acid                                             |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | N-Acetyl-D-Mannosamine                                       |
| soluble corn fiber                              | Ruminococcus                 | decrease   | N-Acetyl-D-Mannosamine                                       |
| resistant starch                                | Ruminococcus                 | increase   | N-Acetyl-D-Mannosamine                                       |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | 2-Formaminobenzoylacetate                                    |
| soluble corn fiber                              | Ruminococcus                 | decrease   | 2-Formaminobenzoylacetate                                    |
| resistant starch                                | Ruminococcus                 | increase   | 2-Formaminobenzoylacetate                                    |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | 12-Ketolithocholic acid                                      |
| soluble corn fiber                              | Ruminococcus                 | decrease   | 12-Ketolithocholic acid                                      |
| resistant starch                                | Ruminococcus                 | increase   | 12-Ketolithocholic acid                                      |
| dietary resistant starch type 4                 | Ruminococcus                 | increase   | Hyocholate                                                   |
| soluble corn fiber                              | Ruminococcus                 | decrease   | Hyocholate                                                   |
| resistant starch                                | Ruminococcus                 | increase   | Hyocholate                                                   |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Hypoxanthine                                                 |
| soluble corn fiber                              | Clostridium                  | increase   | Hypoxanthine                                                 |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Creatine                                                     |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 4-Acetamidobutyric acid                                      |
| fermented soymilk                               | Lachnospiraceae              | decrease   | N\(6\)-Methyllysine                                          |
| fermented soymilk                               | Lachnospiraceae              | decrease   | N-Acetyl-D-Mannosamine                                       |
| fermented soymilk                               | Lachnospiraceae              | decrease   | N-Isovaleroylglycine                                         |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 12-Ketolithocholic acid                                      |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo- |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Murideoxycholate                                             |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Pentahomomethionine                                          |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 7-Hydroxy-3-oxocholanoic acid                                |
| fermented soymilk                               | Lachnospiraceae              | decrease   | Nutriadeoxycholate vulpecholate                              |
| fermented soymilk                               | Lachnospiraceae              | decrease   | 7a-hydroxy-3-oxo-5b-cholanoate                               |
| dietary resistant starch type 4                 | Parabacteroides              | increase   | 2-Hydroxy-2-methylbutanenitrile                              |
| soluble corn fiber                              | Parabacteroides              | increase   | 2-Hydroxy-2-methylbutanenitrile                              |
| dietary resistant starch type 4                 | Parabacteroides              | increase   | Proline                                                      |
| soluble corn fiber                              | Parabacteroides              | increase   | Proline                                                      |
| dietary resistant starch type 4                 | Parabacteroides              | increase   | Valyl-Hydroxyproline                                         |
| soluble corn fiber                              | Parabacteroides              | increase   | Valyl-Hydroxyproline                                         |
| dietary resistant starch type 4                 | Blautia                      | increase   | 1-Methoxypyrene                                              |
| dietary resistant starch type 4                 | Blautia                      | increase   | Valyl-Hydroxyproline                                         |
| soluble corn fiber                              | Ruminococcus sp.             | decrease   | Propionate                                                   |
| dietary resistant starch type 4                 | Eubacterium                  | increase   | Butyrate                                                     |
| soluble corn fiber                              | Eubacterium                  | decrease   | Butyrate                                                     |
| yogurt                                          | Enterobacteriaceae           | decrease   | Phenyl sulfate                                               |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Indole                                                       |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Indole                                                       |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Indole                                                       |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Indole                                                       |
| ketogenic diet                                  | Bacteroides                  | increase   | Indole                                                       |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Indole                                                       |
| soluble corn fiber                              | Clostridium                  | increase   | Indole                                                       |
| yogurt                                          | Enterobacteriaceae           | decrease   | Oxiglutatione                                                |
| yogurt                                          | Enterobacteriaceae           | decrease   | Cysteine-glutathione disulfide                               |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Butyrate                                                     |
| soluble corn fiber                              | Lactobacillus                | increase   | Butyrate                                                     |
| dietary resistant starch type 4                 | Blautia                      | increase   | Butyrate                                                     |
| soluble corn fiber                              | Faecalibacterium prausnitzii | increase   | Methanol, \(methyl-ONN-azoxy\)-                              |
| resistant starch                                | Faecalibacterium prausnitzii | increase   | Methanol, \(methyl-ONN-azoxy\)-                              |
| fermented soymilk                               | Porphyromonadaceae           | increase   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| luten-free diet                                 | Coriobacteriaceae            | increase   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| soluble corn fiber                              | Coriobacteriaceae            | decrease   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| gluten-free diet                                | Bacteroidetes                | decrease   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| probiotic fermented milk                        | Bacteroidetes                | increase   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| gluten-free diet                                | Firmicutes                   | decrease   | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | Deoxycholic acid                                             |
| soluble corn fiber                              | Clostridium                  | increase   | Deoxycholic acid                                             |
| phenolic compounds from red wine and coffee     | Bacteroides                  | increase   | Deoxycholic acid                                             |
| dietary resistant starch type 4                 | Bacteroides                  | increase   | Deoxycholic acid                                             |
| ketogenic low carbohydrate high fat diet        | Bacteroides                  | increase   | Deoxycholic acid                                             |
| the recommended dietary intake of fibre and fat | Bacteroides                  | decrease   | Deoxycholic acid                                             |
| ketogenic diet                                  | Bacteroides                  | increase   | Deoxycholic acid                                             |
| the recommended dietary intake of fibre and fat | Bacteroidaceae               | decrease   | Deoxycholic acid                                             |
| gluten-free diet                                | Firmicutes                   | decrease   | Propionate                                                   |
| luten-free diet                                 | Ruminococcus bromii          | decrease   | Butyrate                                                     |
| gluten-free diet                                | Bacteroidetes                | decrease   | Propionate                                                   |
| probiotic fermented milk                        | Bacteroidetes                | increase   | Propionate                                                   |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | 13-hydroxy-9\(Z\),15\(Z\)-octadecadienoic acid               |
| soluble corn fiber                              | Lactobacillus                | increase   | 13-hydroxy-9\(Z\),15\(Z\)-octadecadienoic acid               |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | 13-oxo-9\(Z\),15\(Z\)-octadecadienoic acid                   |
| soluble corn fiber                              | Lactobacillus                | increase   | 13-oxo-9\(Z\),15\(Z\)-octadecadienoic acid                   |
| phenolic compounds from red wine and coffee     | Clostridium                  | increase   | 3-Indolepropionic acid                                       |
| soluble corn fiber                              | Clostridium                  | increase   | 3-Indolepropionic acid                                       |
| carbohydrates                                   | Bifidobacterium              | increase   | Acetate                                                      |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Acetate                                                      |
| carbohydrates                                   | Bifidobacterium              | increase   | Propionate                                                   |
| soluble corn fiber                              | Bifidobacterium              | decrease   | Propionate                                                   |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Acetate                                                      |
| soluble corn fiber                              | Lactobacillus                | increase   | Acetate                                                      |
| phenolic compounds from red wine and coffee     | Lactobacillus                | increase   | Propionate                                                   |
| soluble corn fiber                              | Lactobacillus                | increase   | Propionate                                                   |





#### Q4 Which genes are reduced in expression by F.prausnitzii in the human gut? What metabolic pathways are these genes involved in?

##### federated query results

```json
[
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "IL12B",
        "Alteration": "decrease",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04620  Toll-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04936  Alcoholic liver disease, hsa04940  Type I diabetes mellitus, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05162  Measles, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05205  Proteoglycans in cancer, hsa05321  Inflammatory bowel disease, hsa05330  Allograft rejection, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "IL12A",
        "Alteration": "decrease",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04620  Toll-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04936  Alcoholic liver disease, hsa04940  Type I diabetes mellitus, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05162  Measles, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05321  Inflammatory bowel disease, hsa05330  Allograft rejection, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "CXCL8",
        "Alteration": "decrease",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04064  NF-kappa B signaling pathway, hsa04072  Phospholipase D signaling pathway, hsa04218  Cellular senescence, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05135  Yersinia infection, hsa05142  Chagas disease, hsa05144  Malaria, hsa05146  Amoebiasis, hsa05161  Hepatitis B, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05219  Bladder cancer, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "NFKB1",
        "Alteration": "decrease",
        "Kegg_pathway": "hsa01523  Antifolate resistance, hsa04010  MAPK signaling pathway, hsa04014  Ras signaling pathway, hsa04024  cAMP signaling pathway, hsa04062  Chemokine signaling pathway, hsa04064  NF-kappa B signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04211  Longevity regulating pathway, hsa04218  Cellular senescence, hsa04380  Osteoclast differentiation, hsa04613  Neutrophil extracellular trap formation, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04623  Cytosolic DNA-sensing pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04668  TNF signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04917  Prolactin signaling pathway, hsa04920  Adipocytokine signaling pathway, hsa04926  Relaxin signaling pathway, hsa04931  Insulin resistance, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05010  Alzheimer disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05030  Cocaine addiction, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05203  Viral carcinogenesis, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05212  Pancreatic cancer, hsa05215  Prostate cancer, hsa05220  Chronic myeloid leukemia, hsa05221  Acute myeloid leukemia, hsa05222  Small cell lung cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05415  Diabetic cardiomyopathy, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "IFNG",
        "Alteration": "decrease",
        "Kegg_pathway": "hsa03050  Proteasome, hsa04060  Cytokine-cytokine receptor interaction, hsa04066  HIF-1 signaling pathway, hsa04217  Necroptosis, hsa04350  TGF-beta signaling pathway, hsa04380  Osteoclast differentiation, hsa04612  Antigen processing and presentation, hsa04630  JAK-STAT signaling pathway, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04940  Type I diabetes mellitus, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05200  Pathways in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05322  Systemic lupus erythematosus, hsa05323  Rheumatoid arthritis, hsa05330  Allograft rejection, hsa05332  Graft-versus-host disease, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Il6",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu01523  Antifolate resistance, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04659  Th17 cell differentiation, mmu04668  TNF signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05321  Inflammatory bowel disease, mmu05323  Rheumatoid arthritis, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Arnt",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04066  HIF-1 signaling pathway, mmu04934  Cushing syndrome, mmu05200  Pathways in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05211  Renal cell carcinoma"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Sox11",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Brd7",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu05225  Hepatocellular carcinoma"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Zbtb17",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04110  Cell cycle, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05222  Small cell lung cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Foxa1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Smad2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04110  Cell cycle, mmu04144  Endocytosis, mmu04218  Cellular senescence, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04926  Relaxin signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05142  Chagas disease, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Fos",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04010  MAPK signaling pathway, mmu04024  cAMP signaling pathway, mmu04210  Apoptosis, mmu04380  Osteoclast differentiation, mmu04620  Toll-like receptor signaling pathway, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04662  B cell receptor signaling pathway, mmu04668  TNF signaling pathway, mmu04713  Circadian entrainment, mmu04725  Cholinergic synapse, mmu04728  Dopaminergic synapse, mmu04915  Estrogen signaling pathway, mmu04917  Prolactin signaling pathway, mmu04921  Oxytocin signaling pathway, mmu04926  Relaxin signaling pathway, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04932  Non-alcoholic fatty liver disease, mmu04935  Growth hormone synthesis, secretion and action, mmu05031  Amphetamine addiction, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05161  Hepatitis B, mmu05162  Measles, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05210  Colorectal cancer, mmu05224  Breast cancer, mmu05231  Choline metabolism in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05323  Rheumatoid arthritis, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "E2f1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04137  Mitophagy - animal, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Mnt",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Stat3",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu04062  Chemokine signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04217  Necroptosis, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04630  JAK-STAT signaling pathway, mmu04659  Th17 cell differentiation, mmu04917  Prolactin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04931  Insulin resistance, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04935  Growth hormone synthesis, secretion and action, mmu05145  Toxoplasmosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05203  Viral carcinogenesis, mmu05205  Proteoglycans in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05212  Pancreatic cancer, mmu05221  Acute myeloid leukemia, mmu05223  Non-small cell lung cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Tnf",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01523  Antifolate resistance, mmu04010  MAPK signaling pathway, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04064  NF-kappa B signaling pathway, mmu04071  Sphingolipid signaling pathway, mmu04150  mTOR signaling pathway, mmu04210  Apoptosis, mmu04217  Necroptosis, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04650  Natural killer cell mediated cytotoxicity, mmu04657  IL-17 signaling pathway, mmu04660  T cell receptor signaling pathway, mmu04664  Fc epsilon RI signaling pathway, mmu04668  TNF signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04930  Type II diabetes mellitus, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05010  Alzheimer disease, mmu05014  Amyotrophic lateral sclerosis, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05205  Proteoglycans in cancer, mmu05310  Asthma, mmu05321  Inflammatory bowel disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05414  Dilated cardiomyopathy, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Il12b",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ppara",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu03320  PPAR signaling pathway, mmu04024  cAMP signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04922  Glucagon signaling pathway, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04936  Alcoholic liver disease, mmu05160  Hepatitis C, mmu05207  Chemical carcinogenesis - receptor activation, mmu05415  Diabetic cardiomyopathy"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hdac3",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04613  Neutrophil extracellular trap formation, mmu04919  Thyroid hormone signaling pathway, mmu05034  Alcoholism, mmu05203  Viral carcinogenesis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Onecut1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04950  Maturity onset diabetes of the young"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Relb",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04010  MAPK signaling pathway, mmu04064  NF-kappa B signaling pathway, mmu04380  Osteoclast differentiation, mmu04625  C-type lectin receptor signaling pathway, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hnf1b",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04950  Maturity onset diabetes of the young"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Tcf4",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Mybl2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04218  Cellular senescence"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Mtpn",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Foxm1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04218  Cellular senescence"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "E2f2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "E2f3",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Mta1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Tfdp1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04110  Cell cycle, mmu04350  TGF-beta signaling pathway"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Yy1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Tfap2c",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ezh2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu00310  Lysine degradation, mmu01100  Metabolic pathways, mmu05206  MicroRNAs in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Elp1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hnf1a",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04950  Maturity onset diabetes of the young"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Nfe2l2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04141  Protein processing in endoplasmic reticulum, mmu05012  Parkinson disease, mmu05200  Pathways in cancer, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05225  Hepatocellular carcinoma, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Fli1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu05202  Transcriptional misregulation in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Plag1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ppargc1a",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04371  Apelin signaling pathway, mmu04714  Thermogenesis, mmu04910  Insulin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04922  Glucagon signaling pathway, mmu04931  Insulin resistance, mmu04936  Alcoholic liver disease, mmu05016  Huntington disease"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ffar2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04024  cAMP signaling pathway"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Cd40",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04064  NF-kappa B signaling pathway, mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05330  Allograft rejection, mmu05340  Primary immunodeficiency, mmu05416  Viral myocarditis, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Il4",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04151  PI3K-Akt signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04664  Fc epsilon RI signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05140  Leishmaniasis, mmu05200  Pathways in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Cdx2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu05226  Gastric cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Sin3a",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04919  Thyroid hormone signaling pathway, mmu05016  Huntington disease, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Esr1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04915  Estrogen signaling pathway, mmu04917  Prolactin signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu04961  Endocrine and other factor-regulated calcium reabsorption, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05224  Breast cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Phf1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Smad3",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04144  Endocytosis, mmu04218  Cellular senescence, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05161  Hepatitis B, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05220  Chronic myeloid leukemia, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Clock",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04710  Circadian rhythm, mmu04728  Dopaminergic synapse"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Cdx1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hif1a",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04066  HIF-1 signaling pathway, mmu04137  Mitophagy - animal, mmu04140  Autophagy - animal, mmu04659  Th17 cell differentiation, mmu04919  Thyroid hormone signaling pathway, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05211  Renal cell carcinoma, mmu05230  Central carbon metabolism in cancer, mmu05231  Choline metabolism in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Lef1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04310  Wnt signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04916  Melanogenesis, mmu04934  Cushing syndrome, mmu04936  Alcoholic liver disease, mmu05132  Salmonella infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05215  Prostate cancer, mmu05216  Thyroid cancer, mmu05217  Basal cell carcinoma, mmu05221  Acute myeloid leukemia, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05412  Arrhythmogenic right ventricular cardiomyopathy"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Stat1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04062  Chemokine signaling pathway, mmu04217  Necroptosis, mmu04380  Osteoclast differentiation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04917  Prolactin signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04935  Growth hormone synthesis, secretion and action, mmu05140  Leishmaniasis, mmu05145  Toxoplasmosis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05212  Pancreatic cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Nfya",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04612  Antigen processing and presentation, mmu05017  Spinocerebellar ataxia, mmu05152  Tuberculosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Gli1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04024  cAMP signaling pathway, mmu04340  Hedgehog signaling pathway, mmu05200  Pathways in cancer, mmu05217  Basal cell carcinoma"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Neurog3",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04950  Maturity onset diabetes of the young"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ctnnb1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04015  Rap1 signaling pathway, mmu04310  Wnt signaling pathway, mmu04390  Hippo signaling pathway, mmu04510  Focal adhesion, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04670  Leukocyte transendothelial migration, mmu04916  Melanogenesis, mmu04919  Thyroid hormone signaling pathway, mmu04934  Cushing syndrome, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05100  Bacterial invasion of epithelial cells, mmu05132  Salmonella infection, mmu05160  Hepatitis C, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05215  Prostate cancer, mmu05216  Thyroid cancer, mmu05217  Basal cell carcinoma, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05412  Arrhythmogenic right ventricular cardiomyopathy, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Egr1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04371  Apelin signaling pathway, mmu04912  GnRH signaling pathway, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05020  Prion disease, mmu05166  Human T-cell leukemia virus 1 infection"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ep300",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu03250  Viral life cycle - HIV-1, mmu04024  cAMP signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04310  Wnt signaling pathway, mmu04330  Notch signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04520  Adherens junction, mmu04630  JAK-STAT signaling pathway, mmu04720  Long-term potentiation, mmu04916  Melanogenesis, mmu04919  Thyroid hormone signaling pathway, mmu04922  Glucagon signaling pathway, mmu04935  Growth hormone synthesis, secretion and action, mmu05016  Huntington disease, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05203  Viral carcinogenesis, mmu05206  MicroRNAs in cancer, mmu05211  Renal cell carcinoma, mmu05215  Prostate cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Pdx1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04911  Insulin secretion, mmu04930  Type II diabetes mellitus, mmu04950  Maturity onset diabetes of the young"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ifng",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu03050  Proteasome, mmu04060  Cytokine-cytokine receptor interaction, mmu04066  HIF-1 signaling pathway, mmu04217  Necroptosis, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04630  JAK-STAT signaling pathway, mmu04650  Natural killer cell mediated cytotoxicity, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04940  Type I diabetes mellitus, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05200  Pathways in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Pparg",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu03320  PPAR signaling pathway, mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04380  Osteoclast differentiation, mmu04714  Thermogenesis, mmu04932  Non-alcoholic fatty liver disease, mmu05016  Huntington disease, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05216  Thyroid cancer, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ahr",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04659  Th17 cell differentiation, mmu04934  Cushing syndrome, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Il12a",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Gata4",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04022  cGMP-PKG signaling pathway, mmu04218  Cellular senescence, mmu04530  Tight junction, mmu04919  Thyroid hormone signaling pathway"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Ets2",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04014  Ras signaling pathway, mmu05166  Human T-cell leukemia virus 1 infection"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Notch1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu01522  Endocrine resistance, mmu04330  Notch signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04919  Thyroid hormone signaling pathway, mmu05020  Prion disease, mmu05165  Human papillomavirus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05224  Breast cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Irf6",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Bmi1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu05202  Transcriptional misregulation in cancer, mmu05206  MicroRNAs in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Smad4",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05161  Hepatitis B, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05220  Chronic myeloid leukemia, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Pgr",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04114  Oocyte meiosis, mmu04914  Progesterone-mediated oocyte maturation, mmu04915  Estrogen signaling pathway, mmu05207  Chemical carcinogenesis - receptor activation, mmu05224  Breast cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hey1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04330  Notch signaling pathway, mmu05165  Human papillomavirus infection, mmu05200  Pathways in cancer, mmu05224  Breast cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Hic1",
        "Alteration": "decrease",
        "Kegg_pathway": "null"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Myc",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04010  MAPK signaling pathway, mmu04012  ErbB signaling pathway, mmu04110  Cell cycle, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04390  Hippo signaling pathway, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04630  JAK-STAT signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu05132  Salmonella infection, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05205  Proteoglycans in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05216  Thyroid cancer, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05221  Acute myeloid leukemia, mmu05222  Small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05230  Central carbon metabolism in cancer"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Klf5",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu05207  Chemical carcinogenesis - receptor activation"
    },
    {
        "Microbiota": "Faecalibacterium_prausnitzii",
        "Gene": "Creb1",
        "Alteration": "decrease",
        "Kegg_pathway": "mmu04022  cGMP-PKG signaling pathway, mmu04024  cAMP signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04261  Adrenergic signaling in cardiomyocytes, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04668  TNF signaling pathway, mmu04710  Circadian rhythm, mmu04713  Circadian entrainment, mmu04714  Thermogenesis, mmu04725  Cholinergic synapse, mmu04728  Dopaminergic synapse, mmu04911  Insulin secretion, mmu04915  Estrogen signaling pathway, mmu04916  Melanogenesis, mmu04918  Thyroid hormone synthesis, mmu04922  Glucagon signaling pathway, mmu04924  Renin secretion, mmu04925  Aldosterone synthesis and secretion, mmu04926  Relaxin signaling pathway, mmu04927  Cortisol synthesis and secretion, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04931  Insulin resistance, mmu04934  Cushing syndrome, mmu04935  Growth hormone synthesis, secretion and action, mmu04962  Vasopressin-regulated water reabsorption, mmu05016  Huntington disease, mmu05020  Prion disease, mmu05030  Cocaine addiction, mmu05031  Amphetamine addiction, mmu05034  Alcoholism, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05203  Viral carcinogenesis, mmu05207  Chemical carcinogenesis - receptor activation, mmu05215  Prostate cancer"
    },
    {
        "response count": 76,
        "response time": "0.669s"
    }
]
```

##### benchmark results

| Microbiota                    | Gene     | Alteration | Kegg\_pathway                                                |
| :---------------------------- | :------- | :--------- | :----------------------------------------------------------- |
| Faecalibacterium\_prausnitzii | IL12B    | decrease   | hsa04060  Cytokine-cytokine receptor interaction, hsa04620  Toll-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04936  Alcoholic liver disease, hsa04940  Type I diabetes mellitus, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05162  Measles, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05205  Proteoglycans in cancer, hsa05321  Inflammatory bowel disease, hsa05330  Allograft rejection, hsa05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | IL12A    | decrease   | hsa04060  Cytokine-cytokine receptor interaction, hsa04620  Toll-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04936  Alcoholic liver disease, hsa04940  Type I diabetes mellitus, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05162  Measles, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05321  Inflammatory bowel disease, hsa05330  Allograft rejection, hsa05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | CXCL8    | decrease   | hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04064  NF-kappa B signaling pathway, hsa04072  Phospholipase D signaling pathway, hsa04218  Cellular senescence, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05135  Yersinia infection, hsa05142  Chagas disease, hsa05144  Malaria, hsa05146  Amoebiasis, hsa05161  Hepatitis B, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05219  Bladder cancer, hsa05323  Rheumatoid arthritis, hsa05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | NFKB1    | decrease   | hsa01523  Antifolate resistance, hsa04010  MAPK signaling pathway, hsa04014  Ras signaling pathway, hsa04024  cAMP signaling pathway, hsa04062  Chemokine signaling pathway, hsa04064  NF-kappa B signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04211  Longevity regulating pathway, hsa04218  Cellular senescence, hsa04380  Osteoclast differentiation, hsa04613  Neutrophil extracellular trap formation, hsa04620  Toll-like receptor signaling pathway, hsa04621  NOD-like receptor signaling pathway, hsa04622  RIG-I-like receptor signaling pathway, hsa04623  Cytosolic DNA-sensing pathway, hsa04625  C-type lectin receptor signaling pathway, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04662  B cell receptor signaling pathway, hsa04668  TNF signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04917  Prolactin signaling pathway, hsa04920  Adipocytokine signaling pathway, hsa04926  Relaxin signaling pathway, hsa04931  Insulin resistance, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05010  Alzheimer disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05030  Cocaine addiction, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05135  Yersinia infection, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05171  Coronavirus disease - COVID-19, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05203  Viral carcinogenesis, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05208  Chemical carcinogenesis - reactive oxygen species, hsa05212  Pancreatic cancer, hsa05215  Prostate cancer, hsa05220  Chronic myeloid leukemia, hsa05221  Acute myeloid leukemia, hsa05222  Small cell lung cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05415  Diabetic cardiomyopathy, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | IFNG     | decrease   | hsa03050  Proteasome, hsa04060  Cytokine-cytokine receptor interaction, hsa04066  HIF-1 signaling pathway, hsa04217  Necroptosis, hsa04350  TGF-beta signaling pathway, hsa04380  Osteoclast differentiation, hsa04612  Antigen processing and presentation, hsa04630  JAK-STAT signaling pathway, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04658  Th1 and Th2 cell differentiation, hsa04659  Th17 cell differentiation, hsa04660  T cell receptor signaling pathway, hsa04940  Type I diabetes mellitus, hsa05140  Leishmaniasis, hsa05142  Chagas disease, hsa05143  African trypanosomiasis, hsa05144  Malaria, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05164  Influenza A, hsa05168  Herpes simplex virus 1 infection, hsa05200  Pathways in cancer, hsa05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, hsa05321  Inflammatory bowel disease, hsa05322  Systemic lupus erythematosus, hsa05323  Rheumatoid arthritis, hsa05330  Allograft rejection, hsa05332  Graft-versus-host disease, hsa05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | Il6      | decrease   | mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu01523  Antifolate resistance, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04623  Cytosolic DNA-sensing pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04659  Th17 cell differentiation, mmu04668  TNF signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05321  Inflammatory bowel disease, mmu05323  Rheumatoid arthritis, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Arnt     | decrease   | mmu04066  HIF-1 signaling pathway, mmu04934  Cushing syndrome, mmu05200  Pathways in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05211  Renal cell carcinoma |
| Faecalibacterium\_prausnitzii | Sox11    | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Brd7     | decrease   | mmu05225  Hepatocellular carcinoma                           |
| Faecalibacterium\_prausnitzii | Zbtb17   | decrease   | mmu04110  Cell cycle, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05222  Small cell lung cancer |
| Faecalibacterium\_prausnitzii | Foxa1    | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Smad2    | decrease   | mmu04110  Cell cycle, mmu04144  Endocytosis, mmu04218  Cellular senescence, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04926  Relaxin signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05142  Chagas disease, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy |
| Faecalibacterium\_prausnitzii | Fos      | decrease   | mmu01522  Endocrine resistance, mmu04010  MAPK signaling pathway, mmu04024  cAMP signaling pathway, mmu04210  Apoptosis, mmu04380  Osteoclast differentiation, mmu04620  Toll-like receptor signaling pathway, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04662  B cell receptor signaling pathway, mmu04668  TNF signaling pathway, mmu04713  Circadian entrainment, mmu04725  Cholinergic synapse, mmu04728  Dopaminergic synapse, mmu04915  Estrogen signaling pathway, mmu04917  Prolactin signaling pathway, mmu04921  Oxytocin signaling pathway, mmu04926  Relaxin signaling pathway, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04932  Non-alcoholic fatty liver disease, mmu04935  Growth hormone synthesis, secretion and action, mmu05031  Amphetamine addiction, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05161  Hepatitis B, mmu05162  Measles, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05210  Colorectal cancer, mmu05224  Breast cancer, mmu05231  Choline metabolism in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05323  Rheumatoid arthritis, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | E2f1     | decrease   | mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04137  Mitophagy - animal, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer |
| Faecalibacterium\_prausnitzii | Mnt      | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Stat3    | decrease   | mmu01521  EGFR tyrosine kinase inhibitor resistance, mmu04062  Chemokine signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04217  Necroptosis, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04630  JAK-STAT signaling pathway, mmu04659  Th17 cell differentiation, mmu04917  Prolactin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04931  Insulin resistance, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04935  Growth hormone synthesis, secretion and action, mmu05145  Toxoplasmosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05163  Human cytomegalovirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05203  Viral carcinogenesis, mmu05205  Proteoglycans in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05212  Pancreatic cancer, mmu05221  Acute myeloid leukemia, mmu05223  Non-small cell lung cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Tnf      | decrease   | mmu01523  Antifolate resistance, mmu04010  MAPK signaling pathway, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04064  NF-kappa B signaling pathway, mmu04071  Sphingolipid signaling pathway, mmu04150  mTOR signaling pathway, mmu04210  Apoptosis, mmu04217  Necroptosis, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04650  Natural killer cell mediated cytotoxicity, mmu04657  IL-17 signaling pathway, mmu04660  T cell receptor signaling pathway, mmu04664  Fc epsilon RI signaling pathway, mmu04668  TNF signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04930  Type II diabetes mellitus, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05010  Alzheimer disease, mmu05014  Amyotrophic lateral sclerosis, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05205  Proteoglycans in cancer, mmu05310  Asthma, mmu05321  Inflammatory bowel disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05414  Dilated cardiomyopathy, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | Il12b    | decrease   | mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Ppara    | decrease   | mmu03320  PPAR signaling pathway, mmu04024  cAMP signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04922  Glucagon signaling pathway, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04936  Alcoholic liver disease, mmu05160  Hepatitis C, mmu05207  Chemical carcinogenesis - receptor activation, mmu05415  Diabetic cardiomyopathy |
| Faecalibacterium\_prausnitzii | Hdac3    | decrease   | mmu04613  Neutrophil extracellular trap formation, mmu04919  Thyroid hormone signaling pathway, mmu05034  Alcoholism, mmu05203  Viral carcinogenesis |
| Faecalibacterium\_prausnitzii | Onecut1  | decrease   | mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04950  Maturity onset diabetes of the young |
| Faecalibacterium\_prausnitzii | Relb     | decrease   | mmu04010  MAPK signaling pathway, mmu04064  NF-kappa B signaling pathway, mmu04380  Osteoclast differentiation, mmu04625  C-type lectin receptor signaling pathway, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection |
| Faecalibacterium\_prausnitzii | Hnf1b    | decrease   | mmu04950  Maturity onset diabetes of the young               |
| Faecalibacterium\_prausnitzii | Tcf4     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Mybl2    | decrease   | mmu04218  Cellular senescence                                |
| Faecalibacterium\_prausnitzii | Mtpn     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Foxm1    | decrease   | mmu04218  Cellular senescence                                |
| Faecalibacterium\_prausnitzii | E2f2     | decrease   | mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer |
| Faecalibacterium\_prausnitzii | E2f3     | decrease   | mmu01522  Endocrine resistance, mmu04110  Cell cycle, mmu04218  Cellular senescence, mmu04934  Cushing syndrome, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05212  Pancreatic cancer, mmu05214  Glioma, mmu05215  Prostate cancer, mmu05218  Melanoma, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05222  Small cell lung cancer, mmu05223  Non-small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer |
| Faecalibacterium\_prausnitzii | Mta1     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Tfdp1    | decrease   | mmu04110  Cell cycle, mmu04350  TGF-beta signaling pathway   |
| Faecalibacterium\_prausnitzii | Yy1      | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Tfap2c   | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Ezh2     | decrease   | mmu00310  Lysine degradation, mmu01100  Metabolic pathways, mmu05206  MicroRNAs in cancer |
| Faecalibacterium\_prausnitzii | Elp1     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Hnf1a    | decrease   | mmu04950  Maturity onset diabetes of the young               |
| Faecalibacterium\_prausnitzii | Nfe2l2   | decrease   | mmu04141  Protein processing in endoplasmic reticulum, mmu05012  Parkinson disease, mmu05200  Pathways in cancer, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05225  Hepatocellular carcinoma, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | Fli1     | decrease   | mmu05202  Transcriptional misregulation in cancer            |
| Faecalibacterium\_prausnitzii | Plag1    | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Ppargc1a | decrease   | mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04371  Apelin signaling pathway, mmu04714  Thermogenesis, mmu04910  Insulin signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04922  Glucagon signaling pathway, mmu04931  Insulin resistance, mmu04936  Alcoholic liver disease, mmu05016  Huntington disease |
| Faecalibacterium\_prausnitzii | Ffar2    | decrease   | mmu04024  cAMP signaling pathway                             |
| Faecalibacterium\_prausnitzii | Cd40     | decrease   | mmu04060  Cytokine-cytokine receptor interaction, mmu04064  NF-kappa B signaling pathway, mmu04514  Cell adhesion molecules, mmu04620  Toll-like receptor signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05166  Human T-cell leukemia virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05322  Systemic lupus erythematosus, mmu05330  Allograft rejection, mmu05340  Primary immunodeficiency, mmu05416  Viral myocarditis, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Il4      | decrease   | mmu04060  Cytokine-cytokine receptor interaction, mmu04151  PI3K-Akt signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04664  Fc epsilon RI signaling pathway, mmu04672  Intestinal immune network for IgA production, mmu05140  Leishmaniasis, mmu05200  Pathways in cancer, mmu05310  Asthma, mmu05320  Autoimmune thyroid disease, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection |
| Faecalibacterium\_prausnitzii | Cdx2     | decrease   | mmu05226  Gastric cancer                                     |
| Faecalibacterium\_prausnitzii | Sin3a    | decrease   | mmu04919  Thyroid hormone signaling pathway, mmu05016  Huntington disease, mmu05169  Epstein-Barr virus infection, mmu05202  Transcriptional misregulation in cancer |
| Faecalibacterium\_prausnitzii | Esr1     | decrease   | mmu01522  Endocrine resistance, mmu04915  Estrogen signaling pathway, mmu04917  Prolactin signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu04961  Endocrine and other factor-regulated calcium reabsorption, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05224  Breast cancer |
| Faecalibacterium\_prausnitzii | Phf1     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Smad3    | decrease   | mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04144  Endocytosis, mmu04218  Cellular senescence, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05161  Hepatitis B, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05220  Chronic myeloid leukemia, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05321  Inflammatory bowel disease, mmu05415  Diabetic cardiomyopathy |
| Faecalibacterium\_prausnitzii | Clock    | decrease   | mmu04710  Circadian rhythm, mmu04728  Dopaminergic synapse   |
| Faecalibacterium\_prausnitzii | Cdx1     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Hif1a    | decrease   | mmu04066  HIF-1 signaling pathway, mmu04137  Mitophagy - animal, mmu04140  Autophagy - animal, mmu04659  Th17 cell differentiation, mmu04919  Thyroid hormone signaling pathway, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05208  Chemical carcinogenesis - reactive oxygen species, mmu05211  Renal cell carcinoma, mmu05230  Central carbon metabolism in cancer, mmu05231  Choline metabolism in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer |
| Faecalibacterium\_prausnitzii | Lef1     | decrease   | mmu04310  Wnt signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04916  Melanogenesis, mmu04934  Cushing syndrome, mmu04936  Alcoholic liver disease, mmu05132  Salmonella infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05215  Prostate cancer, mmu05216  Thyroid cancer, mmu05217  Basal cell carcinoma, mmu05221  Acute myeloid leukemia, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05412  Arrhythmogenic right ventricular cardiomyopathy |
| Faecalibacterium\_prausnitzii | Stat1    | decrease   | mmu04062  Chemokine signaling pathway, mmu04217  Necroptosis, mmu04380  Osteoclast differentiation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04917  Prolactin signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04935  Growth hormone synthesis, secretion and action, mmu05140  Leishmaniasis, mmu05145  Toxoplasmosis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05162  Measles, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05212  Pancreatic cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease |
| Faecalibacterium\_prausnitzii | Nfya     | decrease   | mmu04612  Antigen processing and presentation, mmu05017  Spinocerebellar ataxia, mmu05152  Tuberculosis |
| Faecalibacterium\_prausnitzii | Gli1     | decrease   | mmu04024  cAMP signaling pathway, mmu04340  Hedgehog signaling pathway, mmu05200  Pathways in cancer, mmu05217  Basal cell carcinoma |
| Faecalibacterium\_prausnitzii | Neurog3  | decrease   | mmu04950  Maturity onset diabetes of the young               |
| Faecalibacterium\_prausnitzii | Ctnnb1   | decrease   | mmu04015  Rap1 signaling pathway, mmu04310  Wnt signaling pathway, mmu04390  Hippo signaling pathway, mmu04510  Focal adhesion, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04670  Leukocyte transendothelial migration, mmu04916  Melanogenesis, mmu04919  Thyroid hormone signaling pathway, mmu04934  Cushing syndrome, mmu04936  Alcoholic liver disease, mmu05010  Alzheimer disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05100  Bacterial invasion of epithelial cells, mmu05132  Salmonella infection, mmu05160  Hepatitis C, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05215  Prostate cancer, mmu05216  Thyroid cancer, mmu05217  Basal cell carcinoma, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05412  Arrhythmogenic right ventricular cardiomyopathy, mmu05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | Egr1     | decrease   | mmu04371  Apelin signaling pathway, mmu04912  GnRH signaling pathway, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05020  Prion disease, mmu05166  Human T-cell leukemia virus 1 infection |
| Faecalibacterium\_prausnitzii | Ep300    | decrease   | mmu03250  Viral life cycle - HIV-1, mmu04024  cAMP signaling pathway, mmu04066  HIF-1 signaling pathway, mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04310  Wnt signaling pathway, mmu04330  Notch signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04520  Adherens junction, mmu04630  JAK-STAT signaling pathway, mmu04720  Long-term potentiation, mmu04916  Melanogenesis, mmu04919  Thyroid hormone signaling pathway, mmu04922  Glucagon signaling pathway, mmu04935  Growth hormone synthesis, secretion and action, mmu05016  Huntington disease, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05200  Pathways in cancer, mmu05203  Viral carcinogenesis, mmu05206  MicroRNAs in cancer, mmu05211  Renal cell carcinoma, mmu05215  Prostate cancer |
| Faecalibacterium\_prausnitzii | Pdx1     | decrease   | mmu04911  Insulin secretion, mmu04930  Type II diabetes mellitus, mmu04950  Maturity onset diabetes of the young |
| Faecalibacterium\_prausnitzii | Ifng     | decrease   | mmu03050  Proteasome, mmu04060  Cytokine-cytokine receptor interaction, mmu04066  HIF-1 signaling pathway, mmu04217  Necroptosis, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04630  JAK-STAT signaling pathway, mmu04650  Natural killer cell mediated cytotoxicity, mmu04657  IL-17 signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04659  Th17 cell differentiation, mmu04660  T cell receptor signaling pathway, mmu04940  Type I diabetes mellitus, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05200  Pathways in cancer, mmu05235  PD-L1 expression and PD-1 checkpoint pathway in cancer, mmu05321  Inflammatory bowel disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05418  Fluid shear stress and atherosclerosis |
| Faecalibacterium\_prausnitzii | Pparg    | decrease   | mmu03320  PPAR signaling pathway, mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04380  Osteoclast differentiation, mmu04714  Thermogenesis, mmu04932  Non-alcoholic fatty liver disease, mmu05016  Huntington disease, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05216  Thyroid cancer, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Ahr      | decrease   | mmu04659  Th17 cell differentiation, mmu04934  Cushing syndrome, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species |
| Faecalibacterium\_prausnitzii | Il12a    | decrease   | mmu04060  Cytokine-cytokine receptor interaction, mmu04620  Toll-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04630  JAK-STAT signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05162  Measles, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05200  Pathways in cancer, mmu05321  Inflammatory bowel disease, mmu05330  Allograft rejection, mmu05417  Lipid and atherosclerosis |
| Faecalibacterium\_prausnitzii | Gata4    | decrease   | mmu04022  cGMP-PKG signaling pathway, mmu04218  Cellular senescence, mmu04530  Tight junction, mmu04919  Thyroid hormone signaling pathway |
| Faecalibacterium\_prausnitzii | Ets2     | decrease   | mmu04014  Ras signaling pathway, mmu05166  Human T-cell leukemia virus 1 infection |
| Faecalibacterium\_prausnitzii | Notch1   | decrease   | mmu01522  Endocrine resistance, mmu04330  Notch signaling pathway, mmu04658  Th1 and Th2 cell differentiation, mmu04919  Thyroid hormone signaling pathway, mmu05020  Prion disease, mmu05165  Human papillomavirus infection, mmu05200  Pathways in cancer, mmu05206  MicroRNAs in cancer, mmu05224  Breast cancer |
| Faecalibacterium\_prausnitzii | Irf6     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Bmi1     | decrease   | mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu05202  Transcriptional misregulation in cancer, mmu05206  MicroRNAs in cancer |
| Faecalibacterium\_prausnitzii | Smad4    | decrease   | mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04371  Apelin signaling pathway, mmu04390  Hippo signaling pathway, mmu04520  Adherens junction, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04659  Th17 cell differentiation, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05161  Hepatitis B, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05210  Colorectal cancer, mmu05212  Pancreatic cancer, mmu05220  Chronic myeloid leukemia, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer |
| Faecalibacterium\_prausnitzii | Pgr      | decrease   | mmu04114  Oocyte meiosis, mmu04914  Progesterone-mediated oocyte maturation, mmu04915  Estrogen signaling pathway, mmu05207  Chemical carcinogenesis - receptor activation, mmu05224  Breast cancer |
| Faecalibacterium\_prausnitzii | Hey1     | decrease   | mmu04330  Notch signaling pathway, mmu05165  Human papillomavirus infection, mmu05200  Pathways in cancer, mmu05224  Breast cancer |
| Faecalibacterium\_prausnitzii | Hic1     | decrease   | null                                                         |
| Faecalibacterium\_prausnitzii | Myc      | decrease   | mmu04010  MAPK signaling pathway, mmu04012  ErbB signaling pathway, mmu04110  Cell cycle, mmu04151  PI3K-Akt signaling pathway, mmu04218  Cellular senescence, mmu04310  Wnt signaling pathway, mmu04350  TGF-beta signaling pathway, mmu04390  Hippo signaling pathway, mmu04550  Signaling pathways regulating pluripotency of stem cells, mmu04630  JAK-STAT signaling pathway, mmu04919  Thyroid hormone signaling pathway, mmu05132  Salmonella infection, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05169  Epstein-Barr virus infection, mmu05200  Pathways in cancer, mmu05202  Transcriptional misregulation in cancer, mmu05205  Proteoglycans in cancer, mmu05206  MicroRNAs in cancer, mmu05207  Chemical carcinogenesis - receptor activation, mmu05210  Colorectal cancer, mmu05213  Endometrial cancer, mmu05216  Thyroid cancer, mmu05219  Bladder cancer, mmu05220  Chronic myeloid leukemia, mmu05221  Acute myeloid leukemia, mmu05222  Small cell lung cancer, mmu05224  Breast cancer, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05230  Central carbon metabolism in cancer |
| Faecalibacterium\_prausnitzii | Klf5     | decrease   | mmu05207  Chemical carcinogenesis - receptor activation      |
| Faecalibacterium\_prausnitzii | Creb1    | decrease   | mmu04022  cGMP-PKG signaling pathway, mmu04024  cAMP signaling pathway, mmu04151  PI3K-Akt signaling pathway, mmu04152  AMPK signaling pathway, mmu04211  Longevity regulating pathway, mmu04261  Adrenergic signaling in cardiomyocytes, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04668  TNF signaling pathway, mmu04710  Circadian rhythm, mmu04713  Circadian entrainment, mmu04714  Thermogenesis, mmu04725  Cholinergic synapse, mmu04728  Dopaminergic synapse, mmu04911  Insulin secretion, mmu04915  Estrogen signaling pathway, mmu04916  Melanogenesis, mmu04918  Thyroid hormone synthesis, mmu04922  Glucagon signaling pathway, mmu04924  Renin secretion, mmu04925  Aldosterone synthesis and secretion, mmu04926  Relaxin signaling pathway, mmu04927  Cortisol synthesis and secretion, mmu04928  Parathyroid hormone synthesis, secretion and action, mmu04931  Insulin resistance, mmu04934  Cushing syndrome, mmu04935  Growth hormone synthesis, secretion and action, mmu04962  Vasopressin-regulated water reabsorption, mmu05016  Huntington disease, mmu05020  Prion disease, mmu05030  Cocaine addiction, mmu05031  Amphetamine addiction, mmu05034  Alcoholism, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05167  Kaposi sarcoma-associated herpesvirus infection, mmu05203  Viral carcinogenesis, mmu05207  Chemical carcinogenesis - receptor activation, mmu05215  Prostate cancer |



#### Q5 For human beings, Which microbial abundance and thus which gene expression changes can infliximab interfere with? What metabolic pathways are these genes involved in?

##### federated query results

```json
[
    {
        "Drug": "Infliximab",
        "Microbiota": "Streptococcus",
        "Alteration_microbiota": "increase",
        "Gene": "CXCL6",
        "Alteration_gene": "decrease",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa05133  Pertussis, hsa05323  Rheumatoid arthritis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Streptococcus",
        "Alteration_microbiota": "increase",
        "Gene": "CCL20",
        "Alteration_gene": "decrease",
        "Kegg_pathway": "hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa05323  Rheumatoid arthritis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Gene": "BCL2",
        "Alteration_gene": "decrease",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04064  NF-kappa B signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04140  Autophagy - animal, hsa04141  Protein processing in endoplasmic reticulum, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04261  Adrenergic signaling in cardiomyocytes, hsa04340  Hedgehog signaling pathway, hsa04510  Focal adhesion, hsa04621  NOD-like receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04725  Cholinergic synapse, hsa04915  Estrogen signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05014  Amyotrophic lateral sclerosis, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05145  Toxoplasmosis, hsa05152  Tuberculosis, hsa05161  Hepatitis B, hsa05162  Measles, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05210  Colorectal cancer, hsa05215  Prostate cancer, hsa05222  Small cell lung cancer, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Gene": "BAX",
        "Alteration_gene": "increase",
        "Kegg_pathway": "hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04141  Protein processing in endoplasmic reticulum, hsa04210  Apoptosis, hsa04211  Longevity regulating pathway, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04722  Neurotrophin signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05203  Viral carcinogenesis, hsa05210  Colorectal cancer, hsa05212  Pancreatic cancer, hsa05213  Endometrial cancer, hsa05214  Glioma, hsa05216  Thyroid cancer, hsa05217  Basal cell carcinoma, hsa05218  Melanoma, hsa05220  Chronic myeloid leukemia, hsa05222  Small cell lung cancer, hsa05223  Non-small cell lung cancer, hsa05224  Breast cancer, hsa05225  Hepatocellular carcinoma, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Tgfb1",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu04010  MAPK signaling pathway, mmu04060  Cytokine-cytokine receptor interaction, mmu04068  FoxO signaling pathway, mmu04110  Cell cycle, mmu04218  Cellular senescence, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04390  Hippo signaling pathway, mmu04659  Th17 cell differentiation, mmu04672  Intestinal immune network for IgA production, mmu04926  Relaxin signaling pathway, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05161  Hepatitis B, mmu05166  Human T-cell leukemia virus 1 infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05210  Colorectal cancer, mmu05211  Renal cell carcinoma, mmu05212  Pancreatic cancer, mmu05220  Chronic myeloid leukemia, mmu05225  Hepatocellular carcinoma, mmu05226  Gastric cancer, mmu05321  Inflammatory bowel disease, mmu05323  Rheumatoid arthritis, mmu05410  Hypertrophic cardiomyopathy, mmu05414  Dilated cardiomyopathy, mmu05415  Diabetic cardiomyopathy"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Fn1",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu04151  PI3K-Akt signaling pathway, mmu04510  Focal adhesion, mmu04512  ECM-receptor interaction, mmu04810  Regulation of actin cytoskeleton, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05100  Bacterial invasion of epithelial cells, mmu05135  Yersinia infection, mmu05146  Amoebiasis, mmu05165  Human papillomavirus infection, mmu05200  Pathways in cancer, mmu05205  Proteoglycans in cancer, mmu05222  Small cell lung cancer"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Col1a1",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu04151  PI3K-Akt signaling pathway, mmu04510  Focal adhesion, mmu04512  ECM-receptor interaction, mmu04611  Platelet activation, mmu04926  Relaxin signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04974  Protein digestion and absorption, mmu05146  Amoebiasis, mmu05165  Human papillomavirus infection, mmu05205  Proteoglycans in cancer, mmu05415  Diabetic cardiomyopathy"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Tnf",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu01523  Antifolate resistance, mmu04010  MAPK signaling pathway, mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04064  NF-kappa B signaling pathway, mmu04071  Sphingolipid signaling pathway, mmu04150  mTOR signaling pathway, mmu04210  Apoptosis, mmu04217  Necroptosis, mmu04350  TGF-beta signaling pathway, mmu04380  Osteoclast differentiation, mmu04612  Antigen processing and presentation, mmu04620  Toll-like receptor signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04622  RIG-I-like receptor signaling pathway, mmu04625  C-type lectin receptor signaling pathway, mmu04640  Hematopoietic cell lineage, mmu04650  Natural killer cell mediated cytotoxicity, mmu04657  IL-17 signaling pathway, mmu04660  T cell receptor signaling pathway, mmu04664  Fc epsilon RI signaling pathway, mmu04668  TNF signaling pathway, mmu04920  Adipocytokine signaling pathway, mmu04930  Type II diabetes mellitus, mmu04931  Insulin resistance, mmu04932  Non-alcoholic fatty liver disease, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu04936  Alcoholic liver disease, mmu04940  Type I diabetes mellitus, mmu05010  Alzheimer disease, mmu05014  Amyotrophic lateral sclerosis, mmu05020  Prion disease, mmu05022  Pathways of neurodegeneration - multiple diseases, mmu05132  Salmonella infection, mmu05133  Pertussis, mmu05134  Legionellosis, mmu05135  Yersinia infection, mmu05140  Leishmaniasis, mmu05142  Chagas disease, mmu05143  African trypanosomiasis, mmu05144  Malaria, mmu05145  Toxoplasmosis, mmu05146  Amoebiasis, mmu05152  Tuberculosis, mmu05160  Hepatitis C, mmu05161  Hepatitis B, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05165  Human papillomavirus infection, mmu05166  Human T-cell leukemia virus 1 infection, mmu05168  Herpes simplex virus 1 infection, mmu05169  Epstein-Barr virus infection, mmu05170  Human immunodeficiency virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05205  Proteoglycans in cancer, mmu05310  Asthma, mmu05321  Inflammatory bowel disease, mmu05322  Systemic lupus erythematosus, mmu05323  Rheumatoid arthritis, mmu05330  Allograft rejection, mmu05332  Graft-versus-host disease, mmu05410  Hypertrophic cardiomyopathy, mmu05414  Dilated cardiomyopathy, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Slco4c1",
        "Alteration_gene": "increase",
        "Kegg_pathway": "null"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Gene": "CASP3",
        "Alteration_gene": "increase",
        "Kegg_pathway": "hsa01524  Platinum drug resistance, hsa04010  MAPK signaling pathway, hsa04115  p53 signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa04726  Serotonergic synapse, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05010  Alzheimer disease, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05205  Proteoglycans in cancer, hsa05206  MicroRNAs in cancer, hsa05210  Colorectal cancer, hsa05222  Small cell lung cancer, hsa05416  Viral myocarditis, hsa05417  Lipid and atherosclerosis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Ccl2",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu04060  Cytokine-cytokine receptor interaction, mmu04061  Viral protein interaction with cytokine and cytokine receptor, mmu04062  Chemokine signaling pathway, mmu04621  NOD-like receptor signaling pathway, mmu04657  IL-17 signaling pathway, mmu04668  TNF signaling pathway, mmu04933  AGE-RAGE signaling pathway in diabetic complications, mmu05135  Yersinia infection, mmu05142  Chagas disease, mmu05144  Malaria, mmu05163  Human cytomegalovirus infection, mmu05164  Influenza A, mmu05168  Herpes simplex virus 1 infection, mmu05171  Coronavirus disease - COVID-19, mmu05323  Rheumatoid arthritis, mmu05417  Lipid and atherosclerosis, mmu05418  Fluid shear stress and atherosclerosis"
    },
    {
        "Drug": "Infliximab",
        "Microbiota": "Desulfovibrionaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Ahr",
        "Alteration_gene": "increase",
        "Kegg_pathway": "mmu04659  Th17 cell differentiation, mmu04934  Cushing syndrome, mmu05207  Chemical carcinogenesis - receptor activation, mmu05208  Chemical carcinogenesis - reactive oxygen species"
    },
    {
        "response count": 12,
        "response time": "0.253s"
    }
]
```

##### benchmark results

| Drug       | Microbiota    | Alteration\_microbiota | Gene  | Alteration\_gene | Kegg\_pathway                                                |
| :--------- | :------------ | :--------------------- | :---- | :--------------- | :----------------------------------------------------------- |
| Infliximab | Streptococcus | increase               | CXCL6 | decrease         | hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa05133  Pertussis, hsa05323  Rheumatoid arthritis |
| Infliximab | Streptococcus | increase               | CCL20 | decrease         | hsa04060  Cytokine-cytokine receptor interaction, hsa04061  Viral protein interaction with cytokine and cytokine receptor, hsa04062  Chemokine signaling pathway, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa05323  Rheumatoid arthritis |
| Infliximab | Enterococcus  | increase               | BCL2  | decrease         | hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04064  NF-kappa B signaling pathway, hsa04066  HIF-1 signaling pathway, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04140  Autophagy - animal, hsa04141  Protein processing in endoplasmic reticulum, hsa04151  PI3K-Akt signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04261  Adrenergic signaling in cardiomyocytes, hsa04340  Hedgehog signaling pathway, hsa04510  Focal adhesion, hsa04621  NOD-like receptor signaling pathway, hsa04630  JAK-STAT signaling pathway, hsa04722  Neurotrophin signaling pathway, hsa04725  Cholinergic synapse, hsa04915  Estrogen signaling pathway, hsa04928  Parathyroid hormone synthesis, secretion and action, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05014  Amyotrophic lateral sclerosis, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05145  Toxoplasmosis, hsa05152  Tuberculosis, hsa05161  Hepatitis B, hsa05162  Measles, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05206  MicroRNAs in cancer, hsa05207  Chemical carcinogenesis - receptor activation, hsa05210  Colorectal cancer, hsa05215  Prostate cancer, hsa05222  Small cell lung cancer, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis, hsa05418  Fluid shear stress and atherosclerosis |
| Infliximab | Enterococcus  | increase               | BAX   | increase         | hsa01521  EGFR tyrosine kinase inhibitor resistance, hsa01522  Endocrine resistance, hsa01524  Platinum drug resistance, hsa04071  Sphingolipid signaling pathway, hsa04115  p53 signaling pathway, hsa04141  Protein processing in endoplasmic reticulum, hsa04210  Apoptosis, hsa04211  Longevity regulating pathway, hsa04215  Apoptosis - multiple species, hsa04217  Necroptosis, hsa04722  Neurotrophin signaling pathway, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05130  Pathogenic Escherichia coli infection, hsa05131  Shigellosis, hsa05132  Salmonella infection, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05166  Human T-cell leukemia virus 1 infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05202  Transcriptional misregulation in cancer, hsa05203  Viral carcinogenesis, hsa05210  Colorectal cancer, hsa05212  Pancreatic cancer, hsa05213  Endometrial cancer, hsa05214  Glioma, hsa05216  Thyroid cancer, hsa05217  Basal cell carcinoma, hsa05218  Melanoma, hsa05220  Chronic myeloid leukemia, hsa05222  Small cell lung cancer, hsa05223  Non-small cell lung cancer, hsa05224  Breast cancer, hsa05225  Hepatocellular carcinoma, hsa05226  Gastric cancer, hsa05417  Lipid and atherosclerosis |
| Infliximab | Enterococcus  | increase               | CASP3 | increase         | hsa01524  Platinum drug resistance, hsa04010  MAPK signaling pathway, hsa04115  p53 signaling pathway, hsa04210  Apoptosis, hsa04215  Apoptosis - multiple species, hsa04650  Natural killer cell mediated cytotoxicity, hsa04657  IL-17 signaling pathway, hsa04668  TNF signaling pathway, hsa04726  Serotonergic synapse, hsa04932  Non-alcoholic fatty liver disease, hsa04933  AGE-RAGE signaling pathway in diabetic complications, hsa04936  Alcoholic liver disease, hsa05010  Alzheimer disease, hsa05012  Parkinson disease, hsa05014  Amyotrophic lateral sclerosis, hsa05016  Huntington disease, hsa05020  Prion disease, hsa05022  Pathways of neurodegeneration - multiple diseases, hsa05120  Epithelial cell signaling in Helicobacter pylori infection, hsa05130  Pathogenic Escherichia coli infection, hsa05132  Salmonella infection, hsa05133  Pertussis, hsa05134  Legionellosis, hsa05145  Toxoplasmosis, hsa05146  Amoebiasis, hsa05152  Tuberculosis, hsa05160  Hepatitis C, hsa05161  Hepatitis B, hsa05162  Measles, hsa05163  Human cytomegalovirus infection, hsa05164  Influenza A, hsa05165  Human papillomavirus infection, hsa05167  Kaposi sarcoma-associated herpesvirus infection, hsa05168  Herpes simplex virus 1 infection, hsa05169  Epstein-Barr virus infection, hsa05170  Human immunodeficiency virus 1 infection, hsa05200  Pathways in cancer, hsa05203  Viral carcinogenesis, hsa05205  Proteoglycans in cancer, hsa05206  MicroRNAs in cancer, hsa05210  Colorectal cancer, hsa05222  Small cell lung cancer, hsa05416  Viral myocarditis, hsa05417  Lipid and atherosclerosis |



#### Q6 What intestinal microbial levels are altered by Helicobacter pylori infection in humans? What metabolites are produced by these bacteria?

##### federated query results

```json
[
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Folic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Lactate"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Phenylacetic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "3-Hydroxyphenethyl alcohol"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Dihydrocaffeoyl-glycerol"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "2,3-Dihydroxypropyl (E)-3-(3,4-dihydroxyphenyl)prop-2-enoate"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Dihydrochlorogenic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Dehydroxychlorogenic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "3-(3-Hydroxyphenyl)propanoic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Dihydrocaffeic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Caffeic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bifidobacterium",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Actinobacteria",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Collinsella",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration_Microbiota": "decrease",
        "Metabolite": "Acetate"
    },
    {
        "response count": 20,
        "response time": "0.121s"
    }
]
```

##### benchmark results

| Disorder                        | Microbiota      | Alteration\_Microbiota | Metabolite                                                   |
| :------------------------------ | :-------------- | :--------------------- | :----------------------------------------------------------- |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Propionate                                                   |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Acetate                                                      |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Folic acid                                                   |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Hydroquinone                                                 |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Lactate                                                      |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Phenylacetic acid                                            |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | 3-Hydroxyphenethyl alcohol                                   |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Dihydrocaffeoyl-glycerol                                     |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | 2,3-Dihydroxypropyl \(E\)-3-\(3,4-dihydroxyphenyl\)prop-2-enoate |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Dihydrochlorogenic acid                                      |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Dehydroxychlorogenic acid                                    |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | 3-\(3-Hydroxyphenyl\)propanoic acid                          |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Dihydrocaffeic acid                                          |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Caffeic acid                                                 |
| Helicobacter\_pylori\_infection | Bifidobacterium | decrease               | Trimethylamine oxide                                         |
| Helicobacter\_pylori\_infection | Actinobacteria  | decrease               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Helicobacter\_pylori\_infection | Collinsella     | decrease               | Trimethylamine oxide                                         |
| Helicobacter\_pylori\_infection | Bacteroidetes   | decrease               | Propionate                                                   |
| Helicobacter\_pylori\_infection | Bacteroidetes   | decrease               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Helicobacter\_pylori\_infection | Bacteroidetes   | decrease               | Acetate                                                      |





#### Q7 Which gut microbes are altered by Crohn disease in humans? What metabolites are produced by these microbes?

##### federated query results

```json
[
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Firmicutes",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Firmicutes",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Firmicutes",
        "Alteration_microbiota": "increase",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Actinobacteria",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Cysteine-glutathione disulfide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Oxiglutatione"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Phenyl sulfate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "7a-hydroxy-3-oxo-5b-cholanoate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Nutriadeoxycholate vulpecholate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Pentahomomethionine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Murideoxycholate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo-"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "12-Ketolithocholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Isovaleroylglycine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Acetyl-D-Mannosamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N(6)-Methyllysine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Betonicine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Acetamidobutyric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Creatine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dopamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Veillonella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Klebsiella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Cyanuric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Klebsiella",
        "Alteration_microbiota": "increase",
        "Metabolite": "procollagen type 1 n-terminal propeptide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Klebsiella",
        "Alteration_microbiota": "increase",
        "Metabolite": "type I collagen cross-linked c-telopeptide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Klebsiella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Desulfovibrionaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Tryptophan"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Folic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Phenylacetic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-Hydroxyphenethyl alcohol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrocaffeoyl-glycerol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "2,3-Dihydroxypropyl (E)-3-(3,4-dihydroxyphenyl)prop-2-enoate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrochlorogenic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dehydroxychlorogenic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-(3-Hydroxyphenyl)propanoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrocaffeic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Caffeic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Methanol, (methyl-ONN-azoxy)-"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Hydroxybenzoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Benzoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Amino-1-methyl-6-phenylimidazo[4,5-b]pyridine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Malic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Leucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Serine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium prausnitzii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Bile acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Succinate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Oxalacetic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "increase",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Hypoxanthine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Benzoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Acetyl phosphate(2-)"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Pyruvate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium rectale",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Equol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Genipin"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glycocholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glycerol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Pyridoxic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus bromii",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Tartaric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Lactobacillus fermentum",
        "Alteration_microbiota": "increase",
        "Metabolite": "Ethanol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus torques",
        "Alteration_microbiota": "increase",
        "Metabolite": "Lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus torques",
        "Alteration_microbiota": "increase",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus gnavus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Tryptamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus gnavus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus gnavus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus gnavus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Ursodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus gnavus",
        "Alteration_microbiota": "increase",
        "Metabolite": "beta-D-Fructofuranose"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Akkermansia muciniphila",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Akkermansia muciniphila",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Indoxyl sulfate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Glycocholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Propionate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Succinate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Oxalacetic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Serine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Faecalibacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Leucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Hyocholate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "12-Ketolithocholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Formaminobenzoylacetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Acetyl-D-Mannosamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Cholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Betonicine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Proline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Acetylputrescine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Ursodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "l-Isoleucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Valine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Tyramine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "5-Hydroxyindole-3-acetic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Creatine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glycerophospholipids"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Serine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glycine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Leucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Alanine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus torques",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus torques",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Acetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Hydroquinone"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Hydroxybenzoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Hydroxybenzoic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Eubacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides uniformis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Quercetin"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroides uniformis",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Equol"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Actinobacteria",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "1D-Myo-inositol 1,4,5,6-tetrakisphosphate(8-)"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "[(1S,2R,3S,4S,5R,6S)-2,3,5-Trihydroxy-4,6-diphosphonooxycyclohexyl] dihydrogen phosphate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "1D-Myo-inositol 6-phosphate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "(R)-3-(4-Hydroxyphenyl)lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Ethyl phenyllactate, (-)-"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Quinic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Caffeic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Pipecolic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "1D-Myo-inositol 1,4,5,6-tetrakisphosphate(8-)"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "[(1S,2R,3S,4S,5R,6S)-2,3,5-Trihydroxy-4,6-diphosphonooxycyclohexyl] dihydrogen phosphate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "1D-Myo-inositol 6-phosphate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "(R)-3-(4-Hydroxyphenyl)lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "Ethyl phenyllactate, (-)-"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "Indole"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "Quinic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "Caffeic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Escherichia coli",
        "Alteration_microbiota": "increase",
        "Metabolite": "Pipecolic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium sp.",
        "Alteration_microbiota": "increase",
        "Metabolite": "(R)-3-(4-Hydroxyphenyl)lactate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Clostridium sp.",
        "Alteration_microbiota": "increase",
        "Metabolite": "Ethyl phenyllactate, (-)-"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Valyl-Hydroxyproline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "1-Methoxypyrene"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "l-Isoleucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Serine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Proline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glycine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Leucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Alanine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Blautia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Dialister",
        "Alteration_microbiota": "increase",
        "Metabolite": "Tartaric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Catenibacterium",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Tartaric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Hyocholate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "12-Ketolithocholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "2-Formaminobenzoylacetate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "N-Acetyl-D-Mannosamine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Deoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Cholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Betonicine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Proline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "N-Acetylputrescine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Ursodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "l-Isoleucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Valine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Tyramine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "5-Hydroxyindole-3-acetic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Creatine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Glycerophospholipids"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Serine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Glycine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Leucine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Ruminococcus",
        "Alteration_microbiota": "increase",
        "Metabolite": "Alanine"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Roseburia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Parabacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Valyl-Hydroxyproline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Parabacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Proline"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Parabacteroides",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Hydroxy-2-methylbutanenitrile"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Coprococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Oscillospira",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Pyridoxic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Oscillospira",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Citric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Christensenellaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Collinsella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Muribaculaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-(4-Hydroxy-3-methoxyphenyl)propionic acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Turicibacter",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Tartaric acid"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Turicibacter",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Dihydrocaffeic acid"
    },
    {
        "response count": 208,
        "response time": "0.13s"
    }
]
```

##### benchmark results

| Disorder       | Microbiota                   | Alteration\_microbiota | Metabolite                                                   |
| :------------- | :--------------------------- | :--------------------- | :----------------------------------------------------------- |
| Crohn\_disease | Firmicutes                   | increase               | Propionate                                                   |
| Crohn\_disease | Firmicutes                   | increase               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Crohn\_disease | Firmicutes                   | increase               | Butyrate                                                     |
| Crohn\_disease | Bacteroidetes                | decrease               | Propionate                                                   |
| Crohn\_disease | Bacteroidetes                | decrease               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Crohn\_disease | Bacteroidetes                | decrease               | Acetate                                                      |
| Crohn\_disease | Actinobacteria               | decrease               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Crohn\_disease | Enterobacteriaceae           | increase               | Cysteine-glutathione disulfide                               |
| Crohn\_disease | Enterobacteriaceae           | increase               | Oxiglutatione                                                |
| Crohn\_disease | Enterobacteriaceae           | increase               | Phenyl sulfate                                               |
| Crohn\_disease | Ruminococcaceae              | decrease               | 7a-hydroxy-3-oxo-5b-cholanoate                               |
| Crohn\_disease | Ruminococcaceae              | decrease               | Nutriadeoxycholate vulpecholate                              |
| Crohn\_disease | Ruminococcaceae              | decrease               | Pentahomomethionine                                          |
| Crohn\_disease | Ruminococcaceae              | decrease               | Murideoxycholate                                             |
| Crohn\_disease | Ruminococcaceae              | decrease               | 21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo- |
| Crohn\_disease | Ruminococcaceae              | decrease               | 12-Ketolithocholic acid                                      |
| Crohn\_disease | Ruminococcaceae              | decrease               | N-Isovaleroylglycine                                         |
| Crohn\_disease | Ruminococcaceae              | decrease               | N-Acetyl-D-Mannosamine                                       |
| Crohn\_disease | Ruminococcaceae              | decrease               | N\(6\)-Methyllysine                                          |
| Crohn\_disease | Ruminococcaceae              | decrease               | Betonicine                                                   |
| Crohn\_disease | Ruminococcaceae              | decrease               | 4-Acetamidobutyric acid                                      |
| Crohn\_disease | Ruminococcaceae              | decrease               | Chenodeoxycholic acid                                        |
| Crohn\_disease | Ruminococcaceae              | decrease               | Creatine                                                     |
| Crohn\_disease | Ruminococcaceae              | decrease               | 3-Indolepropionic acid                                       |
| Crohn\_disease | Enterococcus                 | increase               | Dopamine                                                     |
| Crohn\_disease | Enterococcus                 | increase               | Hydroquinone                                                 |
| Crohn\_disease | Enterococcus                 | increase               | 3-Phenylpropionic acid                                       |
| Crohn\_disease | Enterococcus                 | increase               | 2-Imino-1-methylimidazolidin-4-one                           |
| Crohn\_disease | Veillonella                  | increase               | Propionate                                                   |
| Crohn\_disease | Klebsiella                   | increase               | Cyanuric acid                                                |
| Crohn\_disease | Klebsiella                   | increase               | procollagen type 1 n-terminal propeptide                     |
| Crohn\_disease | Klebsiella                   | increase               | type I collagen cross-linked c-telopeptide                   |
| Crohn\_disease | Klebsiella                   | increase               | Trimethylamine                                               |
| Crohn\_disease | Desulfovibrionaceae          | decrease               | Tryptophan                                                   |
| Crohn\_disease | Bifidobacterium              | increase               | Propionate                                                   |
| Crohn\_disease | Bifidobacterium              | increase               | Acetate                                                      |
| Crohn\_disease | Bifidobacterium              | increase               | Folic acid                                                   |
| Crohn\_disease | Bifidobacterium              | increase               | Hydroquinone                                                 |
| Crohn\_disease | Bifidobacterium              | increase               | Lactate                                                      |
| Crohn\_disease | Bifidobacterium              | increase               | Phenylacetic acid                                            |
| Crohn\_disease | Bifidobacterium              | increase               | 3-Hydroxyphenethyl alcohol                                   |
| Crohn\_disease | Bifidobacterium              | increase               | Dihydrocaffeoyl-glycerol                                     |
| Crohn\_disease | Bifidobacterium              | increase               | 2,3-Dihydroxypropyl \(E\)-3-\(3,4-dihydroxyphenyl\)prop-2-enoate |
| Crohn\_disease | Bifidobacterium              | increase               | Dihydrochlorogenic acid                                      |
| Crohn\_disease | Bifidobacterium              | increase               | Dehydroxychlorogenic acid                                    |
| Crohn\_disease | Bifidobacterium              | increase               | 3-\(3-Hydroxyphenyl\)propanoic acid                          |
| Crohn\_disease | Bifidobacterium              | increase               | Dihydrocaffeic acid                                          |
| Crohn\_disease | Bifidobacterium              | increase               | Caffeic acid                                                 |
| Crohn\_disease | Bifidobacterium              | increase               | Trimethylamine oxide                                         |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Butyrate                                                     |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Methanol, \(methyl-ONN-azoxy\)-                              |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | 4-Hydroxybenzoic acid                                        |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Benzoic acid                                                 |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | 2-Amino-1-methyl-6-phenylimidazo\[4,5-b\]pyridine            |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | 2-Imino-1-methylimidazolidin-4-one                           |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Malic acid                                                   |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Leucine                                                      |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Serine                                                       |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | 3-Indolepropionic acid                                       |
| Crohn\_disease | Faecalibacterium prausnitzii | decrease               | Bile acid                                                    |
| Crohn\_disease | Bacteroides                  | increase               | Deoxycholic acid                                             |
| Crohn\_disease | Bacteroides                  | increase               | Indole                                                       |
| Crohn\_disease | Bacteroides                  | increase               | Propionate                                                   |
| Crohn\_disease | Bacteroides                  | increase               | Succinate                                                    |
| Crohn\_disease | Bacteroides                  | increase               | Oxalacetic acid                                              |
| Crohn\_disease | Bacteroides                  | increase               | Hydroquinone                                                 |
| Crohn\_disease | Clostridium                  | decrease               | 3-Indolepropionic acid                                       |
| Crohn\_disease | Clostridium                  | decrease               | Deoxycholic acid                                             |
| Crohn\_disease | Clostridium                  | decrease               | Indole                                                       |
| Crohn\_disease | Clostridium                  | decrease               | Butyrate                                                     |
| Crohn\_disease | Clostridium                  | decrease               | Hypoxanthine                                                 |
| Crohn\_disease | Clostridium                  | decrease               | Benzoic acid                                                 |
| Crohn\_disease | Clostridium                  | decrease               | 3-Phenylpropionic acid                                       |
| Crohn\_disease | Clostridium                  | decrease               | Acetyl phosphate\(2-\)                                       |
| Crohn\_disease | Clostridium                  | decrease               | Pyruvate                                                     |
| Crohn\_disease | Clostridium                  | decrease               | 2-Imino-1-methylimidazolidin-4-one                           |
| Crohn\_disease | Eubacterium rectale          | decrease               | Butyrate                                                     |
| Crohn\_disease | Bacteroides fragilis         | decrease               | Equol                                                        |
| Crohn\_disease | Bacteroides fragilis         | decrease               | Genipin                                                      |
| Crohn\_disease | Bacteroides fragilis         | decrease               | 3-Phenylpropionic acid                                       |
| Crohn\_disease | Bacteroides fragilis         | decrease               | Glycocholic acid                                             |
| Crohn\_disease | Ruminococcus bromii          | decrease               | Butyrate                                                     |
| Crohn\_disease | Ruminococcus bromii          | decrease               | Glycerol                                                     |
| Crohn\_disease | Ruminococcus bromii          | decrease               | Propionate                                                   |
| Crohn\_disease | Ruminococcus bromii          | decrease               | 4-Pyridoxic acid                                             |
| Crohn\_disease | Ruminococcus bromii          | decrease               | Tartaric acid                                                |
| Crohn\_disease | Lactobacillus fermentum      | increase               | Ethanol                                                      |
| Crohn\_disease | Ruminococcus torques         | increase               | Lactate                                                      |
| Crohn\_disease | Ruminococcus torques         | increase               | Acetate                                                      |
| Crohn\_disease | Ruminococcus gnavus          | increase               | Tryptamine                                                   |
| Crohn\_disease | Ruminococcus gnavus          | increase               | Chenodeoxycholic acid                                        |
| Crohn\_disease | Ruminococcus gnavus          | increase               | Deoxycholic acid                                             |
| Crohn\_disease | Ruminococcus gnavus          | increase               | Ursodeoxycholic acid                                         |
| Crohn\_disease | Ruminococcus gnavus          | increase               | beta-D-Fructofuranose                                        |
| Crohn\_disease | Akkermansia muciniphila      | decrease               | Propionate                                                   |
| Crohn\_disease | Akkermansia muciniphila      | decrease               | Acetate                                                      |
| Crohn\_disease | Escherichia                  | increase               | Indole                                                       |
| Crohn\_disease | Escherichia                  | increase               | Indoxyl sulfate                                              |
| Crohn\_disease | Escherichia                  | increase               | Trimethylamine oxide                                         |
| Crohn\_disease | Escherichia                  | increase               | Glycocholic acid                                             |
| Crohn\_disease | Escherichia                  | increase               | Trimethylamine                                               |
| Crohn\_disease | Bacteroides                  | decrease               | Deoxycholic acid                                             |
| Crohn\_disease | Bacteroides                  | decrease               | Indole                                                       |
| Crohn\_disease | Bacteroides                  | decrease               | Propionate                                                   |
| Crohn\_disease | Bacteroides                  | decrease               | Succinate                                                    |
| Crohn\_disease | Bacteroides                  | decrease               | Oxalacetic acid                                              |
| Crohn\_disease | Bacteroides                  | decrease               | Hydroquinone                                                 |
| Crohn\_disease | Faecalibacterium             | decrease               | 2-Imino-1-methylimidazolidin-4-one                           |
| Crohn\_disease | Faecalibacterium             | decrease               | Serine                                                       |
| Crohn\_disease | Faecalibacterium             | decrease               | Leucine                                                      |
| Crohn\_disease | Ruminococcus                 | decrease               | Hyocholate                                                   |
| Crohn\_disease | Ruminococcus                 | decrease               | 12-Ketolithocholic acid                                      |
| Crohn\_disease | Ruminococcus                 | decrease               | 2-Formaminobenzoylacetate                                    |
| Crohn\_disease | Ruminococcus                 | decrease               | N-Acetyl-D-Mannosamine                                       |
| Crohn\_disease | Ruminococcus                 | decrease               | Deoxycholic acid                                             |
| Crohn\_disease | Ruminococcus                 | decrease               | Cholic acid                                                  |
| Crohn\_disease | Ruminococcus                 | decrease               | Betonicine                                                   |
| Crohn\_disease | Ruminococcus                 | decrease               | Proline                                                      |
| Crohn\_disease | Ruminococcus                 | decrease               | N-Acetylputrescine                                           |
| Crohn\_disease | Ruminococcus                 | decrease               | 2-Hydroxy-2-methylbutanenitrile                              |
| Crohn\_disease | Ruminococcus                 | decrease               | Ursodeoxycholic acid                                         |
| Crohn\_disease | Ruminococcus                 | decrease               | Chenodeoxycholic acid                                        |
| Crohn\_disease | Ruminococcus                 | decrease               | l-Isoleucine                                                 |
| Crohn\_disease | Ruminococcus                 | decrease               | Valine                                                       |
| Crohn\_disease | Ruminococcus                 | decrease               | Tyramine                                                     |
| Crohn\_disease | Ruminococcus                 | decrease               | 5-Hydroxyindole-3-acetic acid                                |
| Crohn\_disease | Ruminococcus                 | decrease               | Creatine                                                     |
| Crohn\_disease | Ruminococcus                 | decrease               | Glycerophospholipids                                         |
| Crohn\_disease | Ruminococcus                 | decrease               | Serine                                                       |
| Crohn\_disease | Ruminococcus                 | decrease               | Glycine                                                      |
| Crohn\_disease | Ruminococcus                 | decrease               | Leucine                                                      |
| Crohn\_disease | Ruminococcus                 | decrease               | Alanine                                                      |
| Crohn\_disease | Ruminococcus torques         | decrease               | Lactate                                                      |
| Crohn\_disease | Ruminococcus torques         | decrease               | Acetate                                                      |
| Crohn\_disease | Eubacterium                  | decrease               | Butyrate                                                     |
| Crohn\_disease | Eubacterium                  | decrease               | Hydroquinone                                                 |
| Crohn\_disease | Eubacterium                  | decrease               | 4-Hydroxybenzoic acid                                        |
| Crohn\_disease | Eubacterium                  | decrease               | 3-Hydroxybenzoic acid                                        |
| Crohn\_disease | Eubacterium                  | decrease               | 3-Indolepropionic acid                                       |
| Crohn\_disease | Bacteroides uniformis        | decrease               | Quercetin                                                    |
| Crohn\_disease | Bacteroides uniformis        | decrease               | Equol                                                        |
| Crohn\_disease | Actinobacteria               | increase               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Crohn\_disease | Escherichia coli             | decrease               | 1D-Myo-inositol 1,4,5,6-tetrakisphosphate\(8-\)              |
| Crohn\_disease | Escherichia coli             | decrease               | \[\(1S,2R,3S,4S,5R,6S\)-2,3,5-Trihydroxy-4,6-diphosphonooxycyclohexyl\] dihydrogen phosphate |
| Crohn\_disease | Escherichia coli             | decrease               | 1D-Myo-inositol 6-phosphate                                  |
| Crohn\_disease | Escherichia coli             | decrease               | \(R\)-3-\(4-Hydroxyphenyl\)lactate                           |
| Crohn\_disease | Escherichia coli             | decrease               | Ethyl phenyllactate, \(-\)-                                  |
| Crohn\_disease | Escherichia coli             | decrease               | Indole                                                       |
| Crohn\_disease | Escherichia coli             | decrease               | Quinic acid                                                  |
| Crohn\_disease | Escherichia coli             | decrease               | Caffeic acid                                                 |
| Crohn\_disease | Escherichia coli             | decrease               | Pipecolic acid                                               |
| Crohn\_disease | Escherichia coli             | increase               | 1D-Myo-inositol 1,4,5,6-tetrakisphosphate\(8-\)              |
| Crohn\_disease | Escherichia coli             | increase               | \[\(1S,2R,3S,4S,5R,6S\)-2,3,5-Trihydroxy-4,6-diphosphonooxycyclohexyl\] dihydrogen phosphate |
| Crohn\_disease | Escherichia coli             | increase               | 1D-Myo-inositol 6-phosphate                                  |
| Crohn\_disease | Escherichia coli             | increase               | \(R\)-3-\(4-Hydroxyphenyl\)lactate                           |
| Crohn\_disease | Escherichia coli             | increase               | Ethyl phenyllactate, \(-\)-                                  |
| Crohn\_disease | Escherichia coli             | increase               | Indole                                                       |
| Crohn\_disease | Escherichia coli             | increase               | Quinic acid                                                  |
| Crohn\_disease | Escherichia coli             | increase               | Caffeic acid                                                 |
| Crohn\_disease | Escherichia coli             | increase               | Pipecolic acid                                               |
| Crohn\_disease | Clostridium sp.              | increase               | \(R\)-3-\(4-Hydroxyphenyl\)lactate                           |
| Crohn\_disease | Clostridium sp.              | increase               | Ethyl phenyllactate, \(-\)-                                  |
| Crohn\_disease | Blautia                      | decrease               | Butyrate                                                     |
| Crohn\_disease | Blautia                      | decrease               | Valyl-Hydroxyproline                                         |
| Crohn\_disease | Blautia                      | decrease               | 1-Methoxypyrene                                              |
| Crohn\_disease | Blautia                      | decrease               | l-Isoleucine                                                 |
| Crohn\_disease | Blautia                      | decrease               | Serine                                                       |
| Crohn\_disease | Blautia                      | decrease               | Proline                                                      |
| Crohn\_disease | Blautia                      | decrease               | Glycine                                                      |
| Crohn\_disease | Blautia                      | decrease               | Leucine                                                      |
| Crohn\_disease | Blautia                      | decrease               | Alanine                                                      |
| Crohn\_disease | Blautia                      | decrease               | Trimethylamine oxide                                         |
| Crohn\_disease | Dialister                    | increase               | Tartaric acid                                                |
| Crohn\_disease | Catenibacterium              | decrease               | Tartaric acid                                                |
| Crohn\_disease | Ruminococcus                 | increase               | Hyocholate                                                   |
| Crohn\_disease | Ruminococcus                 | increase               | 12-Ketolithocholic acid                                      |
| Crohn\_disease | Ruminococcus                 | increase               | 2-Formaminobenzoylacetate                                    |
| Crohn\_disease | Ruminococcus                 | increase               | N-Acetyl-D-Mannosamine                                       |
| Crohn\_disease | Ruminococcus                 | increase               | Deoxycholic acid                                             |
| Crohn\_disease | Ruminococcus                 | increase               | Cholic acid                                                  |
| Crohn\_disease | Ruminococcus                 | increase               | Betonicine                                                   |
| Crohn\_disease | Ruminococcus                 | increase               | Proline                                                      |
| Crohn\_disease | Ruminococcus                 | increase               | N-Acetylputrescine                                           |
| Crohn\_disease | Ruminococcus                 | increase               | 2-Hydroxy-2-methylbutanenitrile                              |
| Crohn\_disease | Ruminococcus                 | increase               | Ursodeoxycholic acid                                         |
| Crohn\_disease | Ruminococcus                 | increase               | Chenodeoxycholic acid                                        |
| Crohn\_disease | Ruminococcus                 | increase               | l-Isoleucine                                                 |
| Crohn\_disease | Ruminococcus                 | increase               | Valine                                                       |
| Crohn\_disease | Ruminococcus                 | increase               | Tyramine                                                     |
| Crohn\_disease | Ruminococcus                 | increase               | 5-Hydroxyindole-3-acetic acid                                |
| Crohn\_disease | Ruminococcus                 | increase               | Creatine                                                     |
| Crohn\_disease | Ruminococcus                 | increase               | Glycerophospholipids                                         |
| Crohn\_disease | Ruminococcus                 | increase               | Serine                                                       |
| Crohn\_disease | Ruminococcus                 | increase               | Glycine                                                      |
| Crohn\_disease | Ruminococcus                 | increase               | Leucine                                                      |
| Crohn\_disease | Ruminococcus                 | increase               | Alanine                                                      |
| Crohn\_disease | Roseburia                    | decrease               | 3-Phenylpropionic acid                                       |
| Crohn\_disease | Parabacteroides              | decrease               | Valyl-Hydroxyproline                                         |
| Crohn\_disease | Parabacteroides              | decrease               | Proline                                                      |
| Crohn\_disease | Parabacteroides              | decrease               | 2-Hydroxy-2-methylbutanenitrile                              |
| Crohn\_disease | Coprococcus                  | decrease               | 3-Indolepropionic acid                                       |
| Crohn\_disease | Oscillospira                 | decrease               | 4-Pyridoxic acid                                             |
| Crohn\_disease | Oscillospira                 | decrease               | Citric acid                                                  |
| Crohn\_disease | Christensenellaceae          | decrease               | Butyrate                                                     |
| Crohn\_disease | Collinsella                  | increase               | Trimethylamine oxide                                         |
| Crohn\_disease | Muribaculaceae               | decrease               | 3-\(4-Hydroxy-3-methoxyphenyl\)propionic acid                |
| Crohn\_disease | Turicibacter                 | decrease               | Tartaric acid                                                |
| Crohn\_disease | Turicibacter                 | decrease               | Dihydrocaffeic acid                                          |





#### Q8 What changes in the abundance of gut bacteria will be affected by taking Metformin (a drug for treating diabetes), and what metabolites will be produced?

##### federated query results

```json
[
    {
        "Drug": "Metformin",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Cysteine-glutathione disulfide"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Oxiglutatione"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Phenyl sulfate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "7a-hydroxy-3-oxo-5b-cholanoate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Nutriadeoxycholate vulpecholate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Pentahomomethionine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Murideoxycholate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo-"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "12-Ketolithocholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Isovaleroylglycine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Acetyl-D-Mannosamine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N(6)-Methyllysine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Betonicine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Acetamidobutyric acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Creatine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Ruminococcaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Clostridia",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Estradiol"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Christensenellaceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Butyrate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Acetate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Folic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Hydroquinone"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Lactate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Phenylacetic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-Hydroxyphenethyl alcohol"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrocaffeoyl-glycerol"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "2,3-Dihydroxypropyl (E)-3-(3,4-dihydroxyphenyl)prop-2-enoate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrochlorogenic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dehydroxychlorogenic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-(3-Hydroxyphenyl)propanoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Dihydrocaffeic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Caffeic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Indole-3-acetic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Benzoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "decrease",
        "Metabolite": "l-Isoleucine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Myristic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Indole-3-acetic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Benzoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "increase",
        "Metabolite": "l-Isoleucine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotella",
        "Alteration_microbiota": "increase",
        "Metabolite": "Myristic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Dopamine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Hydroquinone"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Enterococcus",
        "Alteration_microbiota": "decrease",
        "Metabolite": "2-Imino-1-methylimidazolidin-4-one"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Oscillospira",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Pyridoxic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Oscillospira",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Citric acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Megasphaera",
        "Alteration_microbiota": "increase",
        "Metabolite": "procollagen type 1 n-terminal propeptide"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Megasphaera",
        "Alteration_microbiota": "increase",
        "Metabolite": "type I collagen cross-linked c-telopeptide"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia muciniphila",
        "Alteration_microbiota": "increase",
        "Metabolite": "Propionate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia muciniphila",
        "Alteration_microbiota": "increase",
        "Metabolite": "Acetate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia",
        "Alteration_microbiota": "increase",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Tryptophan"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Glycocholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Akkermansia",
        "Alteration_microbiota": "increase",
        "Metabolite": "Creatine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Prevotellaceae",
        "Alteration_microbiota": "increase",
        "Metabolite": "Succinate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "7a-hydroxy-3-oxo-5b-cholanoate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Nutriadeoxycholate vulpecholate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "7-Hydroxy-3-oxocholanoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Pentahomomethionine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Murideoxycholate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo-"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "12-Ketolithocholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Isovaleroylglycine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N-Acetyl-D-Mannosamine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "N(6)-Methyllysine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "4-Acetamidobutyric acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Chenodeoxycholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Creatine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Benzoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Phenylpropionic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Retinol"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "7-Dehydrocholesterol"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Desoxycortone"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Eicosapentaenoic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Cholic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Glutamic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Phenylalanine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Trimethylamine oxide"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "3-Indolepropionic acid"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Phenylacetylglutamine"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "p-Cresol sulfate"
    },
    {
        "Drug": "Metformin",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Metabolite": "Indoxyl sulfate"
    },
    {
        "response count": 84,
        "response time": "0.147s"
    }
]
```

##### benchmark results

| Drug      | Microbiota              | Alteration\_microbiota | Metabolite                                                   |
| :-------- | :---------------------- | :--------------------- | :----------------------------------------------------------- |
| Metformin | Enterobacteriaceae      | increase               | Cysteine-glutathione disulfide                               |
| Metformin | Enterobacteriaceae      | increase               | Oxiglutatione                                                |
| Metformin | Enterobacteriaceae      | increase               | Phenyl sulfate                                               |
| Metformin | Ruminococcaceae         | decrease               | 7a-hydroxy-3-oxo-5b-cholanoate                               |
| Metformin | Ruminococcaceae         | decrease               | Nutriadeoxycholate vulpecholate                              |
| Metformin | Ruminococcaceae         | decrease               | Pentahomomethionine                                          |
| Metformin | Ruminococcaceae         | decrease               | Murideoxycholate                                             |
| Metformin | Ruminococcaceae         | decrease               | 21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo- |
| Metformin | Ruminococcaceae         | decrease               | 12-Ketolithocholic acid                                      |
| Metformin | Ruminococcaceae         | decrease               | N-Isovaleroylglycine                                         |
| Metformin | Ruminococcaceae         | decrease               | N-Acetyl-D-Mannosamine                                       |
| Metformin | Ruminococcaceae         | decrease               | N\(6\)-Methyllysine                                          |
| Metformin | Ruminococcaceae         | decrease               | Betonicine                                                   |
| Metformin | Ruminococcaceae         | decrease               | 4-Acetamidobutyric acid                                      |
| Metformin | Ruminococcaceae         | decrease               | Chenodeoxycholic acid                                        |
| Metformin | Ruminococcaceae         | decrease               | Creatine                                                     |
| Metformin | Ruminococcaceae         | decrease               | 3-Indolepropionic acid                                       |
| Metformin | Clostridia              | decrease               | Estradiol                                                    |
| Metformin | Christensenellaceae     | decrease               | Butyrate                                                     |
| Metformin | Bifidobacterium         | increase               | Propionate                                                   |
| Metformin | Bifidobacterium         | increase               | Acetate                                                      |
| Metformin | Bifidobacterium         | increase               | Folic acid                                                   |
| Metformin | Bifidobacterium         | increase               | Hydroquinone                                                 |
| Metformin | Bifidobacterium         | increase               | Lactate                                                      |
| Metformin | Bifidobacterium         | increase               | Phenylacetic acid                                            |
| Metformin | Bifidobacterium         | increase               | 3-Hydroxyphenethyl alcohol                                   |
| Metformin | Bifidobacterium         | increase               | Dihydrocaffeoyl-glycerol                                     |
| Metformin | Bifidobacterium         | increase               | 2,3-Dihydroxypropyl \(E\)-3-\(3,4-dihydroxyphenyl\)prop-2-enoate |
| Metformin | Bifidobacterium         | increase               | Dihydrochlorogenic acid                                      |
| Metformin | Bifidobacterium         | increase               | Dehydroxychlorogenic acid                                    |
| Metformin | Bifidobacterium         | increase               | 3-\(3-Hydroxyphenyl\)propanoic acid                          |
| Metformin | Bifidobacterium         | increase               | Dihydrocaffeic acid                                          |
| Metformin | Bifidobacterium         | increase               | Caffeic acid                                                 |
| Metformin | Bifidobacterium         | increase               | Trimethylamine oxide                                         |
| Metformin | Prevotella              | decrease               | Indole-3-acetic acid                                         |
| Metformin | Prevotella              | decrease               | Benzoic acid                                                 |
| Metformin | Prevotella              | decrease               | l-Isoleucine                                                 |
| Metformin | Prevotella              | decrease               | Myristic acid                                                |
| Metformin | Prevotella              | increase               | Indole-3-acetic acid                                         |
| Metformin | Prevotella              | increase               | Benzoic acid                                                 |
| Metformin | Prevotella              | increase               | l-Isoleucine                                                 |
| Metformin | Prevotella              | increase               | Myristic acid                                                |
| Metformin | Enterococcus            | decrease               | Dopamine                                                     |
| Metformin | Enterococcus            | decrease               | Hydroquinone                                                 |
| Metformin | Enterococcus            | decrease               | 3-Phenylpropionic acid                                       |
| Metformin | Enterococcus            | decrease               | 2-Imino-1-methylimidazolidin-4-one                           |
| Metformin | Oscillospira            | decrease               | 4-Pyridoxic acid                                             |
| Metformin | Oscillospira            | decrease               | Citric acid                                                  |
| Metformin | Megasphaera             | increase               | procollagen type 1 n-terminal propeptide                     |
| Metformin | Megasphaera             | increase               | type I collagen cross-linked c-telopeptide                   |
| Metformin | Akkermansia muciniphila | increase               | Propionate                                                   |
| Metformin | Akkermansia muciniphila | increase               | Acetate                                                      |
| Metformin | Akkermansia             | increase               | 3-Indolepropionic acid                                       |
| Metformin | Akkermansia             | increase               | Tryptophan                                                   |
| Metformin | Akkermansia             | increase               | Glycocholic acid                                             |
| Metformin | Akkermansia             | increase               | Creatine                                                     |
| Metformin | Prevotellaceae          | increase               | Succinate                                                    |
| Metformin | Lachnospiraceae         | decrease               | 7a-hydroxy-3-oxo-5b-cholanoate                               |
| Metformin | Lachnospiraceae         | decrease               | Nutriadeoxycholate vulpecholate                              |
| Metformin | Lachnospiraceae         | decrease               | 7-Hydroxy-3-oxocholanoic acid                                |
| Metformin | Lachnospiraceae         | decrease               | Pentahomomethionine                                          |
| Metformin | Lachnospiraceae         | decrease               | Murideoxycholate                                             |
| Metformin | Lachnospiraceae         | decrease               | 21H-Biline-8,12-dipropanoic acid, 3,18-diethyl-1,4,5,15,16,19,22,24-octahydro-2,7,13,17-tetramethyl-1,19-dioxo- |
| Metformin | Lachnospiraceae         | decrease               | 12-Ketolithocholic acid                                      |
| Metformin | Lachnospiraceae         | decrease               | N-Isovaleroylglycine                                         |
| Metformin | Lachnospiraceae         | decrease               | N-Acetyl-D-Mannosamine                                       |
| Metformin | Lachnospiraceae         | decrease               | N\(6\)-Methyllysine                                          |
| Metformin | Lachnospiraceae         | decrease               | 4-Acetamidobutyric acid                                      |
| Metformin | Lachnospiraceae         | decrease               | Chenodeoxycholic acid                                        |
| Metformin | Lachnospiraceae         | decrease               | Creatine                                                     |
| Metformin | Lachnospiraceae         | decrease               | Benzoic acid                                                 |
| Metformin | Lachnospiraceae         | decrease               | 3-Phenylpropionic acid                                       |
| Metformin | Lachnospiraceae         | decrease               | Retinol                                                      |
| Metformin | Lachnospiraceae         | decrease               | 7-Dehydrocholesterol                                         |
| Metformin | Lachnospiraceae         | decrease               | Desoxycortone                                                |
| Metformin | Lachnospiraceae         | decrease               | Eicosapentaenoic acid                                        |
| Metformin | Lachnospiraceae         | decrease               | Cholic acid                                                  |
| Metformin | Lachnospiraceae         | decrease               | Glutamic acid                                                |
| Metformin | Lachnospiraceae         | decrease               | Phenylalanine                                                |
| Metformin | Lachnospiraceae         | decrease               | Trimethylamine oxide                                         |
| Metformin | Lachnospiraceae         | decrease               | 3-Indolepropionic acid                                       |
| Metformin | Lachnospiraceae         | decrease               | Phenylacetylglutamine                                        |
| Metformin | Lachnospiraceae         | decrease               | p-Cresol sulfate                                             |
| Metformin | Lachnospiraceae         | decrease               | Indoxyl sulfate                                              |



#### Q9 Which human gut bacteria are altered in abundance by the disease colitis, and which genes are affected by its expression?

##### federated query results

```json
[
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Gene": "Ido1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Gene": "CASP3",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Gene": "BAX",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "increase",
        "Gene": "BCL2",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "increase",
        "Gene": "Arg1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "increase",
        "Gene": "Tjp1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "increase",
        "Gene": "IL22",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "increase",
        "Gene": "MAPK14",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Col1a1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Fn1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Tgfb1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Ccl2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Tnf",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "decrease",
        "Gene": "Slco4c1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Gene": "Il6",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Gene": "Il10",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Gene": "IL10",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Gene": "FOXP3",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroides fragilis",
        "Alteration_microbiota": "decrease",
        "Gene": "FFAR2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Fas",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Cpt1b",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Sirpa",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Cyp7a1",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Fgfr4",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Fgf15",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Nr1h4",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Col1a1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Fn1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Tgfb1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Ccl2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Tnf",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Enterobacteriaceae",
        "Alteration_microbiota": "increase",
        "Gene": "Slco4c1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Gcg",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Il12b",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Il6",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Cd40",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Cd86",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Pdcd1lg2",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Nfkb1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Ffar2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "Ffar3",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "CCL3",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "TNF",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "CXCR2",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "C5AR1",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "GLP1R",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bacteroidetes",
        "Alteration_microbiota": "decrease",
        "Gene": "NR1H4",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "decrease",
        "Gene": "Arg1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "decrease",
        "Gene": "Tjp1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "decrease",
        "Gene": "IL22",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lactobacillus",
        "Alteration_microbiota": "decrease",
        "Gene": "MAPK14",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "decrease",
        "Gene": "Ido1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "decrease",
        "Gene": "CASP3",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "decrease",
        "Gene": "BAX",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Bifidobacterium",
        "Alteration_microbiota": "decrease",
        "Gene": "BCL2",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Lachnospiraceae",
        "Alteration_microbiota": "decrease",
        "Gene": "EGFR",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Parabacteroides distasonis",
        "Alteration_microbiota": "increase",
        "Gene": "Foxp3",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Escherichia",
        "Alteration_microbiota": "increase",
        "Gene": "Gcg",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Hmgcr",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Srebf2",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Fas",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Srebf1",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Tlr2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Chrm2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Nos2",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Il1b",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Tnf",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Il6",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Gcg",
        "Alteration_gene": "decrease"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Prkaa1",
        "Alteration_gene": "increase"
    },
    {
        "Disorder": "colitis",
        "Microbiota": "Clostridium",
        "Alteration_microbiota": "increase",
        "Gene": "Prkaa2",
        "Alteration_gene": "increase"
    },
    {
        "response count": 71,
        "response time": "0.236s"
    }
]
```

##### benchmark results

| Disorder | Microbiota                 | Alteration\_microbiota | Gene     | Alteration\_gene |
| :------- | :------------------------- | :--------------------- | :------- | :--------------- |
| colitis  | Bifidobacterium            | increase               | Ido1     | increase         |
| colitis  | Bifidobacterium            | increase               | CASP3    | increase         |
| colitis  | Bifidobacterium            | increase               | BAX      | increase         |
| colitis  | Bifidobacterium            | increase               | BCL2     | decrease         |
| colitis  | Lactobacillus              | increase               | Arg1     | increase         |
| colitis  | Lactobacillus              | increase               | Tjp1     | increase         |
| colitis  | Lactobacillus              | increase               | IL22     | increase         |
| colitis  | Lactobacillus              | increase               | MAPK14   | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Col1a1   | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Fn1      | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Tgfb1    | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Ccl2     | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Tnf      | increase         |
| colitis  | Enterobacteriaceae         | decrease               | Slco4c1  | increase         |
| colitis  | Bacteroides fragilis       | decrease               | Il6      | increase         |
| colitis  | Bacteroides fragilis       | decrease               | Il10     | increase         |
| colitis  | Bacteroides fragilis       | decrease               | IL10     | increase         |
| colitis  | Bacteroides fragilis       | decrease               | FOXP3    | increase         |
| colitis  | Bacteroides fragilis       | decrease               | FFAR2    | increase         |
| colitis  | Bacteroidaceae             | increase               | Fas      | increase         |
| colitis  | Bacteroidaceae             | increase               | Cpt1b    | decrease         |
| colitis  | Bacteroidaceae             | increase               | Sirpa    | decrease         |
| colitis  | Bacteroidaceae             | increase               | Cyp7a1   | decrease         |
| colitis  | Bacteroidaceae             | increase               | Fgfr4    | increase         |
| colitis  | Bacteroidaceae             | increase               | Fgf15    | increase         |
| colitis  | Bacteroidaceae             | increase               | Nr1h4    | increase         |
| colitis  | Enterobacteriaceae         | increase               | Col1a1   | increase         |
| colitis  | Enterobacteriaceae         | increase               | Fn1      | increase         |
| colitis  | Enterobacteriaceae         | increase               | Tgfb1    | increase         |
| colitis  | Enterobacteriaceae         | increase               | Ccl2     | increase         |
| colitis  | Enterobacteriaceae         | increase               | Tnf      | increase         |
| colitis  | Enterobacteriaceae         | increase               | Slco4c1  | increase         |
| colitis  | Bacteroidetes              | decrease               | Gcg      | increase         |
| colitis  | Bacteroidetes              | decrease               | Il12b    | decrease         |
| colitis  | Bacteroidetes              | decrease               | Il6      | decrease         |
| colitis  | Bacteroidetes              | decrease               | Cd40     | decrease         |
| colitis  | Bacteroidetes              | decrease               | Cd86     | decrease         |
| colitis  | Bacteroidetes              | decrease               | Pdcd1lg2 | decrease         |
| colitis  | Bacteroidetes              | decrease               | Nfkb1    | increase         |
| colitis  | Bacteroidetes              | decrease               | Ffar2    | increase         |
| colitis  | Bacteroidetes              | decrease               | Ffar3    | increase         |
| colitis  | Bacteroidetes              | decrease               | CCL3     | decrease         |
| colitis  | Bacteroidetes              | decrease               | TNF      | decrease         |
| colitis  | Bacteroidetes              | decrease               | CXCR2    | decrease         |
| colitis  | Bacteroidetes              | decrease               | C5AR1    | decrease         |
| colitis  | Bacteroidetes              | decrease               | GLP1R    | increase         |
| colitis  | Bacteroidetes              | decrease               | NR1H4    | decrease         |
| colitis  | Lactobacillus              | decrease               | Arg1     | increase         |
| colitis  | Lactobacillus              | decrease               | Tjp1     | increase         |
| colitis  | Lactobacillus              | decrease               | IL22     | increase         |
| colitis  | Lactobacillus              | decrease               | MAPK14   | increase         |
| colitis  | Bifidobacterium            | decrease               | Ido1     | increase         |
| colitis  | Bifidobacterium            | decrease               | CASP3    | increase         |
| colitis  | Bifidobacterium            | decrease               | BAX      | increase         |
| colitis  | Bifidobacterium            | decrease               | BCL2     | decrease         |
| colitis  | Lachnospiraceae            | decrease               | EGFR     | decrease         |
| colitis  | Parabacteroides distasonis | increase               | Foxp3    | increase         |
| colitis  | Escherichia                | increase               | Gcg      | decrease         |
| colitis  | Clostridium                | increase               | Hmgcr    | decrease         |
| colitis  | Clostridium                | increase               | Srebf2   | decrease         |
| colitis  | Clostridium                | increase               | Fas      | decrease         |
| colitis  | Clostridium                | increase               | Srebf1   | decrease         |
| colitis  | Clostridium                | increase               | Tlr2     | increase         |
| colitis  | Clostridium                | increase               | Chrm2    | increase         |
| colitis  | Clostridium                | increase               | Nos2     | increase         |
| colitis  | Clostridium                | increase               | Il1b     | increase         |
| colitis  | Clostridium                | increase               | Tnf      | increase         |
| colitis  | Clostridium                | increase               | Il6      | increase         |
| colitis  | Clostridium                | increase               | Gcg      | decrease         |
| colitis  | Clostridium                | increase               | Prkaa1   | increase         |
| colitis  | Clostridium                | increase               | Prkaa2   | increase         |



#### Q10 What causes a decrease in Bacteroidetes? Thereby affecting the expression of which genes?

##### federated query results

```
[
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "Crohn_disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "gastritis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "nonalcoholic fatty liver disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "Parkinson's disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "atopic dermatitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "perinatal necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "Wilson disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Disorder": "Helicobacter_pylori_infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "acne",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "colorectal_cancer",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "bipolar disorder",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "obesity",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "Clostridium difficile infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "celiac disease",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "constipation",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "Norovirus infection",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "pre-eclampsia",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Disorder": "necrotizing enterocolitis",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Food": "gluten-free diet",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "NR1H4"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "GLP1R"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "C5AR1"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CXCR2"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "TNF"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "CCL3"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar3"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Ffar2"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Nfkb1"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Pdcd1lg2"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd86"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Cd40"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il6"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Il12b"
    },
    {
        "Drug": "Enrofloxacin",
        "Microbiota": "Bacteroidetes",
        "Alteration": "decrease",
        "Gene": "Gcg"
    },
    {
        "response count": 315,
        "response time": "0.941s"
    }
]
```



##### benchmark results

| Disorder                                                     | Microbiota    | Alteration | Gene     |
| :----------------------------------------------------------- | :------------ | :--------- | :------- |
| Crohn\_disease                                               | Bacteroidetes | decrease   | GLP1R    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | NR1H4    |
| gastritis                                                    | Bacteroidetes | decrease   | GLP1R    |
| gastritis                                                    | Bacteroidetes | decrease   | NR1H4    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | GLP1R    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | NR1H4    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | GLP1R    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | NR1H4    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | GLP1R    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | NR1H4    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | GLP1R    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | NR1H4    |
| Wilson disease                                               | Bacteroidetes | decrease   | C5AR1    |
| Wilson disease                                               | Bacteroidetes | decrease   | GLP1R    |
| Wilson disease                                               | Bacteroidetes | decrease   | NR1H4    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | C5AR1    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | GLP1R    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | NR1H4    |
| acne                                                         | Bacteroidetes | decrease   | C5AR1    |
| acne                                                         | Bacteroidetes | decrease   | GLP1R    |
| acne                                                         | Bacteroidetes | decrease   | NR1H4    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | C5AR1    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | GLP1R    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | NR1H4    |
| bipolar disorder                                             | Bacteroidetes | decrease   | C5AR1    |
| bipolar disorder                                             | Bacteroidetes | decrease   | GLP1R    |
| bipolar disorder                                             | Bacteroidetes | decrease   | NR1H4    |
| obesity                                                      | Bacteroidetes | decrease   | C5AR1    |
| obesity                                                      | Bacteroidetes | decrease   | GLP1R    |
| obesity                                                      | Bacteroidetes | decrease   | NR1H4    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | C5AR1    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | GLP1R    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | NR1H4    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | C5AR1    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | GLP1R    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | NR1H4    |
| celiac disease                                               | Bacteroidetes | decrease   | C5AR1    |
| celiac disease                                               | Bacteroidetes | decrease   | GLP1R    |
| celiac disease                                               | Bacteroidetes | decrease   | NR1H4    |
| constipation                                                 | Bacteroidetes | decrease   | C5AR1    |
| constipation                                                 | Bacteroidetes | decrease   | GLP1R    |
| constipation                                                 | Bacteroidetes | decrease   | NR1H4    |
| Norovirus infection                                          | Bacteroidetes | decrease   | C5AR1    |
| Norovirus infection                                          | Bacteroidetes | decrease   | GLP1R    |
| Norovirus infection                                          | Bacteroidetes | decrease   | NR1H4    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | C5AR1    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | GLP1R    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | NR1H4    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | C5AR1    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | GLP1R    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | NR1H4    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | TNF      |
| Crohn\_disease                                               | Bacteroidetes | decrease   | CXCR2    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | C5AR1    |
| gastritis                                                    | Bacteroidetes | decrease   | TNF      |
| gastritis                                                    | Bacteroidetes | decrease   | CXCR2    |
| gastritis                                                    | Bacteroidetes | decrease   | C5AR1    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | TNF      |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | CXCR2    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | C5AR1    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | TNF      |
| Parkinson's disease                                          | Bacteroidetes | decrease   | CXCR2    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | C5AR1    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | TNF      |
| atopic dermatitis                                            | Bacteroidetes | decrease   | CXCR2    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | C5AR1    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | TNF      |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | CXCR2    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | C5AR1    |
| Wilson disease                                               | Bacteroidetes | decrease   | TNF      |
| Wilson disease                                               | Bacteroidetes | decrease   | CXCR2    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | TNF      |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | CXCR2    |
| acne                                                         | Bacteroidetes | decrease   | TNF      |
| acne                                                         | Bacteroidetes | decrease   | CXCR2    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | TNF      |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | CXCR2    |
| bipolar disorder                                             | Bacteroidetes | decrease   | TNF      |
| bipolar disorder                                             | Bacteroidetes | decrease   | CXCR2    |
| obesity                                                      | Bacteroidetes | decrease   | TNF      |
| obesity                                                      | Bacteroidetes | decrease   | CXCR2    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | CCL3     |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | TNF      |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | CXCR2    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | CCL3     |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | TNF      |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | CXCR2    |
| celiac disease                                               | Bacteroidetes | decrease   | CCL3     |
| celiac disease                                               | Bacteroidetes | decrease   | TNF      |
| celiac disease                                               | Bacteroidetes | decrease   | CXCR2    |
| constipation                                                 | Bacteroidetes | decrease   | CCL3     |
| constipation                                                 | Bacteroidetes | decrease   | TNF      |
| constipation                                                 | Bacteroidetes | decrease   | CXCR2    |
| Norovirus infection                                          | Bacteroidetes | decrease   | CCL3     |
| Norovirus infection                                          | Bacteroidetes | decrease   | TNF      |
| Norovirus infection                                          | Bacteroidetes | decrease   | CXCR2    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | CCL3     |
| pre-eclampsia                                                | Bacteroidetes | decrease   | TNF      |
| pre-eclampsia                                                | Bacteroidetes | decrease   | CXCR2    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | CCL3     |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | TNF      |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | CXCR2    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Ffar2    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Ffar3    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | CCL3     |
| gastritis                                                    | Bacteroidetes | decrease   | Ffar2    |
| gastritis                                                    | Bacteroidetes | decrease   | Ffar3    |
| gastritis                                                    | Bacteroidetes | decrease   | CCL3     |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Ffar2    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Ffar3    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | CCL3     |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Ffar2    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Ffar3    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | CCL3     |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Ffar2    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Ffar3    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | CCL3     |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Ffar2    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Ffar3    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | CCL3     |
| Wilson disease                                               | Bacteroidetes | decrease   | Ffar2    |
| Wilson disease                                               | Bacteroidetes | decrease   | Ffar3    |
| Wilson disease                                               | Bacteroidetes | decrease   | CCL3     |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Ffar2    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Ffar3    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | CCL3     |
| acne                                                         | Bacteroidetes | decrease   | Ffar2    |
| acne                                                         | Bacteroidetes | decrease   | Ffar3    |
| acne                                                         | Bacteroidetes | decrease   | CCL3     |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Ffar2    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Ffar3    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | CCL3     |
| bipolar disorder                                             | Bacteroidetes | decrease   | Ffar2    |
| bipolar disorder                                             | Bacteroidetes | decrease   | Ffar3    |
| bipolar disorder                                             | Bacteroidetes | decrease   | CCL3     |
| obesity                                                      | Bacteroidetes | decrease   | Ffar2    |
| obesity                                                      | Bacteroidetes | decrease   | Ffar3    |
| obesity                                                      | Bacteroidetes | decrease   | CCL3     |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Ffar2    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Ffar3    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Ffar2    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Ffar3    |
| celiac disease                                               | Bacteroidetes | decrease   | Ffar2    |
| celiac disease                                               | Bacteroidetes | decrease   | Ffar3    |
| constipation                                                 | Bacteroidetes | decrease   | Ffar2    |
| constipation                                                 | Bacteroidetes | decrease   | Ffar3    |
| Norovirus infection                                          | Bacteroidetes | decrease   | Ffar2    |
| Norovirus infection                                          | Bacteroidetes | decrease   | Ffar3    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Nfkb1    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Ffar2    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Ffar3    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Nfkb1    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Ffar2    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Ffar3    |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Pdcd1lg2 |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Nfkb1    |
| gastritis                                                    | Bacteroidetes | decrease   | Pdcd1lg2 |
| gastritis                                                    | Bacteroidetes | decrease   | Nfkb1    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Cd86     |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Pdcd1lg2 |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Nfkb1    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Cd86     |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Pdcd1lg2 |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Nfkb1    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Cd86     |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Pdcd1lg2 |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Nfkb1    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Cd86     |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Pdcd1lg2 |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Nfkb1    |
| Wilson disease                                               | Bacteroidetes | decrease   | Cd86     |
| Wilson disease                                               | Bacteroidetes | decrease   | Pdcd1lg2 |
| Wilson disease                                               | Bacteroidetes | decrease   | Nfkb1    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Cd86     |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Pdcd1lg2 |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Nfkb1    |
| acne                                                         | Bacteroidetes | decrease   | Cd86     |
| acne                                                         | Bacteroidetes | decrease   | Pdcd1lg2 |
| acne                                                         | Bacteroidetes | decrease   | Nfkb1    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Cd86     |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Pdcd1lg2 |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Nfkb1    |
| bipolar disorder                                             | Bacteroidetes | decrease   | Cd86     |
| bipolar disorder                                             | Bacteroidetes | decrease   | Pdcd1lg2 |
| bipolar disorder                                             | Bacteroidetes | decrease   | Nfkb1    |
| obesity                                                      | Bacteroidetes | decrease   | Cd86     |
| obesity                                                      | Bacteroidetes | decrease   | Pdcd1lg2 |
| obesity                                                      | Bacteroidetes | decrease   | Nfkb1    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Cd86     |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Pdcd1lg2 |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Nfkb1    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Cd86     |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Pdcd1lg2 |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Nfkb1    |
| celiac disease                                               | Bacteroidetes | decrease   | Cd86     |
| celiac disease                                               | Bacteroidetes | decrease   | Pdcd1lg2 |
| celiac disease                                               | Bacteroidetes | decrease   | Nfkb1    |
| constipation                                                 | Bacteroidetes | decrease   | Cd86     |
| constipation                                                 | Bacteroidetes | decrease   | Pdcd1lg2 |
| constipation                                                 | Bacteroidetes | decrease   | Nfkb1    |
| Norovirus infection                                          | Bacteroidetes | decrease   | Cd86     |
| Norovirus infection                                          | Bacteroidetes | decrease   | Pdcd1lg2 |
| Norovirus infection                                          | Bacteroidetes | decrease   | Nfkb1    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Cd86     |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Pdcd1lg2 |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Cd86     |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Pdcd1lg2 |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Il6      |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Cd40     |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Cd86     |
| gastritis                                                    | Bacteroidetes | decrease   | Il6      |
| gastritis                                                    | Bacteroidetes | decrease   | Cd40     |
| gastritis                                                    | Bacteroidetes | decrease   | Cd86     |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Il6      |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Cd40     |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Il6      |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Cd40     |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Il6      |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Cd40     |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Il6      |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Cd40     |
| Wilson disease                                               | Bacteroidetes | decrease   | Il6      |
| Wilson disease                                               | Bacteroidetes | decrease   | Cd40     |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Il12b    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Il6      |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Cd40     |
| acne                                                         | Bacteroidetes | decrease   | Il12b    |
| acne                                                         | Bacteroidetes | decrease   | Il6      |
| acne                                                         | Bacteroidetes | decrease   | Cd40     |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Il12b    |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Il6      |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Cd40     |
| bipolar disorder                                             | Bacteroidetes | decrease   | Il12b    |
| bipolar disorder                                             | Bacteroidetes | decrease   | Il6      |
| bipolar disorder                                             | Bacteroidetes | decrease   | Cd40     |
| obesity                                                      | Bacteroidetes | decrease   | Il12b    |
| obesity                                                      | Bacteroidetes | decrease   | Il6      |
| obesity                                                      | Bacteroidetes | decrease   | Cd40     |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Il12b    |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Il6      |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Cd40     |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Il12b    |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Il6      |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Cd40     |
| celiac disease                                               | Bacteroidetes | decrease   | Il12b    |
| celiac disease                                               | Bacteroidetes | decrease   | Il6      |
| celiac disease                                               | Bacteroidetes | decrease   | Cd40     |
| constipation                                                 | Bacteroidetes | decrease   | Il12b    |
| constipation                                                 | Bacteroidetes | decrease   | Il6      |
| constipation                                                 | Bacteroidetes | decrease   | Cd40     |
| Norovirus infection                                          | Bacteroidetes | decrease   | Il12b    |
| Norovirus infection                                          | Bacteroidetes | decrease   | Il6      |
| Norovirus infection                                          | Bacteroidetes | decrease   | Cd40     |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Il12b    |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Il6      |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Cd40     |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Il12b    |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Il6      |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Cd40     |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Gcg      |
| Crohn\_disease                                               | Bacteroidetes | decrease   | Il12b    |
| gastritis                                                    | Bacteroidetes | decrease   | Gcg      |
| gastritis                                                    | Bacteroidetes | decrease   | Il12b    |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Gcg      |
| nonalcoholic fatty liver disease                             | Bacteroidetes | decrease   | Il12b    |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Gcg      |
| Parkinson's disease                                          | Bacteroidetes | decrease   | Il12b    |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Gcg      |
| atopic dermatitis                                            | Bacteroidetes | decrease   | Il12b    |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Gcg      |
| perinatal necrotizing enterocolitis                          | Bacteroidetes | decrease   | Il12b    |
| Wilson disease                                               | Bacteroidetes | decrease   | Gcg      |
| Wilson disease                                               | Bacteroidetes | decrease   | Il12b    |
| Helicobacter\_pylori\_infection                              | Bacteroidetes | decrease   | Gcg      |
| acne                                                         | Bacteroidetes | decrease   | Gcg      |
| colorectal\_cancer                                           | Bacteroidetes | decrease   | Gcg      |
| bipolar disorder                                             | Bacteroidetes | decrease   | Gcg      |
| obesity                                                      | Bacteroidetes | decrease   | Gcg      |
| diarrhea and fatigue in patients undergoing pelvic cancer radiotherapy | Bacteroidetes | decrease   | Gcg      |
| Clostridium difficile infection                              | Bacteroidetes | decrease   | Gcg      |
| celiac disease                                               | Bacteroidetes | decrease   | Gcg      |
| constipation                                                 | Bacteroidetes | decrease   | Gcg      |
| Norovirus infection                                          | Bacteroidetes | decrease   | Gcg      |
| pre-eclampsia                                                | Bacteroidetes | decrease   | Gcg      |
| necrotizing enterocolitis                                    | Bacteroidetes | decrease   | Gcg      |

| Food             | Microbiota    | Alteration | Gene     |
| :--------------- | :------------ | :--------- | :------- |
| gluten-free diet | Bacteroidetes | decrease   | NR1H4    |
| gluten-free diet | Bacteroidetes | decrease   | GLP1R    |
| gluten-free diet | Bacteroidetes | decrease   | C5AR1    |
| gluten-free diet | Bacteroidetes | decrease   | CXCR2    |
| gluten-free diet | Bacteroidetes | decrease   | TNF      |
| gluten-free diet | Bacteroidetes | decrease   | CCL3     |
| gluten-free diet | Bacteroidetes | decrease   | Ffar3    |
| gluten-free diet | Bacteroidetes | decrease   | Ffar2    |
| gluten-free diet | Bacteroidetes | decrease   | Nfkb1    |
| gluten-free diet | Bacteroidetes | decrease   | Pdcd1lg2 |
| gluten-free diet | Bacteroidetes | decrease   | Cd86     |
| gluten-free diet | Bacteroidetes | decrease   | Cd40     |
| gluten-free diet | Bacteroidetes | decrease   | Il6      |
| gluten-free diet | Bacteroidetes | decrease   | Il12b    |
| gluten-free diet | Bacteroidetes | decrease   | Gcg      |

| Drug         | Microbiota    | Alteration | Gene     |
| :----------- | :------------ | :--------- | :------- |
| Enrofloxacin | Bacteroidetes | decrease   | NR1H4    |
| Enrofloxacin | Bacteroidetes | decrease   | GLP1R    |
| Enrofloxacin | Bacteroidetes | decrease   | C5AR1    |
| Enrofloxacin | Bacteroidetes | decrease   | CXCR2    |
| Enrofloxacin | Bacteroidetes | decrease   | TNF      |
| Enrofloxacin | Bacteroidetes | decrease   | CCL3     |
| Enrofloxacin | Bacteroidetes | decrease   | Ffar3    |
| Enrofloxacin | Bacteroidetes | decrease   | Ffar2    |
| Enrofloxacin | Bacteroidetes | decrease   | Nfkb1    |
| Enrofloxacin | Bacteroidetes | decrease   | Pdcd1lg2 |
| Enrofloxacin | Bacteroidetes | decrease   | Cd86     |
| Enrofloxacin | Bacteroidetes | decrease   | Cd40     |
| Enrofloxacin | Bacteroidetes | decrease   | Il6      |
| Enrofloxacin | Bacteroidetes | decrease   | Il12b    |
| Enrofloxacin | Bacteroidetes | decrease   | Gcg      |

