
<!-- Project Logo --> <p align="center">  </p> <!-- Project Title --> <h1 align="center">KomorebiRex 🌄</h1> <!-- Project Description --> <p align="center"> Welcome to KomorebiRex, a powerful recommendation engine application that uses user-based, product-based, and hybrid filtering techniques to provide personalized recommendations from the Superstore dataset. </p> <!-- Table of Contents -->

## Table of Contents

-   [Features](#features)
-   [Demo](#demo)
-   [Installation](#installation)
-   [Usage](#usage)
-   [Feedback](#feedback)
-   [Dataset](#dataset)
-   [Contributing](#contributing)
-   [Authors](#authors)
-   [License](#license)

<!-- Features Section -->

## Features

-   **User-Based Filtering:**
    
    -   Fetch personalized recommendations for a specific user.
    -   Select a user from a dropdown menu or type the user's name for recommendations.
-   **Product-Based Filtering:**
    
    -   Obtain content-based recommendations for a specific product.
    -   Input the product name to view relevant recommendations based on product features.
-   **Hybrid Filtering:**
    
    -   Combine user-based and content-based filtering for hybrid recommendations.
    -   Choose a user and product to generate personalized hybrid recommendations.
-   **Interactive Feedback (Hybrid Mode):**
    
    -   Provide feedback by discarding recommended items.
    -   Discarded items won't be recommended to the selected user in future sessions.

<!-- Demo Section -->

## Demo

- **User-Based Menu:**
	![usrbsd](https://i.postimg.cc/L68mbyDd/ezgif-3-39d5206b12.gif)
- **Product-Based Menu:**
		![enter image description here](https://i.postimg.cc/2yB7kdFC/ezgif-3-bd2f740e18.gif)
- **Hybrid Menu:**
	![enter image description here](https://i.postimg.cc/DZ8Sqxrk/ezgif-3-004b5ed7b5.gif)
<!-- Installation Section -->

## Installation

1.  **Clone the repository:**
    
    ```bash
    git clone https://github.com/akshay-rf/KomorebiRex.git
    ```
2.   **Install dependencies:**
	    ```bash 
	    pip install -r requirements.txt 
	    ```
    

<!-- Usage Section -->

## Usage

1.  **Run the application:**
    
    ```bash 
    streamlit run .\main.py
    ``` 
    
2.  **Access the application:** Open a web browser and navigate to `http://localhost:8501` to use KomorebiRex.
    

<!-- Feedback Section -->

## SVD Model
- #### SVD (Singular Value Decomposition), model based approach:
	- This algorithm takes a matrix factorization approach. The user-product rating matrix is factorized into smaller dimension user & item matrices consisting of latent factors (hidden characteristics). By default, number of latent factors is 100. These latent factors are able to capture the known user-item rating preference & in the process are able to predict an estimated rating for all user-item pair where user has not yet rated an item
- #### Hyperparameter tuning with GridSearchCV:
	-   Post Hyperparameter Tuning with GridSearchCV,  the best parameters are found to be different for MAE & RMSE metrics
	-   'n_factors':50, 'n_epochs':10, 'lr_all':0.005 & 'reg_all': 0.2 have been chosen for building recommendations
- #### Model Metrics:
	```
	Unbiased Testing Performance

	MAE: 1.2182
	RMSE: 2.4628
	MAE: 1.2181591303900143, RMSE: 2.4628053726737846
	```
	- The MAE & RMSE metrics for testset are comparable with what was obtained using cross validation & hyperparameter tuning stages with trainset.

	- Chosen model hence, generalizes well.

<!-- Dataset Section -->

## Dataset

The [Superstore](https://uploadnow.io/f/fNQgghb) dataset contains sales data across various product categories and regions. KomorebiRex leverages this dataset to provide insightful recommendations based on user preferences and product features.

<!-- Contributing Section -->

## Contributing

Contributions to KomorebiRex are welcome! If you have ideas, bug fixes, or feature requests, feel free to open an issue or submit a pull request.

<!-- Authors Section -->

## Authors

-   Akshay Mano R F ([@akshay-rf](https://github.com/akshay-rf))
-   Rohit Dharmavaram ([@rohit-d](https://github.com/RohitD1207))

<!-- License Section -->

## License

This project is licensed under the [MIT License](https://github.com/akshay-rf/KomorebiRex/blob/main/LICENSE).
