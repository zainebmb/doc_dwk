# Deepwukong




## Joern old version Installation

clone this repo: https://github.com/ives-nx/dwk_preprocess/tree/main/joern_slicer/joern

### setting the evironment:
- install openjdk8 ( java version 1.8) ( manually)
- install gradle 2.0 ( manually)
- install graphviz
- you should have a python version 3.8 or 3.9 
- prefrebly also install microsoft build tools 
- install pygraphviz (pip install --global-option=build_ext --global-option="-IC:\pathto\Graphviz\include" --global-option="-LC:\pathto\Graphviz\lib" pygraphviz)

when you are done with all the installations:
* add them to your PATH 
* create this sys env var:
name: JAVA_HOME ; value: PATH to your JDK (eg: C:\Program Files\Eclipse Adoptium\jdk-8.0.372.7-hotspot)


### Building joern:
 run  the build.sh shell script or just run gradle build

 after building create these sys env vars:
 1) name: OCTOPUS_HOME ; value: PATH to "octopus" folder inside the joern folder from joern repository that you cloned ( eg: C:\Users\zaineb\Desktop\deepwukong\DeepWukong\dwk_preprocess\joern_slicer\joern\projects\octopus)

now go to the shell script octopus-server.sh under projects/octopus and :
comment this line : OCTOPUS_HOME="$( cd "$( dirname "$0" )" && pwd )"
in the last line change "/" with "\" and ":" with ";" 
 ( this will solve that damned cant find or load main class xD ) you can check by running joern-server.sh 


## EL rasmi xD

clone this repo: https://github.com/jumormt/DeepWukong

Download this data :https://bupteducn-my.sharepoint.com/personal/jackiecheng_bupt_edu_cn/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fjackiecheng%5Fbupt%5Fedu%5Fcn%2FDocuments%2FDataset%2FData%2E7z&parent=%2Fpersonal%2Fjackiecheng%5Fbupt%5Fedu%5Fcn%2FDocuments%2FDataset&ga=1 , and unzip it under project root/data folder.

now go to configs/dwk.yaml and:
change joern_path to your local path of the joern-parse file ( preferably absolute path)


now run : set PYTHONPATH=.
then run python src/joern/joern-parse.py -c config file

