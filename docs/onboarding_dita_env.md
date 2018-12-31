---
id: onboarding_dita_env
title: DITA environment
sidebar_label: DITA environment
---

Before being able to write DITA documentation, you need to setup your environment to match Talend requirements.

## Cloning the DITA repository

DITA content is stored on a repository named documentation-dita.

If you have never used Git before, it is recommended to follow a tutorial to learn about its key features: you should get up to speed with the basics quickly. Most of the team uses TortoiseGit as a Git client, but you can use another one, like SourceTree for instance, or the command line if you feel comfortable with it.

Read through the following [pages about Git](https://in.talend.com/6325053), and perform the steps explained in "Cloning a repository/How to clone a repository from Github".

## Loading the Talend DITA project

The Talend oXygenXML project enables to share preferences, transformation and validation scenarios across the team. It is also used to reference additional framework customization. You should always have this project open when authoring in DITA.

Open the talend.xpr file located at the root folder of the repository.

The Talend project opens into the Project view. The tree view is expanded automatically on the topic currently open in the editor.

## Adding Talend frameworks

Talend extends the two base DITA oXygenXML frameworks to provide custom templates, UI assistance and as-you-type Schematron validation for authors. Custom frameworks are stored under the framework directory.

1. Open Options &gt; Preferences....
2. Go to Document Type Association &gt; Locations.
3. Click Add.
4. Enter `${pd}/framework`.
5. Click Apply then OK.
6. Open the file `talend.xpr`.

You should see Talend DITA and Talend DITA map under Options &gt; Preferences &gt; Document Type Association.

## Setting up your author name

Add your name as a custom oXygenXML variable to populate the map template files.

1. Open Options &gt; Preferences.
2. In Custom Editor Variables, click New.
3. Set the variable name to ${author}, the value to your email username e.g. fviolette, and a description.

When you create a new DITA map from one of the Talend Map templates, you will be added automatically as the author.

> **Note**: If you get a broken reference, ask Information Architects to add the author name to the Author scheme within the Taxonomy.

## Enabling the metadata assistant

In the Author view, the layout helps you tag DITA maps faster, using add, tag and delete controls.

1. Open a DITA map.
2. Click the Styles drop-down menu in the toolbar.
3. Click Talend Map.
The icons ![Image](https://talend.github.io/documentation-dita/images/add_12.png), ![Image](https://talend.github.io/documentation-dita/images/delete_12.png) and ![Image](https://talend.github.io/documentation-dita/images/meta.png) appear above the Author, Category, Product name, Versions and Platform labels.

A footer with links to Fluid Topics, the DITA specification, the Doc Sharepoint folder, the GitHub repository, the online version of the docs and feedback is added.

> **Note**: Play with the buttons to get a sense of how this system works. You may get warnings along the way: trying to fix them is a good exercise.

## Loading the Talend DITA-OT

By cloning the documentation-dita Git repository, you inherit from Talend's reference copy of the DITA Open Toolkit (DITA-OT), stored under build/DITA-OT. This copy contains some additional plugins and plugin customizations compared to the standard distribution package. You need to reference the Talend DITA Open Toolkit in oXygenXML to publish a PDF with the Talend processing and layout. Publishing with the standard PDF transformation will not give the same results.

1. Open Options &gt; Preferences....
2. Select DITA.
3. In the DITA Open Toolkit section, select Custom.
4. Navigate and select the build/DITA-OT folder in your clone of the documentation-dita repository.For Windows users: C:\git\documentation-dita\build\DITA-OT or equivalent.
5. Click Apply then OK.

You can now publish a Talend PDF by creating a transformation scenario under Global and supply the parameters below:

|Parameter|Value|
|-------|---------|
|args.filter|file:/C:/git/documentation-dita/ditaval/tbd_offline.ditaval|
|args.gen.task.lbl|YES|
|dita.dir|${configured.ditaot.dir}|
|generate.copy.outer|3|

Note: The DITAVAL configured in the scenario depends on what you want to publish (args.filter parameter). DITAVALs for PDF end by _offline.

## Installing the Fluid Topics oXygenXML add-on

The Fluid Topics add-on for oXygenXML enables you to directly upload content to the Fluid Topics [test environment](https://talend-rc.fluidtopics.net/). For more information, refer to the official [documentation](https://doc.antidot.net/reader/hKklVq_FN8NIao3uPW7Ryg/qwogka8gZdBQFTQ7xX13Jw).
