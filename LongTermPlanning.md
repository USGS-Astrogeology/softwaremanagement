# Long-term Plan for USGS Astrogeology Science Center Software Development

*Last updated: August 25, 2019*

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
    towards broad participation by external contributors (addresses SAT
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

-   Open Source Community Development (Lead: J. Laura)

-   ASC Software Portfolio Releasees (Lead: S. Stapleton)

-   Indirectly addressed by ISIS Testing Modularization (Lead: J. Maple)

#### Longer-term (5-year horizon):

-   Evaluate the effectiveness of our efforts and make reasonable
    changes to our approach based on community feedback and lessons
    learned.

---

## Objective 2: Improve the performance of the code base and the user experience.

*Note: This is a new objective. If there is agreement that this objective should be called out
specifically, Robin will write up a summary that is consistent with
others in this document.*

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

-   ASC Software Support (Leads: J. Laura, S.Sides)

-   Improvement of ISIS third party dependency management (Lead: K.
    Rodriguez)

-   ISIS Testing Modularization (Lead: J. Maple)

#### Longer-term (5-year horizon):

-   Evaluate the effectiveness of our efforts and continue to be
    response to community feedback and lessons learned.

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

-   ISIS Testing Modularization (K. Rodriguez)

-   Community Sensor Model Bundle Adjustment (Lead: J. Maple)

-   Complete ALE Integration (Leads: J. Laura, J. Maple, K. Berry)

-   Develop and release a Request for Comment (RFC) regarding the ISIS
    Software Modularization plan

    -   Appropriately incorporate community feedback into this plan

    -   Maintain the publicly available ISIS Software Modularization
        plan by updating the document at least annually (addresses SAT
        finding 8).

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

-   Community Sensor Model (Lead: T. Hare)

-   Complete ALE Integration (Leads: J. Laura, J. Maple, K. Berry)

-   Lidar Support (B. Archinal)

#### Longer-term (5-year horizon):

-   PDS4 support may be needed in the near future (in-progress for
    CASSIS and Hayabusa 1), and a means to more easily generate PDS4
    metadata and support files will be required.

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
the military, to standardize camera models for future proposed
instruments.

#### Activities in FY 20:

-   Community Sensor Model (Lead: T. Hare)

-   Community Sensor Model Bundle Adjustment (Lead: J. Maple)

-   Contract NASA AMES to implement these same camera models in AMES
    Stereo Pipeline both to test this standard outside of Astrogeology
    and to help promote this standard across the community (Lead: T.
    Hare).

#### Longer-term (5-year horizon):

-   Determine criteria for transitioning current ISIS sensor models into
    the CSM.

-   Determine a means to continue supporting historical data sets that
    rely on ISIS sensor models.

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

-   Quantitative metrics for control network (Lead: J. Maple)

-   CTX Controlled Mosaic Generation (Lead: J. Laura)

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

-   Occlusion: Robust Orthorectification in ISIS (Lead: A. Paquette)

    -   Research and prototype efforts

-   Continue collaborations with the Small Body Mapping Tool and mission
    teams, with the goal of avoiding duplication of efforts and
    encouraging a unified approach to software in support of small
    bodies with a focus on interoperability.

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


