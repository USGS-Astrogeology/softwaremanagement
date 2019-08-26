Ross A. Beyer

Sagan Center at the SETI Institute and NASA Ames Research Center\
<rbeyer@seti.org>

K. Michael Aye

University of Colorado, Boulder

Nicholas M. Estes

Arizona State University

Carolyn Ernst

Johns Hopkins University Applied Physics Lab

Caleb Fassett

NASA Marshal Space Flight Center

Audrie Fennema

The University of Arizona

Dathon Golish

The University of Arizona

Cynthia Phillips

California Institute of Technology and the Jet Propulsion Laboratory

November 30, 2018

Copyright ©2018 by the authors. This work is licensed under the Creative
Commons Attribution 4.0 International License. To view a copy of this
license, visit <http://creativecommons.org/licenses/by/4.0/>.

Introduction
============

The established a consisting of the authors of this report. The
objectives of this were to execute a review of the present state of the
[ AC@USGS@used ’s ’s (’s) ]{} capabilities and software development.
This was to provide Findings relevant to future development of those
software capabilities and others funded by at the [ AC@USGS@used ’s ’s
(’s) ]{} in Flagstaff, Arizona.

The complete terms of reference for this can be found in Appendix
\[tor\] on page .

The team met regularly from its initial teleconference on 26 June 2018
through the publication of this report, and had an in-person meeting at
the on 28-29 August 2018.

Approximately four years ago, under the auspices of the Planetary
Cartography and Geologic Mapping Working Group (which has since
dissolved, but whose mission carries on with ), an was formed. It
reported Findings on the state of the software and development practices
(a copy of their Findings document can be found in Appendix \[etrp\], on
page ).

As a part of the current effort, we have reviewed the Findings. Some of
those Findings have been addressed, and some were overcome by events.
Specifically, the has carried out successful remedies to the Present
Development Methodology and Professional Development Findings, for which
we commend them. Other Findings were also addressed, and we provide
additional guidance on them in Findings \[accessibility\],
\[universal-binary\], and \[workload\]. We find that some of the
Findings remain un-addressed, and we have revisited some of them
(Findings \[opensource\], \[modularity\], \[dev-builds\],
\[compilation\], and \[leadership\]).

This SAT solicited feedback from the community of users and we summarize
their responses in Appendix \[feedback\] on page .

Some Findings constitute tasks and activities that are important to the
progress of the software portfolio, which we think should be carried out
within six months or a year. Where applicable, we have specified
suggested milestones, and also summarize these suggested milestones in
Appendix \[milestones\] on page . Other Findings are not about specific
tasks, but their suggested remediation constitutes a set of guidelines
or principles that should be adhered to. We have intentionally not
ranked these Findings, and Findings without milestones are no less
relevant than those with milestones.

It is important to note that this document and these Findings address
the entire software portfolio and are not limited to . In the past, the
software was the primary development effort and primary software
deliverable of the , but that scope has broadened even over the last
four years, and based on our conversations with staff, that scope will
continue to evolve. Except where these Findings are -specific, the
intent is that they apply to all software development that the performs.

Furthermore, this understands that the may be moving forward to
discontinue use of the name for a variety of reasons. As future naming
conventions have not yet been established, the terminology used in this
document refers to both the current and any near-future incarnation.

Findings
========

## Planning

### F1 Strategic Planning 
We find that there is no publicly available long-term strategic plan for
the software portfolio.

An overall long-term publicly available strategic plan would support
other Findings about community participation and transparency. It would
would also help the itself to understand the alignment between the
direction of their software portfolio development and missions,
directions, and goals, and help them to ensure that their software
portfolio is supporting the concepts of planetary spatial data
infrastructure.

It would be reasonable for the to develop such a plan within a year.

### F2 Existing functionality and future deprecation decisions


We find that it is important to identify what the core functions are, to
maintain existing versions of the software past the time when new
versions are introduced, and to ensure that existing functionality not
be deprecated unless alternate solutions are common, broadly accessible,
and equally capable.

