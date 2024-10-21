# Example issue with build tool dependencies for swift-java

This repository highlights a bug found with the Swift Package Manager's dependency handling
for build tool plugins. The package doesn't build because the Java2SwiftPlugin isn't seeing
the "JavaKit" dependency of the "JavaMath" target. If we uncomment the marked line in
Package.swift to also add a "JavaKitJar" dependency, we see both the JavaKit and JavaKitJar
dependencies correctly.
