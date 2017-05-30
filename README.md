# EPiServerForms_ScriptsSegregation
Segregation of Episerver Forms and javascripts. Some client frameworks (example Vue.js) requires that scripts are not inline in the content.

##Installation
Install Episerver Forms and just copy the folder (/Views/Shared/ElementBlocks) to your Episerver project.

Requires Episerver Forms 4.5.1

1. critical changes: Moving form container init script into client services (at footer)
https://github.com/huilaaja/EPiServerForms_ScriptsSegregation/commit/c575451986c3684c72add71cd1e1c30dec8a7051

2. critical changes: Commenting out paragraph text element block script for placeholder texts
https://github.com/huilaaja/EPiServerForms_ScriptsSegregation/commit/8fe6f394f4a27285df47125edb1238742efc47b3


Unfortunately the second change will disable placeholder text feature from paragraph text element block:
<img src="https://raw.githubusercontent.com/huilaaja/EPiServerForms_ScriptsSegregation/master/images/ParagraphTextPlaceholder.png" alt="Paragraph Text Placeholder" />
