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
| :warning: | change of direction |

## Themes
Funded development for ASC software has been categorized into three very broad thematic areas: (1) Maintenance and Maintainibility, (2) Value Adding, and (3) Research. In this document, we describe lower level thematic areas that ASC software will focus on. This roadmap is thematically organized because of the amount of synergy between projects. In FY20 (October 1, 2019 - September 30, 2020), we are working in the following thematic areas:

- ISIS modularization
- Continue to improve the build, test, deploy trains
- Grow and support our user community
- Increase the number of supported planetary sensors
- Improve bundle adjustment capabilities and control processes
- Research methods for improverd orthorectification

### ISIS Modularization (ALE integration with ISIS)
  :heavy_check_mark: Complete ALE integration into ISIS

  :running: Develop *ckwriter* and *spkwriter* tools using ALE

### Release Train :train:
  :heavy_check_mark: Three ISIS 3.x.x releases
  
  :heavy_check_mark: Three ISIS 4.x.x releases (2 concurrent with ISIS 3.x.x releases)
  
  :heavy_check_mark: Dependency management with the goal of reducing the number of third-party snowflake dependencies ASC maintains.
  
  :running: ISIS install alongside GDAL
  
  :heavy_check_mark: Remove ASC managed QT dependency

  :heavy_check_mark: Five releases of other ASC software packages, e.g., `plio`, `pyhat`, `autocnet`, `pyhat-gui`, etc.
  
  :heavy_check_mark: Improvements to ISIS testing suites including moving additional unit and application tests to GTest
  
  :heavy_check_mark: Full adoption of the Jenkins-CI environment
  
  :warning: Full adoption GitLFS for ISIS data (testing data and SPICE kernels) NOTE: This was altered to an FY21 project after testing GitLFS and better understanding internal data release policies.

### Community Growth
  :heavy_check_mark: Maintain communication channels established during FY19

  :heavy_check_mark: Improve documentation for external contributions

  :heavy_check_mark: One week per quarter of mission specific support (Git submitted issues and public prioritization meetings)

  :heavy_check_mark: One week per quarter of ASC product development support (Git submitted issues and public prioritization meetings)

  :warning: Two weeks of general community support (Github submitted issues) NOTE: This was integrated into our standard support due to changes in overall project funding.

### Sensor Models (CSM/ISIS)
  :heavy_check_mark: Implementation and verification of five CSM sensor models.

  :heavy_check_mark: Implementation and verification of a HiRISE sensor model.
  
  :heavy_check_mark: Implementation of a generic SAR CSM.
  
  :warning: Phobos88 sensor model - NOTE: The HRSC SRC sensor model was implemented instead
  
  :heavy_check_mark: Implement Kaguya MI sensor in CSM and ISIS. NOTE: This was not originally planned.

### Control and Bundle Adjustment
  :heavy_check_mark: Research quantitative methods for assessing control network health

  :heavy_check_mark: Develop bundle adjustment capability for framing and line scan CSM sensors

### Orthorectification
  :heavy_check_mark: Research into methods for occlusion support on 2.5D surfaces

## Initial Year Summary
In FY20 we are continuing to transition our software to a standard open source model. This focus means we are improving the portability of our tests so that external contributors can more easily participate in a standard development cycle, improving documentation for how contributors can help improve documentation and tutorials, modularizing the software into libraries to improve the developer experience and allow use by external developers in their applications, and supporting the existing user community. We are also focusing on our core competencies, standards support and generation of the highest quality planetary data products. This includes continued development of CSM sensors, tools for assessing control network quality, and implementation of new bundle adjustment software.

## Year End Summary
As we close out FY the breadth of high quality work, executed by all of our contributors in support of planetary science research, is truly remarkable. I believe it is safe to say that, as a community, we have successfully completed all of the major tasks that we enumerated approximately one year ago. We now have he beginnings of a robust community of contributors around not only our software portfolio, but across other commonly used packages in the planetary sciences. We have maintained a consistent release velocity, improved the developer experience, increased the number of arguably gold standard sensor models that are accessible to the community, and improved our ability to continue building high quality science products.