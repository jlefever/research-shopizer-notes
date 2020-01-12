# Shopizer

## Top Level Packages

- sm-core
    - 289 Java files
    - Depends on sm-core-models, sm-core-modules
    

- sm-core-model
    - 178 Java files
    - Depends on nothing

- sm-core-modules
    - 14 Java files
    - Depends on sm-core-model
 
- sm-shop
    - 378 Java files
    - Depends on all other packages
    - Contains Java packages `com.salesmanager.shop.*`
        - Contains main method in `ShopApplication`
    - Contains JSPs and static frontend content (HTML, CSS, JS)
    - Contains localization strings
    - Contains config files

- sm-shop-model
    - 226 Java files
    - Depends on sm-core-model