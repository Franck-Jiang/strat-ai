# Projet LLM Strat-ai


# Introduction

Ce projet vise à développer un assistant/chatbot basé sur un modèle GPT-2 instruction-fine-tuned, augmenté par un Retrieval-Augmented Generation (RAG). L'objectif est de permettre à l'assistant de fournir des réponses précises et pertinentes en exploitant un inventaire de jeux de société, comme par exemple des propositions de jeux en fonction du nombre de joueurs, du temps disponible ou des jeux préférés de chacun.

# Objectif

 L'intégration d'un RAG permet de combler les lacunes des modèles génératifs en leur donnant accès à des bases de connaissances spécifiques. Dans ce projet, nous avons appliqué cette approche à un inventaire de jeux de société afin que l'assistant puisse :
Recommander des jeux en fonction des préférences utilisateur.
Fournir des règles de jeu et des conseils stratégiques.
Comparer différents jeux selon divers critères (durée, nombre de joueurs, complexité, thématique).

# Modèles et implémentation

# Modèle de Base

Le projet repose sur GPT-2, un modèle de langage pré-entraîné lors des labs précédents, qui a été fine-tuné sur un ensemble de paires <instruction, réponse> pour améliorer sa capacité à suivre des consignes spécifiques propre aux jeux de société, comme le nombre de joueurs, le genre etc...

# Intégration du RAG

Le RAG combine un module de recherche documentaire avec le modèle génératif.

# Préparation des Données

Les données ont été recueillies à partir de l’inventaire des jeux présents au Club Strat’, formant ainsi un fichier csv comptant un peu plus de 220 jeux recensé.
Nous avons alors renseigné le nom du jeu, le nombre de joueurs et la durée moyenne d’une partie (variable qualitative : court, moyen, long). En ce qui concerne l’attribution des genres, nous avons utilisé ChatGPT pour compléter les informations manquantes. 
A partir de ces données, nous avons réalisé un script pour générer des prompts types qui nous serviront pour le RAG de notre chatbot/assistant.
Par exemple : Instruction : "Quels jeux de stratégie recommandez-vous pour 4 joueurs ?" Réponse : "D'après notre base de données, voici quelques recommandations : Terraforming Mars, Scythe, et 7 Wonders."

# Résultats & améliorations possibles

L'assistant a été testé sur divers scénarios d'utilisation. Les métriques utilisées incluent

# Conclusion

Ce projet a montré que l'intégration d'un RAG améliore significativement la qualité de la réponse de chatbot de conseil de jeu. Pour améliorer le modèle, on pourrait détailler les caractéristiques des jeux dans les données afin d’affiner les recommandations..

