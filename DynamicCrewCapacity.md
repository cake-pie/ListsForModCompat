# Parts with dynamic crew capacity 

Modded parts that are deployable / inflatable or otherwise have a crew capacity that can change depending on circumstances.

### Why it matters

* **AirlockPlus** [ [forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=160268) | [github](https://github.com/cake-pie/AirlockPlus) ]  
Normally allows airlocks to be used even if the part has zero crew capacity, or is full. For example, on the stock Velocitize craft, the airlock on the Mk1 cockpit can be used by crew in the crew cabin even when the cockpit is occupied -- looking at the IVA, the airlock can be accessed without disturbing the pilot. Straightforward for static/rigid parts, but deployable/inflatable parts complicate matters due to the variety of logical possibilites. New code will be needed to accomodate these; more use cases would justify the time and effort required for implementation.
  * Require part deployed and crew capacity available  
    e.g. Inflatable Airlock from Making History DLC.  
    The part must be in deployed position for the airlock to be usable. Furthermore, the airlock must be free for a kerbal to pass through -- if there is already another kerbal in the airlock, you can't just squeeze past them.
  * Require part deployed, but disregard crew capacity  
    e.g. An airlock connected to the inflatable section of an inflatable module  
    Before the part has been deployed, the airlock leads to a solid wall and is not usable. However, once the part is deployed, even when there are other kerbals seated in the part, there is plenty of space to move around them, so airlock can be used freely to access other parts of the craft without disturbing the occupants of the module.
  * Don't require deployment to use  
    e.g. An airlock connected to the rigid central hub of a module that has an inflatable outer ring  
    Even without deploying the inflatable section, the airlock leads to a rigid section of the module. It doesn't matter if the module has zero crew capacity (seating places) when not deployed as long as the kerbal can "pass through" it and gain access via connected nodes to reach the rest of the craft.

* **Connected Living Space** [ [forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=109972) | [github](https://github.com/codepoetpbowden/ConnectedLivingSpace) ]  
Needs to adjust to reflect changes in the crew capacity of a part.  
Works with stock KSP 1.4+ [`ModuleAnimateGeneric.CrewCapacity`](https://kerbalspaceprogram.com/api/class_module_animate_generic.html#a0b9e3c3d6e5c62c6be229ab8333064bc) since [ConnectedLivingSpace#100](https://github.com/codepoetpbowden/ConnectedLivingSpace/pull/100). Interoperability with other custom plugin `PartModules` needs investigation. Have modded parts migrated to `ModuleAnimateGeneric.CrewCapacity` or are they using their own bespoke plugins?

---
### Making History DLC

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| InflatableAirlock | `ModuleAnimateGeneric` | Y | Y |

---
### Stockalike Station Parts Expansion Redux

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=170211)] [[github](https://github.com/ChrisAdderley/StationPartsExpansionRedux)]

[`ModuleDeployableHabitat`](https://github.com/ChrisAdderley/StationPartsExpansionRedux/blob/master/Source/HabUtils/ModuleDeployableHabitat.cs)  
[`ModuleDeployableCentrifuge`](https://github.com/ChrisAdderley/StationPartsExpansionRedux/blob/master/Source/HabUtils/ModuleDeployableCentrifuge.cs) : `ModuleDeployableHabitat`

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| sspx-inflatable-hab-125-1 | `ModuleDeployableHabitat` |n/a|n/a|
| sspx-inflatable-hab-125-2 | `ModuleDeployableHabitat` |n/a|n/a|
| sspx-inflatable-hab-125-3 | `ModuleDeployableHabitat` |n/a|n/a|
| sspx-inflatable-hab-25-1 | `ModuleDeployableHabitat` |n/a|n/a|
| sspx-inflatable-hab-25-2 | `ModuleDeployableHabitat` |n/a|n/a|
| sspx-inflatable-centrifuge-125-1 | `ModuleDeployableCentrifuge` |n/a|n/a|
| sspx-inflatable-centrifuge-125-2 | `ModuleDeployableCentrifuge` |n/a|n/a|
| sspx-inflatable-centrifuge-25-1 | `ModuleDeployableCentrifuge` |n/a|n/a|
| sspx-expandable-centrifuge-375-1 | `ModuleDeployableCentrifuge` |n/a|n/a|
| sspx-expandable-centrifuge-375-2 | `ModuleDeployableCentrifuge` |n/a|n/a|

---
### USI Modular Kolonization System

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=154587)] [[github](https://github.com/UmbraSpaceIndustries/MKS)]

[`USIAnimation`](https://github.com/UmbraSpaceIndustries/UmbraSpaceIndustries/blob/master/USITools/USITools/USIAnimation.cs)

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| KER_Shelter | `USIAnimation` | Y | N |
| Ranger_MiniHab | `USIAnimation` | Y | N |
| Ranger_HabModule | `USIAnimation` | Y | N |
| Ranger_Workshop | `USIAnimation` | Y | N |
| Ranger_AgModule | `USIAnimation` |n/a|n/a|
| Tundra_275_Hab | `USIAnimation` |n/a|n/a|
| Tundra_425_Hab | `USIAnimation` |n/a|n/a|
| Tundra_HabRing | `USIAnimation` |n/a|n/a|

---
### Angel-125 / WildBlueIndustries

WildBlueTools: [[github](https://github.com/Angel-125/WildBlueTools)]

[`WBIInflatablePartModule`](https://github.com/Angel-125/WildBlueTools/blob/master/Parts/WBIInflatablePartModule.cs)  
[`WBIResourceSwitcher`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIResourceSwitcher.cs) : `WBIInflatablePartModule`  
[`WBIModuleSwitcher`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIModuleSwitcher.cs) : `WBIResourceSwitcher`  
[`WBIAffordableSwitcher`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIAffordableSwitcher.cs) : `WBIModuleSwitcher`  
[`WBIConvertibleStorage`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIConvertibleStorage.cs) : `WBIAffordableSwitcher`  
[`WBIOpsManager`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIOpsManager.cs) : `WBIConvertibleStorage`  
[`WBIMultiConverter`](https://github.com/Angel-125/WildBlueTools/blob/master/Converters/WBIMultiConverter.cs) : `WBIOpsManager`  
[`WBIConvertibleMPL`](https://github.com/Angel-125/WildBlueTools/blob/master/Switchers/WBIConvertibleMPL.cs) : `WBIMultiConverter`  

#### Pathfinder

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=121397)] [[github](https://github.com/Angel-125/Pathfinder)]  

[`WBICoolingTower`](https://github.com/Angel-125/Pathfinder/blob/master/Pathfinder/Parts/WBICoolingTower.cs) : `WBIInflatablePartModule`  
[`WBIMultipurposeStorage`](https://github.com/Angel-125/Pathfinder/blob/master/Pathfinder/Utility/WBIMultipurposeStorage.cs) : `WBIMultiConverter`  
[`WBIMultipurposeHab`](https://github.com/Angel-125/Pathfinder/blob/master/Pathfinder/Habitat/WBIMultipurposeHab.cs) : `WBIMultiConverter`  
[`WBIMultipurposeLab`](https://github.com/Angel-125/Pathfinder/blob/master/Pathfinder/Science/WBIMultipurposeLab.cs) : `WBIMultipurposeHab`  
[`WBIPackingBox`](https://github.com/Angel-125/Pathfinder/blob/master/Pathfinder/Parts/WBIPackingBox.cs) : `WBIMultipurposeLab`

(Bundles MCM, Buffalo)

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| WBI_SmokePipe | `WBICoolingTower` |?|?|
| WBI_Chuckwagon | `WBIMultipurposeStorage` |?|?|
| WBI_Hacienda | `WBIMultipurposeHab` |?|?|
| WBI_Ponderosa | `WBIMultipurposeHab` |?|?|
| WBI_Ponderosa2 | `WBIMultipurposeHab` |?|?|
| WBI_DocSciLab | `WBIMultipurposeLab` |?|?|
| wbiArcReactor | `WBIPackingBox` |?|?|
| wbiCastilloAdapter | `WBIPackingBox` |?|?|
| wbiCastilloFactory | `WBIPackingBox` |?|?|
| wbiCastilloObservatory | `WBIPackingBox` |?|?|
| wbiDrillingRig | `WBIPackingBox` |?|?|
| wbiGroundStation | `WBIPackingBox` |?|?|
| wbiPipeline2 | `WBIPackingBox` |?|?|
| wbiRanchHouse2 | `WBIPackingBox` |?|?|
| wbiRangeland2 | `WBIPackingBox` |?|?|
| wbiStorageDepot | `WBIPackingBox` |?|?|
| wbiWalkway1X | `WBIPackingBox` |?|?|
| wbiWalkway2X | `WBIPackingBox` |?|?|

#### Multipurpose Colony Modules for Pathfinder

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=88605)] [[github](https://github.com/Angel-125/MCM)]

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity | Remarks |
|------|------------------|:---------------------:|:---------------------:|---------|
| WBI_HomesteadMk2 | `WBIMultipurposeLab` |?|?|
| WBI_Stockyard2502 | `WBIInflatablePartModule` |?|?| No crew capacity
| WBI_Stockyard3752 | `WBIInflatablePartModule` |?|?| No crew capacity

#### Buffalo

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=122617)] [[github](https://github.com/Angel-125/Buffalo)]

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity | Remarks |
|------|------------------|:---------------------:|:---------------------:|---------|
| WBI_Wagon2u | `WBIConvertibleStorage` |n/a|n/a| No crew capacity

#### Mark One Laboratory Extensions

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=154893)] [[github](https://github.com/Angel-125/MOLE)]

(Uses modules that support inflation on non-inflated parts.)

---
### Tokamak Industries Refurbished Parts

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=163166)] [[github](https://github.com/linuxgurugamer/Tokamak-Refurbished-Parts)]

[`DeployableHabitat`](https://github.com/linuxgurugamer/Tokamak-Refurbished-Parts/blob/master/PJHabitat/DeployableHabitat.cs)

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| centrifugeSmall | `DeployableHabitat` | N | N |
| TIinflato1 | `DeployableHabitat` | N | N |
| TIinflato2 | `DeployableHabitat` | N | N |
| TIinflatoFlat | `DeployableHabitat` | Y | N |

---
### Kerbalow Aerospace Inflatable / Expandables Parts Pack

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=172622)] [[spacedock](https://www.spacedock.info/mod/1755/Kerbalow%20Aerospace)]

Unable to load and verify due to missing models.  
From configs, these do not appear to actually implement dynamic crew capacity.

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| KEAM | `ModuleAnimateGeneric` |||
| KA330exterior | `ModuleAnimateGeneric` |||

---
### Ven's Stock Revamp 

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=83696)] [[github](https://github.com/Kerbas-ad-astra/Stock-Revamp)]

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| todo ||||

---
### New Mod Template

[[forum](http://forum.kerbalspaceprogram.com/index.php?showtopic=)] [[github]()]

| Part | Animation Module | Airlock req. deployed | Airlock req. capacity |
|------|------------------|:---------------------:|:---------------------:|
| todo ||||
