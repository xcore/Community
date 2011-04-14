Versioning
==========

This document describes how version numbering reflects the type of changes in a new release. 
The version numbering is a normal one: X.Y.Z, where X is major, Y is minor and Z is bugfix release number. If Z is zero, it is omitted from the version string. So, for example, 1.1.2 and 1.2 are valid version numbers but 1.2.0 is not.
Each number is (usually) increased by one at a time, and when one of the numbers is increased, the less significant numbers are reset to zero. To show an example, a valid sequence would be 1.0.3 → 1.0.4 → 1.1 → 1.1.1.

When a new release is made, the version number is increased according to the following rules:

*	If there are only bugfixes and the API hasn’t changed at all, the bugfix number Z is increased, e.g. 1.0.3 → 1.0.4
*	If there are backwards compatible changes (for example, additions to API), the minor number Y is increased, e.g. 1.0.4 → 1.1
*	If there are backwards incompatible changes (for example, changed or removed API), the major number X is increased, e.g. 1.2 → 2.0

This versioning scheme also dictates the development of new features and especially changes in API. There should be a considerable amount of new features when the minor version is increased so that it doesn’t grow very fast. And the major version number should only be increased when there is a serious reason to make backwards incompatible changes to the design.

When a design is in early development, its primary version (X) will be 0.  Users of designs at primary version 0 should have few expectations, these designs may not even build.  However, the transition to version 1.Y.Z requires some compliance to established models, which will depend on the class of design (software component, hardware design etc).  For further details see :doc:`Classes-of-Repository`.

This scheme follows that of `Semantic Versioning <http://semver.org/>`_.