The notes that significant changes are occurring or planned with the
code base, including modularization of libraries, implementation of new
interfaces, incorporation of new core libraries (e.g. ray tracing
engines), etc. Given the broad user community, many of which have
existing workflows and pipelines, we find that it will be important to
maintain existing versions of the software for a period of time, even
when new versions are introduced, until the user community has embraced
the new versions.

In the context of libraries, it will be critical that core functions
continue to exist and function as they do currently while their internal
components are switched to use libraries. The definition of “core”
should be defined by polling developers, internal users, missions, and
the community at large. It might be best to err on the side of a large
pool of “core” functionalities, rather than one that is too limited.
This would best smooth the transition to a library-based, modularized
and toward an open-source community.

In the context of , while there is broader expertise in the community
outside of the for creating that can be wrapped around core
functionality, and the may be considering this as an area from which to
eventually step away from (so their resources can be deployed
elsewhere), the existing level of functionality (e.g. `qview`, `qmos`,
etc.) should not be deprecated unless alternative solutions are equally
capable.

## Community Interaction and Documentation

### F3 User base for ASC Tools
We find that there is an uncertainty about whom the primary user base
should be for the software portfolio.

The has largely developed with a posture clearly focused on experienced
technical users comfortable in non-graphical environments, while
providing some support for beginners in the form of tutorials and
workshops. A continued primary focus on technical users is logical and
appropriate, as this allows the to focus their efforts on building
software that solves technical problems needed to analyze planetary data
that is unique to their skill set and essential for scientific analysis.
For this reason, building new graphical applications that attempt to
unify the current breadth of applications into a singular super- that
tries to offer a comprehensive interface for the majority of the
existing tools for non-expert users is not an avenue that the should
pursue. The current level of per-application graphical interfaces is
adequate.

The core functionality of should still ship as applications or tools
usable without requiring extensive additional coding. In other words,
just shipping libraries and without some user applications is
insufficient. Perhaps the example is a good one: primarily is a software
library, and there are a large variety of operations that can be
accomplished with the library for a user willing to write custom
software. However, also ships with a number of command line applications
that provide substantial functionality easily via the command line.

The should continue its primary focus on technical users.

### F4 Open Source, Community-Driven Development Model


We find that the should continue to be the steward of and future
planetary spatial data infrastructure software releases, but that more
effort must be made to facilitate broad participation by external
contributors.

The 2014 made a similar finding. While there is evidence that the is
moving in this direction, we expected to see more progress in this area
after four years. The development model should be as the steward of a
set of open source packages, meaning that they should “embrace open
exchange, collaborative participation, rapid prototyping, transparency,
and community development” as was stated in their own aspirational
documents in 2014.

We use the term ‘steward’ here instead of the term ‘gatekeeper’ used in
the 2014 . ‘Gatekeeper’ implies defensiveness, while ‘steward’ invokes
service to the community. While executive decisions about the course of
the software should be made at the , those decisions should be guided by
a strong connection to the community of users. Recent discussions with
the indicate that they are considering assembling a technical committee
consisting of external experts in order to address this need, we support
and encourage that course of action.

### F5 Community and User Support Forum 


We find that there is currently no good mechanism in widespread use for
user engagement with the software portfolio and its developers.

The had previously made available an online forum for its user community
that served two functions. First, it enabled users to interact with
developers, ask questions, and report bugs. Second, it enabled
experienced users to support fellow users (e.g. by suggesting tricks and
strategies for certain tasks, answering novice questions, etc). This
forum needed to be discontinued for understandable logistical reasons,
but the unfortunate consequence has been a substantial reduction in
communication both within the user community and between the users and
the developers. We note that the has recently encouraged users to start
using the GitHub Issues system to report issues with ISIS3, but it is
not clear if the intended use is limited to bug-reporting, or if it is
meant to also support discussions of broader topics.

The should consider implementing a new platform to support user-user and
user-developer interactions in the planetary data processing community
and to advertise its use. Six months would be a reasonable timeline to
develop such a platform. If such a platform cannot be hosted within the
compute environment for logistical reasons, should implement it
elsewhere (Google Groups e-mail list, GitHub Issues, many other
possibilities exist with minimal overhead).

### F6 Task-based Workflow Tutorials

