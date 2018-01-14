# AIResearch
AI face detection using Tensorflow for my research lab.

<<<<<<< HEAD
1. describe what the project does
2. its requirements
3. how to use it


=======
To Do List:
1. make a script file to download all necessary packages (python, jupyternotebook, etc.)
2. Follow the tutorial (https://pythonprogramming.net/introduction-use-tensorflow-object-detection-api-tutorial/).
3. ORGANIZE!
>>>>>>> b30cf867b36e2e602095c8d9bc3313008b42e4bf


#instruction found in models/research/object_detection/g3doc/installation.md
#after installation of python & tensorflow
#pip install tensorflow

pip install pillow
pip install lxml
pip install jupyter
pip install matplotlib

git clone https://github.com/tensorflow/models.git

#install protoc if you don't have it already
#to check if you have, run  protoc --version
#https://github.com/google/protobuf/releases
#after installing, run 
    #sudo ./configure
    #sudo make check
    #sudo make install
    
#skip tutorials 2 & 3
    
#directory setup
#Object-Detection
#-data/
#--test_labels.csv
#--train_labels.csv
#-images/
#--test/
#---testingimages.jpg
#--train/
#---testingimages.jpg
#--...yourimages.jpg
#-training
#-xml_to_csv.py

#test directory should have a copy of approx 10% of images with annotation data
#training directory should have a copy of the rest of data with annotations
    
#annotation files need to be in CSV format
    

#run these in the models/research directory
#protoc object_detection/protos/*.proto --python_out=.
#export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim

#from models/research run
    #sudo python setup.py install
    #this formally installs the object_detection library 
    
#go to models/research/object_detection
#open jupyter notebook
#run all object_detection_tutorial.ipynb
    #should get a pic of dogs, people, and kites with boxes


#here!!!
#instruction found in models/research/object_detection/g3doc/preparing_inputs.md
#next step is to generate TFrecords files named XXX_train.record and XXX_val.record in the tensorflow/models/research/ directory.
#The label map for the Pet dataset can be found at object_detection/data/pet_label_map.pbtxt.
    
#models/research/object_detection/g3doc/oid_inference_and_evaluation.md #might not be important
    #pip install pandas
    #pip install contextlib2
    
#models/research/object_detection/g3doc/using_your_own_dataset.md
    #make a label map here models/research/object_detection/data/
    #contents
    
#label map
#item {
#  id: 1
#  name: 'Monkey'
#}
    
    #make a create_monkey_tf_record.py here models/research/object_detection/dataset_tools/

after creating create_monkey_tf_record.py file, and running it, there should be a train.record and test.record under research/object_detection/ file