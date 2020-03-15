# Prova de conceito - Apache Spark

Exemplo realizado para a equipe de migração.

**Passos para instalação do apache spark:**

tar xzvf spark-2.4.5-bin-hadoop2.7.tgz
sudo mv spark-2.4.5-bin-hadoop2.7 /opt/spark-2.4.5

**Colocar -no arquivo ~/.profile**
export PATH="$HOME/anaconda/bin:$PATH"
export SPARK_HOME=/opt/spark-2.4.5
export PATH=$SPARK_HOME/bin:$PATH
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'

**Então executar:** 

source ~/.profile

chown -R $USER /opt/spark-2.4.5

Faça o download do anaconda em:

https://anaconda.org/

Crie um ambiente com os pacotes iniciais abaixo:

conda create --name pyspark python==3.7
conda activate pyspark
conda install py4j
conda install -c conda-forge pyspark
conda install -c conda-forge jupyter_core
conda install -c conda-forge jupyter
conda install -c conda-forge  findspark
conda install matplotlib

**Para usar o driver jdbc do mysql jogue para a pasta jars do spark:**

cp mysql-connector-java-8.0.18/mysql-connector-java-8.0.18.jar /opt/spark-2.4.5/jars