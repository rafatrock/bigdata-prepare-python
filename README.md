# Ready to Process Big Data?

Learn how to handle large amount of Big Data for Machine Learning using Python

## Getting Started

![Quote on BigData by Dan Ariely](https://scontent.fmaa1-4.fna.fbcdn.net/v/t1.0-9/29025597_10156279834452053_6491808424697790464_o.png?_nc_cat=102&_nc_ht=scontent.fmaa1-4.fna&oh=45bac59d9687755dae0cd03d4139ed9d&oe=5D43E986)

This is a step by step guide with necessary codes and configurations for Data Scientists, Data Engineers, Data Analysts, Machine Learning Engineers as well as Business Analysts who are planning to mess with large amount of Big Data for Machine Learning, Deep Learning, Classifications, Predictions or applying Artificial Intelligence by using Python and other possible FREE resources.

### Prerequisites

Generally in our local system we can deal with small amount of data for machine learning. It is efficient and good for small to medium scale of data volume. You can use your local system for even Kaggle like contests. But to deal with enormous amount of data we need a robust strategy. 

The worst part is that you even can't load the data on Microsoft Excel (at most `1,048,576 rows`) or any editor due to their resource constraints. So we need a different strategy and different environment to deal with Big Data.

Before anyone starts the war with Big Data, I beleive these platform(s) and tool(s) are required to be installed and configured properly

```
Python >= 3.x
Apache Spark >= 2.x
DASK >= 1.x
A Cloud Infrastructure (e.g. Google Cloud Platform)
```
### Data Access Strategy

For the last couple of decades `ETL (Extract, Transform, Load)` has been the traditional approach for data warehousing and analytics. The `ELT (Extract, Load, Transform)` approach changes the old paradigm. But, to us it just "T" and "L" are switched.
![ELTvsETL](https://software-advice.imgix.net/wordpress/other_pages/BI/303737_0003.png)

`ETL` requires management of the raw data, including the extraction of the required information and running the right transformations to ultimately serve the business needs. Each stage - extraction, transformation and loading - requires interaction by data engineers and developers, and dealing with capacity limitations of traditional data warehouses. Using `ETL`, analysts and other BI users have become accustomed to waiting, since simple access to the information is not available until the whole ETL process has been completed.

In the `ELT` approach, after you've extracted your data, you immediately start the loading phase - moving all the data sources into a single, centralized data repository. With today's infrastructure technologies using the cloud, systems can now support large storage and scalable compute. Therefore, a large, expanding data pool and fast processing is virtually endless for maintaining all the extracted raw data.

### Difference between ETL and ELT

| Parameters | ETL | ELT |
| ---------- | ---- | --- |
| Process |	Data is transformed at staging server. Then transferred to Datawarehouse DB | Data remains in the DB of the Datawarehouse|
| Usage	| For small amount of data | For high amounts of data |
| Transformation	| Done in ETL server/staging area |	Transformations are performed in the target system |
| Time-Load |	Time intensive | Faster |
| Time-Transformation	| Needs to wait for transformation to complete. As data size grows, transformation time increases |	Speed is never dependant on the size of the data |
| Time- Maintenance	| Highs maintenance | Low maintenance |
| Implementation Complexity	| Easier to implement |	Should have deep knowledge of tools and expert skills |
| Support for Data Warehouse |	On-premises, relational and structured data |	Scalable cloud infrastructure which supports structured, unstructured data sources |
| Complexity	| Loads only the important data, as identified at design time |	Involves development from the output-backward and loading only relevant data |
| Cost	| High costs for small and medium businesses | Low entry costs using online Software as a Service Platforms |
| Aggregations	| Complexity increase with the additional amount of data in the dataset |	Power of the target platform can process significant amount of data quickly |
| Maturity	| The process is used for over two decades. Well documented and best practices easily available |	Relatively new concept and complex to implement |
| Hardware	| Most tools have unique hardware requirements that are expensive |	Being SAAS hardware cost is not an issue |

### The Timely Approach

When we have to deal with Big Data, the best possible option to go with the `ELT` approach considering the benefits of this approach.

### Installing

I am sharing my thoughts on a step by step series of examples that tell you how to get a development environment ready

---

- [x] Using Google Colaboratory
- [ ] Install Apache Spark with Hadoop
- [ ] Connect with a Cloud Data Repository to access Datasets

The first step is to use a Cloud Infrastructure to compute and transform your data. There can be different options. One free option can be using [Google Colaboratory](https://colab.research.google.com). This is free and provide you a good Cloud Environment to run your scripts in Python by using Jupyter Notebook.

![Google Colaboratory](https://cdn-images-1.medium.com/max/1600/1*9tQN6y8rc3Qwr7V70F1F5g.png)

---

- [x] Using Google Colaboratory
- [x] Install Apache Spark with Hadoop
- [ ] Connect with a Cloud Data Repository to access Datasets

The following commands will install Apache Spark 2.3.3, Java 8, Findspark library that makes it easy for Python to work on the given Big Data.

```Shell
$ sudo apt-get install openjdk-8-jdk-headless -qq > /dev/null 
$ wget -q http://apache.osuosl.org/spark/spark-2.3.3/spark-2.3.3-bin-hadoop2.7.tgz 
$ tar xf spark-2.3.3-bin-hadoop2.7.tgz 
$ pip install -q findspark 
```

---

- [x] Using Google Colaboratory
- [x] Install Apache Spark with Hadoop
- [x] Connect with a Cloud Data Repository to access Datasets

Then the next task is to connect the gigantic data sources from Cloud Storage. For testing purposes you can use the repository from [Mega](https://mega.nz).

```Python
import os
os.system('git clone https://github.com/jeroenmeulenaar/python3-mega.git')
os.chdir('python3-mega')
os.system('pip install -r requirements.txt')
```
Alternatively you can use the repository from [Google Cloud Storage](https://cloud.google.com).

```Python
from google.colab import auth
auth.authenticate_user()
```

```Shell
$ gsutil cp -r gs://<source path> /content/<destination path on Google Colaboratory>
```
---

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

See also the list of [contributors](https://github.com/rafatrock/bigdata-prepare-python/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

