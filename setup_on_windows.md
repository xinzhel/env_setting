* Install WSL 2 (with separate linux kernel) from Microsoft Store
* Install [vscode remote server](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode)
* Install [Window Terminal](https://github.com/microsoft/terminal)
* (Optinal for terminal display) Install [Powerline for Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup)
   * add the following content into bash profile
   ```
      # customize prompt
      GOPATH=$HOME/go
      function _update_ps1() {
                  PS1="$($GOPATH/bin/powerline-go -error $?)"
          }
      if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
                  PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
      fi
      source "$HOME/.cargo/env"
   ```

* Use Cuda
    * [Nvidia use guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html)
    * [Microsoft use guide ](https://docs.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)
    * Note [gaps between WSL 2 and native Linux if you use Cuda-based applications](https://developer.nvidia.com/blog/leveling-up-cuda-performance-on-wsl2-with-new-enhancements/)

BTW, in order to have no reliability of any specific OS beyond programming, I only install common apps with web versions which can be accessed by browsers or all mainstream OS, including
onedrive for file management, Zoom (login), Wechat (login), notion (login).