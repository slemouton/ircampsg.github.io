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


|N  |Work            |composer   |year|Rim           |patch date|Sidney Version|Patch                         |software |evenements           |TRoverSF|AudioFiles(Mo)|comments    |
|---|----------------|-----------|----|--------------|----------|--------------|------------------------------|---------|---------------------|--------|--------------|------------|
|   |Mantra          |stockhausen|1970|puckette      |2007      |              |mantra-2013.pd                |Pure Data|patch (message boxes)|90      |0             |            |
|   |Mantra          |stockhausen|1970|              |          |              |                              |??       |                     |100     |0             |            |
|01 |Prologue        |grisey     |1978|daubresse     |2012      |?             |*prologue-concert             |Max 6    |no                   |100     |0             |            |
|   |Jupiter         |manoury    |1987|puckette      |2011      |              |jupiter2011-puredata          |Pure Data|                     |        |              |            |
|02 |Jupiter         |manoury    |1987|lippe         |2011      |              |Jupiter2011-luxembourg-max4   |Max 4    |detonate+qlist       |95      |1             |            |
|03 |Congruences     |jarrell    |1989|muller        |2013      |725           |Congruences_2013_doc          |Max 6    |                     |90      |2800          |kontakte    |
|04 |Spirali         |stroppa    |1989|lemouton      |2014      |734           |Spirali_4LSp_66B_MIRA         |Max 6    |                     |100     |0             |            |
|05 |Rhizomes        |jarrell    |1993|hummel        |2013      |              |2013_Rhizomes-05-venise_faders|Max 5    |antescofo            |92      |14            |            |
|06 |Alma Luvia      |baschet    |1993|baschet       |2014      |774           |AlmaLuvia.2014                |Max 6    |                     |50      |65            |            |
|07 |Entsagung       |essl       |1993|lemouton      |2014      |              |Entsagung_Mac-3-2014          |         |                     |0       |224           |            |
|08 |En echo         |manoury    |1994|stuck         |2010      |              |EN_ECHO.19-2010               |Max 5    |f9+qlist             |97      |3             |            |
|09 |Richiamo        |fedele     |1994|de coudenhove |2013      |              |Richiamo2013                  |Max 6    |detonate+qlist       |0       |400           |            |
|10 |Metallics       |maresz     |1995|lorieux       |2012      |604           |Metallics-bande-patch         |Max 6    |no                   |0       |290           |            |
|11 |Animus          |francesconi|1995|meudic        |2014      |727           | Animus-2013                  |Max 6    |patch (message boxes)|92      |30            |            |
|12 |Spira Manes     |baschet    |1995|lemouton      |1995      |              |ULYSSE-controls-82-2014       |         |                     |55      |105           |            |
|12b|Spira Manes     |baschet    |1995|lemouton      |1995      |              |ULYSSE-DSP-52-2014            |         |                     |55      |105           |            |
|13 |Anthèmes II     |boulez     |1997|nouno         |2013      |27            |Anthèmes2_MMXI_55_6r          |Max 6    |antescofo            |95      |40            |            |
|14 |Related Rocks   |lindberg   |1998|lemouton      |2014      |711           |RelatedRocksSamplors-v4-venise|         |                     |100     |30            |            |
|15 |Ballata         |francesconi|2002|daubresse     |2002      |              | Ballata-max6                 |Max 6    |patch (message boxes)|25      |460           |            |
|16 |noon            |manoury    |2003|lemouton      |2011      |              |NOON                          |Max 5    |detonate+qlist       |80      |250           |            |
|17 |4th quartet     |harvey     |2003|nouno         |2011      |              | String_Quartet_93_all_6r     |Max 5    |qlist                |95      |60            |            |
|18 |Filastrocca     |baschet    |2003|faia          |2014      |777           |***filastrocca2014            |Max 6    |qlist                |50      |480           |            |
|19 |Swarming essence|fujikura   |2006|poletti       |2010      |296           |SwarmingEssence2010-04        |Max 5    |coll                 |10      |585           |            |
|20 |Wagner Dream    |harvey     |2007|nouno         |2012      |630           | Wagner Dream 171 Glasgow     |Max 5    |qlist                |70      |1000          |            |
|20b|Wagner Dream    |harvey     |2007|nouno         |2012      |630           | Wagner Dream Sampler 22(fr)  |Max 5    |                     |70      |              |            |
|21 |AnimusII        |meudic     |2007|francesconi   |2013      |728           |animusII                      |Max 6    |coll                 |50      |1600          |            |
|22 |Speakings       |harvey     |2008|nouno         |2011      |              | Speakings2012 68             |Max 5    |antescofo            |70      |220           |            |
|22b|Speakings       |harvey     |2008|nouno         |2011      |              | Speakings_formantize_17      |Max 5    |                     |75      |              |            |
|23 |La Muette       |baschet    |2010|lemouton      |2010      |              | laMuette20                   |Max 6    |pattr                |40      |1500          |            |
|24 |Mimesys         |vitoria    |2011|vitoria       |2011      |              |00-concert-patch-00           |Max 5    |pattr                |45      |180           |            |
|25 |Quartett        |francesconi|2011|lemouton      |2013      |              | quartett-70-Lille            |Max 6    |antescofo            |40      |2600          |            |
|26 |Foris           |cendo      |2012|bruckert      |2012      |850           |_Cendo_ForisV4_MANIFESTE      |Max 5    |qlist                |45      |500           |jamoma      |
|27 |Unendlichkeit   |kahn       |2012|goepfer       |2012      |582           |0-DSP-2b                      |Max 6    |antescofo            |50      |230           |            |
|28b|Partita II      |manoury    |2012|lemouton/nouno|2012      |              | P2_spat_01                   |Max 6    |                     |50      |              |            |
|28c|Partita II      |manoury    |2012|lemouton/nouno|2012      |              | P2_string-02                 |Max 6    |                     |50      |              |            |
|28d|Partita II      |manoury    |2012|lemouton/nouno|2012      |              | P2_synful-00                 |Max 6    |                     |50      |              |            |
|28 |Partita II      |manoury    |2012|lemouton/nouno|2012      |              | Partita-Deux-+3FC-15-2014    |Max 6    |antescofo            |95      |130           |            |
|29 |germinations    |herve      |2013|lemouton      |2010      |673           | germinations-ESPRO-12        |Max 6    |pattr                |20      |880           |            |
|30 |Branenwelten 6  |platz      |2013|meier         |2013      |641           |_branenwelten6-scofo          |MAX+Live |antescofo            |40      |950           |Ableton Live|
|31 |double bind     |chin       |2007|meudic        |2007      |717           |double-bind2013               |Max 6    |qlist                |75      |70            |            |
|10b|Metallics       |maresz     |1995|meudic        |2014      |              |140922_MetalX-2014            |Max 6    |                     |50      |              |            |
|32 |l’evanoui       |levinas    |2009|meudic        |2009      |713           |evanoui                       |Max 6    |qlist                |20      |500           |            |
|32b|l’evanoui       |levinas    |2009|meudic        |2009      |713           |microton                      |Max 6    |                     |20      |600           |            |
|33 |Tesla           |blondeau   |2014|blondeau      |2014      |              |Tesla_Patch_vSolo             |Max 6    |antescofo            |90      |700           |csound      |
