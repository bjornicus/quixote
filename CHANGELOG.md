# Quixote Change Log

Changes are listed by minor version, from newest to oldest. Under each minor version, patches are listed from oldest to newest.


## Work in Progress

*Fixed:*

* ElementEdge.diff() reports correct edge (instead of saying 'top' for everything)


## 0.2: Basic Position Diff

**14 Oct 2014.** The `diff()` call on QElement allows you to check multiple things with call. In this release, it supports the most basic positioning information: the position of the top, right, bottom, and left edge of the element. 

*Breaking changes:*

* quixote.createFrame() and Frame.create() callbacks now pass err as first argument (always null, for now)

*New methods:*

* QElement
  * top, right, bottom, left
  * diff()

*New classes:*

* ElementEdge
  * diff()

*Changed:*

* Frame.create() and quixote.createFrame() return frame immediately. You still need to wait for the callback before using the frame, but it can be convenient in some test runners.

*Fixed:*

* IE 8 workaround: IE 8 includes frame border in position calculations. We now create the test frame with frameborder=0 attribute so IE 8's positions are consistent with other browsers. 


## 0.1: Raw Styles and Positions

**13 Oct 2014.** Basic API for setting up a test frame and getting raw (non cross-browser-compatible) style and positioning information. Minimally viable... but viable.
 
*New modules, classes, and methods:*

* quixote
  * createFrame()
  
* Frame
  * Frame.create()
  * reset()
  * toDomElement()
  * remove()
  * addElement()
  * getElement()
  
* QElement
  * getRawStyle()
  * getRawPosition()
  * toDomElement()
  * toString()
  * equals()
  

## 0.0: Infrastructure

**30 Sept 2014.** Project infrastructure.

Patches:

* *0.0.1, 30 Sept 2014:* Initial build, integration, and release scripts.   
* *0.0.2, 1 Oct 2014:* Release script publishes to npm and GitHub.   
* *0.0.3, 1 Oct 2014:* Final test of release script.
* *0.0.4, 6 Oct 2014:* Placeholder documentation site at quixote-css.com.