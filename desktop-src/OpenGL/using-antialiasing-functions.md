---
title: 使用消除鋸齒功能
description: 下表列出鳶尾花 GL 消除鋸齒函式及其對等的 OpenGL 函數。
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- 鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植至 OpenGL，消除鋸齒
- 從鳶尾花 GL 的 OpenGL 移植，消除鋸齒
- 消除鋸齒 (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab36f41e3b639447b4f246d706e11c134d8f920528cde1e946d26af057a95951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980344"
---
# <a name="using-antialiasing-functions"></a>使用消除鋸齒功能

下表列出鳶尾花 GL 消除鋸齒函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                                      | 意義                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( GL \_ 點 \_ 平滑 )    | 啟用點的消除鋸齒功能。   |
| **linesmooth**   | **glEnable** ( GL \_ 行 \_ 平滑 )                      | 啟用線條的消除鋸齒功能。    |
| **polysmooth**   | [**glEnable**](glenable.md) ( GL \_ 多邊形 \_ 平滑 )  | 啟用多邊形的消除鋸齒功能。 |



 

使用對等的 [**glDisable**](gldisable.md) 呼叫來關閉消除鋸齒功能。

在鳶尾花 GL 中，您可以藉由呼叫下列方法來控制消除鋸齒的品質：


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL 提供類似的 controluse [**glHint**](glhint.md)：


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



其中 *hintMode* 是下列其中一項：

-   GL \_ 最好 (使用最高品質的平滑處理。 ) 
-   GL 最 \_ 快速 (使用最有效率的凹凸貼圖 ) 
-   GL \_ 別 \_ 在意

鳶尾花 GL 也會藉由呼叫下列內容來允許結束修正：


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL 對此函式沒有對等專案。

 

 




