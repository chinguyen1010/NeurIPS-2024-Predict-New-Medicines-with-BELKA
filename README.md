# NeurIPS-2024: Predict New Medicines with BELKA
Predict small molecule-protein interactions using the Big Encoded Library for Chemical Assessment (BELKA)

Overview:

In this competition, you’ll develop machine learning (ML) models to predict the binding affinity of small molecules to specific protein targets – a critical step in drug development for the pharmaceutical industry that would pave the way for more accurate drug discovery. You’ll help predict which drug-like small molecules (chemicals) will bind to three possible protein targets.


Description
Small molecule drugs are chemicals that interact with cellular protein machinery and affect the functions of this machinery in some way. Often, drugs are meant to inhibit the activity of single protein targets, and those targets are thought to be involved in a disease process. A classic approach to identify such candidate molecules is to physically make them, one by one, and then expose them to the protein target of interest and test if the two interact. This can be a fairly laborious and time-intensive process.

The US Food and Drug Administration (FDA) has approved roughly 2,000 novel molecular entities in its entire history. However, the number of chemicals in druglike space has been estimated to be 10^60, a space far too big to physically search. There are likely effective treatments for human ailments hiding in that chemical space, and better methods to find such treatments are desirable to us all.

To evaluate potential search methods in small molecule chemistry, competition host Leash Biosciences physically tested some 133M small molecules for their ability to interact with one of three protein targets using DNA-encoded chemical library (DEL) technology. This dataset, the Big Encoded Library for Chemical Assessment (BELKA), provides an excellent opportunity to develop predictive models that may advance drug discovery.

Datasets of this size are rare and restricted to large pharmaceutical companies. The current best-curated public dataset of this kind is perhaps bindingdb, which, at 2.8M binding measurements, is much smaller than BELKA.

This competition aims to revolutionize small molecule binding prediction by harnessing ML techniques. Recent advances in ML approaches suggest it might be possible to search chemical space by inference using well-trained computational models rather than running laboratory experiments. Similar progress in other fields suggest using ML to search across vast spaces could be a generalizable approach applicable to many domains. We hope that by providing BELKA we will democratize aspects of computational drug discovery and assist the community in finding new lifesaving medicines.

Here, you’ll build predictive models to estimate the binding affinity of unknown chemical compounds to specified protein targets. You may use the training data provided; alternatively, there are a number of methods to make small molecule binding predictions without relying on empirical binding data (e.g. DiffDock, and this contest was designed to allow for such submissions).

Your work will contribute to advances in small molecule chemistry used to accelerate drug discovery.

<img width="779" height="415" alt="Screenshot 2025-11-07 at 12 36 07 AM" src="https://github.com/user-attachments/assets/1a9d10e7-2851-4752-a984-d4753b3a3f9d" />



Additional Details
Chemical Representations
One of the goals of this competition is to explore and compare many different ways of representing molecules. Small molecules have been represented with SMILES, graphs, 3D structures, and more, including more esoteric methods such as spherical convolutional neural nets. We encourage competitors to explore not only different methods of making predictions but also to try different ways of representing the molecules.

We provide the molecules in SMILES format.

SMILES
SMILES is a concise string notation used to represent the structure of chemical molecules. It encodes the molecular graph, including atoms, bonds, connectivity, and stereochemistry as a linear sequence of characters, by traversing the molecule graph. SMILES is widely used in machine learning applications for chemistry, such as molecular property prediction, drug discovery, and materials design, as it provides a standardized and machine-readable format for representing and manipulating chemical structures.

The SMILES in this dataset should be sufficient to be translated into any other chemical representation format that you want to try. A simple way to perform some of these translations is with RDKit.

Details about the experiments
DELs are libraries of small molecules with unique DNA barcodes covalently attached
Traditional high-throughput screening requires keeping individual small molecules in separate, identifiable tubes and demands a lot of liquid handling to test each one of those against the protein target of interest in a separate reaction. The logistical overhead of these efforts tends to restrict screening collections, called libraries, to 50K-5M small molecules. A scalable solution to this problem, DNA-encoded chemical libraries, was described in 2009. As DNA sequencing got cheaper and cheaper, it became clear that DNA itself could be used as a label to identify, and deconvolute, collections of molecules in a complex mixture. DELs leverage this DNA sequencing technology.

These barcoded small molecules are in a pool (many in a single tube, rather than one tube per small molecule) and are exposed to the protein target of interest in solution. The protein target of interest is then rinsed to remove small molecules in the DEL that don’t bind the target, and the remaining binders are collected and their DNA sequenced.

DELs are manufactured by combining different building blocks
An intuitive way to think about DELs is to imagine a Mickey Mouse head as an example of a small molecule in the DEL. We attach the DNA barcode to Mickey’s chin. Mickey’s left ear is connected by a zipper; Mickey’s right ear is connected by velcro. These attachment points of zippers and velcro are analogies to different chemical reactions one might use to construct the DEL.

We could purchase ten different Mickey Mouse faces, ten different zipper ears, and ten different velcro ears, and use them to construct our small molecule library. By creating every combination of these three, we’ll have 1,000 small molecules, but we only needed thirty building blocks (faces and ears) to make them. This combinatorial approach is what allows DELs to have so many members: the library in this competition is composed of 133M small molecules. The 133M small molecule library used here, AMA014, was provided by https://www.alphama.com.cn/en/about/. It has a triazine core and superficially resembles the DELs described https://www.nature.com/articles/nchembio.211


<img width="3000" height="2100" alt="image" src="https://github.com/user-attachments/assets/f13b3445-c43a-4342-b858-1324d782053b" />
<img width="764" height="610" alt="Screenshot 2025-11-07 at 12 38 29 AM" src="https://github.com/user-attachments/assets/db3d3371-a454-4f3a-a606-af6442093a92" />


NeurIPS 2024
This competition is an official NeurIPS 2024 competition and its results will be presented at the NeurIPS 2024 conference. The contribution of the winning team(s) will be highlighted. Attending the workshop is not required to participate in the competition.

The thirty-eighth annual NeurIPS conference will be held Mon. Dec 9th through Sun the 15th, 2024 at the Vancouver Convention Center.

Citation:

Andrew Blevins, Ian K Quigley, Brayden J Halverson, Nate Wilkinson, Rebecca S Levin, Agastya Pulapaka, Walter Reade, and Addison Howard. NeurIPS 2024 - Predict New Medicines with BELKA. https://kaggle.com/competitions/leash-BELKA, 2024. Kaggle.

