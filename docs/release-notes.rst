.. This work is licensed under a Creative Commons Attribution 4.0 International License.
.. http://creativecommons.org/licenses/by/4.0
.. Copyright 2019 AT&T Intellectual Property.  All rights reserved.
.. _release_notes:


VVP Project Release Notes
===============================


Version: 9.0.0
--------------

:Release Date: 2021-10-13

**Removed Features**
- None

**New Features**

- Increase timeout value for requests. (``VVP-555``)
- Support for modeling service < 1.0. (``VVP-556``)
- Support for first time VSP users. (``VVP-535``)

**Bug Fixes**

- None

**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no
Critical vulnerability was found.

VVP code also is passing the mandatory test coverage percentage (%55).

- `Validation Scripts <https://sonarcloud.io/dashboard?id=onap_vvp-validation-scripts>`__
- `Test Engine <https://sonarcloud.io/dashboard?id=onap_vvp-test-engine>`__

Additionally, all VVP code is still scanned using the `Bandit <https://bandit.readthedocs.io/en/latest/>`__
library.  All potential issues reported this scanning process have been
addressed or marked as non-issues using the ``# nosec`` marker in the source
code.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_


Version: 8.0.0
--------------

:Release Date: 2021-03-23

**Removed Features**
- None

**New Features**

- Performance improvements for test-engine. This reduces runtime for 
  OVP VNF Life-Cycle validation tests. (``VVP-503`` ``VVP-504``)

**Bug Fixes**

- None

**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no
Critical vulnerability was found.

VVP code also is passing the mandatory test coverage percentage (%55).

- `Validation Scripts <https://sonarcloud.io/dashboard?id=onap_vvp-validation-scripts>`__
- `Test Engine <https://sonarcloud.io/dashboard?id=onap_vvp-test-engine>`__

Additionally, all VVP code is still scanned using the `Bandit <https://bandit.readthedocs.io/en/latest/>`__
library.  All potential issues reported this scanning process have been
addressed or marked as non-issues using the ``# nosec`` marker in the source
code.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_


Version: 7.0.0
--------------

:Release Date: 2020-11-18

**Removed Features**
- None

**New Features**

- Added additional test for resource group parameters. (``VVP-438``)
- Updated validation for R-610030: An incremental module must have
  a server or volume. (``VVP-451``)
- Various enhancements for performance and stability of
  onap-client. (``VVP-487``)

**Bug Fixes**

- Fixed the error message returned for test_get_attr_usage.py. (``VVP-420``)
- Fixed false posive testing port resource ids. (``VVP-346``)
- Various fixes for preload generation. (``VVP-440``)


**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no
Critical vulnerability was found.

VVP code also is passing the mandatory test coverage percentage (%55).

- `Validation Scripts <https://sonarcloud.io/dashboard?id=onap_vvp-validation-scripts>`__
- `Test Engine <https://sonarcloud.io/dashboard?id=onap_vvp-test-engine>`__

Additionally, all VVP code is still scanned using the `Bandit <https://bandit.readthedocs.io/en/latest/>`__
library.  All potential issues reported this scanning process have been
addressed or marked as non-issues using the ``# nosec`` marker in the source
code.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_


Version: 6.0.0
--------------

:Release Date: 2020-05-14

**Removed Features**
- None

**New Features**

- Added plugin capability to preload template generation. End users can
  now create their own python plugins for VVP to generate preload templates
  in the method and format of their choosing. (``VVP-339``)
- The ``vvp/test-engine`` repository has been revived and repurposed, and
  is now used to maintain the code for the following two enhancements:

    - Enhanced OVP VNF Heat validation to execute stand-alone, and moved into
      the VVP test-engine repository. (``VVP-381``)
    - Created onap-client python api client to interact with various ONAP
      applications. (``VVP-381``)

- Added validation test for new VNF Heat Template requirement R-55307
  . (``VVP-354``)
- Enhanced validation for nested resources R-17528. (``VVP-357``)
- Updated test_02_no_duplicate_keys_in_file to check environment files
  for duplicate keys. (``VVP-284``)
- Enhanced validation for R-90279 based on updated VNF Heat Template
  requirements. (``VVP-360``)
- Enhanced resiliency of preload template generation to support more
  general case VNF Heat Templates. (``VVP-335``)

**Bug Fixes**

- Resolved false negatives for internal network floating IP parameters
  parameter format checks. (``VVP-340``)
- Resolved false negatives checking required sections of a VNF Base
  Template module. (``VVP-365``)


**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no
Critical vulnerability was found.

VVP code also is passing the mandatory test coverage percentage (%55).

- `Validation Scripts <https://sonarcloud.io/dashboard?id=onap_vvp-validation-scripts>`__
- `Test Engine <https://sonarcloud.io/dashboard?id=onap_vvp-test-engine>`__

Additionally, all VVP code is still scanned using the `Bandit <https://bandit.readthedocs.io/en/latest/>`__
library.  All potential issues reported this scanning process have been
addressed or marked as non-issues using the ``# nosec`` marker in the source
code.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_


