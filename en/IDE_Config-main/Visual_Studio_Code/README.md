<!-- *************************************************java.json**************************************************** -->
# java.json 

Automatically adds a `main` method with a `String[] args` parameter via snippets when typing 'main' and pressing Tab.

## How to Configure Snippets in VS Code

Follow the steps below to add or modify Java snippets in Visual Studio Code:

1. Go to **File** > **Preferences** > **Configure User Snippets**.
2. Select the **Java** language to begin editing the specific snippet file for this language.
3. Add the code snippet to your file.

<!-- ************************************************** Bar ***************************************************** -->

  <img src="https://github.com/PkLavc/PkLavc/blob/94f67aca0f96f0e9cef748c2c27877c02586f77d/resources/Rainbow.gif" width="100%">
  
<!-- *************************************************settings.json**************************************************** -->
# settings.json

Configuration of the `settings.json` file to customize the development environment, appearance, and behavior of various extensions such as Code Runner.

## Getting Started

To open the `settings.json` file in Visual Studio Code:

1. Go to **Manage** > **Settings** > **Open Settings (JSON)**.

## Detailed Configuration

### User Interface Theme

- `"workbench.colorTheme": "Default Dark Modern"`
  - Sets the color theme for the VS Code user interface. "Default Dark Modern" is applied, modifying the visual appearance of the editor, panels, status bar, and other UI elements to this dark theme.

### File Explorer Behavior

- `"explorer.compactFolders": false`
  - Controls whether the File Explorer should compact folders that contain only one subfolder into a single line. Setting this to `false` means each folder and subfolder is displayed on its own line, making the directory structure easier to view.

### Icon Theme

- `"workbench.iconTheme": "material-icon-theme"`
  - Sets the icon theme for the File Explorer in Visual Studio Code. The "material-icon-theme" provides a set of icons inspired by Material Design, improving visual navigation and intuitiveness.

### Code Execution Settings

- `"code-runner.executorMap":`
  - A specific configuration for the Code Runner extension that allows defining custom commands for executing code in different programming languages.
    - `"python": "clear ; python -u"`
      - Specifies the command to execute Python code. `clear` clears the terminal before running the script, and `python -u` runs the Python script in unbuffered mode, ensuring outputs are promptly displayed.
    - `"java": "clear && javac $fileName && java $fileNameWithoutExt"`
      - For Java, the command clears the terminal (`clear`), compiles the Java file (`javac $fileName`), and runs the compiled code (`java $fileNameWithoutExt`). `$fileName` represents the current file name, and `$fileNameWithoutExt` is the file name without its extension.

### Run in Integrated Terminal

- `"code-runner.runInTerminal": true`
  - This setting allows Code Runner to execute code directly in VS Code's integrated terminal instead of using the default output panel at the bottom. This is beneficial for programs that require interaction during execution or benefit from a full terminal environment.

### Ignore Selection When Running

- `"code-runner.ignoreSelection": true`
  - When enabled, Code Runner will always execute the entire file regardless of any selection. If set to `false`, Code Runner would attempt to execute only the selected code portion.
    
<!-- ************************************************** Bar ***************************************************** -->

  <img src="https://github.com/PkLavc/PkLavc/blob/94f67aca0f96f0e9cef748c2c27877c02586f77d/resources/Rainbow.gif" width="100%">
  
<!-- ****************************************************************************************************************** -->
