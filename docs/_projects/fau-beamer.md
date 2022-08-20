---
permalink: /projects/fau-beamer/
title: "fau-beamer"
header:
  overlay_image: /assets/img/fau-beamer/header.png
  overlay_filter: "0.5"
  teaser: /assets/img/fau-beamer/colors.gif
toc: true
toc_sticky: true
---

# A beamer template

<p align="center">
  <img src="/assets/img/fau-beamer/colors.gif" width="1000">
</p>

A LaTeX beamer template according to the 2021 [style guide](https://www.intern.fau.de/kommunikation-marketing-und-corporate-identity/corporate-identity/) of [Friedrich-Alexander-Universität Erlangen-Nürnberg](https://www.fau.de/). 

I created this template in the fall of 2021 to be consistent with the new corporate style of FAU since the provided templates back then were created in Microsoft PowerPoint. After submitting it to the FAU corporate team it became the official LaTeX template of the university. The old template was created by Balthasar Reuther, which after he left FAU was polished by me and can still be accessed on [GitHub](https://github.com/TimRoith/fau-beamer). The new template is written from scratch but reuses some elements and strategies from the old one.

# Where can I find fau-beamer?

There are different ways to use the template, we go over them in the following.

## Via GitHub

The easiest way to use ```fau-beamer``` is to checkout the [GitHub repo](https://github.com/FAU-AMMN/fau-beamer). It is part of the FAU-AMMN GitHub organization of our chair but is managed and maintained by me, so if you have any questions or requests you can either open an issue in the repo or write me a mail.

Also any changes or modifications to the template are incorporated in this repo, therefore it always provides the newest version.

## Via Overleaf

The template is also available on the overleaf gallery, which makes it very easy to use for collaboration. You can access the template [here](https://www.overleaf.com/latex/templates/fau-beamer/zxnnwqfqfhnt). 

Note however that I can not update this template directly and every change to it, has to be approved by overleaf. For this reason it is most likely not the newest version of the template. This shouldn't matter too much, however, if you want the most updated version you should probably checkout the [GitHub repo](https://github.com/FAU-AMMN/fau-beamer).

## Via the FAU website

You can also download the LaTeX code from the corporate website of FAU, [here](https://www.intern.fau.de/kommunikation-marketing-und-corporate-identity/vorlagen/praesentationsvorlagen-powerpoint/). The version provided their is probably the most outdated. This is due to the fact that I can not directly influence any uploads to this website. Nevertheless, I always try to keep the version as close as possible to the actual one.

# <i class="fas fa-cog"></i> Usage and Most Important Options

In the following we briefly explain some important features. The provided example file in the repo provides a mor extensive documentation.

## <i class="fas fa-university"></i> Choosing The Institute

The option ```institute``` specifies which institute template should be used. For example

```LaTeX
\usepackage[institute=FAU]{styles/beamerthemefau}
```

can be used to use the generic FAU style. The following style are available

* ```[institute=FAU]```: Generic style for FAU,

* ```[institute=Med]```: style for Medizinische Fakultät,

* ```[institute=Nat]```: style for Naturwissenschaftliche Fakultät,

* ```[institute=Phil]```: style for Philosophische Fakultät und Fachbereich Theologie,

* ```[institute=RW]```: style for Rechts- und Wirtschaftswissenschaftliche Fakultät,

* ```[institute=Tech]```: style for Technische Fakultät

This option influences

1. the color scheme,

2. the left word mark for the title page

see the sections on colors and logos. The default option is ```[institute=FAU]```.

## <i class="fas fa-paint-brush"></i> Colors

The template employs the color scheme as specified by the FAU style guide. Each institute has two colors a base color and a dark base color. These colors are available via the commands ```\BaseColor``` and ```\BaseDarkColor```

| Institute | ```\BaseColor``` | RGB | ```\BaseDarkColor``` | RGB |
| --------- | ---------------- | --- | ----------------- | --- |
| FAU       | <img src="https://user-images.githubusercontent.com/44805883/169272361-71da6b14-2b6d-454c-ae73-f581dd75640b.png" width="100" height="100"> | 0,47,108 | <img src="https://user-images.githubusercontent.com/44805883/169272896-3e2e90bf-5465-4f9a-afc4-4c0f952a7ce3.png" width="100" height="100"> | 4,30,66 |
| Med       | <img src="https://user-images.githubusercontent.com/44805883/169273738-b598bb45-5538-4b3b-b5ff-b120019e71d6.png" width="100" height="100"> | 0, 163, 224 | <img src="https://user-images.githubusercontent.com/44805883/169273182-326a694e-0511-4e3c-a8d3-523b5b5a72aa.png" width="100" height="100"> | 0, 97, 160 |
| Nat       | <img src="https://user-images.githubusercontent.com/44805883/169273312-2f7d0130-1dd4-44e5-a920-497cbc8a4374.png" width="100" height="100"> | 67, 176, 42 | <img src="https://user-images.githubusercontent.com/44805883/169273381-0f8fcaed-54b1-4fb4-9c60-4b47af35af25.png" width="100" height="100"> | 34, 136, 72 |
| Phil      | <img src="https://user-images.githubusercontent.com/44805883/169273473-6008ad50-2d7f-4ada-b01f-39325940c8bd.png" width="100" height="100"> | 255, 184, 28 | <img src="https://user-images.githubusercontent.com/44805883/169273551-f059d603-75c9-49ed-91cc-610fd83a4a58.png" width="100" height="100"> | 232, 119, 34 |
| RW        | <img src="https://user-images.githubusercontent.com/44805883/169273830-aeec45b8-16f6-436e-8e3c-99b87da42d3a.png" width="100" height="100"> | 200, 16, 46 | <img src="https://user-images.githubusercontent.com/44805883/169273919-371bcf69-9e5d-4070-8e1f-ba1939979f51.png" width="100" height="100"> | 151,27,47 |
| Tech      | <img src="https://user-images.githubusercontent.com/44805883/169273976-d9cd9890-883f-4a1a-9994-b6eae1333492.png" width="100" height="100"> | 119, 159, 181 | <img src="https://user-images.githubusercontent.com/44805883/169274039-0e0f4f96-8f2d-4191-96cd-641332769acb.png" width="100" height="100"> | 65, 116, 141 |


## <i class="fas fa-file-image"></i> Logos

The following files

* ```FAUWortmarkeBlau.pdf```
* ```FAUWortmarkeWhite.pdf```

are the same for every institute and are therefore placed directly in the ```/template-art``` folder. The files for each institute are now placed in the subfolder ```/<Institute>```, where you find


* ```<Institute>Kennung.pdf```
* ```<Institute>KennungWhite.pdf```
* ```<Institute>Title.jpg```

# <i class="fas fa-search"></i> Implementation Details

I plan to note down some thoughts and considerations for the implementation of this template. This might help me and others for future projects. It is empty right now, but I might write down something soon.

# <i class="fas fa-magic"></i> Tips n' Tricks

Some hacks and tricks that are not in the scope of the regular tutorial.

## Table of Contents

If you want to print a table of contents as a overview at the start of your slides you might do something like this

```LaTeX
\begin{frame}{Table of contents}
\tableofcontents
\end{frame}
```

which gives the following result

<p align="center">
  <img src="/assets/img/fau-beamer/toc.png" width="500">
</p>

However, this does not look like the table of content view, at the start of a section

<p align="center">
  <img src="/assets/img/fau-beamer/toc_2.png" width="500">
</p>

where also only the current section is not grayed out. In order to achieve the same look for the main overview toc, we put the respective frame within a group that sets the necessary properties. The following code snippet can be used to do this


```LaTeX
{
\setbeamertemplate{headline}[headline title]
\setbeamertemplate{sidebar left}[sidebar title theme]
\setbeamertemplate{frametitle}[frametitle title]
\setbeamertemplate{footline}[footline title]
\setbeamercolor{background canvas}{bg=BaseColor}
\setbeamercolor{section in toc}{fg=TitleFont}
\setbeamercolor{subsection in toc}{fg=TitleFont}

% toc frame
\begin{frame}{-}
\usebeamerfont{title}%
\hypersetup{linkcolor=TitleFont}
\tableofcontents
\end{frame}
}
```

## Citing and Link color

Sometimes colored links and especially colored citations are a problem because they are the same color as their background. E.g., when you use ```\cite``` in the title of a block it is not properly visible. Furthermore you can not just use ```\textcolor``` or something similar.

In order to change the color such text **locally** you need to redefine the setup within a group,

```LaTeX
{\hypersetup{citecolor=white}{\cite{--}}}
```

If you forget the brackets ```{ }``` to put everything in a group, the color will also changes in other places. 

For reusability, you can use this strategy to define your commands like so

{% raw %}
```LaTeX
\newcommand{\colorcite}[3]{{\hypersetup{citecolor=#1}{\cite[#2]{#3}}}}
```
{% endraw %}

where the first argument is the color, the second additional options for the ```\cite``` command and the third one the reference you want to cite.
