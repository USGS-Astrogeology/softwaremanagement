# Roadmap 2020

Herein, we present the ASC fiscal year 2020 software roadmap. The themes and associated tasks are ASC funded work to be completed during FY20. The enumerated tasks are those that ASC is committing to execute, but are not a complete listing of the work that could be undertaken. As an open source project, we are actively soliciting contributions from the community.

We have labeled some tasks as investigations to identify those places where we need additional information before we can estimate the full complexity and scope of a task. These tasks can lead to future work, a decision to defer, or a decision that additional information is required. 

Tasks on this roadmap are living. They may move ahead to future years, be identified as being completed, or be identified as not needed. Our ultimate goal is to engage the user community to identify where we can add value.

Tasks status is identified using the following shorthand:

| Mark | Meaning |
|------|---------|
| bullet| work not yet started|
| check | work completed|
| :runner: | on-going work |
| :muscle: | stretch goal |

## Themes
Funded development for ASC software has been categorized into three very broad thematic areas: (1) Maintenance and Maintainibility, (2) Value Adding, and (3) Research. In this document, we describe lower level thematic areas that ASC software will focus on. This roadmap is thematically organized because of the amount of synergy between projects. In FY20 (October 1, 2019 - September 30, 2020), we are working in the following thematic areas:

- ISIS modularization
- Continue to improve the build, test, deploy trains
- Grow and support our user community
- Increase the number of supported planetary sensors
- Improve bundle adjustment capabilities and control processes
- Research methods for improverd orthorectification

### ISIS Modularization (ALE integration with ISIS)
  - Complete ALE integration into ISIS
  - Develop *ckwriter* and *spkwriter* tools using ALE

### Release Train :train:
  - Three ISIS 3.x.x releases
  - Three ISIS 4.x.x releases (2 concurrent with ISIS 3.x.x releases)
  - Dependency management with the goal of reducing the number of third-party snowflake dependencies ASC maintains.
    - ISIS install alongside GDAL
    
    :muscle: Remove ASC managed QT dependency
  - Five releases of other ASC software packages, e.g., `plio`, `pyhat`, `autocnet`, `pyhat-gui`, etc.
  - Improvements to ISIS testing suites including moving additional unit and application tests to GTest
  - Full adoption of the Jenkins-CI environment
  - Full adoption GitLFS for ISIS data (testing data and SPICE kernels)

### Community Growth
  - Maintain communication channels established during FY19
  - Improve docuemntation for external contributions
  - One week per quarter of mission specific support (Git submitted issues and public prioritization meetings)
  - One week per quarter of ASC product development support (Git submitted issues and public prioritization meetings)
  - Two weeks of general community support (Github submitted issues)

### Sensor Models (CSM/ISIS)
  - Implementation and verification of five CSM sensor models.
  - Implementation and verification of a HiRISE sensor model.
  - Implementation of a generic SAR CSM.
  
  :muscle: Phobos88 sensor model

### Control and Bundle Adjustment
  - Research quantitative methods for assessing control network health
  - Develop bundle adjustment capability for framing and line scan CSM sensors

### Orthorectification
  - Research into methods for occlusion support on 2.5D surfaces

## Summary
In FY20 we are continuing to transition our software to a standard open source model. This focus means we are improving the portability of our tests so that external contributors can more easily participate in a standard development cycle, improving documentation for how contributors can help improve documentation and tutorials, modularizing the software into libraries to improve the developer experience and allow use by external developers in their applications, and supporting the existing user community. We are also focusing on our core competencies, standards support and generation of the highest quality planetary data products. This includes continued development of CSM sensors, tools for assessing control network quality, and implementation of new bundle adjustment software.
