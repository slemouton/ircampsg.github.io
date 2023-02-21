# ircampsg.github.io
Ircam Patching Style Guides : guide des bonnes pratiques et outils pour des patches plus durables

Rédaction en cours du guide des bonnes pratiques : 
	
* [document partagé](https://docs.google.com/document/d/1DkeBZTyxq9hNiS9KM6nopzfdL6JkV7vhkxyA8KBNcI0/edit?usp=sharing)
* [slides](https://docs.google.com/presentation/d/e/2PACX-1vRLaxeaecwIzTk74gxoKtkxkjWx4YQ2DmqrLgj_ePM_SKx9xuPnbxP2jZ0YViv1QUaHQfqzNcEjrGc8/pub?start=false&loop=true&delayms=3000) 



# Groupe de travail
## Réunions et compte rendu
### première réunion : 21 fevrier 2023
- présents : Serge, Benjamin et Augustin
- présentation du fonctionnement du groupe de travail :
    - reunions régulières
    - document partagé (lien sur la page du projet)
- page du projet : https://slemouton.github.io/ircampsg.github.io/
- à faire (serge) : diffusion de l'outil "patcher dashboard"
- trouver le nom du groupe de travail ?

## Good Practices

* Documentation is better than no documentation
* Style guides (PEP8 for max?)
* Preserve is good but think about preserving the preservation (metapreservation)
* If you can print it you can keep it
* TDD : use Test Driven Development method
* Impossible rules
	* Don’t use commercial software 
	* Dont use 3rd party externals if not open source
* Open Source is not (necessarily) a guarantee of durability
* If you can, use code : javascript, antescofo, ...

## Tools

* Style guides (PEP8 is also a tool) 
* Proposal for establishing a style guide for max, pd and similar languages 
* Patcher Dashboard : analysing patch content (max package)
* Unit testing
* Database storage and patch distribution system
* Conversion to other audio software environements (max to pd/pd to max) 
* Version tracking (git)
* Validation tools
* Data mining tools (checking all the patchs from sidney, for example ...)
* the reality check project (Miller Puckette/Eric Lindeman) : http://msp.ucsd.edu/tools/reality/

## la contribution de ChatGPT
Max programming style is a programming style commonly used in the Max programming language, which is often used for audio and multimedia programming. Here are some good practices concerning Max programming style:

1. Use clear and descriptive object names: Use object names that clearly describe their function and purpose, so that it is easier for you and others to understand the patch. For example, use [metro] to indicate a metronome object, [gain~] to indicate a gain control object, etc.
1. Keep your patch organized: Use different colors for different types of objects, group objects that are related or part of the same function, and use comments to explain complex sections of your patch.
1. Use subpatches to simplify complex patches: When a section of your patch becomes too complex, you can create a subpatch to simplify it. This helps you to keep your main patch organized and easy to understand.
1. Avoid spaghetti connections: Try to keep your patch connections as simple and direct as possible. Avoid overlapping or crossing connections as much as possible, as it can make it difficult to understand the patch.
1. Use message boxes for communication between objects: Instead of connecting objects directly, use message boxes to send data between objects. This makes it easier to understand the flow of data in your patch.
1. Use abstraction to create reusable code: When you have created a section of patch that you might need to use again in another patch, you can turn it into an abstraction. This way, you can reuse your code and avoid duplicating work.
1. Test your patch regularly: Make sure to test your patch regularly to ensure it is functioning as expected. Try to catch errors early, and debug them systematically to avoid confusion.

These are some good practices that can help you write cleaner, more organized, and more efficient Max patches. Remember, as with any programming language, good programming practices can make your work more efficient, and help you create more complex and sophisticated programs.

