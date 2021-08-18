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
ms.openlocfilehash: 18ef24ad81942681b3d70a303a22e89e9573aa609d3f08f52a92583ae88e0e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012066"
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

 

 




