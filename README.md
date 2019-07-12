# Usage

clone darknet and make it

    git clone https://github.com/AlexeyAB/darknet.git

download this and put it in the bitwise dir

    wget https://pjreddie.com/media/files/darknet19_448.conv.23

put the bitwise directory in the darknet directory then run this from the darknet directory

    ./darknet detector train bitwise/obj.data bitwise/yolo-obj.cfg bitwise/darknet19_448.conv.23





based on this https://medium.com/@manivannan_data/how-to-train-yolov2-to-detect-custom-objects-9010df784f36



get some premade training weights
wget https://pjreddie.com/media/files/darknet19_448.conv.23


put these files in the darknet/cfg directory
obj.data
obj.names
yolo-obj.cfg

put these files and folders in thet darknet directory
train.txt
test.txt
darknet19_448.conv.23
nfpa_dataset

run this
./darknet detector train cfg/obj.data cfg/yolo-obj.cfg darknet19_448.conv.23

./darknet detector train obj.data yolo-obj.cfg darknet19_448.conv.23


# How to 

copy from ec2
scp -r -i ~/.ssh/id_rsa.pub ubuntu@13.236.66.105:/home/ubuntu/output ~/output

test weights
./darknet detector test cfg/obj.data cfg/yolo-obj.cfg yolo-obj_11000.weights darknet_training_demo/nfpa_dataset/pos-1.jpg


test weights
./darknet detector test obj.data yolo-obj.cfg yolo-obj_11000.weights pos-286.jpg
