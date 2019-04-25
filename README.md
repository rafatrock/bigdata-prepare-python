# Ready to Process Big Data?

Learn how to handle large amount of Big Data for Machine Learning using Python

## Getting Started

![Quote on BigData by Dan Ariely](https://scontent.fmaa1-4.fna.fbcdn.net/v/t1.0-9/29025597_10156279834452053_6491808424697790464_o.png?_nc_cat=102&_nc_ht=scontent.fmaa1-4.fna&oh=45bac59d9687755dae0cd03d4139ed9d&oe=5D43E986)

This is a step by step guide with necessary codes and configurations for Data Scientists, Data Engineers, Data Analysts, Machine Learning Engineers as well as Business Analysts who are planning to mess with large amount of Big Data for Machine Learning, Deep Learning, Classifications, Predictions or applying Artificial Intelligence by using Python and other possible FREE resources.

### Prerequisites

Generally in our local system we can deal with small amount of data for machine learning. It is efficient and good for small to medium scale of data volume. You can use your local system for even Kaggle like contests. But to deal with enormous amount of data we need a robust strategy. 

```PowerShell
systeminfo | findstr /C:"Total Physical Memory"
systeminfo | findstr /C:"Processor(s)"
```

Even you can't load the data on Microsoft Excel (at most `1,048,576 rows`) or any editor 

Before anyone starts the war with Big Data I beleive these platform(s) and tool(s) are required to be installed and configured properly

```
Python >= 3.x
Apache Spark >= 2.x
CSVKit >= 1.X
A Cloud Infrastructure (e.g. Google Cloud Platform)
```

### Installing

I am sharing my thoughts on a step by step series of examples that tell you how to get a development env ready

- [x] Using Google Colaboratory
- [ ] Install Apache Spark with Hadoop
- [ ] Install CSVKit for handling CSV files
- [ ] Connect with a Cloud Data Repository to access Datasets

The first step is to use a Cloud Infrastructure to compute and transform your data. There can be different options. One free option can be using Google Colaboratory. This is free and provide you a good Cloud Environment to run your scripts in Python bu using Jupyter Notebook.

![Google Colaboratory](https://cdn-images-1.medium.com/max/1600/1*9tQN6y8rc3Qwr7V70F1F5g.png)

---

- [x] Using Google Colaboratory
- [x] Install Apache Spark with Hadoop
- [x] Install CSVKit for handling CSV files
- [ ] Connect with a Cloud Data Repository to access Datasets

The following commands will install Apache Spark 2.3.3, Java 8, Findspark and most importantly CSVKit library that makes it easy for Python to work on the given Big Data.

```Shell
$ sudo apt-get install openjdk-8-jdk-headless -qq > /dev/null 
$ wget -q http://apache.osuosl.org/spark/spark-2.3.3/spark-2.3.3-bin-hadoop2.7.tgz 
$ tar xf spark-2.3.3-bin-hadoop2.7.tgz 
$ pip install -q findspark 
$ pip install -q csvkit
```

---

- [x] Using Google Colaboratory
- [x] Install Apache Spark with Hadoop
- [x] Install CSVKit for handling CSV files
- [x] Connect with a Cloud Data Repository to access Datasets

Then the next task is to connect the gigantic data sources from Cloud Storage. For testing purposes we have taken the repository from [Mega](https://mega.nz).

```Python
import os
os.system('git clone https://github.com/jeroenmeulenaar/python3-mega.git')
os.chdir('python3-mega')
os.system('pip install -r requirements.txt')
```

## Built With

* [Apache Spark](https://spark.apache.org) - A unified analytics engine for large-scale data processing
* [Google Colaboratory](https://colab.research.google.com) - Cloud research platform from Google
* [Python](https://www.python.org) - The most popular programming language for dealing Big Data

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

**Rubaiyat Islam Rafat** - *Initial work* - [rafatrock](https://github.com/rafatrock)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

