# .mvn

This directory marks the root of the multi-module build. Maven sets
`maven.multiModuleProjectDirectory` to the nearest ancestor that has a `.mvn` directory, so a module
built from its own directory still finds the repository root, which the book uses to include
listings from the modules' sources and tests.
