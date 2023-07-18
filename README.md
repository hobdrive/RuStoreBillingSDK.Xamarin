
# RuStore Xamarin binding project

No dependencies included!

Inside of AndroidDependencies run:
    `gradle app:copy_deps`
to resolve and download all the required binaries jars and aars.

Please notice that if your project uses some of the JARs from dependencies - you'll probably
get "Class defined in two places" error during final build.

In that case just remove the jar from this project.

# JAR deps problems / duplicates

Xamarin studio can not derive Packages from inner project.
Probably a bug.
This means for many  dependencies you have to specify packages in your main Xamarin Android App project.
Example working package list is available as an example in this repo `packages.config.example`.
Notice this should be used in your main Xamarin project!

## Some possible conflicting packages

core-1.9.0
core-runtime-2.1.0
tracing-1.0.0
lifecycle-common-2.5.1
constraintlayout-solver-2.0.4.jar

## Packages upgraded from what rustore specifies by default

lifecycle-runtime-ktx-2.5.1.jar
    replacement by lifecycle-common 2.6.1