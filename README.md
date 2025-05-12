## NeMo Curator Dataset Curation Pipeline
This project implements three variations of a curation pipeline for text datasets using NVIDIA's NeMo Curator framework. 
The pipeline applies various filters to clean and prepare text data for language model training and analyzes how the different configurations of curation result in distinct filtering of the data.

### This project:
* Loads CommonCrawl CreativeCommons Corpus (C5) data
* Preventively identifies and fixes unicode problems
* Implements three levels of text filtering:
  - Basic: Removes non-alphanumeric content, symbols, numbers, URLs, etc.
  - C4: Focuses on more nuanced filters, looking for boilerplate, extremely long words, lack or excess of punctuation
  - Full: Combines all filters for maximum quality
* Results analysis and comparison between filtering strategies

## Data Processing
* Load the CommonCrawl CreativeCommons Corpus (C5) data from a HuggingFace dataset
* Samples and preprocesses the data
* Applies the three curation processes
* Compares filtering effectiveness across different configurations
* Outputs metrics on data retention percentages
