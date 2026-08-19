# Relay\_Cooperation



This repository contains the script and data tables used in the *Relay cooperation between women and girls during foraging trips* *among BaYaka hunter-gatherers in the Republic of the Congo* paper from Visine \& Jang.



\## Abstract



Children in small-scale societies contribute to subsistence and infant care and learn these roles through everyday participation. To examine how such participation is organised in practice, we focus on women’s daily foraging activities among BaYaka hunter-gatherers in the Congolese rainforest, where children frequently accompany adults. Using focal follows, we recorded mothers’ activity states—foraging, travelling, and resting—alongside helping behaviours of all group members, including childcare, foraging, and basket carrying. We find that childcare, subsistence, and load-carrying responsibilities are dynamically redistributed through relay cooperation between women and children—particularly girls—who are not necessarily kin. Infant care is frequently transferred from women to girls, enabling mothers to continue foraging without carrying infants. When mothers pause to rest or breastfeed, girls temporarily take over foraging tasks. These role shifts occur repeatedly within trips. This pattern reveals a structured yet flexible system that allows mothers to manage the energetic and mobility constraints of childcare while maintaining productivity. At the same time, relay cooperation provides girls with repeated opportunities to engage in both caregiving and subsistence, supporting learning through participation beyond the mother–child dyad. These findings provide insight into how children develop as cooperative actors through active participation in women’s subsistence and caregiving activities from an early age.



\\



\## Presentation of the script



This script will, from the observational data, produce descriptive statistics used in the paper.



This file was produced using a \[Rmarkdown Cheatsheet] (https://rstudio.github.io/cheatsheets/html/rmarkdown.html).





This script loads the data from focal follows, with the files a) \*Waypoints\_relay\_coop\*, a csv file containing for each row a change of activity in mother's activities, childcare responsibilities or basket carrying.  

This csv contains the columns:  



1\. Focal follow / focal woman identifier

&#x20;   - ID\_focal:           focal woman and trip ID; num. from 1 to 18



2\. Focal woman activity

&#x20;   - Time:               hour::minute::second of the day when the focal woman \*\*starts\*\* a different behaviour/ activity

&#x20;   - resting\_behaviour:  is the focal woman resting? log. TRUE/FALSE

&#x20;   - walking:            is the focal woman travelling? log. TRUE/FALSE

&#x20;   - foraging:           is the focal woman foraging? log. TRUE/FALSE

&#x20;   - labour:             is the focal woman working? foraging is included in this measure as well log. TRUE/FALSE

&#x20;   - breastfeed:         did the focal woman start breastfeeding? log. TRUE/FALSE



\\



We also load b) \*focal\_follow\_relay\_coop\*, which describes and summarises each focal follow independently (\*i.e.\*, one row per focal follow = 18 rows). When loaded, it contains the columns:



1\. Focal follow / focal woman identifier

&#x20;   - ID\_focal:           focal woman and trip ID; num. from 1 to 18

&#x20;   - trip\_duration:      total duration of the foraging trip in seconds



2\. Group composition

&#x20;   - n\_girls:            total number of girls present during the foraging trip

&#x20;   - n\_women:            total number of women present during the foraging trip

&#x20;   - n\_boys:             total number of boys present during the foraging trip

&#x20;   - n\_men:              total number of men present during the foraging trip

&#x20;   - husband\_presence:   presence of the focal woman's husband (and infant father); log. TRUE/FALSE

&#x20;   

\\



Then we load c) \*infant\_caregiver\*, a table describing the infant caregiver at any time of the trip. It has 3 columns:

&#x20;   - trip\_id:      focal woman and trip ID; num. from 1 to 18

&#x20;   - caregiver:    identity of the infant caregiver at a given time (mother or girl or woman or boy or father or ground or unknown)

&#x20;   -duration:      duration of the caregiving configuration in seconds (cumulative duration for each ID equals to the total trip duration)



\\



Finally we load c) \*basket\_carrier\*, a table describing the focal woman's basket carrier at any time of the trip. It has the same 3 columns:

&#x20;   - trip\_id:      focal woman and trip ID; num. from 1 to 18

&#x20;   - caregiver:    identity of the basket carrier at a given time (mother or girl or woman or boy or father or ground or unknown)

&#x20;   -duration:      duration of the carrying configuration in seconds (cumulative duration for each ID equals to the total trip duration)



\\



\## R Software Requirements



Analyses were run in \*\*R (version 4.3.0)\*\*. Required packages (auto-installed by the script if missing):



\- `readr` — data handling

\- `ggplot2` — visualisation



\\



\## Ethics Statement



Permissions to conduct research in the Republic of the Congo were obtained from the Institut National de

Recherche en Sciences Sociales et Humaines (INRSSH) in Brazzaville. All study procedures were carried out in accordance with national laws and with the relevant guidelines and regulations of the Republic of the Congo, as well as the ethical standards of the Max Planck Institute for Evolutionary Anthropology, Germany (Application No: 2023 7). Prior to data collection, we presented an overview of the project, including its objective and methods, at a public meeting with all inhabitants of the study village and obtained informed consent at the community level. Individual informed consent was subsequently obtained from each participant before every focal-follow observation, including consent to accompany the focal woman on her foraging trip and consent from all accompanying group members, both adults and children. Each morning, researchers walked through the village to recruit individuals who were available and willing to participate. For each potential participant, it was explained that participation was entirely voluntary and that declining to participate would involve no negative consequences. All explanations and consent procedures were conducted in the BaYaka language, with the assistance of BaYaka translators and research assistants fluent in BaYaka and Lingala. Individuals who agreed to participate and provided verbal consent were accompanied by researchers during their foraging trips. All personal and identifying information was anonymised.



\\



\## Funding



This research was funded by the Department of Human, Behavior, Ecology, and Culture at the Max Planck

Institute for Evolutionary Anthropology in Germany.



\\



\## Citation



If you use these data or scripts, please cite the associated manuscript (full citation to be added upon publication).



\\



\## Contact



For questions about the data or code, please contact the corresponding author (see manuscript for details).



