prendre une serviette
## SUPERVISÉ 
- data augmentation like crop etc… 
- ESSAYER POUR CNN 
- learning curve 
- essayer data augmentation avec un SNN
- rajouter les premieres features des umap et t-sne 
- regarder tips and tricks feature engineering. 
- regarder le kurtosis et la skewness comme dans la notebook kaggle. 
- essayer de stacker plusieurs datasets qui n’ont pas les memes provenances, comme CNN 
- avec fcnn, xgboost, Knn … 
- regarder exploratory data analysis
- regarder autoML

## NON SUPERVISÉ: 

- Kernel PCA UMAP, t-SNE, ACP, clustering avec K-means et Shared-Nearest-Neighbor
- Monte Carlo VAE ? 

## A FAIRE 
- BFEM pour clustering 
- pour le CNN avec image transformation, regarder si on peut pas ajouter les PCs 3,4 et 5,6 et + ??! 
- Regarder data augmentation for supervisés data.
- How pyraug deals with y ? Peut être qu'en classification c'est plus simple … 
- regarder pour regression
- SEMI-supervised learning !
- Voting papier neurips 
- Faire un repo github ou mettre les données 
- LSTM 
- data visualization 
- feature engineering 
- faire un truc qui permet de sauvegarder directement les datasets et leur résultat 
- pytorch lightning
- Tester GPU
- Re regarder les vidéos de ML machine learnia

[https://www.kaggle.com/c/tabular-playground-series-oct-2021](https://www.kaggle.com/c/tabular-playground-series-oct-2021)

- Regarder la skewness, kurtosis du dataset avec le notebook kaggle. regarder le coeff de Spearman and pearson.

  

## A PENSER 

- Regarder la skewness, kurtosis du dataset avec le notebook kaggle. regarder le coeff de Spearman and pearson.
- PolynomialFeatures après avoir normalisé. Par bloc car sinon trop de variables 
- Regarder Quantile Transformer, powerTransformer. Fait pour normaliser les données ! 

## PREPROCESSING
- Normaliser: 
	- Robust scaler
	- Standard Scaler
	- MinMaxScaler
- go to kaggle if no idea
  

- enlever outliers
- essayer les xgboost, CNN tout ca après réduction de dimension avec UMAP, t-SNE et ACP. 
- Rajouter les features des clusterings comme one-hot encoder pour avoir un feature en plus
- Regarder score et distribution des erreurs 
[https://www.kaggle.com/c/tabular-playground-series-oct-2021](https://www.kaggle.com/c/tabular-playground-series-oct-2021)
- GAN ? Mais comment trouver le y ? 
- Faire de la data augmentation avec le VAE 
- BFEM pour clustering 
  

## TRANSFORMATION des données 

- prendre le log, prendre la valeur absolue, le carré, la racine carré …
- Prendre moins de points ou alors des plus petits points sinon on voit pas les données  

## FEATURE ENGINEERING

- Bucketing
- crossing
- mutliplier des variables entre elle, dont une au carré par ex. 
- diviser des variables ! 
- regarder les features correlées et essayer de les combiner
- regarder la définition des features. 
- diviser par cluster par ex. 
- regarder des clusters sur des sous ensembles de données. 
- normalize by the sum to get percentage. What features could be better with percentage ? 
- possible to add some features. For example, add all the feature that have only positive values ! or only negative values. 

- ne pas renormaliser les donées que l’on divise par cluster
- take the root or log of only positive or only negative values. 
- minus the absolute value. absolute value is for feature where their magnitures are important. 
- faire un algo qui detecte créé toutes les features et accepte que les bonnes. 
- regarder ou on se trompe beaucoup, et essayer de séparer ceux ou on se trompe pour ensuite le donner en feature. 

  

  

## DATA EXPLORATION

- table statistics summary
- univariate decision trees
- Identify interaction terms
- calculate scaling options
- histogram plots
- colinearity testing
- sign-off 
- regarder tips and tricks
- faire une feature de si on est plus dans l’indice ou si on vient de rentrer dedans
- elever les outliers