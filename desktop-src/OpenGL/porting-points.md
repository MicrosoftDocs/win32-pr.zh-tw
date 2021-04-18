---
title: 移植點
description: OpenGL 沒有可繪製單一點的命令。 否則，移植點函數很簡單。 下表列出繪製點的鳶尾花 GL 函式及其對等的 OpenGL 函數。
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- 鳶尾花 GL 移植，點
- 從鳶尾花 GL、點進行移植
- 從鳶尾花 GL 移植至 OpenGL，點
- 從鳶尾花 GL （點）移植的 OpenGL
- 繪圖函數、點
- 點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969053"
---
# <a name="porting-points"></a>移植點

OpenGL 沒有可繪製單一點的命令。 否則，移植點函數很簡單。 下表列出繪製點的鳶尾花 GL 函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數           | OpenGL 函數                                                   | 意義                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pnt**                    |                                                                   | 繪製單一點。                                                                                                                                |
| **bgnpoint**， **端點** | [**glBegin**](glbegin.md) ( GL \_ 點 ) 、 [ **glEnd**](glend.md) | 將頂點解釋為點。                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | 設定點大小（以圖元為單位）。                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( GL \_ 點 \_ 平滑 )                 | 開啟點消除鋸齒。  (如需點消除鋸齒的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。 )  |



 

如需相關 get 函數的詳細資訊，請參閱 [**glPointSize**](glpointsize.md)。

??

 

 




