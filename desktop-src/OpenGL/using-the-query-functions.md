---
title: 使用查詢函數
description: 使用查詢函數
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL、查詢函數
- 查詢函式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967824"
---
# <a name="using-the-query-functions"></a>使用查詢函數

有四個查詢函式可用來取得簡單狀態變數，另一個用於判斷是否啟用或停用特定狀態：

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

查詢函式的原型如下：

**void** **glGetBooleanv** (**GLenum** *pname* ， **GLboolean \*** *params* ) ;

**void** **glGetIntegerv** (**GLenum** *pname* ， **GLint \*** *params* ) ;

**void** **glGetFloatv** (**GLenum** *pname* ， **GLfloat \*** *params* ) ;

**void** **glGetDoublev** (**GLenum** *pname* ， **GLdouble \*** *params* ) ;

查詢函數會分別取得布林值、整數、浮點數或雙精確度狀態變數。 *Pname* 參數是一個符號常數，表示要傳回的狀態變數，而 *params* 是指向所指定類型陣列的指標，以放置傳回的資料。 *Pname* 的可能值會列在 [OpenGL 狀態變數](opengl-state-variables.md)中。 如果需要傳回所需的變數做為要求的資料類型，則會執行類型轉換。

[**GlIsEnabled**](glisenabled.md)的原型是：

**GLboolean** **glIsEnabled** (GLenum *cap* ) ;

如果已啟用 *cap* 所指定的模式， **GLISENABLED** 會傳回 GL \_ TRUE。 如果 *端點* 指定的模式已停用， **GLISENABLED** 會傳回 GL \_ FALSE。 *上限* 的可能值會列在 [OpenGL 狀態變數](opengl-state-variables.md)中。

其他特製化函數會傳回特定狀態變數。 若要瞭解使用這些函數的時機，請參閱 OpenGL 狀態變數和 *Opengl 參考手冊*。 如需 OpenGL 的錯誤處理功能和 **glGetError** 函式的詳細資訊，請參閱 [錯誤處理](error-handling.md)。

傳回特定狀態變數的函式為：

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 




