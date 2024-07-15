# Custom Cloud Native Builder

This repository provides a custom Cloud Native Buildpack builder configuration using a `custom_builder.toml` file.
This configuration file specifies the buildpacks to include, the order in which they should be used, and the stack images for both the build and run phases.

## Usage
### Prerequisites

- Docker
- pack CLI

### Steps

1. **Customize the Builder Configuration**

   Update the <path/to/your/buildpack/directory> with the actual path to your buildpack directory and adjust other values as needed.

2. **Create the Builder Image**

   Use the `pack` CLI to create a custom builder image:

   ``pack builder create custom-builder:latest --config custom_builder.toml``

3. **Use the Custom Builder**

    ``pack build my-app --path /path/to/your/application --builder custom-builder:latest``

## Configuration Details

**Buildpacks**: Specifies the buildpacks to include in the builder.<br>
**Order**: Defines the order in which the buildpacks should be applied.<br>
**Build Image**: The image used during the build phase.<br>
**Run Images**: The images used during the run phase, including any mirrors.<br>
**Stack**: Defines the stack, including the build and run images.<br>


By following these steps and guidelines, you should be able to create and use a custom Cloud Native Buildpack builder with ease.



