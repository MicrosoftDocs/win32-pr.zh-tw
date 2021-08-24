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
ms.openlocfilehash: 8d13719964412bf8b74b9d2f4ef58d5a153a56fc2f8d15a3d8788cef94762637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144160"
---
# <a name="obtaining-state-information"></a>取得狀態資訊

OpenGL 會維護許多會影響許多函數行為的狀態變數。 其中有些變數有專門的查詢函數。

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

若要取得其他狀態變數的值，請視需要使用 [**glGetBooleanv**](glgetbooleanv.md)、 [**glGetDoublev**](glgetdoublev.md)、 [**glGetFloatv**](glgetfloatv.md)或 [**glGetIntegerv**](glgetintegerv.md)。 如需如何使用這些函數的詳細資訊，請參閱 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 。 您可能想要使用的其他查詢函數包括 [**glGetError**](glgeterror.md)、 [**glGetString**](glgetstring.md)和 [**glIsEnabled**](glisenabled.md)。  (請參閱 [處理錯誤](handling-errors.md) ，以取得與錯誤處理相關之函式的詳細資訊。 ) 若要儲存和還原狀態變數集，請使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)。

-   [使用查詢函數](using-the-query-functions.md)
-   [錯誤處理](error-handling.md)
-   [OpenGL 錯誤碼](opengl-error-codes.md)
-   [儲存和還原狀態變數集](saving-and-restoring-sets-of-state-variables.md)
-   [OpenGL 狀態變數](opengl-state-variables.md)
-   [狀態資訊參考](state-information-reference.md)

 

 




