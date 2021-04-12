---
title: 移植 v 函數
description: 在鳶尾花 GL 中，您可以使用 v 函數的變化來指定頂點。 對等的 OpenGL 函式 glVertex 如下所示的 glVertex 範例。
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- 鳶尾花 GL 移植，頂點
- 從鳶尾花 GL、頂點移植
- 從鳶尾花 GL （頂點）移植至 OpenGL
- 從鳶尾花 GL、頂點移植的 OpenGL
- 繪圖函數、頂點
- 頂點，從鳶尾花 GL 移植
- 鳶尾花 GL 移植，v 函數
- 從鳶尾花 GL、v 函數移植
- 從鳶尾花 GL、v 函式移植至 OpenGL
- 從鳶尾花 GL、v 函式移植的 OpenGL
- 繪圖函式，v 函數
- v 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300588"
---
# <a name="porting-v-functions"></a>移植 v 函數

在鳶尾花 GL 中，您可以使用 **v** 函數的變化來指定頂點。 對等的 OpenGL 函數是 [glVertex](glvertex-functions.md)：以下是 **glVertex** 的範例。

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

**GlVertex** 函式會採用與其他 OpenGL 呼叫相同的方式來採用尾碼。 呼叫的向量版本會採用適當大小的陣列做為引數。 在2D 版本中，z = 0 和 w = 1。 在3-d 版中，w = 1。

 

 




