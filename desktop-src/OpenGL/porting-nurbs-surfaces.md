---
title: 移植 NURBS 表面
description: 下表列出用來繪製 NURBS 表面的鳶尾花 GL 函式，以及其對等的 OpenGL 函式。
ms.assetid: d34ac6af-55d7-4128-bcd9-3c910607895f
keywords:
- 鳶尾花 GL 移植，NURBS 表面
- 從鳶尾花 GL、NURBS 表面移植
- 從鳶尾花 GL、NURBS 表面移植至 OpenGL
- 從鳶尾花 GL、NURBS 表面移植的 OpenGL
- NURBS 表面
- 'NURBS (非統一的有理 B 曲線) '
- '非統一的有理 B 曲線 (NURBS) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7260750db4d221743d3e764d6dd30e2de499383
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674543"
---
# <a name="porting-nurbs-surfaces"></a>移植 NURBS 表面

下表列出用來繪製 NURBS 表面的鳶尾花 GL 函式，以及其對等的 OpenGL 函式。



| 鳶尾花 GL 函數 | OpenGL 函數                            | 意義                       |
|------------------|--------------------------------------------|-------------------------------|
| **bgnsurface**   | [**gluBeginSurface**](glubeginsurface.md) | 開始介面定義。  |
| **nurbssurface** | [**gluNurbsSurface**](glunurbssurface.md) | 指定介面屬性。 |
| **endsurface**   | [**gluEndSurface**](gluendsurface.md)     | 結束介面定義。    |



 

下表列出介面類別型的鳶尾花 GL 參數及其對等的 OpenGL 參數。



| 鳶尾花 GL 類型 | OpenGL 類型                 | 意義                                                |
|--------------|-----------------------------|--------------------------------------------------------|
| N \_ V3D       | GL \_ List.map2 \_ 頂點 \_ 3         | 多項式曲線。                                      |
| N \_ V3DR      | GL \_ List.map2 \_ 頂點 \_ 4         | 有理數曲線。                                        |
| N \_ C4D       | GL \_ List.map2 \_ 色彩 \_ 4          | 控制點會在 (R、G、B、) 表單中定義色彩介面。 |
| N \_ C4DR      |                             |                                                        |
| N \_ T2D       | GL \_ List.map2 \_ 材質 \_ COORD \_ 2 | 控制點是材質座標。                |
| N \_ T2DR      | GL \_ List.map2 \_ 材質 \_ COORD \_ 3 | 控制點是材質座標。                |
|              | GL \_ List.map2 \_ 正常            | 控制點是法線。                            |



 

如需可用評估工具類型的詳細資訊，請參閱 [**glMap2**](glmap2.md)。

下列程式碼範例會繪製修剪的 NURBS 介面：


```C++
/* 
 *  trim.c 
 *  This program draws a NURBS surface in the shape of a 
 *  symmetrical hill, using both a NURBS curve and pwl 
 *  (piecewise linear) curve to trim part of the surface 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
GLfloat ctlpoints[4][4][3]; 
 
GLUnurbsObj *theNurb; 
 
/* 
 *  Initializes the control points of the surface to  
 *  a small hill. The control points range from -3 to  
 *  +3 in x, y, and z 
 */ 
void init_surface(void) 
{ 
    int u, v; 
    for (u = 0; u < 4; u++) { 
        for (v = 0; v < 4; v++) { 
            ctlpoints[u][v][0] = 2.0*((GLfloat)u - 1.5); 
            ctlpoints[u][v][1] = 2.0*((GLfloat)v - 1.5); 
 
            if ( (u == 1 || u == 2) && (v == 1 || v == 2)) 
                ctlpoints[u][v][2] = 3.0; 
            else 
                ctlpoints[u][v][2] = -3.0; 
        } 
    } 
} 
 
/*  Initialize material property and depth buffer 
 */ 
void myinit(void) 
{ 
    GLfloat mat_diffuse[] = { 0.6, 0.6, 0.6, 1.0 }; 
    GLfloat mat_specular[] = { 0.9, 0.9, 0.9, 1.0 }; 
    GLfloat mat_shininess[] = { 128.0 }; 
 
    glClearColor (0.0, 0.0, 0.0, 1.0); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_diffuse); 
    glMaterialfv(GL_FRONT, GL_SPECULAR, mat_specular); 
    glMaterialfv(GL_FRONT, GL_SHININESS, mat_shininess); 
 
    glEnable(GL_LIGHTING); 
    glEnable(GL_LIGHT0); 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glEnable(GL_AUTO_NORMAL); 
    glEnable(GL_NORMALIZE); 
 
    init_surface(); 
 
    theNurb = gluNewNurbsRenderer(); 
    gluNurbsProperty(theNurb, GLU_SAMPLING_TOLERANCE, 50.0); 
    gluNurbsProperty(theNurb, GLU_DISPLAY_MODE, GLU_FILL); 
} 
 
void display(void) 
{ 
    GLfloat knots[8] = {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat edgePt[5][2] = /* counter clockwise */ 
    {{0.0, 0.0}, {1.0, 0.0}, {1.0, 1.0}, {0.0, 1.0}, 
     {0.0, 0.0}}; 
    GLfloat curvePt[4][2] = /* clockwise */ 
    {{0.25, 0.5}, {0.25, 0.75}, {0.75, 0.75}, {0.75, 0.5}}; 
    GLfloat curveKnots[8] = 
        {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat pwlPt[4][2] = /* clockwise */ 
        {{0.75, 0.5}, {0.5, 0.25}, {0.25, 0.5}}; 
 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glPushMatrix(); 
    glRotatef(330.0, 1.,0.,0.); 
    glScalef (0.5, 0.5, 0.5); 
 
    gluBeginSurface(theNurb); 
    gluNurbsSurface(theNurb, 
            8, knots, 
            8, knots, 
            4 * 3, 
            3, 
            &ctlpoints[0][0][0], 
            4, 4, 
            GL_MAP2_VERTEX_3); 
    gluBeginTrim (theNurb); 
        gluPwlCurve (theNurb, 5, &edgePt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluBeginTrim (theNurb); 
        gluNurbsCurve (theNurb, 8, curveKnots, 2, 
                &curvePt[0][0], 4, GLU_MAP1_TRIM_2); 
        gluPwlCurve (theNurb, 3, &pwlPt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluEndSurface(theNurb); 
 
    glPopMatrix(); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLdouble)w/(GLdouble)h, 3.0, 8.0); 
 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity(); 
    glTranslatef (0.0, 0.0, -5.0); 
} 
 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 500, 500); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 




