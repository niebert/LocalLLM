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


## Image to 3D Model
Convert an 2D image into a 3D model that students can work on in [Blender](https://www.blender.org/) UTL: https://www.blender.org/.

### AnyDepth2 
Depth map is a 2D image that encodes the depth as 3rd dimension with colors or grey scale image.
* GitHub-URL:  https://github.com/DepthAnything/Depth-Anything-V2
* Interactive Webinterface: https://huggingface.co/spaces/depth-anything/Depth-Anything-V2
