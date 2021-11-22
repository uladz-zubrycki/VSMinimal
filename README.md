# Visual Studio Minimal

Visual Studio 2022 configuration adjustments to get clean visual style and as less bloat as possible. Highly opinionated.
I use it to develop stuff with C#, so it's the only language tested. I use ReSharper so don't need many built-in features.

### Visual studio look and behavior:

1. Disable file hierarchy (types, members, etc) in solution explorer:

    `Computer\HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\<version>_<id>` `DWORD UseSolutionNavigatorGraphProvider=0`  
2. `Tools`>`Environment`>`General` `On startup, open` choose `Show empty environment`;
3. `Tools`>`Environment`>`Tabs and Windows`>`Preview Tab` uncheck root `Allow new files to be opened in the Preview tab`;
4. `Tools`>`Customize`>`Toolbars` uncheck everything;
5. `Tools`>`Customize`>`Commands` remove ones you don't use;
6. `Tools`>`Options` `Source Control`>`Plug-in Selection` set to `None` to remove source control integration;
7. `Tools`>`Options` `Text Editor`>`General` uncheck `Track changes` to remove scroll bar marks for changed/deleted/inserted lines;
8. `Tools`>`Options` `Text Editor`>`All languages`>`Code lens` uncheck `Enable Code Lens` to disable annotations like usages count and source control history rendered near code symbols; 
9. `Tools`>`Options` `Text Editor`>`All languages`>`Scroll bars` uncheck everything, but `Show errors` under `Show annotations over vertical scroll bar`;
10. `Tools`>`Options` `Text Editor`>`All languages` check `Line numbers`;
11. `Tools`>`Options` `Text Editor`>`All languages` uncheck `Enable single click URL navigation` to make urls non clickable and without noisy styling;
12. `Tools`>`Options` `Text Editor`>`All languages` uncheck `Navigation bar` to gemove members dropdown in the top of open tab;
13. `Tools`>`Options`>`Intellicode` disable everything;
14. `Tools`>`Options` `Projects and Solutions`>`General` uncheck `Reopen documents on solution load`;
15. `Tools`>`Options` `Projects and Solutions`>`General` uncheck `Restore solution explorer project hierarchy state on solution load`;

### CSharp Syntax highlighting:

A minimalistic setup inspired by https://github.com/tonsky/vscode-theme-alabaster for a light visual studio theme.

Here is how it looks like:
1. Locals and variables are highlighted with blue;
2. Comments are coloured green;
3. Literals and enums are violet;
4. All the rest is black, while keywords are grayed-out a little.

![image](https://user-images.githubusercontent.com/5411526/142902871-6c5b878f-4dbb-4d3c-97f9-3be81bd7e5f7.png)

Use `Tools` > `Import and export settings` to get it applied. Don't forget to save your current setup before. You will probably need to replace `Theme Id="{Guid}"` to use your current theme id.

`fonts_colors-2022.vssettings` is the file to export.