We find that improved documentation for all programs would increase the
utility of the software. Specifically, we find that more concrete,
practical, modern workflow examples would be extremely useful for users.

While most applications have adequate documentation, the real power of
using comes from chaining programs together into a workflow. While there
are some tutorials that provide examples of these workflows, there are
not enough to cover the broad applicability of . Additionally, more
documentation about the general ‘theory’ of how and when to use certain
options for a particular workflow or program would increase the utility
of documentation over a simple, terse listing of program options.

### F7 ISIS on the Windows Subsystem for Linux

We find that many users want a version of that is functional in a
Windows environment, and that new technology available in Windows 10
(the Windows Subsystem for Linux) would allow it. Documentation for how
to install on the Windows Subsystem for Linux is now referenced by the .

It is important to note that there have been many requests over the
years to provide a version of that runs on Windows. The historical
problem with this request is that it would have required a substantial
development effort to create a Windows-native version of that would have
run on the Windows Command Prompt. Beyond that, creating a Windows
program that could be double-clicked upon and operated from a
comprehensive graphical interface–which is what many users mean when
they request a Windows version–would require even more effort. Such an
effort would have diverted resources from developing new
planetary-science-relevant functionality, addressing bugs, and working
on critical functionalities within the core codebase. We find that the
historical decision not to develop a Windows version was correct, given
the limitation of resources.

The new Windows subsystem for Linux allows (and its future modular
descendants) to run on a Windows machine in an analogous manner to the
way that it currently does on Apple Macintosh machines; not because a
special new development effort was made to run on Macs, but because
macOS provided a unix-like enough environment for to run on. The is to
be commended for publicly linking to a blog post which documents the
process for getting installed and working in the Windows Subsystem for
Linux within the documentation.

The should incorporate the instructions from the external blog post to
the documentation, though maintaining appropriate caveats about this
installation method being not strongly supported is reasonable. As
practicable, we encourage the to test against and maintain at least
installation support for on the Windows Subsystem for Linux going
forward.

# Core Functionality

### F8 Code Modularity

We find that the has not divided the functionality into a core,
stand-alone library and a set of applications and utilities, as
specified in the Findings. We find that developing such a strategy is of
high priority and should be vigorously pursued.

We agree with the finding that this definition of a clear and concise
will encourage and aid outside developers using and contributing to the
software codebase. Discussions with indicate that they have developed a
preliminary strategy for accomplishing this modularization effort, and
the intent is to identify separable, foundational functionality within
the codebase (camera models, SPICE interactions, etc.), write
stand-alone libraries with a clean to provide that functionality, and
then replace the current functionality with calls to those , which would
address this finding.

The is encouraged to develop a detailed, 5-year plan for this
modularization including a specified order for which functionalities
will be modularized and implementation milestones for that plan. One
year is a reasonable timeframe to develop such a plan.

### F9 Code Accessibility 

We find that the has placed their main development trunk for and most of
their non-proprietary software development on the public GitHub site, as
the 2014  finding on Code Accessibility recommended.

This placement allows the outside community to more actively participate
and collaborate with developers on the code. This is a major shift from
their previous development methodology of , and they are to be commended
for it.

We encourage the to continue to develop all major, non-proprietary
software projects in the open in this manner.

### F10 Issue Tracking 

We find that the issue-tracking system that was in place for some time
at the was opaque to external developers and users, and that their
recent switch to GitHub Issues for is an improved issue-tracking and
resolution system that will greatly benefit that project. However, not
all software projects do so.

Since is using GitHub for development, using the GitHub Issues system
would likely be the best solution. Doing so would reduce effort for all
parties, because known issues can be found by simple search, which saves
contributors from duplicating effort. Also, new error cases for known
issues could be easily facilitated by adding to existing findable GitHub
Issues. Additionally, the already opened GitHub pull requests are
usually directly linked to issues being tracked. The sequence of opening
GitHub Issues and solving them via GitHub pull requests is a well known
and highly accepted procedure for software provenance.

The should consider using the GitHub Issues system for issue-tracking
with all software portfolio projects (not just ). Six months is a
reasonable timeline to accomplish this.

