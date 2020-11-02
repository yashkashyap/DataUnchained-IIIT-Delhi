<h1>Data Unchained IIIT Delhi</h1>
<p><i>Participated in a team with Puneet Kumar as <strong>Zindagi Ki Yahi Reet Hai</strong></i></p>
<br>

<h3>Round 1</h3>
<p>The data was already pretty clean, and did not have much to play with. We implemented an ensemble of CatBoost, LightGBM and XGBoost after generating several new features. We stood second on the Private Leaderboard.</p>
<hr>

<h3>Round 2</h3>
<p>We used the roberta-base model from sentence-transformers library to generate the word embeddings. The embeddings along with a few more features were then fed to CatBoost, LightGBM and XGBoost models and the model with the best validation score was used to create the final submission. We bagged 7th position in this round.</p>
<hr>

<h3>Round 3</h3>
<p>This round had a very interesting dataset. The Train, Test and Validation folders further contained several folders named with their respective id's. Each id folder had 8 images and a json file. We were supposed to use all the 8 images together to generate the predictions. Link for the data is <a href="https://drive.google.com/file/d/1p5xIPI2e362RK9wgKP3NOwO4U6hNh2q1/view?usp=sharing">here</a>. Go through the data for a better understanding.</p>
<p>Anyways, to solve this problem, we initially used the DenseNet201 pretrained model to generate features out from each image for an id and the combined them into a numpy array. These features were then made to pass through the GRU layers and the Dense layers. We extracted the ouput from one of the hidden layers and trained them using the CatBoost model to generate out submission file.</p>
<p>We secured 1st position in the final and deciding round.</p>