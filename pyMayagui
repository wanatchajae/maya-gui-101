import maya.cmds as cmds
class create_Window(object):
        
    def __init__(self):
            
        self.window = "create_Window"
        self.title = "Create Poly"
        self.size = (400, 200)

        #close an Old Window
        if cmds.window(self.window, exists = True):
            cmds.deleteUI(self.window, window = True)
            
        #create New Window
        self.window = cmds.window(self.window, title=self.title, widthHeight=self.size)
        
        cmds.columnLayout(rs=5, adjustableColumn=True) #to create Space between buttons and the Window can be resize)
        
        #create Text Field to input Sizes
        cmds.text(self.title)
        cmds.separator(height=20)
        
        self.cubeName = cmds.textFieldGrp(label= 'Cube Name: ')
        self.cubeSize = cmds.floatFieldGrp(numberOfFields=3, label='Size: ', value1=1, value2=1, value3=1)
        self.cubeSubd = cmds.intSliderGrp(field=True, label='Subdivisions: ', minValue=1, maxValue=10, value=1)
        
        #create Button for Specific Cube (that you can put the xyz and subdivisions)
        self.specificBt = cmds.button(label='Create Specific Cube',bgc=(0, 0.8, 0.8), height=35, command=self.specificCube)
        
        #create Button for Normal Polygons
        cmds.button(label='Create Normal Cube', height=35, command=create_cube)
        cmds.button(label='Create Normal Sphere', height=35, command=create_sphere)
        cmds.button(label='Create Normal Cylinder', height=35, command=create_cylinder)

        #Display New Window
        cmds.showWindow()
        
    def specificCube(self, *args): #to create Specific Cube)
        name = cmds.textFieldGrp(self.cubeName, query = True, text = True)
        
        width = cmds.floatFieldGrp(self.cubeSize, query = True, value1 = True)
        height = cmds.floatFieldGrp(self.cubeSize, query = True, value2 = True)
        depth = cmds.floatFieldGrp(self.cubeSize, query = True, value3 = True)
        
        subdivs = cmds.intSliderGrp(self.cubeSubd, query = True, value = True)
        
        cmds.polyCube(name=name, width=width, height=height, depth=depth, 
                      subdivisionsWidth=subdivs, subdivisionsHeight=subdivs, subdivisionsDepth=subdivs)
                       
myWindow = create_Window()
