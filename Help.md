| **Name** |  **Status** | Stable | Work but need more test | Nightly | **Updated by** |
| --- | --- | --- | --- | --- | --- |
| **Matrix By Object** | **Version** | 1.4 | 2.0 | 2.x | Mathias PFAUWADEL |

# Description:
Allow you to display matrix of association between objects that are connected too a father object.
You can display properties of association in cells. This layout is for object page.

# Screenshot:
![](https://raw.githubusercontent.com/nevakee716/cwLayoutMatrixByObject/master/screen/layoutExemple.png)

#Options

## Custom Association Properties Display
Use the field inside Layout Custom Matric by Object to set what properties of the association you want to see.
Use the following syntaxe: 
SCRIPTNAME1:nameToDisplayIfCheckBoxCheck, SCRIPTNAME2:nameToDisplayIfCheckBoxCheck...
If you don’t put nameToDisplayIfCheckBoxCheck, the layout will display the property name if it’s a checkbox or the value of the property in other case.

## Connection-policy
Display only objects that are connected to the father object
If for exemple we have the following metamodel
Process -> Organisation -> Activity
If this options is check it will display, only the Organisation and the activity that are associated to the Process of the object page


#Exemples 

## Standard Case

Here we have a process lvl 2, which is associated to some process lvl3 which are associated to application
We want to display the matrix between the process lvl3 and the application.
Here is the following configuration.

![](https://raw.githubusercontent.com/nevakee716/cwLayoutMatrixByObject/master/screen/simple_config.png)


## Object that describe a diagram

Here we have a process, that is described by a diagram, we have some activity and organisation on the diagram.
We want to display the matrix of the association between the activity and the organisation that are on the diagram.
We also want to display property RACI of the association.

Here is the following configuration.
![](https://raw.githubusercontent.com/nevakee716/cwLayoutMatrixByObject/master/screen/evolve_interface.png)

don't forget to add the property of the intersection you want to display
![](https://raw.githubusercontent.com/nevakee716/cwLayoutMatrixByObject/master/screen/evolve_interface2.png)

#Changing CSS

You customize some parameter of the CSS to have the display you want 
C:\Casewise\Evolve\Site\bin\webDesigner\custom\Marketplace\libs\MatrixByObject\src\cwLayoutMatrixByObject.less
for exemple, you can change the font size of the property text, by adding font-size: 10px; in .cellChecked





