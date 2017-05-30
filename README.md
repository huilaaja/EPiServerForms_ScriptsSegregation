# EPiServer.Forms Scripts Segregation from form element templates

Some client frameworks (example Vue.js) requires that scripts and html are segregated. So the __javascripts should not be inline__ in the content (alias html-template).

These changes will relocate the javascripts to be loaded in footer instead of middle of html.
Javascrips will be rendered with following command: @Html.RequiredClientResources("Footer")

### Installation

Install Episerver Forms and just copy the folder (/Views/Shared/ElementBlocks) to your Episerver project and place the client resources (@Html.RequiredClientResources("Footer")) at the end of your layout file.

### Requirements and Changes

Requires Episerver Forms 4.5.1

1. critical changes: Moving form container init script into client services (at footer)
https://github.com/huilaaja/EPiServerForms_ScriptsSegregation/commit/c575451986c3684c72add71cd1e1c30dec8a7051

2. critical changes: Commenting out paragraph text element block script for placeholder texts
https://github.com/huilaaja/EPiServerForms_ScriptsSegregation/commit/8fe6f394f4a27285df47125edb1238742efc47b3


### Known issues

Unfortunately the second change will __disable__ placeholder text feature from paragraph text element block:
<img src="https://raw.githubusercontent.com/huilaaja/EPiServerForms_ScriptsSegregation/master/images/ParagraphTextPlaceholder.png" alt="Paragraph Text Placeholder" />

