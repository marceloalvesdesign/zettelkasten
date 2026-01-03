---
title: YAML Language Server for Databricks
date: Tue Jul 15 16:27:55 JST 2025
---

Install the `yaml-language-server` (yamlls) for NeoVim.

This is automatically highlight the `databricks.yml` file, but it won't
highlight the pipeline files.

To solve this you can visit the [Schema Store Catalog](https://www.schemastore.org/api/json/catalog.json) and search for
`databricks`. Copy the schema store url and paste the following at the top of
your databricks pipeline file.

```yaml
# yaml-language-server: $schema=https://www.schemastore.org/databricks-asset-bundles.json
```

