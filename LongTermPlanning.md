# 2022 - 2027 Strategic Plan

## Executive Summary
This document outlines the 2022-2027 strategic plan for the Astrogeology Science Center software section. The plan describes four overlapping thematic areas of effort: Cloud & Software as a Service, Sensor Models & Photogrammetric Control, Improved Usability & Independently Identified Capabilities, and Documentation & User Training. Within each thematic area, individual capabilities are organized as must-have, should-have, and could-have within the next five years.

This document also describes the intended audience and proposes that this document be used to support the development and related funding decisions of the ASC software portfolio over the coming five years. The process used to generate this document is described to provide context to the reader about from whom information was sourced and how this document was drafted. This document describes how funding is currently organized. Finally, a plan for the longer-term maintenance and update cadence of the document is provided.

## Intended Audience and Use
This document is intended for contributors to the ASC software portfolio who may be proposing new work, contributors seeking to make changes to component of the software portfolio under existing work agreements, software management as a tool to help prioritize proposed efforts under larger funding agreements, and users with an interest in the long-term trajectory of software within the ASC portfolio. This document describes the methods used for information gathering and the organizational approach used. This documented also provides context for how tasks have historically been categorized under previous funding agreements and provide forward guidance for the approximate distribution of tasks during future fiscal years. 

The ASC development team and ASC technical management are more than happy to collaborate with and support the broader contributing community that may wish to propose to a funding opportunity to make improvements or modifications on software within the ASC software portfolio. This document should serve as a community organized guide to the capabilities and thematic areas for development that have been identified as high value. 

## Development and Organization
This document is a snapshot of work initiation in July 2021 to collect ideas, input, and direction from the ASC software development team, contributors to ASC software development projects, the ISIS Technical Committee, and the broad ISIS user base. The members of these groups participated in close to a dozen in-person brainstorming and context building sessions in order to build a framework from which this LTP has been developed. 