### F11 Software Development Standards

We find that the does not have a set of consistent and logical software
development standards for their software portfolio.

There are currently some loose standards and a style guide available for
, but given the anticipated evolution of the codebase and other projects
in the software portfolio, a new comprehensive set of industry
best-practice standards is needed. These standards are not just style
guides, but also the guiding philosophies about how to write software
for projects. Once these standards are in place, all newly developed
code should adhere to these standards. The existing large codebase is
unlikely to conform to these new standards, and a massive ‘conversion’
project is not needed, but as older pieces of the codebase are modified
and updated, they should be brought into conformance with the new
standards. These standards must be followed by all external
contributors, as well as developers. The establishment of these
standards will simplify maintenance, revision, and shared use of code,
thereby supporting the move to an open source model.

Furthermore, a natural corollary of this Finding is an evaluation of how
much of any particular codebase meets these established standards. The
should look into reporting a variety of code quality and coverage
statistics for their software portfolio.

Establishing a set of such comprehensive software development standards
and making them available to the community would support the move
towards an open source model. A year is a reasonable timeframe to
accomplish this.

### F12 Universal Binary 



We find that the did not work to create a more universal binary under
their old distribution system, but with the November 2018 move to their
new `conda`-based distribution system, this goal is now realized.

The 2014 included a finding about creating a more universal binary
distribution of . The concept was that such a ‘universal’ binary
distribution would have fewer dependencies on the host system, at the
cost of being larger to download, but with the benefit of being able to
run on a wider variety of systems.

The new `conda`-based distribution system addresses the essential desire
of the 2014 Finding to allow to be installed on a wider variety of
systems. This is because much of the system-dependent library
installation issues are handled by the `conda` system which allows
installation on a much broader spectrum of systems than allowed under
the previous binary distributions.

### F13 Binary Installation 

We find that the `rsync` installation process that had been in use for
many years functioned well and was dependable for highly technical
users, but that it had many pitfalls for less technical users. However,
in November 2018, with 3.6.0, the has removed it in favor of a
`conda`-only installation process.

Under the `rsync` mechanism, warnings in the documentation about losing
data when the installation would be performed incorrectly were
frightening to potential new users. Incorrect use of the `rsync`
mechanism caused accidental deletions or unintended data duplication for
users. A Java-based graphical installer was supported in the past, but
it is no longer functional and is not maintained. While that effort had
the best of intentions, there are a number of practical reasons why it
is not functional, and we are not suggesting that it be revived.

As of the 3.6.0 release, the has discontinued the `rsync` mechanism for
software download, and is using the `conda` package management system,
making it a required installation in order to install . The new `conda`
system does help users ensure that they get the right files in the right
places, and that is ultimately a good thing. However, as it is a new
installation system, more work needs to be done to streamline the
user-experience. Such a mechanism could also enable installations of
beta-versions or mission-specific versions for testing.

It is reasonable for the to expect a larger number of user issues
related to the new installation system. They should be especially
vigilant for unforeseen issues that might cause difficulty with mission
or instrument team installations, and be ready to support them. If
absolutely necessary the could fall back on the `rsync` mechanism.

### F14 Development Builds 

We find that the availability of development builds of (referred to as
pre-release, weekly, nightly, edge or dev builds, not just the
release-candidate builds that are available) continues to be limited.

The 2014  found that the existing weekly builds being generated at
should be released to external users; however, these builds are still
not available. Access to such development builds allows users to verify
bug fixes, investigate new functionality, and generally close the loop
faster with developers leading to increased software quality and less
pipeline downtime. The stated that due to occasional proprietary code in
the source tree, weekly builds cannot be automatically released and that
work is ongoing via a new continuous integration platform to make
development builds available to external users.

The should consider how to make these development builds (at whatever
cadence more frequent than official releases is practical) available in
some form (`rsync`, `conda`, tarballs on GitHub, etc.). One year is a
reasonable timeframe to accomplish this.

### F15 Software Compilation

We find that there have been improvements to the build system, allowing
external developers to compile the source code. However, it is still
problematic for external developers to build and test the system.

