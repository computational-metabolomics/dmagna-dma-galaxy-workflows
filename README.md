# DMA of *D. magna* - Galaxy workflows 

## Overview

The three Galaxy workflows used for the *Daphnia magna* deep metabolome annotation.

These Galaxy workflows were specifically developed to handle and conduct metabolite annotation across the diverse data types generated, encompassing (U)HPLC-HRMS(/MS) and DI-HRMS(MSn) from LC fractionation. By leveraging the extensive replication provided by the experimental workflow, data averaging and filtering were applied to both (U)HPLC-HRMS(/MS) and DI-HRMS(MSn) datasets to ensure that high-quality, reproducible fragment peaks were utilized for various complementary computational metabolite annotation strategies.

**Abbreviations:**
- (U)HPLC-HRMS(/MS): (Ultra)high-performance liquid chromatography-high resolution tandem mass spectrometry
- DI-HRMS(MSn): Direct infusion-high resolution mass spectrometry with multiple-stage fragmentation



## Workflows

The three workflows are:

- **W1 (Galaxy-Workflow-W1_LC-MSMS_DIMS_DIMSn_FRAC_DMA.ga)**: Full (U)HPLC-HRMS(/MS) and DI-HRMS(MSn) from the LC fractionation
- **W2 (Galaxy-Workflow-W2_LC-MSMS_DMA.ga)**: Just (U)HPLC-HRMS(/MS) analysis
- **W3 (Galaxy-Workflow-W3_LC-MSMS_MSM_DMA.ga)**: (U)HPLC-HRMS(/MS) specifically for the analysis of the metabolite standard mixture (MSM) used to assess the performance of the full experimental and computational DMA workflow

## Availability and Access

Complete Galaxy workflows, analysis histories, and detailed tool version information are accessible through the dedicated Galaxy instance at https://dma.galaxy.bham.ac.uk/histories/list_published and https://dma.galaxy.bham.ac.uk/workflows/list_published. The workflows are also downloadable from this repository under the GPL-3.0 license. 

These resources encompass the complete Galaxy workflow analysis; however, re-running all analyses of the DMA of *D. magna*, especially outside of the provided Galaxy instances, would require additional setup due to both the high computational resource demands of this large dataset, as well as software updates to some of the underlying Galaxy tools since the analysis in this manuscript was performed.


## Software and Galaxy tools summary

### Pre-existing software and Galaxy tools

| Project name | Galaxy tools | Galaxy tool code home page | Underlying software code home page | Licence | Language |
|-------------|-------------|----------------------------|-----------------------------------|--------|----------|
| MSnBase | MSnBase.readMSData | https://github.com/workflow4metabolomics/tools-metabolomics | https://www.bioconductor.org/packages/release/bioc/html/MSnbase.html | Underlying software: Artistic-2.0; Galaxy tool: GPL-3.0 | R |
| XCMS | xcms.findChromPeaks; xcms.findChromPeaks Merger; xcms.groupChromPeaks | https://github.com/workflow4metabolomics/tools-metabolomics | http://bioconductor.org/packages/release/bioc/html/xcms.html | GPL (≥2) | R |
| CAMERA | CAMERA.annotate | https://github.com/workflow4metabolomics/tools-metabolomics | https://www.bioconductor.org/packages/release/bioc/html/CAMERA.html | GPL (≥2) | R |
| BEAMSpy | BEAMSpy | https://github.com/computational-metabolomics/beamspy-galaxy | https://github.com/computational-metabolomics/beamspy; https://more.bham.ac.uk/beams/ | GPL-3.0 | R |
| DIMSpy | dimspy.processScans; dimspy.mergePeaklists; dimspy.alignSamples; dimspy.blankFilter; dimspy.getPeaklist | https://github.com/computational-metabolomics/dimspy-galaxy | https://github.com/computational-metabolomics/dimspy | GPL-3.0 | Python |

---

### Software and/or Galaxy tools developed by authors

| Project name | Galaxy tools | Galaxy tool code home page | Underlying software code home page | Licence | Language |
|-------------|-------------|----------------------------|-----------------------------------|--------|----------|
| **msPurity** | msPurity.purityA; msPurity.flagRemove; msPurity.frag4feature; msPurity.filterFragSpectra; msPurity.averageFragSpectra; msPurity.createMSP; msPurity.createDatabase; msPurity.spectralMatching; msPurity.combineAnnotations; msPurity.dimsPredictPurity | https://github.com/computational-metabolomics/mspurity-galaxy | https://www.bioconductor.org/packages/release/bioc/html/msPurity.html | GPL-3.0 | R |
| **MSnPy** | MSnPy.group-scans; MSnPy.process-scans; MSnPy.create-spectral-trees; MSnPy.annotate-trees; MSnPy.convert-spectral-trees | https://github.com/computational-metabolomics/msnpy-galaxy | https://github.com/computational-metabolomics/msnpy | GPL-3.0 | Python |
| **msp2db** | msp2db | https://github.com/computational-metabolomics/dmatools-galaxy | https://github.com/computational-metabolomics/msp2db | GPL-3.0 | Python |
| **CAMERA DIMS** | CAMERA DIMS | https://github.com/computational-metabolomics/dmatools-galaxy | https://github.com/computational-metabolomics/cameraDIMS | GPL (≥2) | R |
| *SIRIUS CSI:FingerID* † | SIRIUS CSI:FingerID | https://github.com/computational-metabolomics/sirius-csifingerid-galaxy | https://bio.informatik.uni-jena.de/software/sirius/ | Underlying software: GNU AGPL; Galaxy tool: GPL-3.0 | Java (Python for Galaxy wrapper) |
| *MetFrag* † | MetFrag | https://github.com/computational-metabolomics/metfrag-galaxy | https://ipb-halle.github.io/MetFrag/ | Underlying software: GPL (≥2); Galaxy tool: GPL-3.0 | Java (Python for Galaxy wrapper) |
| **LC fractionation processor** | LC fractionation processor | https://github.com/computational-metabolomics/lcfrac-galaxy | (all functionality within Galaxy tool) | GPL-3.0 | Python |
| **deconrank** § | deconrank | https://github.com/computational-metabolomics/dmatools-galaxy | https://github.com/computational-metabolomics/deconrank | GPL-3.0 | Python |

---

**Footnotes**:
**bold**: New underlying software and Galaxy tool developed by authors  
†Galaxy tool developed by authors  
§Not used directly in the annotation workflows but used in the directed acquisition workflows described in the supplemental of publication


## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.
