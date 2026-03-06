# Neos - Ideal project structure

## Neos Package

```filesystem-structure
Vendor.Site:
    |- Documentation/                   # <- Written or generated Documentation
    |- api/                             # <- API definition like OpenAPI docs
    |- Classes/
        |- Service/
        |- Security/
            |- Authentication/
                |- Provider/
                |- Token/
        |- Domain/
            |- Model/                   # <- Database Models
            |- Repository/              # <- Repository for Database Models
            |- Service/
    |- Configuration/
        |- Development                  # <- Context specific configs
        |- Production                   # <- Context specific configs
        Settings.yaml
    |- NodeTypes/                       # <- YAML definitions for NodeTypes
    |- Resources/
        |- Public/
            |- JavaScript/              # <- bundled/compiled JavaScript
            |- Styles/                  # <- bundled/compiled CSS
            |- Assets/                  # <- Icons, Images, maybe Fonts etc. but no Videos
        |- Private/
            |- Fusion/
                |- Module/              # <- For the Neos CMS Backend modules
                    |- <ModuleName>
                        |- Action/
                            |- <ActionName>.fusion
                        |- Component/   
                    |- Routes.fusion
                |- Component/
                |- Root.fusion
    |- composer.json
    |- Readme.md
```
