---
title: 移植已編輯的顯示清單
description: 雖然您無法編輯 OpenGL 顯示清單，但您可以藉由嵌套顯示清單來取得類似的結果，然後終結和建立新版本的清單子。
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- 鳶尾花 GL 移植，顯示清單
- 從鳶尾花 GL 進行移植，顯示清單
- 從鳶尾花 GL 移植至 OpenGL，顯示清單
- 從鳶尾花 GL 的 OpenGL 移植，顯示清單
- 顯示清單，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13f1630b0560091482d47f85e038d908dcfab202ae772c4d35dc388324b46075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485578"
---
# <a name="porting-edited-display-lists"></a>移植已編輯的顯示清單

雖然您無法編輯 OpenGL 顯示清單，但您可以藉由嵌套顯示清單來取得類似的結果，然後終結和建立新版本的清單子。 例如：

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




