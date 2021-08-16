---
title: 矩陣轉換
description: 頂點和法線會由模型和投射矩陣進行轉換，然後才會用來在畫面格緩衝區中產生影像。
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- OpenGL 處理管線，矩陣
- 矩陣 OpenGL
- 模型矩陣
- 投射矩陣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937317"
---
# <a name="matrix-transformations"></a>矩陣轉換

頂點和法線會由模型和投射矩陣進行轉換，然後才會用來在畫面格緩衝區中產生影像。 使用 [**glMatrixMode**](glmatrixmode.md)、 [ * *glMultMatrix \** _](glmultmatrix.md)、 [_*glRotate \**_](glrotate.md)、 [_*\* glTranslate*_](gltranslate.md)和 [_*glScale \**_](glscale.md)等函數來撰寫所需的轉換。 或直接使用 [_*glLoadMatrix \**_](glloadmatrix.md)和 [_ *glLoadIdentity* *](glloadidentity.md)指定矩陣。 使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) ，在其各自的堆疊上儲存和還原模型和投射矩陣。

 

 




