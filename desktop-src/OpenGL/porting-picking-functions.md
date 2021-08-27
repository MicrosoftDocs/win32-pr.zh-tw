---
title: 移植挑選函數
description: 所有鳶尾花 GL 挑選函式都有 OpenGL 對等專案，但 clearhitcode 除外。 下表列出鳶尾花 GL 挑選函數及其對等的 OpenGL 函數。
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- 鳶尾花 GL 移植，挑選
- 從鳶尾花 GL 進行移植，挑選
- 從鳶尾花 GL 移植至 OpenGL，挑選
- 鳶尾花 GL 的 OpenGL 移植，挑選
- 採摘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2cbeed54a18e7f1d3f26ec01dca2ad352aa4e190fbdc667ed75a60badec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034808"
---
# <a name="porting-picking-functions"></a>移植挑選函數

所有鳶尾花 GL 挑選函式都有 OpenGL 對等專案，但 **clearhitcode** 除外。 下表列出鳶尾花 GL 挑選函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                | OpenGL 函數                                                                           | 意義                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | 不支援。                                                                            | 清除全域變數和 hitcode。    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) ( GL \_ 選取 )                                        | 切換至選取範圍或挑選模式。 |
| **enDPIckendselect**<br/> | [**glRenderMode**](glrendermode.md) ( GL 轉譯 \_ )                                        | 切換至轉譯模式。            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | 設定傳回陣列。                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

如需有關挑選的詳細資訊，請參閱 [**gluPickMatrix**](glupickmatrix.md)。

 

 