The has already opened up the development process for to be visible on
GitHub and has stated that it wants to create an open-source community
around the software tools. For this to happen it is important that the
general build process is stable and well documented, so that the
community can participate, as indicated in a 2014  Finding.

There are many difficulties for compiling by external developers. The
precise list of compiler flags and version requirements for different
operating systems should be well documented. Additionally, availability
of appropriate test data is needed, but seems to be partially addressed
by the new 3.6.0 release which allows test data to be `rsync`ed. For
successful integration and participation of an open-source community a
test system that can run on a public continuous integration system like
TravisCI or similar would be advantageous.

The is encouraged to continue to work to make the primary development
branch of and other software easy to compile by external developers.

### F16 Software Optimization

We find that improving current application performance, where practical,
is warranted.

Applications with performance issues (e.g. `cam2map`) should be
investigated and identified. Efforts should focus on applications with
the greatest opportunity for performance improvement, prioritizing those
that can be easily or quickly fixed. Planning for growth and performance
should be a consideration in all future development.

# Methodology

### F17 Support for Active Missions

We find that the ASC's role in mission support
has been a cornerstone of the planetary science community, and it should
continue and improve.

No other organization is in a position to provide live development and
processing support to the wide variety of planetary missions being
flown. This has long been one of ASC's most
visible roles. The ability to continue to support mission and instrument
teams depends on improving the responsiveness that is able to offer
those active teams. Early involvement and consistent communication with
mission and instrument teams will help to maintain this support. Having
a technical contact role between and the team, rather than just purely
scientific or administrative contacts, is crucial to this communication.
We note that the open source framework toward which is headed would help
to ease this tension, as mission and instrument teams would be able to
develop and apply hot-fixes, or even additional features, themselves,
with the understanding that those changes could be integrated back into
the codebase. That framework requires clearly defined guidelines for
code development, submission, and review to reduce friction for both and
mission developers as illustrated in other Findings in this document.

The is encouraged to develop more flexible approaches to dealing with
mission and instrument needs by clearly communicating to missions
regarding scheduling and other resource constraints that allow both
parties to plan and adequately budget for mission support.

should consider ways to encourage and enforce more planning with respect
to planetary spatial data infrastructure by mission and instrument teams
early in their formulation, which could stimulate the formation of
partnerships with the (or other technical providers) earlier in their
lifecycle.

### F18 Support for small irregularly shaped bodies 

We find that support for small, irregularly shaped bodies in the
software suite is important to the planetary science community, given
the increasing number of current and pending small bodies missions.

That work has successfully started with the implementation of support
for the [ AC@NAIF@used ’s ’s (’s) ]{} , as well as additional ray
tracing engines (Embree, Bullet), fundamentally enabling active
missions. However that support currently has a number of known issues,
including efficiency, accuracy, occlusion, limb regions, overhanging
terrain, non-unique lat/lon points, additional projections for
irregularly shaped bodies, and alternative shape model formats (e.g.
`.obj`). We support the [ AC@ASC@used ’s ’s (’s) ]{} stated objective to
expand their capabilities for small bodies. is in a unique position,
with its core set of expertise, to advance the community in these
respects. We agree that coordination with missions, who may have active
development of tools and techniques for processing images of small
bodies, can help to make that effort more efficient. It is also
important to note that there is expertise in the broader community for
visualization of image data in 2D and 3D, e.g. , , , etc. The does not
need to reproduce that functionality. Given the variety of potential
downstream users of small-body data that might be produced in , this is
an area where export of data to standard 3D formats, as specified by a
planetary spatial data infrastructure, is important.

### F19 Automated image matching and feature recognition


We find that additional focus on improving the automated matching of
datasets has clear value as datasets get larger.

currently has many powerful tools for building control networks manually
and via area-based and feature-based image matching. The has made
investments in solutions and tools to improve control network creation
and management with humans-in-the-loop (e.g. the , ). We note that the
optimal tool or workflow for automated matching in a given situation is
often not evident to users at present. In addition, some of the tools
that are presently released are difficult to use in practice
(e.g. `findfeatures`). We recognize that the already has some projects
related to this finding underway, and encourage developments of improved
automated matching capabilities in to continue.

