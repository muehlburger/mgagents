# MGAgents

Dieses Repository enthält den Code für verschiedene Agenten, die in unterschiedlichen Umgebungen wie Ollama und LM Studio laufen.

## Geplante Agenten

Diese Agenten sind dafür konzipiert, verschiedene Aufgaben zu übernehmen und effizient auf Benutzeranfragen zu reagieren.

### Agentenübersicht

- **Agent A: Benutzeranfragen**
  - **Funktion:** Hauptkontaktpunkt für Benutzeranfragen und Weiterleitung an die entsprechenden Spezialagenten.
  
- **Agent B: Internetrecherche**
  - **Funktion:** Durchsucht das Internet und führt Abfragen durch, um relevante Informationen zu finden.
  
- **Agent C (Caren): Kritische Analyse**
  - **Funktion:** Prüft alle Informationen kritisch auf ihre Richtigkeit und Zuverlässigkeit.
  
- **Agent D: Speech-to-Text**
  - **Funktion:** Wandelt gesprochene Sprache mithilfe der Whisper-Technologie in Text um.
  
- **Agent E: Textzusammenfassungen**
  - **Funktion:** Erstellt Zusammenfassungen von Texten, wie Gesprächsprotokolle und wissenschaftliche Publikationen.
  
- **Agent F: Vector Store (Chroma DB)**
  - **Funktion:** Greift auf eine Vektordatenbank zu, um spezifische Anfragen basierend auf gespeicherten Daten zu beantworten.

## Arbeitsweise der Agenten

Die Agenten arbeiten zusammen, um komplexe Anfragen zu bearbeiten und optimale Ergebnisse zu liefern:

1. **Anfragebearbeitung:** Agent A nimmt die Anfrage entgegen und leitet sie weiter.
2. **Internetrecherche:** Agent B sucht nach externen Informationen.
3. **Kritische Prüfung:** Agent C bewertet die Informationen.
4. **Speech-to-Text:** Agent D wandelt gesprochene Informationen in Text um.
5. **Zusammenfassung:** Agent E fasst relevante Texte zusammen.
6. **Datenbankabfragen:** Agent F beantwortet Anfragen basierend auf der Vektordatenbank.

## Installation

### Ollama

1. Lade Ollama von [ollama.com](https://ollama.com/download) herunter und installiere es.
2. Ändere den Speicherort der Ollama-Modelle, wie im [FAQ](https://github.com/ollama/ollama/blob/main/docs/faq.md#how-do-i-set-them-to-a-different-location) beschrieben.

### LM Studio

1. Lade LM Studio von [lmstudio.ai](https://lmstudio.ai) herunter und installiere es.

### Autogen Studio

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

Starte die Autogen Studio UI auf Port 8081:
```sh
autogenstudio ui --port 8081
```

## Konfiguration von Autogen Studio für Ollama-Modelle

Installiere verschiedene lokale LLMs mit:
```sh
ollama pull phi3
```

Verfügbare Modelle findest du in der [Ollama Bibliothek](https://ollama.com/library). Beispielkonfiguration für das "phi3"-Modell:

- **Modellname:** phi3
- **API-Schlüssel:** ollama
- **Basis-URL:** `http://localhost:11434/v1`

## Tipps & Tricks

Dieses [Video](https://www.youtube.com/watch?v=lRu_-yFY-4M&t=333s) zeigt, wie man ChatGPT nutzen kann, um Ollama Studio Skills zu schreiben.