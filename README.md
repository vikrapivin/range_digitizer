# Range_digitizer
This is a work in progress, first part of a project to digitize poker ranges found online. The first part of this project takes a screenshot and extracts the range. See `examples` and `out` for a visual demonstration of what is extracted.

Data in directory is used under fair use.

To run:
1. download the repo
2. create a folder called `detr-resnet-50_finetuned_pkr/`
3. Extract [checkpoint-10648.zip](https://github.com/vikrapivin/range_digitizer/releases/tag/0.0) to `detr-resnet-50_finetuned_pkr/`
4. Create a new python environment/ anaconda environment and do `pip install -r requirements.txt`
5. Run the code in the `range_extractor.ipynb` notebook

# Todo

1. Go from extracted range image to categorization of number of actions and whether mixed ranges are represented vertically, horizontally, or both (e.g. vertical for % of missing range and horizontal for mixed actions)
2. Digitize each box of the range as 100% action or the distribution of actions when a player plays a mixed action in a certain spot

# Part 1 method
1. This data is acquired from scraping Google/ Duckduckgo.
2. Data is then manually labeled for ~500 examples.
3. 20% of data is used as test dataset and this model achieves 99% accuracy in the test dataset (as expected as this is an easy task).