### F20 Broadening the SPICE web service

We find that it would be desirable to update existing routines that do
not fully support the SPICE web service to function in all cases.

Currently, there is a limitation preventing the use of the SPICE web
service for a few missions/instruments (e.g. MESSENGER, CASSINI, HiRISE)
because instrument calibration routines rely on local SPICE kernels. For
multiple reasons (user convenience, improving consistency of behavior
across the code base, centralizing SPICE management, etc.), it would be
an improvement to update existing routines to make the SPICE web service
functional.

### F21 Python API

We find that a Python for would be of broad use by the community.

A Python for was discussed during our on-site meeting at the as one of
the foreseen interfaces to the future core library. We encourage to
openly discuss the planning of this Python soon, as the implementation
of it will increase the ability of non-computer scientist application
developers to create planetary science processing pipelines based on .
Currently, developers rely on custom solutions, or third party Python
wrappers (e.g. `pysis`) that create system calls to applications, and a
fully supported Python would be welcome.

# Personnel

### F22 Software Management Leadership

We find that the has not identified a lead architect for the software
base as specified in the 2014 .

We agree with the Finding that such a position is critical for this
software, and the broader software suite that envisions. We believe that
this role could likewise be fulfilled by a steering committee with
decision-making authority that meets regularly to guide development. A
key component of this leadership is to ensure responsiveness and
traceability to and community scientific use cases, funded projects, and
mission support.

The should consider establishing a lead architect or steering committee
for all cartography and image processing software development with
overall technical responsibility for strategic direction of cartography
and spatial data infrastructure software development. One year is a
reasonable timeframe to accomplish this.

### F23 Workload

We find that the has followed the 2014 Finding on Workload by both
hiring new developers and successfully outsourcing work to external
contractors.

This mixed model of adding local talent and going to external groups has
been a successful approach and should continue. It allows for expertise
to be retained at the . It also allows the to be flexible if they either
lack a particular expertise, or available on-site developer hours.

# Oversight

### F24 Continued Funding for Support and Maintenance

We find that continued funding for software support and maintenance are
critical parts of [ AC@ASC@used ’s ’s (’s) ]{} role as stewards of and
their -funded software portfolio.

The initial lack of funding for software support in the FY2019 budget
curtailed [ AC@ASC@used ’s ’s (’s) ]{} ability to acknowledge and
address bugs submitted by the community. The FY2019 budget under the
agreement allowed only for maintenance activities, which we understand
to be mission-supported updates. This left the community at large,
outside of funded missions, without support for a major piece of
software. We understand that this oversight has been corrected, but it
was a troubling omission.

We encourage and the to view the software portfolio as fundamental
infrastructure for planetary science that requires ongoing support and
maintenance.

### F25 External review of ASC annual funding requests

We find that it would be valuable for management of software and
development funding under the annual to include some component of
external review.

The review that we imagine would not require an extensive review process
(i.e. an in-person panel). Instead, a process whereby one or two
external reviewers examine the priorities and levels of effort proposed
by the would have potential to improve outcomes.

should consider soliciting this type of external feedback on the same
cadence as new work effort is proposed under the .

# Terms of Reference

The NASA Mapping and Planetary Spatial Infrastructure Team (MAPSIT) will
establish a Special Action Team (SAT) with the objective of executing a
review of the present state of the U.S. Geological Survey’s Integrated
Software for Imagers and Spectrometers (ISIS) software capabilities and
software development to provide findings relevant to future development
of those software capabilities and others funded by NASA at the U.S.
Geological Survey’s (USGS’s) Astrogeology Science Center (ASC).

This SAT will be composed of individuals with scientific programming
experience drawn from academia, industry, and the US Federal Government.
The membership will be established by the MAPSIT Discipline Scientist,
Dr. Sarah Noble, and the Chair of MAPSIT, Dr. Jani Radebaugh.

The final deliverable will be a written report containing findings and
where applicable, discrete suggestions for potential improvements
pertaining to future cartography and image processing software
development.

The panel may choose to meet in person at the ASC in Flagstaff, Arizona.
The final deliverable will be due to the NASA MAPSIT Discipline
Scientist and the MAPSIT Chair no later than 30 November 2018.

