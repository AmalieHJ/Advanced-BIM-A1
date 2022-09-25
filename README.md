# 41934 Advanced BIM, Assignment 1
## Group 16: Isabella Vad (s183616) and Amalie Hartvig Jensen (s183619)

**Chosen use case**

Finding a model's material CO2 emission contribution in a Life Cycle Assessment (LCA) is chosen as the project use case, as minimising CO2 emissions is a highly prioritised field in the building industry with yet further development potential. 
Today, LCA is to be found in all aspects of the built environment. This is mainly due to the coming law regulation of CO2 emissions on buildings starting in 2023. 
It is currently time consuming to perform an LCA model as well as gathering the right LCI (Life Cycle Inventory) from the building model. 
In order to make sure that the law regulations are met when the building is complete, iterative and continuously CO2 check points are beneficial. But due to the time spent on making an LCA it is not realistic to make iterative LCA checks for the time being. 
With our chosen use case within LCA, the goal is to make a script that links CO2 emissions from building materials to elements within an IFC model, thus enabling quick comparison of LCA climate impact for different choice of material within the model.  

The use case only relate to choice of materials within the LCA. Thus it does not take the energy frame into account which is normally part of the LCA. 
The IFC model does not contain information on source of energy for the building. Additionally, it is assumed that the energy supply varies only little as a cause of using different building skin materials, why the change in contribution is insignificant for the overall LCA results. It is assumed that the IFC model satisfies the requirements of the Danish building regulations (BR18). 
 
**Stakeholders of the use case**

The use case recipients are primarily consulting engineers but other stakeholders such as architects or the contractor could also find it useful. 
The engineers would be able to interpret the LCA results directly from above mentioned script run on an IFC model. From different design proposals relating to shift in materials, the script would quickly highlight the more sustainable choice of materials. 
This would be an arguement for the contractor to use in the decision making processes on material choices. 
Furtermore, the script might also be introduced to the architects to guide the iterative design processes towards sustainable material choices early on in the building project's early design phase. 

**Disciplinary expertise used to solve the use case**

LCA was the non BIM disciplinary expertise used to solve the use case. 

**IFC concepts in the script**

All physical entities and properties that affect CO2 emissions would be used in the script. That is:
- *Area*: for the analysis output unit of *kg CO2-eq per m^2 per year*.   
- *Element dimensions*: to calculate the volume of the elements
- *Element materials*: to find the CO2-emissions of the elements

**Disciplinary analysis required**

Obviously a Life Cycle Analysis is required for the chosen use case. 

**Building elements**

All physical elements in the building model are of interest in the use case. 

**Dependency on other use cases**

The use case is dependent on several other use cases such as structural, acoustics, fire, daylight, indoor climate and architecture as these cases impact choice of materials and thus evidently influence the LCA results.

The structural analysis reveal dimensions of the load-bearing structures thus the material quantities. As different materials hold different carrying capacities, the choice of structural material may have a huge influence on material quantities used. 

Both acoustics and fire may introduce elements such as acoustic panels and fire retardants respectively to be included in the LCA.  
Likewise, indoor climate provide the systems such as ventilation channels that should also be included in the LCA.

Daylight decides on number and type of openings that influence the energy frame. In spite of neglecting the energy aspect in our use case, the choice and number of windows still affect the LCA on materials. 

Finally, the architecture establish the aesthetic arguments on choice of material.   

**Input data for use case**

Area (m^2) and Volume (m^3).

**Other use cases dependent on our use case**

The use cases waiting for our use case to complete are:
- *Costs*: The more sustainable choice of material is not neccessarily the most cost effective one. 
- *Code validation*

NOTE til vedligehold: kan man flette materialerne levetider ind ift potentiel udskiftning i bygningens levetid?? (hvis et materiale skal udskiftes én gang i bygningens levetid da vil CO2 udledningen tælle dobbelt!).

