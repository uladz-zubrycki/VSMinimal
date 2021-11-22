# Visual Studio Minimal

Visual Studio 2022 configuration adjustments to get clean visual style and as less bloat as possible. Highly opinionated.
I use it to develop stuff with C#, so it's the only language tested. I use ReSharper so don't need many built-in features.

Visual studio behavior:

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

Syntax highlighting:

A minimalistic setup inspired by https://github.com/tonsky/vscode-theme-alabaster for a light visual studio theme.

Use `Tools` > `Import and export settings` to get it applied. Don't forget to save your current setup before. You will probably need to replace `Theme Id="{Guid}"` to use your current theme id.

Here is how it looks like:
1. Locals and variables are highlighted with blue;
2. Comments are coloured green;
3. Literals and enums are violet;
4. All the rest is black, while keywords are grayed-out a little.

![image](https://user-images.githubusercontent.com/5411526/142902871-6c5b878f-4dbb-4d3c-97f9-3be81bd7e5f7.png)

```
<UserSettings>
    <ApplicationIdentity version="17.0"/>
    <ToolsOptions>
        <ToolsOptionsCategory name="Environment" RegisteredName="Environment"/>
    </ToolsOptions>
    <Category name="Environment_Group" RegisteredName="Environment_Group">
        <Category name="Environment_FontsAndColors" Category="{1EDA5DD4-927A-43a7-810E-7FD247D0DA1D}" Package="{DA9FB551-C724-11d0-AE1F-00A0C90FFFC3}" RegisteredName="Environment_FontsAndColors" PackageName="Visual Studio Environment Package">
            <PropertyValue name="Version">2</PropertyValue>
            <FontsAndColors Version="2.0">
                <Theme Id="{EF6E5404-F4FD-4739-A322-7F31ED787FD2}"/>
                <Categories>
                    <Category GUID="{58E96763-1D3B-4E05-B6BA-FF7115FD0B7B}" FontName="Consolas" FontSize="12" CharSet="1" FontIsDefault="No">
                        <Items>
                            <Item Name="Visible Whitespace" Foreground="0x00E8E8E8" Background="0x01000018" BoldFont="No"/>
                            <Item Name="Indicator Margin" Foreground="0x01000017" Background="0x00F2EEEE" BoldFont="No"/>
                            <Item Name="Inactive Selected Text" Foreground="0x01000017" Background="0x00EADBD3" BoldFont="No"/>
                            <Item Name="Selected Text" Foreground="0x01000017" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="Plain Text" Foreground="0x02000000" Background="0x00F7F7F7" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{E0187991-B458-4F7E-8CA9-42C9A573B56C}" FontName="Consolas" FontSize="12" CharSet="1" FontIsDefault="No">
                        <Items>
                            <Item Name="XML Attribute Value" Foreground="0x02000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XML Attribute" Foreground="0x02000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XML Name" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XML Comment" Foreground="0x00278C44" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XML Delimiter" Foreground="0x02000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XML Keyword" Foreground="0x02000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Markup Extension Parameter Value" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Markup Extension Parameter Name" Foreground="0x02000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Markup Extension Class" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Attribute Value" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Attribute" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Comment" Foreground="0x00278C44" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Delimiter" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="XAML Keyword" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Number" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="String" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Comment" Foreground="0x00278C44" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Keyword" Foreground="0x00494141" Background="0x01000001" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{FF349800-EA43-46C1-8C98-878E78F46501}" FontName="Consolas" FontSize="12" CharSet="1" FontIsDefault="No">
                        <Items>
                            <Item Name="Breakpoint - Mapped (Enabled)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Error Message" Foreground="0x0100000C" Background="0x02000000" BoldFont="No"/>
                            <Item Name="Breakpoint (Enabled)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint - Selected" Foreground="0x00DBFCFF" Background="0x01000018" BoldFont="No"/>
                            <Item Name="Breakpoint (Warning)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint (Error)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Executing Thread IP" Foreground="0x00000000" Background="0x008CF7FF" BoldFont="No"/>
                            <Item Name="Current Statement" Foreground="0x00000000" Background="0x008CF7FF" BoldFont="No"/>
                            <Item Name="Breakpoint - Advanced (Error)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint - Mapped (Error)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint - Mapped (Warning)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint - Advanced (Warning)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Breakpoint - Advanced (Enabled)" Foreground="0x00000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="Track Changes before save" Foreground="0x02000000" Background="0x009CD6FC" BoldFont="No"/>
                            <Item Name="other error" Foreground="0x000000FF" Background="0x01000018" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{FA937F7B-C0D2-46B8-9F10-A7A92642B384}" FontIsDefault="Yes">
                        <Items>
                            <Item Name="Artboard Background" Foreground="0x02000000" Background="0x02000000" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{FC88969A-CBED-4940-8F48-142A503E2381}" FontIsDefault="Yes">
                        <Items>
                            <Item Name="IndicatorText" Foreground="0x00828282" Background="0x01000018" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{B36B0228-DBAD-4DB0-B9C7-2AD3E572010F}" FontName="Segoe UI" FontSize="9" CharSet="1" FontIsDefault="No">
                        <Items>
                            <Item Name="Odd Row Items" Foreground="0x00000000" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Even Row Items" Foreground="0x00000000" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Not Downloaded" Foreground="0x006D6D6D" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Target Only" Foreground="0x00000000" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Source Only" Foreground="0x00000000" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Identical content" Foreground="0x00000000" Background="0x00FFFFFF" BoldFont="No"/>
                            <Item Name="Different content" Foreground="0x000014E5" Background="0x00FFFFFF" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{75A05685-00A8-4DED-BAE5-E7A50BFA929A}" FontName="Consolas" FontSize="12" CharSet="1" FontIsDefault="No">
                        <Items>
                            <Item Name="HTML Tag Delimiter" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Server-Side Script" Foreground="0x00000000" Background="0x00DDDDDD" BoldFont="No"/>
                            <Item Name="HTML Operator" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Entity" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Element Name" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Comment" Foreground="0x00278C44" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Attribute Value" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="HTML Attribute Name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="JSON Property Name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="xml doc comment - text" Foreground="0x006E6E6E" Background="0x01000001" BoldFont="No"/>
                            <Item Name="xml doc comment - entity reference" Foreground="0x006E6E6E" Background="0x01000001" BoldFont="No"/>
                            <Item Name="parameter name" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="local name" Foreground="0x00C05C32" Background="0x01000001" BoldFont="No"/>
                            <Item Name="type parameter name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="struct name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="module name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="interface name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="enum name" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="delegate name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="record struct name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="record class name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="class name" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="keyword - control" Foreground="0x00494141" Background="0x01000001" BoldFont="No"/>
                            <Item Name="string - verbatim" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="RoslynActiveStatementTag" Foreground="0x01000000" Background="0x00EADBD3" BoldFont="No"/>
                            <Item Name="MarkerFormatDefinition/HighlightedWrittenReference" Foreground="0x00000000" Background="0x00EADBD3" BoldFont="No"/>
                            <Item Name="MarkerFormatDefinition/HighlightedDefinition" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="HtmlClientTemplateValueFormatDefinition" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="ReSharper Rearrange Up/Down Code Hint" Foreground="0x00000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="ReSharper Context Exit" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="ReSharper Navigation Highlight" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="ReSharper Read Usage" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="ReSharper Highlight" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="Inactive Selected Text" Foreground="0x01000000" Background="0x00EADBD3" BoldFont="No"/>
                            <Item Name="Selected Text" Foreground="0x01000000" Background="0x00FEDBBF" BoldFont="No"/>
                            <Item Name="urlformat" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Visible Whitespace" Foreground="0x00E8E8E8" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Track Changes before save" Foreground="0x01000000" Background="0x009CD6FC" BoldFont="No"/>
                            <Item Name="Line Number" Foreground="0x00BEC5C0" Background="0x01000001" BoldFont="No"/>
                            <Item Name="other error" Foreground="0x000000FF" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Number" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Type" Foreground="0x00000000" Background="0x01000001" BoldFont="No"/>
                            <Item Name="String" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Literal" Foreground="0x009D3E7A" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Keyword" Foreground="0x00494141" Background="0x01000001" BoldFont="No"/>
                            <Item Name="Comment" Foreground="0x00278C44" Background="0x01000001" BoldFont="No"/>
                            <Item Name="MarkerFormatDefinition/FindHighlight" Foreground="0x01000000" Background="0x005DBCFA" BoldFont="No"/>
                            <Item Name="MarkerFormatDefinition/BreakpointInScrollBar" Foreground="0x01000000" Background="0x00DBFCFF" BoldFont="No"/>
                            <Item Name="XML Doc Comment" Foreground="0x006E6E6E" Background="0x01000001" BoldFont="No"/>
                            <Item Name="MarkerFormatDefinition/HighlightedReference" Foreground="0x01000000" Background="0x00EADBD3" BoldFont="No"/>
                        </Items>
                    </Category>
                    <Category GUID="{1F987C00-E7C4-4869-8A17-23FD602268B0}" FontName="Leelawadee UI" FontSize="10" CharSet="0" FontIsDefault="No">
                        <Items/>
                    </Category>
                </Categories>
            </FontsAndColors>
        </Category>
    </Category>
</UserSettings>
```
