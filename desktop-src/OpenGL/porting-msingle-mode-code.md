---
title: 移植 MSINGLE 模式程式碼
description: OpenGL 對 MSINGLE、單一矩陣模式沒有對等專案。
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- 鳶尾花 GL 移植，MSINGLE 模式
- 從鳶尾花 GL （MSINGLE 模式）移植
- 從鳶尾花 GL （MSINGLE 模式）移植至 OpenGL
- 鳶尾花 GL，MSINGLE 模式的 OpenGL 移植
- MSINGLE 模式
- 鳶尾花 GL 移植，單一矩陣模式
- 從鳶尾花 GL （單一矩陣模式）移植
- 從鳶尾花 GL （單一矩陣模式）移植至 OpenGL
- 從鳶尾花 GL （單一矩陣模式）移植的 OpenGL
- 單一矩陣模式
- 雙矩陣模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372367"
---
# <a name="porting-msingle-mode-code"></a>移植 MSINGLE 模式程式碼

OpenGL 對 **MSINGLE**、單一矩陣模式沒有對等專案。 雖然不建議使用此模式，但這是鳶尾花 GL 的預設值。 如果您的鳶尾花 GL 程式使用單一矩陣模式，您必須將它重寫為只使用雙矩陣模式。 OpenGL 一律採用雙矩陣模式，且一開始是 GL \_ 模型模式。

MSINGLE 模式中大部分的鳶尾花 GL 程式碼看起來像這樣：

``` syntax
projectionmatrix();
```

其中 *projectionmatrix* 是下列其中一個： **ortho**、 **ortho2**、 **透視圖** 或 **window**。 若要移植至 OpenGL，請將 **MSINGLE** 模式的 *projectionmatrix* 函式取代為：


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




