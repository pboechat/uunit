uunit
=====

A simple *xUnit* style framework for unit testing inside Unity IDE

---

Port from the original code (in BooScript) to C#. 

Features added for 0.4:

	1.	New assertions (on UUnitAssert).<br>
	2.	UUnitTestRunner run all tests (Ctrl + Shift + T on Unity).<br>


The official project page can be found at:
http://www.unifycommunity.com/wiki/index.php?title=UUnit

---

_This project was not started by me, but by the unity forum member "Ryuuguu"_
(http://forum.unity3d.com/threads/6036-UUnit)

Introduction
------------

First of all, you have to download and import UUnit package to your project.
I suggest all test cases to be located on a separate folder inside your project's "Assets root" (ie: Assets/Scripts-tests/).
It's also a good practice to organize your test cases on folders that mirror the structure of the code being tested.
(ie.: Assets/Scripts/Weapons/Laser.cs
      Assets/Scripts-tests/Weapons/LaserTest.cs)
Here's a quick recipe for a new test case (feel free to copy and paste it to your file):

```C#
using UnityEngine;

public class YourClassTest : UUnitTestCase
{

  protected override void SetUp() {
  }

  [UUnitTest]
  public void ShouldDoSomething() {
  }

  protected override void TearDown() {
  }

}
```