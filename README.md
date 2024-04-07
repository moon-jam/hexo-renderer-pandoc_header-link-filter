# hexo-renderer-pandoc_header-link-filter

This project provides a Lua filter for [Hexo's Pandoc renderer](https://github.com/hexojs/hexo-renderer-pandoc) to add header links to your files.  

## Usage

1. Download the [`header-link-filter.lua`](./header-link-filter.lua) script from this repository and add it to your Hexo project. We recommend placing it in the `./source/_data` directory for organization, but you can choose a location that suits your project structure.

2. Update your `_config.yml` to include the Lua filter along with other Pandoc arguments. If you placed the `header-link-filter.lua` file in a different location, make sure to update the path accordingly:

```yml
pandoc:
    args:
        - "-f"
        - "markdown"
        - "-t"
        - "html"
        - "--mathjax"
        - '--lua-filter'
        - './source/_data/header-link-filter.lua'
```

## Notes

This filter is an opt-in feature and is not hard-coded into the source code of the hexo-renderer-pandoc plugin. This allows for greater flexibility and customization based on individual project needs.
