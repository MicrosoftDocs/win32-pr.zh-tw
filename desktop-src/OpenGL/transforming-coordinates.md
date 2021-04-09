---
title: 轉換座標
description: OpenGL 公用程式程式庫 (X.GLU 隊) 提供數個常用的矩陣轉換函數。
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- OpenGL 公用程式 (X.GLU 隊) 、矩陣轉換函式
- X.GLU 隊 (OpenGL 公用程式) ，矩陣轉換函式
- 矩陣轉換函式 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、轉換座標
- X.GLU 隊 (OpenGL 公用程式) ，轉換座標
- 轉換座標 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675491"
---
# <a name="transforming-coordinates"></a>轉換座標

OpenGL 公用程式程式庫 (X.GLU 隊) 提供數個常用的矩陣轉換函數。 您可以使用 GluOrtho2D、標準的透視圖磁片區（使用 [**gluPerspective**](gluperspective.md)），或以指定的 Eyepoint （ [**gluLookAt**](glulookat.md)）為中心的視圖磁片區，設定一個具有 [](gluortho2d.md)的二維正向查看區域。 這些函式中的每一個都會建立想要的矩陣，並使用 [**glMultMatrix**](glmultmatrix.md)將它套用至目前的矩陣。

[**GluPickMatrix**](glupickmatrix.md)函式會藉由建立矩陣，將繪圖限制在區域的小型區域，以簡化挑選矩陣的選取。 如果您在套用這個矩陣之後，以選取模式重新轉譯場景，則會選取所有將繪製在游標附近的物件，而這些物件的相關資訊將會儲存在選取範圍緩衝區中。 如需選取模式的詳細資訊，請參閱 [執行選取](performing-selection-and-feedback.md)專案和意見反應。

若要判斷要在視窗中繪製物件的位置，請使用 [**gluProject**](gluproject.md)，它會將指定的物件座標 *objx*、 *Objy* 和 *objz* 為使用 *modelMatrix*、 *projMatrix* 和 *視口* 的視窗座標。 結果會儲存在 *winx*、 *winy* 和 *winz* 中。 如果函式成功，則傳回值為 GL \_ TRUE。 如果函式失敗，則傳回值為 GL \_ FALSE。

[**GluUnProject**](gluunproject.md)函式會執行反向轉換：它會使用 *modelMatrix*、 *projMatrix* 和 *視口* 來將指定的視窗座標 *winx*、 *winy* 和 *winz* 轉換成物件座標。 結果會儲存在 *objx*、 *objy* 和 *objz* 中。 如果函式成功，則傳回值為 GL \_ TRUE。 如果函式失敗，則傳回值為 GL \_ FALSE。

 

 




