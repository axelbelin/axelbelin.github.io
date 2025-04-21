---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home

title: Welcome on my Portfolio
---

<!-- Variables: -->

{% assign me = site.data.aboutMe %}


{% assign name = me.name %}

{% assign function = me.function %}

{% assign interests = me.interests %}

{% assign filterDiplomas = me.diplomas | where: "id", "engineering-diploma" %}
{% assign degree = filterDiplomas[0] %}
{% assign degreeName = degree.name %}
{% assign school = degree.school %}
{% assign university = degree.university %}
{% assign degreeType = degree.type %}

{% assign jobs = me.jobs %}
{% assign currentJob = jobs[0] %}
{% assign currentJobName = currentJob.title %}
{% assign currentCompany = currentJob.company %}
{% assign currentJobTeam = currentJob.team %}
{% assign currentJobType = currentJob.type %}
{% assign filterApprenticeship = jobs | where: "type", "Apprentice" %}
{% assign apprenticeship = filterApprenticeship[0] %}
{% assign apprenticeshipName = apprenticeship.title %}


{% assign technicalSkills = me.technicalSkills %}

{% assign technicalSkillsfilterByProgrammingLanguages = technicalSkills | where: "type", "programmingLanguages" %}
{% assign programmingLanguages = technicalSkillsfilterByProgrammingLanguages[0] %}
{% assign programmingLanguagesByLevels = programmingLanguages.levels %}

{% assign filterExpertProgrammingLanguages = programmingLanguagesByLevels | where: "level", "expert" %}
{% assign expertProgrammingLanguages = filterExpertProgrammingLanguages[0] %}
<!-- TODO gérer ", " -->
{% assign expertProgrammingLanguagesStr = expertProgrammingLanguages.names | join: " and " %}

{% assign filterProficientProgrammingLanguages = programmingLanguagesByLevels | where: "level", "proficient" %}
{% assign proficientProgrammingLanguages = filterProficientProgrammingLanguages[0] %}
<!-- TODO gérer " and " -->
{% assign proficientProgrammingLanguagesStr = proficientProgrammingLanguages.names | join: ", " %}

{% assign technicalSkillsfilterByVirtualization = technicalSkills | where: "type", "virtualization" %}
{% assign virtualizationSkills = technicalSkillsfilterByVirtualization[0] %}
<!-- TODO gérer ", " -->
{% assign virtualizationSkillsStr = virtualizationSkills.names | join: " or " %}

<!-- End Variables -->

Hi, I'm {{ name }}, a {{ function }} with a keen interest in {{ interests[0] }}, {{ interests[1] }} and {{ interests[2] }}.

In 2024, I got graduated from an {{ degreeName }} at {{ school }}: engineering school of the {{ university }}. Involved in this {{ degreeType }} as an {{ apprenticeshipName }} at {{ currentCompany }}, I've been hired as a {{ currentJobType }} within the {{ currentJobTeam }} at the end of my diploma.

After nearly four years with this company, I’m looking for a new environment and aiming to join another organization that offers professional opportunities in North America. My goal is to gain international experience in this region within the next one to three years.

- I'm experienced in full-stack development (mainly back-end), infrastructure and site reliability.
- I'm highly skilled in {{ expertProgrammingLanguagesStr }}, and proficient in {{ proficientProgrammingLanguagesStr }}.
- I'm used to work with Linux based environment within virtualized infrastructures built on {{ virtualizationSkillsStr }}.

I’m a fast learner and I’m able to adapt quickly to new technologies and environments. In fact, I’m improving my knowledge whenever I can, especially by developing skills as part of the projects I’m contributing.

## Take a look at my Posts below to read more about my experience:
