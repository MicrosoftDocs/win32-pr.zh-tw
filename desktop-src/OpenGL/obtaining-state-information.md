---
title: 取得狀態資訊
description: 取得狀態資訊
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL、state information
- OpenGL、state 變數
- 狀態資訊 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672679"
---
# <a name="obtaining-state-information"></a>取得狀態資訊

OpenGL 會維護許多會影響許多函數行為的狀態變數。 其中有些變數有專門的查詢函數。



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glGetClipPlane**](glgetclipplane.md) | [**glGetPixelMap**](glgetpixelmap.md)             | [**glGetTexImage**](glgetteximage.md)                   |
| [**glGetLight**](glgetlight.md)         | [**glGetPolygonStipple**](glgetpolygonstipple.md) | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |
| [**glGetMap**](glgetmap.md)             | [**glGetTexEnv**](glgettexenv.md)                 | [**glGetTexParameter**](glgettexparameter.md)           |
| [**glGetMaterial**](glgetmaterial.md)   | [**glGetTexGen**](glgettexgen.md)                 |                                                          |



 

若要取得其他狀態變數的值，請視需要使用 [**glGetBooleanv**](glgetbooleanv.md)、 [**glGetDoublev**](glgetdoublev.md)、 [**glGetFloatv**](glgetfloatv.md)或 [**glGetIntegerv**](glgetintegerv.md)。 如需如何使用這些函數的詳細資訊，請參閱 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 。 您可能想要使用的其他查詢函數包括 [**glGetError**](glgeterror.md)、 [**glGetString**](glgetstring.md)和 [**glIsEnabled**](glisenabled.md)。  (請參閱 [處理錯誤](handling-errors.md) ，以取得與錯誤處理相關之函式的詳細資訊。 ) 若要儲存和還原狀態變數集，請使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)。

-   [使用查詢函數](using-the-query-functions.md)
-   [錯誤處理](error-handling.md)
-   [OpenGL 錯誤碼](opengl-error-codes.md)
-   [儲存和還原狀態變數集](saving-and-restoring-sets-of-state-variables.md)
-   [OpenGL 狀態變數](opengl-state-variables.md)
-   [狀態資訊參考](state-information-reference.md)

 

 




