# LocalLLM
This is a repository to support students in running a local Large Language Model for different purpose.

## Code Completion and Programming
The implementation of local code completion requires the following tools:
* Integrated Development Environment - tested [VS Codium](https://vscodium.com/) URL: https://vscodium.com/
* Install Continue locally on your computer (Linux computer) 

```javascript
curl -fsSL https://raw.githubusercontent.com/continuedev/continue/main/extensions/cli/scripts/install.sh | bash
```

* [Continue Plugin](https://docs.continue.dev/ide-extensions/install) for Code completion
    * Installation Continue Extension: https://docs.continue.dev/ide-extensions/install
* local LLM to performing the task of code completion - tests for
   * [Ollama](https://ollama.com/).
     
## Ollama
The following commands are mentioned in the following sections.
* start ollama service on Linux
* stop ollama service on Linux
* list downloaded models
* download/pull a specific model

### Start Ollama service
To start ollama on your Linux machine call the following command to start the ollama server
```sh
ollama serve &
```
### Stop Ollama service
To start ollama on your Linux machine call the following command to stop the ollama server
```sh
sudo systemctl stop ollama.service
```
### List Ollama Models
To list all available (i.e. locally downloaded) LLMs in Ollama on your Linux machine you call the following command
```sh
ollama list
```
### Pull a specific LLM 
To download a specific LLM you can pull the LLM with the following command to your local machine to run offline:
```sh
ollama pull mistral
```
Downloading takes a while ....

## Continue - Code Completion 
Continue.dev is a configurable open-source AI coding assistant that can be run from the console and with an IDE like [VS Codium](https://vscodium.com/).

### Config Files of Continue
On Linux the config file of continue is stored in the subdirectory `.continue` of your home directory. An example `config.yaml` is provided in this repository.
```yaml
ame: Continue Config for Linux
version: 0.0.1
schema: v1
models:
  - name: Codestral
    provider: ollama
    model: codestral:latest
    apiBase: http://localhost:11434
    systemMessage: "provide just the code as source code"
    roles:
      - chat
      - edit
      - apply
      - rerank
      - autocomplete
```

### Call Continue from Shell
To check your installation before calling the code assistant form your IDE you can test Continue with a specific Config.
```sh
cn --config ./continue/config.yaml
```


## Image to 3D Model
Convert an 2D image into a 3D model that students can work on in [Blender](https://www.blender.org/) UTL: https://www.blender.org/.

### AnyDepth2 
Depth map is a 2D image that encodes the depth as 3rd dimension with colors or grey scale image.
* GitHub-URL:  https://github.com/DepthAnything/Depth-Anything-V2
* Interactive Webinterface: https://huggingface.co/spaces/depth-anything/Depth-Anything-V2
* Youtube Video: Blender Depthmap  https://www.youtube.com/watch?v=JJE-byQmfws
