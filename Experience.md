# Custom crew specialization/class types and skills

Several mods implement their own custom crew specialization/class types (`ExperienceTrait`) and crew skills (`ExperienceEffect`).

### Why it matters

* **Kerbal Status Effects** [ [forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=183734) | [github](https://github.com/cake-pie/KerbalStatusEffects) ]  
  * Having a comprehensive list of crew specialization types and skills will serve as a useful reference for downstream modders when they define their status effects.  
    * Eligibility of various specialization types (that modder was not previously aware of) to be affected by a status effect.  
      e.g. if `off-duty` status does not apply to `Tourist` (stock), also consider `Civilian` (modded).
    * Target and scope skill changes appropriately.  
      e.g. `off-duty` status should only affect work-related skills and not penalize passive stats like `GeeForceTolerance`
  * For skills that specify `modifiers` or `level`, need to know if larger values are better (e.g. `GeeForceTolerance`) or vice-versa (e.g. `EVAChuteSkill`) in order to compound the effects of multiple status effects correctly.
* **Better Sandbox Specializations** [ [forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=183776) | [github](https://github.com/cake-pie/BetterSandboxSpecializations) ]  
  Among other things, provides an option to give "all crew" SAS abilities in science/sandbox modes (fixes a bug in stock implementation); "all crew" actually excludes some specializations, e.g. `Tourist` (stock) and `Civilian` (modded), need to know if others ought to be excluded as well.

* **Community Trait Icons** [ [forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=162509) | [github](https://github.com/cake-pie/CommunityTraitIcons) ]  
  Consider supporting modded specialization/class types if there is sufficient demand.

---
### Stock KSP

Specializations: Pilot, Engineer, Scientist, Tourist

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| AutopilotSkill |-|-
| ConverterSkill |-|-
| DrillSkill |-|-
| ExternalExperimentSkill |-|-
| FailureRepairSkill |-|-
| FullVesselControlSkill |-|-
| PartScienceReturn | increasing |-
| RepairSkill |-|-
| ScienceResetSkill |-|-
| ScienceSkill |-|-
| SpecialExperimentSkill |-|-
| VesselScienceReturn | increasing |-
| GeeForceTolerance | increasing |- | passive
| EVAChuteSkill |- | decreasing | passive
| EnginePower | increasing? |- | defunct
| FuelUsage | decreasing? |- | defunct
| HeatProduction | decreasing? |- | defunct
| MaxThrottle | increasing? |- | defunct

---
### USI Modular Kolonization System

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=154587)] [[github1](https://github.com/UmbraSpaceIndustries/UmbraSpaceIndustries)] [[github2](https://github.com/UmbraSpaceIndustries/MKS)]  
Specializations: Kolonist, Biologist, Farmer, Geologist, Mechanic, Medic, Miner, Quartermaster, Scout, Technician

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| AgronomySkill |-|-
| BotanySkill |-|-
| ExplorerSkill |-|-
| GeologySkill |-|-
| LogisticsSkill |-|-
| MedicalSkill |-|-
| FundsBoost |-|-
| RepBoost |-|-
| ScienceBoost |-|-

---
### Progressive Colonization System

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=181852)] [[github](https://github.com/SteveBenz/ProgressiveColonizationSystem)]  
Specializations: Biologist, Farmer, Geologist, Mechanic, Miner, Technician (interoperates with MKS)

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| PksConstructionSkill |- | decreasing
| PksFarmingSkill |- | decreasing
| PksHydroponicsSkill |- | decreasing
| PksManufacturingSkill |- | decreasing
| PksScanningSkill |- | decreasing
| PksScroungingSkill |- | decreasing

---
### Extraplanetary Launchpads

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=54284)] [[github](https://github.com/taniwha/Extraplanetary-Launchpads)]  
Specializations: -

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| ELConstructionSkill |-|-
| ELSurveySkill |-|-

---
### Ground Construction / Global Construction

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=154167)] [[github](https://github.com/allista/GroundConstruction)]  
Specializations: -

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| ConstructionSkill |-|-

---
### Terras Ignotas

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=179652)] [[github](https://github.com/KSP-DDR/Terras-Ignotas)]  
Specializations: LeptonSailor

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| TIInterstellarSkill |-|-

---
### Better Sandbox Specializations

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=183776)] [[github](https://github.com/cake-pie/BetterSandboxSpecializations)]  
Specializations: -

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| SandboxAutopilotSkill |-|-

---
### Civilian Population

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=162204)] [[github](https://github.com/rleroy/CivilianPopulation)] Pamynx  
[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=143823)] [[github](https://github.com/maanderson22/CivilianPopulationRevived)] Tralfagar (Newbier Newb's)  
[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=140127)] [[github](https://github.com/GGumby/CivilianPopulationRevived)] GGumby  
[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=111815)] [[github](https://github.com/rabidninjawombat/CivilianPopulation/)] rabidninjawombat  
[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=101058)] michaelhester07  
Specializations: Civilian

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| SpecialistClass |-|- | Appears to be for testing only

---
### Colonists!

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=149488)] [[github](https://github.com/maculator/Colonists-)] (defunct?)  
Specializations: Colonist

---
### New Mod Template

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=)] [[github]()]  
Specializations: todo

| Skill | modifiers | level | Remarks |
|-------|-----------|-------|---------|
| todo

---
