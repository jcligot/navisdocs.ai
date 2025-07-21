Voici un modèle d’amélioration pour le README.md de ton projet, selon les standards GitHub :

---

# navisdocs.ai

## Description

Mise en œuvre d’un système de recherche neurale de nouvelle génération avec ColBERT (interaction tardive) et Vespa, intégré à Paperless-ngx AI et Ollama/vllm pour les modèles LLM sur CPU, via Docker Compose.

## Sommaire

- [Introduction](#introduction)
- [Architecture](#architecture)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Exemples](#exemples)
- [Configuration](#configuration)
- [Dépendances](#dépendances)
- [Licence](#licence)
- [Contributeurs](#contributeurs)
- [Sources](#sources)

---

## Introduction

*(Résumé du contexte, innovation, objectifs du projet)*

## Architecture

```mermaid
graph TD;
    Utilisateur["Utilisateur"] -->|"Etape 1 : Requête"| Intermediaire;
    Intermediaire["Service Intermédiaire (Orchestration RAG)"] -->|"Etape 2 : Extraction"| Paperless;
    Paperless["Paperless-ngx AI"] -->|"Etape 3 : Documents et Métadonnées"| Intermediaire;
    Intermediaire -->|"Etape 4 : Génération Embeddings"| ColBERT;
    ColBERT["ColBERT"] -->|"Etape 5 : Stockage Embeddings"| Vespa;
    Intermediaire -->|"Etape 6 : Recherche sémantique"| Vespa;
    Vespa["Vespa"] -->|"Etape 7 : Documents pertinents"| Intermediaire;
    Intermediaire -->|"Etape 8 : Contexte et Requête"| Ollama;
    Ollama["Ollama LLM"] -->|"Etape 9 : Réponse générée"| Intermediaire;
    Intermediaire -->|"Etape 10 : Réponse finale"| Utilisateur;