# -Classification-des-Tweets (NLP, Kmeans, Python) 

> #### DESCRIPTION:
• Maitriser l’API de twitter pour l’extraction des tweets<br/>
• Maitriser la partie NLP (natural language processing) avec NLTK en Python<br/>
• Appliquer les principes de nettoyage des données<br/>
• Classer les tweets : regrouper ensemble les tweets qui sont similaires. C’est une étape qui peut
être considérée comme une étape 

# 0. Prerequisite: What will we need?
>1. Environnement:<br/>
Tout d'abord, nous avons besoins de préparer l'environnement du travail.
* [ANACONDA For windows](https://www.anaconda.com/products/individual)
>2. Needed libraries:<br/>
Les exigences que nous devrons installer sont:<br/>
* [NumPy](http://www.numpy.org/): NumPy est une bibliothèque Python utilisée pour travailler avec des tableaux.
Il a également des fonctions pour travailler dans le domaine de l'algèbre linéaire, de la transformée de Fourier et des matrices.
* [Pandas](http://pandas.pydata.org/): Pandas est une bibliothèque Python permettant la manipulation et l'analyse des données.
* [Tweepy](http://www.tweepy.org/): Une bibliothèque Python facile à utiliser pour accéder à l'API Twitter.
* [Matplotlib](http://matplotlib.org/): Matplotlib est une bibliothèque Python destinée à tracer et visualiser des données sous formes de graphiques. Elle peut être combinée avec les bibliothèques python de calcul scientifique NumPy et SciPy.
* [NLTK](https://www.nltk.org//): est une bibliothèque logicielle en Python permettant un traitement automatique des langues.
Maintenant, toutes ces bibliothèques sont installées depuis: !pip install <nom_biblio>

**Now that we have all the requirements, let's get started!**

# 1. Extracting twitter data (tweepy + pandas)<br/>
## Step 1 — How do we get a Twitter Consumer Key and Consumer Secret key?<br/>
Tout d'abord, nous devons créer un compte Twitter et obtenir les informations d'identification nécessaires sur la plateforme de développement Twitter pour accéder à l'API Twitter en suivant ces étapes:<br/>
### Apply for a Developer Account:
* Si vous avez déjà des applications, connectez-vous sur https://apps.twitter.com/ avec votre nom d'utilisateur et votre mot de passe Twitter.Puis accédez à Demander un compte développeur.<br/>
* Si vous n'avez pas d'applications, accédez à demander un compte développeur en connectant sur [How to apply for a Twitter Developer account](https://www.extly.com/docs/autotweetng_joocial/tutorials/how-to-auto-post-from-joomla-to-twitter/apply-for-a-twitter-developer-account/#apply-for-a-developer-account)<br/>
### Get the needed Keys:
Allez dans l'onglet Clés API, nous y trouverons notre clé Consumer et nos clés secrètes Consumer.
## Step 2 — How do we connect to the Twitter API<br/>
Maintenant que nous sommes prêts avec les informations d'identification Twitter requises, passons à l'étape suivante, qui est l'extraction des données . Nous utilisons la bibliothèque tweepy pour extraire les tweets. Si vous ne disposez pas de cette bibliothèque, vous pouvez l'installer en utilisant pip install tweepy dans votre invite de commande.
[Extracting twitter data (tweepy + pandas)](https://github.com/GhadaHirch/-Classification-des-Tweets/blob/master/Extract_Tweets.ipynb)<br>

# 2. Tweets Classification 

> Go back to the [README](https://github.com/RodolfoFerro/pandas_twitter/blob/master/README.md)<br>
> Go next to [1. Extracting twitter data (tweepy + pandas)](https://github.com/RodolfoFerro/pandas_twitter/blob/master/01-extracting-data.md)<br>
