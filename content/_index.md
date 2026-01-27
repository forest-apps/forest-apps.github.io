---
title: Hextra Theme
layout: hextra-home
---

<div class="hx-mt-6 hx-mb-6">
{{< hextra/hero-headline >}}
   Design, Modelling and Analysis Tools for Naval Architecture and Ocean Engineering
{{< /hextra/hero-headline >}}
</div>

<div class="hx-mb-12">
{{< hextra/hero-subtitle >}}
  Forest Apps is a collection of practical software tools and numerical utilities developed for naval architects, ocean engineers, and offshore engineers. 
  The site focuses on engineering-oriented workflows, efficient modelling, and reproducible analysis, supporting both preliminary design and research activities in marine and offshore engineering.

  <br/>
  
  We provide lightweight, engineer-friendly applications covering key analysis tasks commonly encountered in floating offshore structures, marine renewable energy, and ship & offshore system design.The tools are designed to complement commercial software by offering open, inspectable, and extensible implementations suitable for education, research, and early-stage engineering studies.
{{< /hextra/hero-subtitle >}}
</div>

<div class="hx-mb-6">
{{< hextra/hero-button text="Contact us via email: forestapps@hotmail.com" link="about" >}}
</div>

<div class="hx-mt-6"></div>

{{< hextra/feature-grid cols="2">}}

  {{< hextra/feature-card
    title="DP Capability Tool"
    subtitle="Evaluate the **station-keeping capability** of DP vessels under combined wind, wave, and current loads. The tool generates **DP capability plots** (**rose plots**) to support operability assessment and to identify limiting environmental conditions. Both **feasibility calculations** and DP capability analysis are supported for **intact conditions** and defined **failure modes**, with built-in utilities aligned with **DNVGL-ST-0111** and **ABS DP guidelines**" 
    link="/dp_capability_tool"
    class="hx-aspect-auto md:hx-aspect-[1.1/1] max-md:hx-min-h-[340px]"
    image="images/dp_image_01.webp"
    imageClass="hx-top-[40%] hx-left-[24px] hx-w-[180%] sm:hx-w-[110%] dark:hx-opacity-80"
    style="background: radial-gradient(ellipse at 50% 80%,rgba(194,97,254,0.15),hsla(0,0%,100%,0));"
  >}}

  {{< hextra/feature-card
    title="Wave Scatter Diagram Tool"
    subtitle="The Wave Scatter Diagram Tool generates **global wave scatter diagrams** in accordance with **DNVGL-RP-C205**. It uses the DNV-recommended Conditional Modelling Approach (CMA) to estimate sea state occurrence for different navigational zones, supports Weibull and Log-Normal distributions for HS and TZ(**Nautic zones**, **North Atlantic** and **World Wide trade**), allows user-defined bin settings, and enables export of data and figures for direct use in reports." 
    link="/wave_scatter_diagram"
    class="hx-aspect-auto md:hx-aspect-[1.1/1] max-md:hx-min-h-[340px]"
    image="./images/Snipaste_2026-01-27_10-06-43.png"
    imageClass="hx-top-[40%] hx-left-[24px] hx-w-[180%] sm:hx-w-[110%] dark:hx-opacity-80"
    style="background: radial-gradient(ellipse at 50% 80%,rgba(194,97,254,0.15),hsla(0,0%,100%,0));"
  >}}
  
  {{< hextra/feature-card
    title="HydroModeller"
    subtitle="Cloud-based panel model and Morison model modelling tool for hydrodynamic analysis of typical floaters."
    link="/hydro_modeller"
    class="hx-aspect-auto md:hx-aspect-[1.1/1] max-lg:hx-min-h-[340px]"
    image="images/hm_deepcwind.webp"
    imageClass="hx-top-[40%] hx-left-[36px] hx-w-[180%] sm:hx-w-[110%] dark:hx-opacity-80"
    style="background: radial-gradient(ellipse at 50% 80%,rgba(142,53,74,0.15),hsla(0,0%,100%,0));"
  >}}
  
  {{< hextra/feature-card
    title="FreeFloating"
    subtitle="Free 3D modeling tool for wave diffraction and radiation analysis, utilizing the open-source solver HAMS."
    link="/free_floating"
    class="hx-aspect-auto md:hx-aspect-[1.1/1] max-lg:hx-min-h-[340px]"
    image="images/ff_image_01.webp"
    imageClass="hx-top-[40%] hx-left-[36px] hx-w-[180%] sm:hx-w-[110%] dark:hx-opacity-80"
    style="background: radial-gradient(ellipse at 50% 80%,rgba(142,53,74,0.15),hsla(0,0%,100%,0));"
  >}}
{{< /hextra/feature-grid >}}
