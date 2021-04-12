---
title: 移植弧形和圓形
description: 使用 OpenGL，填滿的弧形和圓形會以與空心弧形和圓形相同的呼叫來繪製。 下表列出鳶尾花 GL arc 和 circle 函數，以及其對等的 OpenGL (X.GLU 隊) 函式。
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- 鳶尾花 GL 移植，弧形
- 從鳶尾花 GL、弧形移植
- 從鳶尾花 GL （弧形）移植至 OpenGL
- 從鳶尾花 GL、弧形移植的 OpenGL
- 繪製函數，弧形
- 鳶尾花 GL 移植，圓形
- 從鳶尾花 GL、圓形進行移植
- 從鳶尾花 GL 移植至 OpenGL，圓形
- 從鳶尾花 GL、圓形的 OpenGL 移植
- 繪圖函數、圓形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372615"
---
# <a name="porting-arcs-and-circles"></a>移植弧形和圓形

使用 OpenGL，填滿的弧形和圓形會以與空心弧形和圓形相同的呼叫來繪製。 下表列出鳶尾花 GL arc 和 circle 函數，以及其對等的 OpenGL (X.GLU 隊) 函式。



| 鳶尾花 GL 函數 | OpenGL 函數                          | 意義                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | 繪製弧形。           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | 繪製圓形或磁片。 |



 

您可以使用鳶尾花 GL 無法進行的 OpenGL 弧形和圓形來做一些事情。 OpenGL 會分別呼叫弧形和圓形、磁片和部分磁片。

移植弧形和圓形時，請記住下列關於 OpenGL 的重點：

-   角度是以度為單位，而不是以十分之一度為單位。
-   開始角度是從正 y 軸（而不是從 X 軸）來測量。
-   立即的掃描角度（而不是逆時針）。

??

 

 




