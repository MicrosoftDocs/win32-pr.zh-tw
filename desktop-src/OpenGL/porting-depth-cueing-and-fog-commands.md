---
title: 移植深度提示和霧化命令
description: 移植深度提示和霧化命令
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- 鳶尾花 GL 移植，深度提示
- 從鳶尾花 GL、深度提示移植
- 從鳶尾花 GL 移植至 OpenGL，深度提示
- 從鳶尾花 GL、深度提示的 OpenGL 移植
- 鳶尾花 GL 移植，霧化
- 從鳶尾花 GL 進行移植，霧化
- 從鳶尾花 GL 移植至 OpenGL，霧化
- 從鳶尾花 GL 的 OpenGL 移植，霧化
- 深度提示
- 霧
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183899"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>移植深度提示和霧化命令

移植深度提示和霧化命令時，請記住下列幾點：

-   鳶尾花 GL 呼叫 **fogvertex** 會設定會影響該模式的模式和參數。 在 OpenGL 中，您可以呼叫 [**glFog**](glfog.md) 一次來設定模式，然後再次呼叫兩次以上來設定各種參數。
-   在 OpenGL 中，深度提示並非個別的功能。 使用線性霧而非深度提示。  (本節提供如何執行這項操作的範例。 ) 下列鳶尾花 GL 函數沒有直接 OpenGL 對等專案：

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   若要調整霧化品質，請使用 [**glHint**](glhint.md) ( GL \_ 霧化 \_ 提示 ) 。

下表列出用來管理霧化的鳶尾花 GL 函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數         | OpenGL 函數                                     | 意義                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glFog**](glfog.md)                              | 設定各種霧化參數。      |
|  \_ ) 上的 fogvertex ( FG  | [**glEnable**](glenable.md) ( GL \_ 霧化 )             | 開啟霧化。                     |
| **fogvertex** ( FG \_ OFF )  | [**glDisable**](gldisable.md) ( GL \_ 霧化 )           | 關閉霧化。                    |
| **depthcue**             | [**glFog**](glfog.md) ( gl \_ 霧化 \_ MOD，gl \_ 線性 )  | 使用線性霧化進行深度提示。 |



 

下表列出可傳遞至 **glFog** 的參數。



| 霧化參數    | 意義                       | 預設                  |
|------------------|-------------------------------|--------------------------|
| GL \_ 霧化 \_ 密度 | 霧化密度。                  | 1.0                      |
| GL \_ 霧化 \_ 開始   | 線性模糊的近距離。 | 0.0                      |
| GL \_ 霧化 \_ 結束     | 線性模糊的遠距離。  | 1.0                      |
| GL \_ 霧化 \_ 索引   | 霧化色彩索引。              | 0.0                      |
| GL \_ 霧化 \_ 色彩   | 霧化 RGBA 色彩。               |  (0、0、0、0)              |
| GL \_ 霧化 \_ 模式    | 霧化模式。                     | 請參閱下表。 |



 

OpenGL 的霧化密度參數與鳶尾花 GL 中的霧化密度參數不同。 它們的關聯如下：

-   if *fogMode* = EXP2
     

    *openGLfogDensity* = (*irisGLfogDensity* )  ( **sqrt** ( **記錄** ( 1/255 ) ) ) 
-   如果 *fogMode* = EXP
     

    *openGLfogDensity* = (*irisGLfogDensity* )  ( **記錄** ( 1/255 ) ) 

其中 **sqrt** 是平方根運算， **log** 是自然對數、 *irisGLfogDensity* 是鳶尾花 GL 霧密度，而 *openGLfogDensity* 是 OpenGL 霧化密度。

若要在計算每圖元模式和每個頂點模式的霧化之間切換，請使用 [**glHint**](glhint.md) ( GL \_ 霧化 \_ 提示， *hintMode*) 。 有兩個提示模式可用：

-   GL \_ 最好每圖元霧化計算
-   GL \_ 每個頂點的最快速霧化計算

下表列出鳶尾花 GL 霧化模式及其 OpenGL 對等專案。



| 鳶尾花 GL 霧化模式                       | OpenGL 霧化模式 | 提示模式                         | 意義                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ ANALYSTS.VTX \_ EXP、FG \_ PIX \_ EXP<br/>   | GL \_ EXP         | GL \_ 最快、GL \_ 最好<br/> | 繁重的霧化模式 (預設) 。                |
| FG \_ Analysts.vtx \_ EXP2、FG \_ PIX \_ EXP2<br/> | GL \_ EXP2        | GL \_ 最快、GL \_ 最好<br/> | 迷霧模式。                               |
| FG \_ ANALYSTS.VTX \_ LIN、FG \_ PIX \_ LIN<br/>   | GL \_ 線性      | GL \_ 最快、GL \_ 最好<br/> | 線性霧化模式。  (用於深度提示。 )  |



 

下列程式碼範例示範 OpenGL 中的深度提示：


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





