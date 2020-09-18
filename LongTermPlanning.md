# Long-term Plan for USGS Astrogeology Science Center Software Development

*Last updated: September 10, 2020*

For additional information about the projects listed under each objective, please see the associated directory for the given fiscal year. For example, if you are interested in the *ISIS PVL and BLOB Extraction* project listed under objective 1, please see the FY21 directory README.

## Objective 1: Initiate and foster an open source community, initially centered around software developed by the ASC (including ISIS).

The ASC software portfolio, including the source code, has always been
distributed at no cost, but the planetary community has not had a means
to contribute any modifications, enhancements, or original solutions to
this portfolio. By Open Sourcing the ISIS (and other) software, the ASC
intends to build a community of users and developers who can more easily
modify and share enhancements to this software. This change would
improve our collective ability to meet community needs by bringing
together experts in sensor models, projections, and spatial data who
collectively will make a more robust and functional software than any
single group could do alone. This objective also directly addresses
several findings from the [NASA-MAPSIT Special Action Team (SAT) review](https://github.com/USGS-Astrogeology/softwaremanagement/tree/master/SpecialActionTeam_Review)
of the ASC software portfolio, including findings 4, 5, 9, 11, 13, and
15.

#### Ongoing Efforts:

-   Continue to be the steward of ISIS, continue to facilitate and work
    towards broad participation by contributors (addresses SAT
    finding 4).

-   Maintain mechanisms for widespread use for user engagement with the
    ASC software portfolio and its developers (addresses SAT finding 5).

-   Maintain a formal Open Source governance policy that clearly
    describes how outside contribution can be submitted, including
    required coding standards, and the process for incorporating them
    into the code base (addresses SAT finding 11).

-   Continue to release the ASC software portfolio code base on a public
    GitHub (addresses SAT finding 9).

-   Release all ISIS general and test data so that outside developers
    can also run, and expand upon, these tests (addresses SAT findings
    13 and 15).

#### Activities in FY 20:

-   Open Source Community Development 
-   ASC Software Portfolio Releasees 
-   Indirectly addressed by ISIS Testing Modularization 

#### Acitvities in FY 21:

- Open Source Community Development
- ISIS Application Modularization
- ISIS PVL and BLOB Extraction

#### Longer-term (5-year horizon):

-   Evaluate the effectiveness of our efforts and make reasonable
    changes to our approach based on community feedback and lessons
    learned.
- Support a planetary software stack composed of ASC and non-ASC software packages
- Build and support the external development of community desired analytical tools that make use of our lower level, gold standard, libraries.

---

## Objective 2: Improve the performance of the code base and the user experience.
The ASC will build, support, and integrate with the infrastructure necessary for users to install our software with a minimum amount of effort. The ASC will also release software at a cadence selected to support the largest possible subset of the community. Additionally, ASC will seek to improve the user experience by, when possible, reducing the total volume of data necessary to store locally and improving the overall performance (speed) of the code base.

#### Ongoing Efforts:

-   Continue to improve the ISIS build system, through regular support
    and maintenance.

-   Continue to improve the ISIS distribution system by maintaining the
    conda-based distribution system to provide a more universal binary
    distribution of ISIS (addresses SAT finding 12) and continuing to
    improve this distribution system in response to user feedback
    (addresses SAT finding 13).

-   Continued software support and maintenance of the ISIS codebase
    (addresses SAT finding 24).

-   Improve the availability of appropriate test data (addresses SAT
    finding 15).

-   Maintain continuous deployment.

-   Improve application performance, when needed (addresses SAT finding
    16).

-   Continue to improve ISIS program documentation both as new
    functionality is developed and as performance or accuracy concerns
    are identified and addressed within the legacy codebase (addresses
    SAT finding 6).

#### Activities in FY 20:

-   ASC Software Support 
-   Improvement of ISIS third party dependency management 
-   ISIS Testing Modularization 

#### Activities in FY21:
- Remote SPICE Calibration 
- ISIS3 to ISISX cleanup
- ISIS Application Modularization
- ISIS PVL and BLOB Extraction
- 

#### Longer-term (5-year horizon):

-   Evaluate the effectiveness of our efforts and continue to be
    response to community feedback and lessons learned.
- Fully transition to supporting remote SPICE server capibility reducing the total data volume significantly.
- Explore the potential for remote data processing in line with the general shift to cloud based data storage and processing in collaboration with our user base.

---

## Objective 3: Modularize components of ISIS and support published APIs.

The ASC will build and maintain a stable software API and separate,
smaller libraries, which will, over time, replace the current ISIS
software portfolio. Like ISIS, this suite of Open Source applications
will continue to meet the infrastructural needs of the planetary
community. We envision a transitional approach to replacing the ISIS
software system (as opposed to a ‘cut-over’), while continuing to
provide high-level support to current missions and ensuring that data
processing and product production pipelines are interrupted as little as
possible.

#### Activities in FY 20:

-   ISIS Testing Modularization 
-   Community Sensor Model Bundle Adjustment 
-   Complete ALE Integration 
-   Develop and release a Request for Comment (RFC) regarding the ISIS
    Software Modularization plan
    -   Appropriately incorporate community feedback into this plan
    -   Maintain the publicly available ISIS Software Modularization
        plan by updating the document at least annually (addresses SAT
        finding 8).

#### Activites in FY 21:

- ISIS Application Modularization
- ISIS PVL and BLOB Extraction

#### Longer-term (5-year horizon):

-   Transition the suite of ISIS control network programs into a
    stand-alone application.
-   Evaluate the benefits of developing a Python API for ISIS by openly
    discussing and planning this API with the OS community (addresses
    SAT finding 21).
-   Astro will deprecate old software by (when applicable) processing
    data using that software, releasing these minimally derived products
    to the community in a usable format, and archiving the software
    itself (potentially in the PDS).

---

### Objective 4: Maintain and improve software support for ongoing, legacy, and future missions, with a focus on interoperability and reduced maintenance costs.

The Astrogeology Science Center (ASC) has historically supported
planetary missions that are currently active, are being developed, and
are no longer operational (i.e., retired missions).  In addition, an
external review board found that the ASC’s role in NASA mission support
has been a cornerstone of the planetary science community, and that it
should continue and improve (SAT finding 17). The ASC supports missions
by developing and maintaining camera models, aiding in the development
of data processing pipelines, developing software and the capability to
generate Digital Terrain Models (DTMs) for planetary sensors, and can
provide guidance in the geometric calibration of the instrument both
before and after flight. The support of missions is a fundamental
service that ASC currently provides, not only to the mission, but by
extension to the planetary community as a whole and is a role that we
should continue to fill.

#### Ongoing Efforts:

-   Address mission-related software concerns, often through the Open
    Source community and in direct collaboration with mission teams (addresses
    SAT finding 17).

    -   Continue to improve the responsiveness that ASC can offer active
        mission teams.

    -   Advocate for early involvement and consistent communication with
        mission and instrument teams to help to maintain support.

    -   Offer to provide mission teams a technical contact role between
        the ASC and the team.

    -   Continue to clearly communicate to missions scheduling and other
        resource constraints that allow both parties to plan and
        adequately budget for mission support.

-   Preserve and maintain support for current sensor models and develop
    new sensor models

-   Increase camera/sensor model interoperability

-   Improve SPICE infrastructure

#### Activities in FY 20:

-   Community Sensor Model 
-   Complete ALE Integration 
-   Lidar Support 

#### Activities in FY 21:
- Community Sensor Model
- PDS4 Support
- ISIS Mission Support
- Community Support (Participation in both the PlanetarySoftware and ISIS Technical Committee Organizations)
- Remote SPICE

#### Longer-term (5-year horizon):

-   ~~PDS4 support may be needed in the near future (in-progress for
    CASSIS and Hayabusa 1), and a means to more easily generate PDS4
    metadata and support files will be required.~~ (Executing in FY21.)
- Work as members of the ISIS TC to determine mission needs with respect to software development and release practices.
- Work as members of mission teams for intial implementation of rigurously tested sensor models, ingestion programs, and where appropriate processing pipelines that support many foundational aspects of mission success.
- Work as members of the support community to address issues as they are reported to our software projects.
- Continue to modularize our software with the goals of (1) improving our testing confidence and the confidence of mission teams in the efficacy of their pipelines and (2) making the process of pipeline development using components of our software portfolio more straight forward.

---

## Objective 5: Continue to develop and integrate the Community Sensor Model into planetary science applications.

Rigorous sensor models are a fundamental requirement for computing the
geospatial properties for planetary image observations and are used
widely in the core cartographic, control solutions, and
orthorectification applications. The creation of accurate orthorectified
planetary images (ortho-images) is critical for a wide variety of
geospatial activities including production of digital mosaics, digital
elevation models from stereo imagery, change detection, landing site
analysis, geologic mapping, rover traverse planning, and spectral
analysis. To better support software interoperability between different
photogrammetric applications (including ISIS), we will continue to
implement the Community Sensor Model (CSM) standard. Over the last two
years, Astrogeology has been actively developing and testing the CSM
standard in order to support interoperability across a range of software
tools including SOCET GXP, ENVI, ISIS, and within a stand-alone Python
testing environment. For the CSM standard, there are much longer-term
goals to see this standard used across the community, as it is used by
the military, to standardize sensor models for future proposed
instruments.

#### Activities in FY 20:

-   Community Sensor Model 
-   Community Sensor Model Bundle Adjustment 
-   Contract NASA Ames to implement these same camera models in Ames
    Stereo Pipeline both to test this standard outside of Astrogeology
    and to help promote this standard across the community

#### Activities in FY 21:
- Community Sensor Model
- Contract NASA Ames to implement these same camera models in Ames
    Stereo Pipeline both to test this standard outside of Astrogeology
    and to help promote this standard across the community.

#### Longer-term (5-year horizon):

-   ~~Determine criteria for transitioning current ISIS sensor models into
    the CSM.~~ (Executing in FY21)
-   Determine a means to continue supporting historical data sets that
    rely on ISIS sensor models.
- Determine whether dual sensor model development is a valuable method to support additional rigurous testing.

---

## Objective 6: Improve the scalability of ASC control applications.

The development of rigorous geodetic and/or photogrammetric control
networks are fundamental to generating local, regional, and global
mosaics, and subsequent foundational products such as image-based
topography and orthoimagery. The ASC has established itself as a leader
in the field of planetary geodetic and photogrammetric control. However,
continued leadership requires that we continue to improve our technical
capabilities.

#### Ongoing Efforts:

-   Improve our capability to identify and monitor the health of a
    photogrammetric control network.
-   Develop new and improve existing automated matching capabilities for
    image datasets (addresses SAT finding 19).
-   Develop methods to automate tying to ground

#### Activities in FY20:

-   Quantitative metrics for control network 
-   CTX Controlled Mosaic Generation 


#### Activities in FY21:
-   Operationalize FY 20 Quantitative metrics for control network
-   Continue CTX Controlled Mosaic Generation

#### Longer-term (5-year horizon):

-   Develop improved capabilities to handle large data and network
    volumes.
-   Include robust error propagation in bundle adjustment and improved
    documentation describing the bundle adjustment output.

---

## Objective 7: Increase our support of small and irregular-shaped bodies

Small bodies are an increasingly high priority to NASA Headquarters. To
date, specific missions have funded the ASC to develop software
solutions to address the specific needs of that mission (e.g., ROSSETTA,
DAWN, OSIRIS-Res). Although many of these solutions are applicable to
all small and irregular bodies, the improved coordination of these
efforts, both within the ASC and with outside collaborators), will
maximize the ability of the community to support both existing and
future missions. The ASC will continue to develop generic solutions that can then
be applied to a wide range of small bodies and coordinate efforts with
missions and collaborators.

