# Day 2 AAS

## Starlight Suppression Workshop
Discuss current status of star suppression tech for HWO

**Requirements**
- 1e-10 Contrast
- Picometer Stability

### Decadal Survey & the HWO: Bruce Macintosh
Is a dog person, massive green flag. This talk will be simmilar to ExoPAG talk.

Context
- We can't cover everything now, let's be flexible about the approach
- JWST/Roman brought a lot of uncertainty, but things are going well
- Habex/Luvoir teams got us started!
- $11 billion total, need to meet this budget

Eta_Earth
- 25 planet spectra will help constrain uncertainty
- uncertainty in this was baked into the Decadal report

Technology Limits
- The coronagraph is actually not the hard part
- Telescope stability is more concerning!
    - Can we build coronagraphs that aren't sensitive to spontaneous misalignments?

### Tracing Exoplanet Science Requirements to Mission Requirements for HWO: Chris Stark
Science Traceability Matrix: turns out everyone hates it!

Ballparking Mission Requirements for Exoearth spectroscopy
- Contrast ~1e-10
- Noise ~1e-11
- OWA ~ 50 L/D
- IWA ~ 1.7 LD (not sure about this one)
- AH MISSED IT I wonder if he would be willing to share slides

Need for a flexible DRM as the mission matures
- STM is quite static
- DRM would allow us to establish and update as trade studies are ongoing
- Exoplanet DRM's started with TPF
- "Obscurational Completeness" (Brown 2004)
- Equally important is how you use the observatory! Optimize observations

Stark et al 2015
- Use toy models of coronagraphs/missions to map sensitivities
- Yield is most sensitive to aperture
- Limiting Magnitude is a huge cliff to fall off

DRM's have come a long way
- Reflectivity of coatings matters a lot!
- Trade bandwidth for throughput, UV coronagraphy reduces throughput at all wavelengths by up to 0.5
- Efficiently parallelizing coronagraphs may be essential for wavelength coverage
- Simulating independent time series into the coronagraph and computing the residuals after the PSF subtraction
    - Juanola-parramon 2022, Portier 2022
    - Connecting engineering models to coronagraph, complete loop of engineering model with science yield

Exoplanet Yields aren't everything
- Spectral quality / coverage
- Exposure times
- WFSC times
- Orbit retrieval
- Schedulability

Opportunities for improvement
- WFS-based PSF subtraction
- PIAA / other high-throughput coronagrpahs
- Parabolic DM's

### Starlight Suppression Tech for LUVOIR and HABEX: Rhonda Morgan (JPL)
Two main tech
- Coronagraph, img of VVC
    - challenge: precision optics
- Starshade
    - challenge: formation flying

LUVOIR (3.5 - 64 L/D for UV-VIS-IR)
- APLC for on-axis
    - High throughput hard
- VVC for off-axis
    - Favorable!
- Segments for both have ultra-stability plans

HabEx (2.4 - 32 L/D)
- VVC
- Why did it need a coronagraph + starshade?
    - starshades aren't that chromatic
    - small IWA
    - Have to transit to get to different stars!
- Laser metrology, coating, + monoliths are TRL 4
- Starshade-only case
    - Relax tolerances by 1000x, can be on-axis

~got distracted looking at Ewan's notes

### Recent Advances in Starlight Suppression Technologies :Bertrand Menneson
COVID advances! 

HWO Musts!
- dmag > 25 at < 70mas from FGK stars
- 2.1 L/D at 950nm and D = 6m

What have we done in the lab?
- HCIT got to 4e-10 contrast for 1 polarization
- How long can the coronagraph hold this contrast?
- getting a few times 10e-9
- Obscured / segmented apertures are being done by Soummer at HiCAT
    - PAPLC with knife-edge
    - getting a few times 10e-8 in air
    - PIAACMC getting a few times 10e-8 in vacuum

Current limitations
- Coronagraphs are well-known, going to be demonstrated with Roman, need nimble pointing
- Combination of required contrast, bandwidth, and IWA not yet demonstrated
- Best performance significantly worse when switching 
- uv coronagraphy is uniquely challenging

Near term priorities for improving technical readiness
- 

Starshade latest performance
- Starlight suppression, scattered sunlight, formation flying, shape accuracy
- Princeton results with a huge tunnel to get F = 13
- IWA is 1.7 L/D
- Can't be tested at scale from the ground
- No in space demo planned

Near-term priorities for improving starshades
- consider cubesat-level starshade?
- Need more overall technology maturation for starshades

### Future of Starlight Suppression Technologies : Olivier Guyon
He got his mic fixed!

Wish List
- Deeper contrast
- Higher throughput
- Smaller IWA
- Larger OWA
- Wider spectral range
- High spectral resolution
- Spectro-astrometry

Chromatic Problems
- Shorter wavelengths require more wavefront control
- Longer wavelengths have larger IWA

Key Enabling Technologies
- Photon-counting detectors
- Optical Manufacturing
    - Large optics
    - Coronagraph masks
    - Deformable mirrors
    - Microlenses, fibers

Wavefront Control Algorithms
- Predictive Control / sensor fusion (LDFC)
- Continuous wfsc without dm probing

Coronagraph + Fundamental Limits
- Theoretical coronagraph has 1/2x in IWA than current designs
- We are quite close! Can we get closer?
    - PIC's with photonic nulling make Olivier's idea possible
    - Interferometer approach to starlight suppression
- GLINT Nuller Testbed
    - Null output!

### New Initiatives of ExEp : Pin Chen

Coronagraph Technology Roadmap Development
1) Create a roadmap for coronagraph tech to get to TRL 5, and describe path to TRL 6
2) inform NASA on reccomendations for investment in technology
- Pin Chen, Laurent Pueyo
- Full model of Coronagraph (WFE, WFSC, Detectors, Post-processing)

DM Technology
- Same bullets as above

Coronagraph Architecture Survey
- Database of coronagraph architectures
- Went quick on this slide and missed it

Segmented OTA
- Need simulator that integrates into testbed to generate dynamic WFE
- Consider asking Rus and Chris Stark about **Coronagraph Architecture Survey**

### Q&A / Discussion Session

Q: Are we doing a monolith or a segmented aperture? State of the art for both are very different in TRL. To what extent are the challenges we face for segmented aperture shared with monoliths + how does our work on monoliths help us if we decide to go segments?
- A: (Pin) Typical design is geared toward quasi-static aberrations driving requirements. If segments are generally moving, we need more integrated modeling tools!

Q: (Aki) Can Olivier explain the Photonic Nulling's limits?
- A: Implementing the coronagraph as a nulling interferometer, kinda like TPF-I. Gives more flexibility so that's how we get closer in. But if you want a large OWA it doesn't quite work
- Null depth in broadband light has not been demonstrated

Q: (Bruce) Hi I'm worried because of bertrand's talk
- A: (Bertrand) Happy to curb your enthusiasm
- A: (Bertrand) Yeah we are far behind! We gotta try segmented in vacuum.

Q: (Lee Feinberg) We were at TRL 3-4 with JWST when we started, we did a bunch of competetive trades with people working 7 days a week with long days.
- Um?

