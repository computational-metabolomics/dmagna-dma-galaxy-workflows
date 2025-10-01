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

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.