#### Activities in FY 20:

-   Occlusion: Robust Orthorectification in ISIS 

    -   Research and prototype efforts

-   Continue collaborations with the Small Body Mapping Tool and mission
    teams, with the goal of avoiding duplication of efforts and
    encouraging a unified approach to software in support of small
    bodies with a focus on interoperability.

#### Activities in FY 21:
- Collaboration between ASC staff and the Small Body Mapping Tool development team

#### Longer-term (5-year horizon):

-   Through discussions with the broader planetary community, determine
    clear data processing, projection, and analysis needs, and determine
    how the ASC can best contribute.

---

## Objective 8: Continually improve the effectiveness by which the ASC manages software development.

The planetary community relies on the infrastructural software developed
by the ASC to process planetary data and generate higher-order derived
products. As a result, it is paramount that the ASC software portfolio
is developed with a strategic long-term vision that integrates the needs
of active and developing missions, research scientists, and developers
building upon the applications provided. We acknowledge that substantial
internal variability over time in various parts of the ISIS codebase has
occurred, and that these inconsistencies make developing external code
against ISIS very difficult. We seek to minimize these difficulties,
both for internal ASC developers and for the outside community and
facilitate the development of a community-based set of infrastructural
software through means discussed below.

#### Ongoing Efforts:

-   Maintain an ASC software management structure, which includes the
    following (addresses SAT finding 22):

    -   Software Development Lead (currently Jay Laura;
        <jlaura@usgs.gov> / @jlaura)

        -   Ensure responsiveness and traceability to ASC and community
            scientific use cases, funded projects, and mission support

        -   Serves as a public advocate for the Astro software portfolio

        -   Encourages participation in the OS community

        -   Facilitates addressing concerns from the community

        -   Gathers comprehensive information regarding community
            software needs and the effectiveness this software
            management model.

        -   Technical responsibility for strategic direction of software
            development by ensuring that the strategic goals are
            technically feasible and appropriate.

    -   Technical Operations Lead (currently Robin Fergason;
        <rfergason@usgs.gov> / @rfergason)

        -   Provides direct oversight to help ensures that the ASC
            software development portfolio meets user needs and
            completes funded obligations.

        -   Supports the Software Development Lead in fulfilling
            actions.

        -   Aids in gathering comprehensive information regarding
            community software needs and the effectiveness this software
            management model.

        -   General responsibility for strategic direction of software
            development by ensuring responsiveness to the high-priority
            needs of a broad community.