The ASC software lead has been tasked with collating the information gathered from the contributor and user community. Once collated, the identified thematic development areas have been brought into alignment with some of the driving planetary science community documents (e.g., [NASA Planetary Decadal (2013-2022)](https://science.nasa.gov/science-red/s3fs-public/atoms/files/Planetary_DS.pdf), [NASA PDE Recommendations and Findings (2021)](https://science.nasa.gov/files/science-red/s3fs-public/atoms/files/PDE%20IRB%20Final%20Report.pdf), [ISIS SAT Review (2018)](https://github.com/USGS-Astrogeology/softwaremanagement/tree/master/SpecialActionTeam_Review), [NASA Strategy for Data Management and Computing  for Groundbreaking Science 2019-2024](https://science.nasa.gov/science-red/s3fs-public/atoms/files/SDMWG%20Strategy_Final.pdf)) and with the long-term planning documents from other ASC sections. Capability prioritization (described below) was ultimately done by the ASC software lead, with significant input from the aforementioned group of people during brainstorming and context building sessions.

The breadth of capability development desired by the user community and development team exceeds the capabilities of the ASC software development team. This is one indicator that a thriving software portfolio exists with high user engagement. One organizational approach would be to be exclusive and remove tasks or development areas which are likely outside the reasonable scope of effort or expertise of the core development team (primarily ASC employees). Instead, this document is organizing capabilities first into larger thematic areas and then into must-do, should-do, and can-do categories with the understanding that can-do activities are likely to no be completed by the ASC development team in the next five years unless (a) unforeseen changes occur that move capabilities into different categories or (b) the addition of can-do capabilities are a natural and low effort addition to other higher priority work. In our view, it is important to explicitly describe the organizational structure and limitations of time in order to maintain shared expectations with all readers.

Capabilities identified in this document are presented in a form like a traditional user story. The general form is 'In five years, <user> will be able to <activity> to <outcome>'.  This form is being used because it is exceptionally concrete. A reader is immediately aware of the capability that a user will be using and anyone wishing to develop said capability has at least a minimal definition of done for their proposed task. Where appropriate, this document identified precursor work, but this document is neither prescient nor inclusive. Readers should feel free to identify necessary pre-work and [open an issue] to discuss those ideas with others.

Finally, this document makes every effort to explicitly link capabilities to identified use cases to ensure the highest likelihood of adoption of capabilities. As a development group, we have found the highest user satisfaction comes from tight integration and high communication during the development process. It is important to support the high communication development model at all levels of the development process, from this document to the fix of a bug.


## Thematic Development Areas

### Cloud and Software as a Service
##### Context and Description:

##### In the next five years, the ASC software portfolio must:
1. include cloud enabled services with well documented APIs that are accessible by end users. One example of this is the current work to cloud enable the SPICE server with support for USGSCSM and ISIS style sensor models. These services should be documented such that they can be deployed by anyone to the same cloud hosting provider that ASC deploys them to [^clouddeploy].
    - Projects using this capability: (1) most, if not all, internal users transitioning to using the remote, cloud enabled SPICE service, (2) control projects using AutoCNet transitioning to using cloud SPICE services, (3) STAC search, data/metadata management, and catalog APIs, (4) nomenclature capabilities as more accessible APIs, and (4) other unidentified cloud enabled services which should be able to link to at least one project or user community that will make use of the service.
1. provide user accessible data necessary to use libraries in the software portfolio via the cloud.
    - Projects using this capability: (1) all users performing an installation of our code base.
  
##### In the next five years, the ASC software portfolio should:
1. provide examples of containerized software libraries (ISIS) that are cloud deployed, including examples creating processing pipelines using one or more linked services.
    - Projects using this capability:
1. release a cloud deployed AutoCNet with *qnet* style point/measure visualization and analysis. This need not be an AutoCNET SaaS solution for users and can rather be components such that users can (re)create the same processing environment.
    - Projects using this capability: (1) any remote (over-the-wire, where data are not local) control work can make use of a *qnet* style visualization solution, (2) control work using AutoCNet, (3) other SaaS solutions identified in the future can make use of the lessons learned.
1. provide explicit descriptions attached to each ASC software portfolio library describing if said library can be cloud enabled and if the library has been cloud enabled.
    - Projects using this capability: All users and developers and the bringing the lifecycles into alignment with expectations supports everyone.

##### In the next five years, the ASC software portfolio could:
1. develop a accessible cloud ISIS with HTTP(S) access to ISIS applications demonstrating an ISIS as a service (SaaS) solution. Initially private and then possibly publicly accessible.
    - Projects using this capability: An users wishing to move from desktop to SaaS environments.

### Sensor Models & Photogrammetric Control
##### In the next five years, the ASC software portfolio must:
1. have fully adopted ALE, SpiceQL, and the updated ISIS ingestion programs. This includes the deprecation of currently deployed capabilities across **all** sensor models. This also incudes the development, testing, and deploy of CSM sensor models for past, current, and future missions.
    - Projects using this capability: All ISIS users will be using this capability. Implementation of this capability removes the dual maintenance burden that currently exists by having two (legacy and new) implementations concurrently supported.
1. provide automated solutions for ground control point selection using varied ground truth data sets.
    - Projects using this capability: All control projects include, but not limited to Kaguya TC, CTX, etc.
1. include tools of workflows for adding observations to existing control projects.
    - Projects using this capability: THEMIS, CTX, LROC-NAC, Europa Clipper (presumptive)

##### In the next five years, the ASC software portfolio should:
1. create prototype examples of CSM sensor models for (1) multi- and hyper-spectral spectrometers and (2) incredibly long exposure time observations when one wants fine grained timing control.
    - Projects using this capability: Continued CSM development efforts as this capability completes demonstration of the CSM across all major sensor types we encounter. 
1. understand how to (or not to) support J2000 within a CSM sensor model.
    - Projects using this capability: Continued CSM development efforts as this capability answers questions about the broad usability of the specification. 
1. include tools for improved interoperability between the NASA Ames Stereopipeline, ISIS, and SocetGXP using the Community Sensor Model (CSM).
    - Projects using this capability: ASC APPL group DTM generation
1. distributed (HPC) photogrammetric bundle adjustment in support of exceptionally large control networks.
    - Projects using this capability: CTX, KaguyaTC, likely LROC-NAC North and South polar mosaics
1. enhance the existing bundle adjustment library to support sequential photogrammetric control estimation and adjustment.
    - Projects using this capability: Large global solutions, regional solutions with high resolution data (LROC NAC or HiRISE control), and missions with sequentially updated data (e.g., THEMIS IR or to be acquired Europa Clipper data).
    
##### In the next five years, the ASC software portfolio could:
1. support simultaneous photogrammetric control solutions for Lidar and image observation data.
    - Projects using this capability: Control projects where lidar data are available.
1. improve GIS footprint generation
    - Projects using this capability: control projects and analysis ready data generation pipelines all benefit from improvements in GIS ready footprint generation.
1. be able to apply photogrammetric adjustment to solve for period, phase, and amplitude for librational movements for bodies.
    - Projects using this capability: Outer planets control research.
1. support adding increased metadata to points and measures within control networks including, but not limited to photometric and/or image resolution metadata.
    - Projects using this capability: Photogrammetric control projects
1. add capabilities to control network image registration to support adaptive reference measure selection and/or registration chaining whereby registration success is stateful and metadata about a successful registration is used in subsequent processing. 
    - Projects using this capability: Photogrammetric control projects
1. provide additional capabilities for control network analysis.
    - Projects using this capability: Photogrammetric control projects


### Improved Usability & Independently Identified Capabilities

##### Context and Description:
##### In the next five years, the ASC software portfolio must:
1. release one or more versions of ISIS making use of a standard and stand-alone Input/Output library (either off-the-shelf or homegrown) with support for performance enhancing capabilities (e.g., image pyramids).
    - Projects using this capability: All ISIS users benefit from this capability due to improved performance, reduced maintenance costs (intended consequence), and standardization that should improve interoperability.
1. provide consistent installation experiences for users on explicitly supported packages including improved dependency management, installation instructions, and installation tooling.
    - Projects using this capability: Given the complex dependency versioning interactions on the ISIS project, this the prime candidate for removing installation friction though all ASC projects would benefit from lessons learned.
1. expose and document Python (or other broadly use, higher-level language) access to library APIs.
    - Projects using this capability: ISIS is the primary target and beneficiary of this work. API access is **not** at the application level, rather it is at some API level.
1. standardize onto a single set of web3.0 technologies and frameworks to support data accessibility, discoverability, and access by users such that data access portals can be developed at lower costs across project areas
    - Projects using this capability: All ASC Data section releases seeking custom online solutions (e.g., terrestrial analogs data portal, nomenclature, PDS web mapping and processing portal, geologic mapping data portal, etc.)
  

##### In the next five years, the ASC software portfolio should:
1. provide improved photometric modelling capabilities including examples of off-the-shelf tools for large data visualization and analysis, and support for the inclusion of atmospheric and/or band information in the analysis process.
    - Projects using this capability: Improved generation of cosmetically appealing image mosaics
1. support the development of cosmetically appealing and scientifically accurate image mosaics using photometric information.
    - Projects using this capability: All control projects.
1. begin supporting remote data visualization and analysis include, but not limited to observation and control network data and metadata. 
    - Projects using this capability: AutoCNet based control solutions will immediately benefit from this work. Any remote workers and users wishing to setup remote (perhaps on HPC resources) solutions.
1. package off-the-shelf and/or custom solutions for the generation of analysis ready data and associated metadata including tooling for processing, metadata generation, and metadata management. Metadata management includes the need to update metadata and manage sematic linkages between data sets.
    - Projects using this capability: All analysis ready data (ARD) releases.

##### In the next five years, the ASC software portfolio could:
1. provide tools for the extraction of limb profiles and limb topography to improve photogrammetric control capabilities and improve shape estimation, primarily for flyby missions.
    - Projects using this capability: Science investigations
1. include generic tools for dejittering line scan data that build off of the open source HiRISE dejittering pipeline or develop new and novel techniques for line scan dejittering to support high efficacy DTM generation. (Note: this requires a non-trivial amount of research before the software team can productionize a solution. Should that research occur, this could transition higher in the priorities).
    - Projects using this capability: DTM generation (HiRISE, CTX, LROC NAC)
1. update the ISIS library be callable using Unix style command line interfaces, (e.g., man spiceinit) in order to improve the sematic interoperability between ISIS tools and other standard Unix command line tools.
    - Projects using this capability: No projects explicitly use this capability. Instead, all users would potentially benefit from logical consistency across tools.
1. include increased adoption of targeted parallelization efforts in order to improve single machine performance for tasks with long runtimes.
    - Projects using this capability: Potential benefit across a range of users
1. provide an updated method for unique observation identification (i.e., serial numbers).
    - Projects using this capability: Described in the context of control. Needs additional project linkages if work is undertaken.


### Documentation & User Training
##### Context and Description:
Documentation is a foundational piece of any software with a user base broader than the person who wrote the code. Documentation can take many forms, from the published manuals and books of old to a series of blog posts or YouTube videos demonstrating example usages. Currently, the ASC software portfolio maintains many different documentation types across an equally large number of locations. The documentation and user training thematic area for future work focuses first and foremost on centralizing the current offerings and future offerings. Centralization is not just a matter of having a single remote accessible location to discover and access documentation, but also the adoption of a standard organizational schema to ensure continuity in documentation across individual projects within the portfolio.

The overriding philosophy is that documentation needs to be pervasive across the above thematic areas so that technical and non-technical users can adopt our libraries and tools. 

The highest priority capabilities that must be realized over the next five years focus on improving the discoverability and readability of ASC documentation, as well as the democratization of said documentation by enabled (and ultimately soliciting) contributions from all users. Having this framework in place adds significantly to the value of work done under the should and could categories as that work will ultimately be more accessible. Capabilities that should be added in the next five years complement the existing documentation and make use of ASC published software as components in larger processing and/or analysis pipelines more accessible to users. Efforts that should be undertaken also support adoption of ASC services and the improved communication of expectations between developers and users by explicitly describing library maturity [^maturity]. Finally, capabilities that could be added in the next five years include usage tracking metrics and in-person trainings. This latter capability warrants a small amount of additional discussion.

The person-time cost to generate in-person learning experiences, particularly by persons without pedagogical training is quite high. The scope of impact from in-person training opportunities is limited by the number of persons in attendance and then further limited by the follow-on opportunities for those attendees to practice the skills learned. The development time of high quality, asynchronously accessible tutorials and learning examples, backed by a thriving question and answer community, for example via a Q&A website, can also be high. The ability for learners to not only use, but also asynchronously interact with other learners and project contributors is why this document prioritizes this type of documentation and learning over in-person activities.

This section does not link explicitly to projects that benefit because improved documentation is broadly impactful.

##### In the next five years, the ASC software portfolio must:
1. make centralized and searchable documentation available to all users using a standard deploy framework.
1. adopt a cross project documentation standard whereby all projects provide the same style(s) of documentation in largely the same forms to improve cross library documentation readability for users.
1. provide ability for external contributions to the documentation that is largely maintained by ASC personnel.
1. work to increase adoption of CSM sensor models beyond SocetGXP in order to create a robust planetary user community around this standard.

##### In the next five years, the ASC software portfolio should:
1. publish examples and tutorials that demonstrate workflows across applications, including examples demonstrating how to use applications in different computing environments (e.g., cloud, HPC, desktop).
1. increase documentation quality by enacting processes to improve communication during development between implementor and user.
1. develop the ability to generate documentation from processing pipelines to support reproducibility of product generation including examples of cross-application processing.
1. select an explicit schema for describing the maturity of projects in the software portfolio and draft public facing policies that describe said schema. 
1. evangelize the availability of API backed services for use by external service and tool developers to support de-duplication of effort. Together with this effort is the adoption of services provided by others.

##### In the next five years, the ASC software portfolio could:
1. select off-the-shelf or develop and deploy metrics tracking for adoption of remotely accessible APIs (i.e., services).
1. initiate efforts to actively train novice users across communities (with a focus on reaching traditionally underserved communities) through workshops, office hours, or other face-to-face (digital or in-person) efforts. 


## Organization of Funding
Historically, the software development efforts at the ASC have been divided into three areas: Maintenance and Maintainability (M&M), Value-Adding, and Research. Maintenance and Maintainability tasks have accounted for between fifty-five and sixty percent of the overall work effort each year. These tasks include the release of our software portfolio to the community, maintenance of software library data areas, support sprints for our customers, Open-Source community development around ASC libraries, and iterative improvements to the code base such as migration of the ISIS tests to GTest or the modularization of the ISIS PVL and Blob classes into independently compilable libraries. Value-Adding tasks have accounted for between twenty-five and thirty-five percent of the overall work effort. These tasks have included efforts such as the development of Community Sensor Model (CSM) sensors, PDS4 support, and development and release of the Abstraction Library for Ephemerides (ALE). Finally, Research tasks account for between five and fifteen percent of the overall work effort in any given year. These tasks focus on developing and testing prototype capabilities that may or may not become a standard part of the ASC software portfolio. In previous fiscal years, tasks have included change detection, automated control network generation, bundle adjustment using the CSM, and photometric data analysis and correction capabilities.

Significant improvements to the development process by the ASC development team and wider community of contributors have supported the gradual reduction in the total cost of M&M tasks while improving both the developer and end-user experience. Our goal is to continue to seek strategic process efficiencies in order to either accelerate M&M tasks (such as the continued reduction in testing data volumes which in turn better supports robust software deploys and non-ASC developer participation) or to slowly transition work to the Value-Adding area. In other words, by automating a non-trivial amount of daily work, adopting industry norms for many development processes, and normalizing user expectations for maintenance and release cadence work, we can and will reallocate those work hours to other tasks.

The Research area of the portfolio has been successful in incubating capabilities that have successfully transitioned into our Value-Adding area. Therefore, the plan is to maintain five to fifteen percent of total work effort in those tasks. In contrast to the current model, moving forward research tasks will be time limited to at most ~5% of the total work effort. The goal is to increase the diversity of research tasks. The downside to capping research tasks is that the timeline for transitioning from research to production may be extended, but the increased diversity should provide the ASC development group with improved flexibility to meet ever evolving community needs. Note also that research tasks can and should span the breadth of our portfolio and are not limited to traditional science only research operation. Research into new development, release, or data sharing processes, development frameworks, or other technical solutions are all valuable research contributions.

## Intended Long Term Plan Maintenance
In contrast with the previous software LTP, this document is intended to be updated annually with the following goals:
  - Do no harm. The current trajectory of multi-year efforts should be maintained, and projects should be fully completed unless a significant, program level change has been identified or a project scope has grown to an untenable level.
  - Maintain agility in strategic execution by supporting the movement of development goals between the must-do, could-do, and should-do categories on an annual basis.
  - Develop and maintain a sixth-year backlog of development ideas that are agilely incorporated into existing thematic areas / categories, or cycle off as a tool for seeding the annual updating of this document.

[^clouddeploy]: In our experience, generalized deploy anywhere including cloud solutions are frequently homegrown making them hard to maintain. Even a 'simple' solution like making a  Docker container available to users that is deployed to Amazon EKS (a Kubernetes cluster) causes friction on the deployer side (as they are not using some cloud native infrastructure they might want to use) and on the user side (as we would not be making the K8 configuration files available to end users.
[^maturity]: The description of library maturity also supports better classification of our releases as per USGS software release guidelines and brings the ASC software portfolio into full compliance with our release requirements.
