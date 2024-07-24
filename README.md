# MGAgents

Dieses Repository enthält Code für verschiedene Agents. Wir nutzen verschiedene Umgebungen, um Lokale Sprachmodelle (LLMs) auszuführen, wie Ollama und LM Studio.

## Installation

### Ollama

Lade Ollama von [ollama.com](https://ollama.com/download) herunter und installiere es.

#### Ollama Models Ordner ändern

Im [FAQ](https://github.com/ollama/ollama/blob/main/docs/faq.md#how-do-i-set-them-to-a-different-location) wird beschrieben, wie man mittels Umgebungsvariablen den Speicherort von Ollama Models ändert.

### LM Studio

Lade LM Studio von [lmstudio.ai](https://lmstudio.ai) herunter und installiere es.

### Autogen Studio

Autogen Studio kann über pip in einer neuen Conda-Umgebung installiert werden. Folge diesen Schritten:

1. Erstelle eine neue Conda-Umgebung:
    ```sh
    conda create -n autogenstudio python=3.11
    ```

2. Aktiviere die Umgebung:
    ```sh
    conda activate autogenstudio
    ```

3. Installiere Autogen Studio:
    ```sh
    pip install autogenstudio
    ```

## Verwendung

Um die Autogen Studio UI auf Port 8081 zu starten, führe folgenden Befehl aus:
```sh
autogenstudio ui --port 8081
```

## Konfiguration von Autogen Studio für Ollama-Modelle (z.B. phi3)

Du kannst verschiedene lokale LLMs installieren mit:
```sh
ollama pull phi3
```

Verfügbare Modelle findest du in der [Ollama Bibliothek](https://ollama.com/library). In diesem Beispiel verwenden wir das "phi3"-Modell.

### Konfigurationsdetails:

- Modellname: phi3
- API-Schlüssel: ollama
- Basis-URL: `http://localhost:11434/v1`

## Tips & Tricks

- Dieses [Video](https://www.youtube.com/watch?v=lRu_-yFY-4M&t=333s) zeigt, wie man ChatGPT dazu nutzen kann, um Ollama Studio Skills zu schreiben.