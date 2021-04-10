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
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183405"
---
# <a name="matrix-transformations"></a>矩陣轉換

頂點和法線會由模型和投射矩陣進行轉換，然後才會用來在畫面格緩衝區中產生影像。 使用 [**glMatrixMode**](glmatrixmode.md)、 [**glMultMatrix \***](glmultmatrix.md)、 [**\* glRotate**](glrotate.md)、 [**\* glTranslate**](gltranslate.md)和 [**glScale \***](glscale.md)等函數來撰寫所需的轉換。 或直接使用 [**glLoadMatrix \***](glloadmatrix.md)和 [**glLoadIdentity**](glloadidentity.md)指定矩陣。 使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) ，在其各自的堆疊上儲存和還原模型和投射矩陣。

 

 




