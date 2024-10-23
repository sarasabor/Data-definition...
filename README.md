# Data-definition...

Pour créer le modèle relationnel avec les tables Customer, Product, et Orders en utilisant SQL, ainsi que pour ajouter les colonnes demandées, voici les instructions SQL appropriées :

Création des tables```sqlCREATE TABLE Customer (
Customer_id VARCHAR2(20) PRIMARY KEY,
Customer_Name VARCHAR2(20) NOT NULL,
Customer_Tel NUMBER);

CREATE TABLE Product (
Product_id VARCHAR2(20) PRIMARY KEY,
Product_Name VARCHAR2(20) NOT NULL,
Price NUMBER CHECK (Price >0)
);

CREATE TABLE Orders (
Customer_id VARCHAR2(20),
Product_id VARCHAR2(20),
Quantity NUMBER,
Total_amount NUMBER,
FOREIGN KEY (Customer_id) REFERENCES Customer(Customer_id),
FOREIGN KEY (Product_id) REFERENCES Product(Product_id)
);



sql
### Ajout des colonnesPour ajouter la colonne `Catégorie` à la table `Product` et la colonne `Date de commande` à la table `Orders`, vous pouvez utiliser les commandes suivantes :  

```sql-- Ajouter une colonne Catégorie à la table ProductALTER TABLE ProductADD Category VARCHAR2(20);  

-- Ajouter une colonne Date de commande à la table OrdersALTER TABLE OrdersADD Order_Date DATE DEFAULT SYSDATE;


Ces instructions SQL vont créer les tables avec leurs contraintes respectives, puis ajouter les nouvelles colonnes comme spécifié.
