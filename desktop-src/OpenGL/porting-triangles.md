---
title: 移植三角形
description: 您可以在 OpenGL 個別三角形、三角形條紋和三角形風扇中繪製三種類型的三角形。
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- 鳶尾花 GL 移植，三角形
- 從鳶尾花 GL、三角形進行移植
- 從鳶尾花 GL （三角形）移植至 OpenGL
- 從鳶尾花 GL （三角形）進行 OpenGL 移植
- 繪圖函數、三角形
- 三角形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301372"
---
# <a name="porting-triangles"></a>移植三角形

您可以在 OpenGL 中繪製三種類型的三角形：個別三角形、三角形條紋和三角形風扇。

OpenGL 對鳶尾花 GL **swaptmesh** 函數沒有對等專案。 您可以使用三角形、三角形條紋和三角形風扇的組合來達成相同的效果。

下表列出用來繪製三角形的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數           | 對等的 glBegin 參數 | 意義                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | GL \_ 三角形                | 被解釋為三角形的三倍頂點。 |
| **bgntmesh**、 **endtmesh** | GL \_ 三角形 \_ 條紋          | 三角形的連結去除。                   |
|                            | GL \_ 三角形 \_ 風扇            | 三角形的連結風扇。                     |



 

??

 

 




