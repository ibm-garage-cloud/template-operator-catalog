# Operator Catalog template

Template repository for an Operator Lifecycle Manager catalog. The `bundles.txt` will contain a list of operator bundle images that should be included in the operator catalog. Each bundle version will be on its own line. You can manually add images to the bundles file, or better yet, allow the operator build pipeline do it for you each time there is a new release of the operator.

## Getting started

### Update the catalog-source.yaml

After you create a new repository from this template, the first thing to do is update the `deploy/catalog-source.yaml` file. Change the metadata name and the display name to match your catalog. The display name will appear in the operators view in the console with the list of catalogs. The metadata name should be unique and typically will match the name of the repository.

## Building locally

The repository includes a Makefile that can be used to build the bundle. Run `make` or `make build` to kick off the process.

**Note:** The build process depends on the `opm` cli in order to create the catalog image.