Version: 5.0.1
--------------

:Release Date: 2019-09-30

**Removed Features**
- None

**New Features**

- OpenStack Heat Validation - VVP now includes the latest version of OpenStack
  Heat, and can be used to validate that the Heat not only complies with ONAP
  rules, but is also valid Heat (similar to stack-validate) (``VVP-218``)
- Preload Template Generation - VVP will now create preload templates based
  on the Heat template being validated. The user can optionally populate the
  template by specifying environment files (``VVP-227``, ``VVP-277``)
- Added ``checks.py`` to consolidate various quality checks that can now
  be performed cross-platform and consistently between the local and build
  environment.

    - Added quality check to ensure VVP includes the latest version of Heat
      requirements from the VVP project
    - All code is now scanned for security issues using the Bandit library
      (``VVP-244``)

- Updated Availability Zone tests to align with latest VNF Requirements
  (``VVP-226``)
- Performance enhancements - improved performance of validation of large
  templates by 30-70% (``VVP-225``)
- VVP GUI can be customized to display configurable disclaimer text, and
  also allow the acceptance of terms-and-condition, or other legal agreements
  before allowing the user to use the tool (``VVP-195``)
- Enhanced report readability by removing unnecessary columns and other
  enhancements (``VVP-184``)
- Removed dependency on ``yamllint`` library to remove dependency on L/GPL code
  (``VVP-201``)
- Allow error messages with line breaks (``VVP-225``)
- Various enhancements to remove redundant tests or improve error messages



**Bug Fixes**

- Fixed errors in ``test_environment_file_parameters`` where wrong variables
  were being checked (``VVP-267``)
- VVP GUI fails to open reports when tools is launched from a network share
  (``VVP-266``)
- Escape error messages before display in HTML report (``VVP-159``)
- Improved error message when Heat archives included nested directories which
  are not allowed (``VVP-217``)
- Relaxed validation of ``get_param`` usage to better comply with SDC
  implementation (``VVP-220``)


**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no
Critical vulnerability was found.

Additionally, all VVP code is now scanned using the `Bandit <https://bandit.readthedocs.io/en/latest/>`__
library.  All potential issues reported this scanning process have been
addressed or marked as non-issues using the ``# nosec`` marker in the source
code.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_



Version: 4.0.0
--------------

:Release Date: 2019-05-10

**Removed Features**

- The VVP web application has been deprecated and is no longer supported
  as of the Dublin release.  The validation scripts continue to be supported
  and enhanced, but contributions to the web-related repositories are now locked
  and VVP will no longer be supported for deployment via ONAP Operations
  Manager (OOM).

  The following repositories are now locked as of this release:

    - ``vvp/ansibile-ice-bootstrap``
    - ``vvp/cms``
    - ``vvp/devkit``
    - ``vvp/engagementmgr``
    - ``vvp/gitlab``
    - ``vvp/image-scanner``
    - ``vvp/jenkins``
    - ``vvp/portal``
    - ``vvp/postgresql``
    - ``vvp/test-engine``

**New Features**

- A new :doc:`GUI application <humaninterfaces>` has been contributed and can
  be used to execute validations in a user-friendly way without using complex
  command line options.
- VVP is now packaged as a Docker container eliminating the need to run the
  application from source code.  See the :ref:`Docker Execution <vvp-docker-execution>`
  instructions for more details.
- VVP Validation Scripts now cover all mandatory, testable HOT requirements from VNFRQTS

**Known Issues**

- None

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no Critical vulnerability was found.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_


Version: 3.0.0
--------------

:Release Date: 2018-11-30

**New Features**

- Created mapping of validation scripts to VNF Guidelines
- Increase validation script test coverage
- Created HTML report generation in validation scripts repository

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no Critical vulnerability was found.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_

Version: 2.0.0
--------------

:Release Date: 2018-06-07

**New Features**

- Initial release of VNF Validation Program (VVP) for Open Network Automation Platform (ONAP).
- This intitial releases is based on seed documents that came from Open-O and Open ECOMP.
- This release provides a process to allow VNFs to be incubated and validated against the ONAP Heat Requirements.

**Bug Fixes**
- None

**Known Issues**

- As of now, the VVP Project has been created to check Validity for VNFs using Heat Orchestration Templates.
- Only deployable using OOM, will be a standalone toolkit in the future.
- UWSGI webserver dependencies.

**Security Notes**

VVP code has been formally scanned during build time using NexusIQ and no Critical vulnerability was found.

Quick Links:

- `VVP project page <https://wiki.onap.org/display/DW/VNF+Validation+Program+Project>`_
- `Passing Badge information for VVP <https://bestpractices.coreinfrastructure.org/en/projects/1738>`_

**Upgrade Notes**

- Initial release - none

**Deprecation Notes**

- Initial release - none

**Other**

	NA

===========

End of Release Notes
