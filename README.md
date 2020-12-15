# Classification-des-Tweets (NLP, Kmeans, Python) 

## Description<br/>
Dans ce workshop, nous allons:<br/>
• Utiliser l’API de twitter pour l’extraction des tweets à l'aide de tweepy et apprenez à les gérer à l'aide de pandas.<br/>
• Maitriser la partie NLP (natural language processing) avec NLTK en Python<br/>
• Appliquer les principes de nettoyage des données<br/>
• Classer les tweets : regrouper ensemble les tweets qui sont similaires.<br/>
## 0. Prerequisite: What will we need?
* ### Environnement:<br/>
Tout d'abord, nous avons besoins de préparer l'environnement du travail.
[ANACONDA For windows](https://www.anaconda.com/products/individual)
* ### Needed libraries:<br/>
Les exigences que nous devrons installer sont:<br/>
* [NumPy](http://www.numpy.org/): NumPy est une bibliothèque Python utilisée pour travailler avec des tableaux.
Il a également des fonctions pour travailler dans le domaine de l'algèbre linéaire, de la transformée de Fourier et des matrices.
* [Pandas](http://pandas.pydata.org/): Pandas est une bibliothèque Python permettant la manipulation et l'analyse des données.
* [Tweepy](http://www.tweepy.org/): Une bibliothèque Python facile à utiliser pour accéder à l'API Twitter.
* [Matplotlib](http://matplotlib.org/): Matplotlib est une bibliothèque Python destinée à tracer et visualiser des données sous formes de graphiques. Elle peut être combinée avec les bibliothèques python de calcul scientifique NumPy et SciPy.
* [NLTK](https://www.nltk.org//): est une bibliothèque logicielle en Python permettant un traitement automatique des langues.
Maintenant, toutes ces bibliothèques sont installées depuis: !pip install <nom_biblio>

**Now that we have all the requirements, let's get started!**

## 1. Extracting twitter data (tweepy + pandas)<br/>
### Step 1 — How do we get a Twitter Api Key, Api Secret Key, Consumer Key and Consumer Secret key?<br/>
Tout d'abord, nous devons créer un compte Twitter et obtenir les informations d'identification nécessaires sur la plateforme de développement Twitter pour accéder à l'API Twitter en suivant ces étapes:<br/>
#### Apply for a Developer Account:
* Si vous avez déjà des applications, connectez-vous sur https://apps.twitter.com/ avec votre nom d'utilisateur et votre mot de passe Twitter.Puis accédez à Demander un compte développeur.<br/>
* Si vous n'avez pas d'applications, accédez à demander un compte développeur en connectant sur [How to apply for a Twitter Developer account](https://www.extly.com/docs/autotweetng_joocial/tutorials/how-to-auto-post-from-joomla-to-twitter/apply-for-a-twitter-developer-account/#apply-for-a-developer-account)<br/>
#### Get the needed Keys:
Allez dans l'onglet Clés API, nous y trouverons notres clés.<br/>
### Step 2 — How do we connect to the Twitter API<br/>
Maintenant que nous sommes prêts avec les informations d'identification Twitter requises, passons à l'étape suivante, qui est l'extraction des données . Nous utilisons la bibliothèque tweepy pour extraire les tweets. Si vous ne disposez pas de cette bibliothèque, vous pouvez l'installer en utilisant pip install tweepy dans votre invite de commande.<br/>
> Go to the [Extracting twitter data (tweepy + pandas)](https://github.com/GhadaHirch/-Classification-des-Tweets/blob/master/Extract_Tweets.ipynb)<br>

## 2. Tweets Classification and clustering (Kmeans)<br/>
### 2.1. Data Set:<br/>
Une rapide inspection de la DataSet []() nous permet de voir que la compréhension de certains tweets est difficile même pour des êtres-humains. Le nettoyage sera d’autant plus important.
### 2.2. Preprocessing:<br/>
#### Cleanning Tweets(text):<br/>
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés.Pour cela, on va utiliser NLP.<br/>
En NLP, on commence toujours par construire un pipeline de nettoyage des données "clean_text". Personnellement j’utilise les Reg-ex avec le module Python re qui permettent de faire cela facilement.<br/>
Le nettoyage des tweets comprendra plusieurs choses :<br/>
* Enlever les emojis.<br/>
* Retirer la ponctuation : très facile avec les reg-ex<br/>
* Retirer les caractères spéciaux : très facile avec les reg-ex mais tous les caractères ne seront pas retirés dans un premier temps. Les tweets sont des objets très sales !<br/>
* Retirer les chiffres et l'url(http): avec une Reg-ex aussi<br/>
* Changer les lettres majuscules en minuscules: pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents.<br/>
>##### Ce pipeline nous permet d’avoir des tweets à peu prés propres.<br/>
#### Tokenization, Lemmatization and removing stopwords:<br/>
>* stopwords:<br/>
>Les mots vides sont des mots couramment utilisés dont la présence dans une phrase a moins de poids que d'autres mots. Ils incluent des mots comme «et», «ou», «a».<br/>
>* Tokenization:<br/>
>La tokenisation est le processus de division d'une chaîne en une liste de jetons. Une phrase peut être réduite en mots et un mot peut être réduit en lettres à l'aide des 
tokenizers appropriés.<br/>
>* Lemmatization:<br/>
>La lemmatisation réduit un mot à sa forme racine. Par exemple, la forme de racine des « roches » est « roche ».<br/>
### 2.3. Tweets Classification:<br/>
Cette approche utilise la technique de création d'un ensemble de mots qui peuvent être classés à une catégorie particulière pour chacune des 4 classes. (economic, social, culture et health)<br/>
Les tweets sont chacun comparés aux 4 séries et attribués à un score de similitude. Il existe la similitude Jaccard pour calculer le score de similarité entre les tweets.<br/>
### 2.4. Clustered Data Frame:<br/>
Nous souhaitons créer une Dataframe contenant le nombre total de tweets par catégorie.<br/>
Cela peut être réalisé d'abord en créant un bloc de données contenant les scores Jaccard pour chaque tweet pour chaque catégorie, puis en attribuant un tweet à une catégorie en fonction du score le plus élevé et enfin en regroupant les tweets.<br/>
>##### Après avoir classé les tweets, les sommes sont effectuées dans les catégories par tweet, puis le clustering K Means entre en jeu.
### 2.5. KMeans Clustering:<br/>
La méthode de clustering k-means est une technique d'apprentissage automatique non supervisée utilisée pour identifier des clusters d'objets de données dans un ensemble de données.<br/>
>Go to the []()
