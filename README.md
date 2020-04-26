# Homebrew World
*"The missing Homebrew command"*

Homebrew World keeps track of manually installed formulae, and safely clean orphaned dependencies when they are uninstalled.
## Installation
```
brew tap axesd9/world
```
## Migration Steps
* Create a file which contains all installed formulae
```
brew list > ~/new-world
```
* Edit the file, and keep only the manually installed formulae
* Add all of them to your new world
```
brew world add `cat ~/new-world`
```
* [Clean the world](#manually-clean-orphaned-dependencies)
* Remove the file
```
rm ~/new-world
```
## Basic Usage
### Install a formula, and add it to the world
```
brew world install <formula>
```
### Uninstall a formula, remove it, and automatically clean orphaned dependencies
```
brew world uninstall <formula>
```
### List all formulae around the world
```
brew world list
```
### Add a formula to the world
```
brew world add <formula>
```
### Delete a formula from the world
```
brew world delete <formula>
```
### Manually clean orphaned dependencies
```
brew world clean
```
### Delete all formulae from the world, and reset the first clean flag
```
brew world destroy
```
### Display help information
```
brew world help
```
## Uninstallation
[Destroy the world](#remove-all-formulae-from-the-world), then
```
brew untap axesd9/world
```
