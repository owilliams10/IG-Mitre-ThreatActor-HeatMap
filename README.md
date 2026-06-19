# Building a Heat Map of TTPs Used by Threat Groups Relevant to IG

<img width="1888" height="827" alt="image" src="https://github.com/user-attachments/assets/6990006a-5090-495e-a587-bf1140af6ccd" />


## Introduction

In this project, I use the Mitre Att&ck Navigator tool to build a heat map of techniques used by threat groups that are relevant to the Insight Global attack surface. IG's attack surface includes financial data, PII, SaaS (third-party software), employment pipelines, and possible malicious indsiders.

## Creating the First Layer

First, we'll navigate to the Attack Navigator and create the layer for our first threat group: FIN7. FIN7 targets PII and financial/billing systems:

<img width="1531" height="917" alt="creatingLayer" src="https://github.com/user-attachments/assets/d1f0f44d-f867-4dde-a609-1c6800358cda" />


In the Layer Controls Tab use the Layer Settings feature to name the layer and add a description:

<img width="1887" height="910" alt="nameDescribeLayerFIN7" src="https://github.com/user-attachments/assets/9c237762-9109-4696-8fa7-1169de79eb72" />


On the Selection Controls tab, we'll use the Search & Multiselect feature to search for FIN7 and select the all of its TTPs to show on this layer:

<img width="1898" height="967" alt="selectFIN7TTPs" src="https://github.com/user-attachments/assets/1e139f55-1f0d-42e6-a64f-d8c4d0947ed0" />


On the Layer Controls tab, use the Color Setup feature to set the Scoring Gradient colors to green-to-red, and the score range to 0-to-3, then select the show option:

<img width="1880" height="807" alt="FIN7colorGradient" src="https://github.com/user-attachments/assets/d16bdbe7-b4aa-458d-a024-fa04e893133e" />


Now on the Technique Controls Tab, use the Scoring feature to set the score to 0:

<img width="1897" height="968" alt="FIN7scoring" src="https://github.com/user-attachments/assets/7d4167a2-7c08-4ba9-9fc1-ebbf2b70b2a5" />


<b> Repeat the above steps to create a new layer for Raspberry Robin, ATP29, and ATP 41. Here's what each of these layers looks like individually: <b>

FIN7:
<img width="1895" height="910" alt="image" src="https://github.com/user-attachments/assets/51bfd9da-bd03-489e-a2ac-7b9ca533d185" />

Raspberry Robin:
<img width="1902" height="832" alt="image" src="https://github.com/user-attachments/assets/7b4f44d6-ca42-4ef9-b30b-9791fa6a0a5c" />

ATP29:
<img width="1897" height="827" alt="image" src="https://github.com/user-attachments/assets/52e334d5-8297-40a9-8e7b-05a03c005614" />

ATP 41:
<img width="1903" height="922" alt="image" src="https://github.com/user-attachments/assets/0ad8b99a-2420-489d-974e-760f7fd4e193" />


<b> For the Insdier Threats layer, we'll individually select the techniques specifically related to Privilege & Credential Abuse, Data Collection and Staging, Data Exfiltration, Sabotage and Impact: <b>
<img width="1902" height="871" alt="addingTTPsforInsiderThreats" src="https://github.com/user-attachments/assets/04e8502e-43f5-4838-93d0-a2216189d50d" />

<img width="1893" height="912" alt="image" src="https://github.com/user-attachments/assets/2ea4e38a-336a-4964-983a-cca98b17c9ce" />

Now we'll build the layer that will become our Heat Map. Well need to create a new tab then select the Create Layer from Other Layers option. We'll select the latest version of Enterprise Mitre Attack as the domain, and add all of the layers to the score expression:
<img width="1547" height="926" alt="startingCombinedLayer" src="https://github.com/user-attachments/assets/38efbaab-2d27-4674-b05e-30a3dd42ec27" />

Use the Color Setup feature to set the Scoring Gradient colors to green-to-red, and the score range to 1-to-4, then select the show option:
<img width="1900" height="971" alt="combinedLayerScoringGradient" src="https://github.com/user-attachments/assets/b50d6fcb-f93e-4d2b-a535-ea7cd3ffb416" />

Now go to each layer and set the score to 1 for all of them like so:
<img width="1897" height="962" alt="setScoreTo1" src="https://github.com/user-attachments/assets/7211bc60-3f9e-42d5-8536-e109b4ffb65c" />

Our final heat map shows techniques in red that are used by atleast 4 of the threat groups we analyzed. Techniques used by 3 groups are orange, techniques used by 2 groups are light green, and techniques used by only 1 group are green:

<img width="1902" height="923" alt="image" src="https://github.com/user-attachments/assets/f7543983-5d9d-44c9-a682-4c7f0bddaaf7" />

Here are examples of techniques that scored 4, 3, and 2:
<img width="1129" height="487" alt="image" src="https://github.com/user-attachments/assets/a3f99602-65d3-44e6-a76b-92795baabc6a" />

<img width="1153" height="533" alt="image" src="https://github.com/user-attachments/assets/9f2198d3-ae94-4ff9-848c-66f4fbc8c2b2" />

<img width="1067" height="480" alt="image" src="https://github.com/user-attachments/assets/baa6363c-51f8-42e4-bb64-47f8b7f8fb1c" />


We can export the heat map as an SVG or Excel file:
<img width="1906" height="393" alt="ExportHeapMapSVGEXCELpng" src="https://github.com/user-attachments/assets/9af0b114-b164-432b-a562-47d11a71a8ed" />

RESOURCES:

Mitigations for Techniques Most Commonly used Amongst the Threat Groups: [MITIGATIONS FOR TTPs THAT SCORED 3 or HIGHER.pdf](https://github.com/user-attachments/files/29150832/MITIGATIONS.FOR.TTPs.THAT.SCORED.3.or.HIGHER.pdf)

## Conclusion

In this project, a heat map was created to highlight some of the most common techniques used by threat group types that are likely to target IG based on our attack surface. This information can be used by the Cyber Operations teams to prepare the necessary detection and mitigation capabilities.
