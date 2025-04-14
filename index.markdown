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

{% assign filterJobs = me.jobs | where: "current", true %}
{% assign currentJob = filterJobs[0] %}
{% assign currentJobName = currentJob.title %}
{% assign currentCompany = currentJob.company %}
{% assign currentJobTeam = currentJob.team %}
{% assign currentJobType = currentJob.type %}


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

In 2024, I got graduated from an {{ degreeName }} at {{ school }}: engineering school of the {{ university }}.

TODO ICICICICI translate .....

J'ai effectué ma formation en {{ degreeType }} en tant que ... software engineer apprentice ... chez {{ currentCompany }} qui m'a ensuite embauché en {{ currentJobType }} comme {{ currentJobName }} au sein du {{ currentJobTeam }}.

.....

I'm currently a {{ currentJobType }} for {{ currentCompany }}, working as a {{ currentJobName }} from the {{ currentJobTeam }}.




- What I want

TODO compléter + translate ....

Travaillant depuis presque 4 ans pour {{ currentCompany }}, j'ai envie de changer d'horizon / d'air dans l'optique d'accomplir mon rêve de travailler / de vivre / d'avoir une expérience professionnelle aux USA / en Amérique du Nord.
En effet, ayant eu l'opportunité d'étudier pendant environ 5 mois dans une université canadienne et de voyager aux USA, j'ai été séduit par le lifestyle, .... et ....


I'm experienced in full-stack development (mainly back-end), infrastructure and site reliability.

I'm highly skilled in {{ expertProgrammingLanguagesStr }}, and proficient in {{ proficientProgrammingLanguagesStr }}. <!-- and Bash. -->

I'm used to work with Linux based environment within virtualized infrastructures built on {{ virtualizationSkillsStr }}.


I’m improving my knowledge whenever I can, especially by developing skills as part of the projects I’m contributing.

## Take a look at my Posts below to read more about my experience:
