# wfip3-noreaster-analysis
In this project, we analyze wind data from profiling lidars deployed during the Third Wind Forecast Improvement Project (WFIP3; https://psl.noaa.gov/renewable_energy/wfip3/):

Block Island (BLOC) — Rhode Island

Martha’s Vineyard (MVCO) — Massachusetts

Nantucket (NANT) — Massachusetts

Public data portals:
BLOC: https://wdh.energy.gov/ds/wfip3/bloc.lidar.z03.c0

MVCO: https://wdh.energy.gov/ds/wfip3/mvco.lidar.z03.c0

NANT: https://wdh.energy.gov/ds/wfip3/nant.lidar.z01.c0

More datasets will be incorporated as the project progresses.

The lidar datasets vary in both time and height. For BLOC and MVCO, the sampling interval is roughly 2 minutes, the vertical resolution is about 20 meters, and measurements span from ~40 meters to ~220 meters above ground level. Each record at these sites is already a 2-minute scalar average provided in the dataset. For NANT, the sampling interval is ~30 seconds, the vertical resolution is ~26 meters, and heights range from ~91 meters up to ~5 kilometers.

The project goal is to characterize wind-flow behavior during the January 9-11, 2024 nor’easter, a severe storm that strongly affected the region. We examine how the observed flow compares with standards-related quantities used in wind-turbine (WT) design. To frame the analysis, we reference the onshore IEA 3.4-MW WT (https://nrel.github.io/turbine-models/IEA_3.4MW_130_RWT.html), which has a 130-meter rotor diameter and a 110-meter hub height.

The repository includes a Python script (i.e., wfip3_analysis.py) that performs the analysis and requires standard scientific Python libraries (e.g., NumPy, pandas, matplotlib). The script computes probability-density distributions for several flow variables and compares them with standard WT metrics. It expects the WFIP3 data files to be located in the same directory, and each dataset is provided as one file per day.
