# Maha-s-hack
Name: MAHALAKSHMI M
Email: infommahalakshmi@gmail.com
college name: Mepco Schlenk Engineering College

Task Table:
Tasks Attempted:8
1. Image Metadata Analysis (50)
2. Indoor/Outdoor Classifier (100)
3. Search Images with Text (100)
4. Search Images with an Image (125)
5. Object Segmentation & Cropping – Person Blur (150)
6. Image Similarity Scoring (150)
7. Search for Objects with an Image Query (150)
8. Investigator Web Tool (175)

Setup environment:
bash env_setup.sh
(or)
python -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt

Datasets/Models:
1. 50 images go in data/images50/.
2. YOLOv8 and CLIP weights will auto-download on the first run.
3. Large files (datasets, pretrained models) are not committed.
4. Each task folder contains sample input/output screenshots for reference.
   
How to Run Tasks:
Task 1 – Metadata Analysis
python task1_metadata_analysis/main.py --image data/samples/sample.jpg --out task1_metadata_analysis/out.json

Task 2 - Indoor/Outdoor Classification
python task2_indoor_outdoor/cli.py --image data/samples/room.jpg

Task 3 – Text Search
Build index:
python task3_text_search/build_index.py --img_dir data/images50 --index task3_text_search/index.faiss --meta task3_text_search/index.pkl
Search by text:
python task3_text_search/search_text.py --query "desert" --topk 5

Task 4 – Image Search
python task4_image_search/search_image.py --query data/samples/query.jpg --topk 5

Task 5 – Person Blur
python task5_person_blur/blur_people.py --image data/samples/street.jpg --out task5_person_blur/blurred.jpg

Task 6 – Similarity Scoring
python task6_similarity_scoring/similarity.py --image data/samples/subject.jpg --out task6_similarity_scoring/scores.csv

Task 7 – Object Query Search
python task7_object_query_search/search_object.py --query data/samples/object.jpg --topk 5

Task 8 – Investigator Web App
streamlit run task8_investigator_web/app.py

Requirements:
Install dependencies with:
pip install -r requirements.txt


