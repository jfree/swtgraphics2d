SWTGraphics2D
=============

Version 1.0 - 20 February 2016.

(C)opyright 2006-2021, by Object Refinery Limited and Contributors.  All rights reserved.

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.jfree/swtgraphics2d/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.jfree/swtgraphics2d)

Overview
--------
A Graphics2D implementation that targets an SWT graphics context, allowing the use of Java2D code in SWT.  This class was originally developed as part of the JFreeChart project (http://www.jfree.org/jfreechart).  It is now a standalone project.

Include
-------
SWTGraphics2D is published to the Central Repository.  You can include it in your projects with the following dependency:

    <dependency>
      <groupId>org.jfree</groupId>
      <artifactId>swtgraphics2d</artifactId>
      <version>1.0</version>
    </dependency>

Testing
-------
**SWTGraphics2D** is being tested using [Graphics2D Tester](https://github.com/jfree/graphics2d-tester) and produces the output shown below (using the not-yet-released version of `SWTGraphics2D`)

Due to limitations of the SWT Graphics API, there are several Java2D features that cannot be supported:

- the Porter-Duff compositing rules in `AlphaComposite
- multi-linear and radial gradient paints.
  
Areas that still need work:

- clipping functions are not yet fully correct
- font metrics are approximated

![SWT test output](swtgraphics2d.png)

License
-------
SWTGraphics2D is free software under the terms of the GNU Lesser General Public License (LGPL) version 2.1 or later.  

Please note that SWTGraphics2D is distributed WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  Please refer to the license for details.

Change History
--------------

Version 1.1.0 (not yet released)
- added support for `GradientPaint` (without cyclic attribute) in `setPaint()`
- apply winding rule in `fill(Shape)`
- improved correctness and efficiency of transformations
- fixed `setFont()` method for `null` argument
- fixed interaction between `setPaint()` and `setColor()`
- fixed failing tests for `drawImage()` methods with `null` arguments
- implemented `create()` method
- implemented `getDeviceConfiguration()`.

Version 1.0 (20 February 2016)
- initial release as a standalone project (previously included with JFreeChart SWT support).