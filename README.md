> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# Next.js for Platform.sh

This template builds a simple application using the Next.js web framework. It includes a minimal application skeleton that demonstrates how to set up an optimized build using Next.js and Yarn, as well as how to begin defining individual pages (such as the `/api/hello`) endpoint that comes pre-defined with this template.

Next.js is an open-source web framework written for Javascript.

## Features

* Node.js 14
* Automatic TLS certificates
* yarn-based build

## Customizations

The following files and additions make the framework work on Platform.sh, modified from the `npx` command [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.
* An additional module, [`config-reader-nodejs`](https://github.com/platformsh/config-reader-nodejs), has been added.  It provides convenience wrappers for accessing the Platform.sh environment variables.
* A `handle_mounts.sh` script has been added. This script handles committed files pushed to directories also defined as mounts on Platform.sh.

## References

* [Next.js](https://nextjs.org/)
* [Node.js on Platform.sh](https://docs.platform.sh/languages/nodejs.html)
