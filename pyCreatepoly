import maya.cmds as cmds
#to Create Polygons

def create_cube(*args):

    cube = cmds.polyCube()[0]
    cmds.scale(2, 2, 2, cube, r=True)
    cmds.move(5, 1, 0, r=True)
    cmds.select(cube)
    
def create_sphere(*args):
    
    sphere = cmds.polySphere()[0]
    cmds.move(0, 1, 0, r=True)
    cmds.select(sphere)
    
def create_cylinder(*args):
    
    cylinder = cmds.polyCylinder()[0]
    cmds.move(-5, 1, 0, r=True)
    cmds.select(cylinder)