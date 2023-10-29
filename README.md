
# **Examen de Deep learning**

## **Sujet: Reconnaissance Automatique de la Parole (ASR) et Analyse de Sentiment**

### **Parte 1 : Mise en place d’un modèle ASR (transcription)**

Pour construire notre modèle ASR, nous avons choisi **de fine-tuner notre modèle à partir d’un modèle pré-entrainé (Transformers)**.

La démarche suivie est la suivante :

>- Importer les librairies nécessaires

>- Charger notre notre dataset  à partir de `"mozilla-foundation/common_voice_11_0"`

>- Charger le modèle pré-entrainé "openai/whisper-small"

> - Effectuer un data processing en faisant du feature extractor sur les audios reçus en entrées.

> - Entrainer notre modèle sur note dataset : en évaluant la performance et en ajustant les valeurs de nos hyper-paramètres

> - Pusher le modèle entrainer sur huggingface

Pour plus détails sur le code, se référer au notebook :
`ASR_FineTune_Transcription_KOULARAMBAYE_TONEDEAG.ipynb`

> Le modèle a été pusher sur huggingface à l’adresse : [https://huggingface.co/etonkou/whisper-small-fr](https://huggingface.co/etonkou/whisper-small-fr)

#

### **Parte 2 : Mise en place d’un modèle transcription**

La démarche suivante a été utilisée pour construire notre modèle d’analyse de sentiment :

> - Importer les librairies nécessaires

> - Charger notre notre dataset (pris sur Kaggle)

> - Faire un pre-processing sur notre dataset (supprimer les colonnes initules etc..)

> - Charger le modèle pré-entrainé BERT "bert-base-uncased" avec son tokenizer

> - Transformer notre input dataset en un format approprié pour l’entrainement. (Special tokens: classifier[CLS] , separator[SEP], padding [PAD] ).

> - Passer les données transformées au modèle BERT et commencer l’entrainement.

Pour plus détails sur le code, se référer au notebook : `TextClassification_KOULARAMBAYE_Tonedeag.ipynb`
