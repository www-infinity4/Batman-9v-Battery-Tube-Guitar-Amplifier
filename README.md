# Batman 9V Battery Tube Guitar Amplifier

Research/build-data repository for a genuinely low-voltage, battery-oriented tube guitar amplifier.

## Historical design trail

The starting point is Kris/KJW's 2013 Antique Radio Forums guitar-amplifier experiments and the replies from Flipperhome. That work documented practical battery-amp concerns including LM386 gain/tone control, supply bypassing, end-of-note "fizzle", battery drain, oscillation/layout, speaker loading, and the danger of exceeding an LM386's supply rating.

The tube branch follows late-1950s low-voltage car-radio practice rather than pretending a conventional high-B+ guitar tube works normally from 9 V. Period car-radio families included low-voltage/space-charge designs intended to operate around a 12-V electrical system.

## Candidate tube architecture

The strongest documented low-voltage guitar-amp lineage found so far is the Sopht-style approach:

- **12U7** — low-voltage dual-triode voltage-gain/preamp candidate.
- **12K5** — low-voltage space-charge power tetrode candidate designed for 12-V car-radio service.
- One low-voltage supply can conceptually serve heater and B+ in the 12-V design family.
- Published experiment measurements put a single 12K5 guitar-amp implementation in the tens-of-milliwatts range at 12 V, so speaker efficiency matters greatly.

The 12K5 is especially important because Antique Radio Forums discussion identifies it as a power tetrode specifically designed for 12-V car-radio use. Other forum material documents 1957–62-era car radios using space-charge tubes with roughly 12 V on their plates.

## 9-V constraint

"9V" is the Batman product constraint, but it is **not yet an assumption that a rectangular PP3 battery directly powers a 12K5 correctly**. The historical tube architecture is nominally 12 V. A production design therefore needs measured validation of one of these paths:

1. a suitable battery pack whose nominal system voltage matches the tube design;
2. a regulated 9-V-to-12-V conversion stage sized for heater + plate current; or
3. a different tube set with verified operating curves at the chosen battery voltage.

The build must not silently over-voltage heaters or rely on ordinary high-voltage tubes at operating points unsupported by their data.

## Build-data goals

- Preserve KJW/Flipperhome battery-amp lessons.
- Favor true low-voltage tube operation.
- Measure current draw, runtime, gain, clipping onset, frequency response and output power.
- Treat supply bypassing and physical layout as first-class requirements.
- Match the output transformer and speaker to the measured tube operating point.
- Prefer a high-efficiency speaker because expected output is intentionally small.
- Keep high-voltage boost designs separate from the native-low-voltage Batman baseline.

## Research sources

- Antique Radio Forums, **LM386 Guitar Amp Pots** (KJW + Flipperhome): https://antiqueradios.com/forums/viewtopic.php?t=226614
- Antique Radio Forums, **Assistance requested with a superhet build**: discussion identifies 12K5 as a power space-charge tube designed specifically for 12-V car-radio service.
- Antique Radio Forums, **Which Car Radios Worth Saving?**: historical discussion of 12-V space-charge car-radio designs.
- Antique Radio Forums, **70.7 V line transformers as output xfmrs & voltage concerns**: Flipperhome's practical output-transformer observations.
- Sopht low-voltage amplifier material (archived/republished): experimental 12U7/12K5 guitar-amplifier lineage.

## Status

This repository currently stores the research baseline. Component values and a final schematic should be promoted to the build specification only after the operating point is checked against tube data and bench measurements.