-   Support the efforts of ASC project specific [Technical Steering
    Committee](https://github.com/USGS-Astrogeology/TSC) by allowing
    those committee members to make decisions on how to implement
    identified community needs/tasks into the existing OS software
    (addresses SAT finding 22).

    -   Subject-based committee that provides technical expertise for
        topics that effect multiple missions and projects

    -   Input from broad community expertise (rather than expertise
        within Astro alone) is included in design decisions, with the
        goal of reaching very high-quality decisions with large
        community buy-in

    -   Promotes communication across multiple users and projects

    -   Ensures consistency across multiple projects and missions

-   Maintain the publicly available [Software Long-Term Plan](https://github.com/USGS-Astrogeology/softwaremanagement/blob/master/LongTermPlanning.md) document
    by updating the document at least annually
    (addresses SAT finding 1).

#### Longer-term (5-year horizon):

-   Evaluate the effectiveness of our efforts and make reasonable
    changes to our approach based on community feedback and lessons
    learned.

---

## Objective 9: Provide training opportunities for ASC staff

Improving our software development capacities and efficiency requires
well trained software developers, product owners, and product creators.
In order to support and retain a knowledgeable and motivated software
development team, we must provide both professional development
opportunities and career pathways for early- and mid-career developers.
In addition, Product Owners must be trained to improve project
management (e.g., clear definition of deliverables), and new processors
must be trained to maintain a skilled workforce.

#### Ongoing Efforts:

-   Ensure that funded projects exist to continue the development of
    both new and deeper expertise

-   Assign project work to software developers in a team-structured
    manner that facilitates cross-training among members.

-   Continue sending developers to conferences and workshops

-   Continue management training (for supervisors, project, and
    technical managers)

#### Longer-term (5-year horizon):

-   Continuing the above training


