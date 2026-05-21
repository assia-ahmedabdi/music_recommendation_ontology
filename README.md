# 🎵 Semantic Spotify Playlist Recommender

A music recommendation system that suggests personalized Spotify playlists based on your musical taste and the current weather — powered by semantic web technologies and ontology-driven reasoning.

## 📖 Description

This project explores the intersection of **semantic web**, **knowledge graphs**, and **music recommendation**. Rather than relying solely on collaborative filtering or raw statistics, we model musical knowledge explicitly through an ontology, enabling richer, more explainable recommendations.

The system takes two inputs:
- 🎧 **User music preferences** — listening history, favorite genres, artists, and audio features
- 🌤️ **Real-time weather** — temperature, sky conditions, and atmosphere, summarized by day

It then queries the populated ontology to surface the most contextually appropriate Spotify playlist for the moment.

## 🕸️ Semantic Network Schema

![Ontology Schema](ontology_protege/schema.png)

## 🛠️ Technologies

| Layer | Tools |
|---|---|
| **Knowledge Modeling** | [Protégé](https://protege.stanford.edu/) — ontology design (OWL/RDF) |
| **Ontology Population** | [OntoWeaver](https://github.com/ontoweaver) — YAML-driven data-to-ontology mapping |
| **Data Processing** | Python, Pandas — dataset cleaning and preparation |
| **Notebooks** | Google Colab (Jupyter `.ipynb`) |
| **Data Sources** | [Kaggle Spotify dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset), [weather dataset](https://www.visualcrossing.com/weather-history/Paris,%20%C3%8Ele-de-France,%20France/us/last15days/) and listening history dataset from Deezer 

## ⚙️ Process

### 1. 🧠 Ontology Design
The knowledge model is built using **Protégé**. It defines concepts such as `Track`, `Artist`, `Genre`, `Weather`, and the relationships between them (e.g., `has_genre`, `has_acousticness `, `has_weather`).

### 2. 🧹 Data Preparation
Run `Preparation_datasets.ipynb` to clean and format the Spotify and weather datasets into a structure compatible with OntoWeaver's YAML pipeline.

### 3. 🔗 Ontology Population
Run `ontoweaver_python_file.ipynb` to inject the processed data into the ontology using the YAML configuration files located in `ontoweaver/recommendation_system/`. This step produces a fully populated knowledge graph ready for querying.

## 🔭 Future Work

- **Neo4j Integration** — Connect the populated ontology to a Neo4j graph
  database to visualize relationships between artists, genres, playlists,
  and weather conditions, and run Cypher queries to refine recommendations.
- **User Interface** — Build a simple UI where the user inputs their location
  and instantly receives a playlist recommendation.
- **Data Enrichment** — Incorporate additional contextual signals such as
  time of day, self-reported mood, or current activity.

  
## 👥 About

This project was developed as part of an academic exploration of **semantic AI**. It combines our passion for music with curiosity about knowledge representation and intelligent systems.

We chose Spotify's playlist personalization as our use case because it sits at a compelling crossroads: rich semantic data (genres, moods, audio features) meets subjective human experience (taste, context, emotion). Adding **weather as a contextual signal** pushes the system beyond simple preference matching into situational awareness.

The project demonstrates how **ontologies and semantic reasoning** can serve as a transparent, interpretable backbone for recommendation — an alternative to black-box machine learning approaches.

---

## 🏷️ Tags

`spotify` `recommendation-system` `semantic-web` `ontology` `knowledge-graph` `protege` `ontoweaver` `owl` `rdf` `music` `playlist` `weather` `personalization` `python` `google-colab` `ai` `nlp` `data-science` `information-retrieval` `neo4j` `graph-database` `cypher`
