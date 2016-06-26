# YelpDataset
We are generating some basic insights on the yelp Data using Hive.

Dataset used for this insights is review dataset provided by Yelp for academic purpose.

<b>Prep or Setup :</b>
<br>A hadoop cluster with any distribution(CDH,HDP,MapR,Apache). I am using CDH5.7 for this exercise. 
<br>Hive installed in the cluster.
<br>Data is downloaded from the internet.

<b>Steps:</b>
<ol>
<li>Get the data into Linux Machine
    <br>      we can perform a wget on the linux gateway node or copy the dataset from windows using winscp or filezilla tool.</li>
<li>Load the data into hadoop
    <br>    dfs -put yelp_academic_dataset_review.json /hdev1/db/testing/yelp_academic_review/ </li>
<li> once data is loaded open a hive client session and run the commands in the following order
        <ol>
        <li>json table creation</li>
        <li>parquet table creation</li>
        <li>insert data into parquet table from json table</li>
        <li>run the queries</li>
        </ol>
    Alternatively we can use hive -f to run the commands from linux edgenode.</li>
</ol>
<b>Dependency:</b>
 <repositories>
    <repository>
      <id>cloudera</id>
      <url>https://repository.cloudera.com/artifactory/cloudera-repos/</url>
    </repository>
  </repositories>


