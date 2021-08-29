---
title: 移植區、Screenmasks 和 Scrboxes
description: 下列鳶尾花 GL 視口函數沒有 OpenGL 對等函式
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- 鳶尾花 GL 移植，視口函數
- 從鳶尾花 GL、視口函數移植
- 從鳶尾花 GL （視口函式）移植至 OpenGL
- 從鳶尾花 GL、視口函式移植的 OpenGL
- 視口函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb1a01cfb038faf87e48381856fe281bf2c935d13fedb78b79266e2af4fe15e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776908"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>移植區、Screenmasks 和 Scrboxes

下列鳶尾花 GL 視口函數沒有 OpenGL 對等專案：

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

使用鳶尾花 GL **視口** 函式時，您可以指定區座標的 x 座標 (（以圖元為單位），以及頂端和底部的 y 座標（以圖元為單位）) 。 不過，使用 OpenGL [**glViewport**](glviewport.md) 函式時，您可以將的 x 和 y (座標（以圖元為單位）指定為以圖元) 為單位的矩形，以及其寬度和高度。

下表列出鳶尾花 GL 視口函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                          | OpenGL 函數                                                                                         | 意義                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **視口** ( 左、右、下、頂端 )  | [**glViewport**](glviewport.md) ( x、y、寬度、高度 )                                                 | 設定 [區]。           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ 區 \_ 位 ) <br/> | 推送和 pop 堆疊。   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 區 )                | 傳回視口維度。 |



 

??

 

 





