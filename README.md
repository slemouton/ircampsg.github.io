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

## code review

etude critique de patches : 

cf https://hal.science/hal-01944619v1

Serge Lemouton, Samuel Goldszmidt. La préservation des œuvres du répertoire IRCAM : Présentation du modèle Sidney et analyse des dispositifs temps réel. Journées d’Informatique musicale, 2016, Albi, France. hal-01944619

collection de patch de tests
(choisis pseudo-aleatoirement dans sidney)

	Work	composer	year	Rim	patch date
	Mantra	stockhausen	1970	puckette	2007
	!Prologue	grisey	1978	daubresse	2012
	Jupiter	manoury	1987	puckette	2011
	Jupiter	manoury	1987	lippe	2011
	Congruences	jarrell	1989	muller	2013
	Spirali	stroppa	1989	lemouton	2014
	Rhizomes	jarrell	1993	hummel	2013
	Alma Luvia	baschet	1993	baschet	2014
	Entsagung	essl	1993	lemouton	2014
	En echo	manoury	1994	stuck	2010
	!Richiamo	fedele	1994	de coudenhove	2013
	Metallics	maresz	1995	lorieux	2012
	!Animus	francesconi	1995	meudic	2014
	Spira Manes	baschet	1995	lemouton	1995
	Spira Manes	baschet	1995	lemouton	1995
	Anthèmes II	boulez	1997	nouno	2013
	Related Rocks	lindberg	1998	lemouton	2014
	!Ballata	francesconi	2002	daubresse	2002
	Noon	manoury	2003	lemouton	2011
	!4th quartet	harvey	2003	nouno	2011
	Filastrocca	baschet	2003	faia	2014
	Swarming essence	fujikura	2006	poletti	2010
	!Wagner Dream	harvey	2007	nouno	2012
	!AnimusII	meudic	2007	francesconi	2013
	!Speakings	harvey	2008	nouno	2011
	!La Muette	baschet	2010	lemouton	2010
	Mimesys	vitoria	2011	vitoria	2011
	!Quartett	francesconi	2011	lemouton	2013
	Foris	cendo	2012	bruckert	2012
	Unendlichkeit	kahn	2012	goepfer	2012
	!Partita II	manoury	2012	lemouton/nouno	2012
	!Germination	herve	2013	lemouton	2010
	!Branenwelten	platz	2013	meier	2013