## High Level Questions defined by MAPSIT 

This SAT will be tasked with providing findings to MAPSIT addressing the
following topics:

##### Core Needs:

The SAT will assess what the core functionality of ISIS should be.

##### Personnel:

The SAT will provide findings on the needed development expertise to
facilitate future ISIS development.

##### Methodology:

The SAT will assess the present development methodology of ISIS and will
provide the ASC with a viewpoint regarding where it stands with respect
to current industry best practices. This includes the approach to
software task planning, the organization structure, the development
philosophy, version control, bug tracking, quality assurance, and
testing.

##### Documentation and Community Interaction:

The SAT will assess the state of ISIS public user documentation and
training aids and provide findings about whether the content reflects
future community needs.

##### Strategic Planning:

The SAT will consider the feasibility of future plans for ISIS
development, particularly the relationship between the current version
of ISIS 3 and the proposed ASC roadmap for future cartographic software
development and capabilities.

##### User Growth:

The SAT will evaluate the present impediments towards the use of ISIS on
alternative scientific computing platforms, and its ability to integrate
with other software systems (as a library or part of a tool chain).

##### Governance:

SAT will assess whether alternate ISIS governance models (for example, a
USGS-led consortium approach) are feasible and could increase the
long-term sustainability of ISIS development.

##### Review of ETRP:

Many of these topics were addressed by the 2014 ISIS External Technical
Review Panel, and this SAT will review those findings and evaluate how
well the USGS has met them, and whether those findings remain relevant.

##### Relevance to PSDI:

The SAT will assess how ISIS and future software development and
capabilities envisioned by the ASC are relevant to Planetary Spatial
Data Infrastructure.

# Findings

The pages that follow are the Statement of Findings from the 2014. [Addendum from @jlaura - this document is available only as a PDF and is therefore, not included in this repo. Please `@` one of the maintainers on this repo if you would like a copy of the 2014 findings.]

# Community Feedback

The solicited feedback from the general user community by creating an
online form through which individuals could provide input into our
process. There was a long-form text box soliciting questions for
individuals for which the should get answers, comments about their
previous user experiences with , and suggestions for future -funded
software development in this area.

The took all of the gathered information into account during our review,
but did not specifically respond to each of the 30 responses.

In general, the public feedback was extremely positive, indicating that
the software was very useful, and crucial for remote sensing data
analysis from many spacecraft missions. The developers were praised for
being responsive to user inquiry. There was also sentiment that funding
and support should continue for the software development efforts at the
.

Several people asked for more instructive documentation and mission or
instrument specific workflow tutorials, which we have addressed in
Finding \[tutorial\] on page .

Finally, there were requests for a Windows version of . This topic is
specifically addressed in Finding \[windows\] on page .

# Suggested Milestones

Several of the Findings indicate a suggested timeline for
accomplishment. We have gathered them together in this table to provide
an overview:

  |                     | Finding                          | Milestone |
  |---------------------|----------------------------------|-----------|
  F5 |     Community and User Support Forum | Summer 2019 |   
  F10 |    Issue Tracking                   | Summer 2019 |
  F1 |   Strategic Plan                     |  |
  F8 |      Code Modularity plan | |               
  F11 |       Software Development Standards | Winter 2019 |    
  F14 |     Development Builds  ||  
  F22 |     Software Management Leadership ||     

# Citing this Report

Please cite this report as:

Ross A. Beyer, K. Michael Aye, Nicholas M. Estes, Carolyn Ernst, Caleb
Fassett, Audrie Fennema, Dathon Golish, and Cynthia Phillips. 2018.
MAPSIT Special Action Team Report on Cartography and Image Processing
Software at the Astrogeology Science Center. DOI: 10.5281/zenodo.2280984

# Note:
This report has been formatted from the original available at [https://zenodo.org/record/2280984#.XV3AEMZlAUE](https://zenodo.org/record/2280984#.XV3AEMZlAUE). Any alterations made are either noted as an `[addendum]` or are intended to be purely cosmetic to account for the conversion between LaTeX and Markdown.
