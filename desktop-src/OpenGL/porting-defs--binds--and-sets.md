---
title: 移植 Defs、系結和集合
description: 移植 Defs、系結和集合
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- 鳶尾花 GL 移植，定義
- 從鳶尾花 GL、定義進行移植
- 從鳶尾花 GL 移植至 OpenGL，定義
- 從鳶尾花 GL （定義）進行 OpenGL 移植
- 鳶尾花 GL 移植，系結
- 從鳶尾花 GL 進行移植，系結
- 從鳶尾花 GL 移植至 OpenGL，系結
- 從鳶尾花 GL 進行 OpenGL 移植，系結
- 鳶尾花 GL 移植，設定
- 從鳶尾花 GL 進行移植，設定
- 從鳶尾花 GL 移植至 OpenGL，設定
- 從鳶尾花 GL 進行 OpenGL 移植，設定
- 定義
- 綁定
- 集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968824"
---
# <a name="porting-defs-binds-and-sets"></a>移植 Defs、系結和集合

OpenGL 沒有預存定義的資料表;您不能將光源模型、材質、材質、線條樣式或模式定義為與鳶尾花 GL 不同的物件。 因此，OpenGL 與下列鳶尾花 GL 函式沒有直接對等專案：

-   **Imdef** 和 **Imbind**
-   **tevdef** 和 **tevbind**
-   **textdef** 和 **textbind**
-   **definestyle** 和 **>setstyle**
-   **defpattern** 和 **setpattern**

您可以使用 OpenGL 顯示清單來模仿鳶尾花 GL 定義/系結機制。 例如，以下是鳶尾花 GL 中的材質定義：


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



下列 OpenGL 程式碼範例會在顯示清單中定義 **MYMATERIAL** 所定義清單編號所參考的相同材質。


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




