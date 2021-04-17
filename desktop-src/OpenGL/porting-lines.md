---
title: 移植線
description: 移植鳶尾花 GL 程式碼來繪製線條相當簡單，不過您應該注意 OpenGL stipples 方式的差異。 下表列出用來繪製線條的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- 鳶尾花 GL 移植，線路
- 從鳶尾花 GL 進行移植，行
- 從鳶尾花 GL 移植至 OpenGL，行
- 從鳶尾花 GL 的 OpenGL 移植，行
- 繪製函數，線條
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183896"
---
# <a name="porting-lines"></a>移植線

移植鳶尾花 GL 程式碼來繪製線條相當簡單，不過您應該注意 OpenGL stipples 方式的差異。 下表列出用來繪製線條的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                               | OpenGL 函數                                                                                         | 意義                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**、**endclosedline**<br/> | [**glBegin**](glbegin.md) ( GL \_ 線路 \_ 迴圈 ) [ **glEnd**](glend.md)<br/>                          | 繪製封閉線。                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( GL \_ 行 \_ 帶 )                                                           | 繪製線段。                                                                                                                         |
| **寬**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | 設定線條寬度。                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 行 \_ 寬度 )             | 傳回目前的線條寬度。                                                                                                                  |
| **deflinestyle**、**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | 指定行 stipple 模式。                                                                                                            |
| **lsrepeat**                                   | **glLineStipple** 的因數引數                                                                    | 設定線條樣式的重複因數。                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ 模式 )  | 傳回 line stipple 模式。                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 行 \_ STIPPLE \_ 重複 )   | 傳回重複因數。                                                                                                                       |
| **linesmooth**、 **smoothline**                 | [**glEnable**](glenable.md) ( GL \_ 行 \_ 平滑 )                                                        | 開啟線條消除鋸齒 (如需消除鋸齒的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。 )  |



 

OpenGL 不會使用表格進行行 stipples;它只會維護一個行 stipple 模式。 您可以使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 在不同的 stipple 模式之間切換。

舊版的鳶尾花 GL 線條樣式函式 (例如 **draw**、 **lsbackup**、 **Getlsbackup** 等等) 不受 OpenGL 支援。

如需繪製反鋸齒線條的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。

??

 

 





