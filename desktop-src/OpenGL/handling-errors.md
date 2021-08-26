---
title: 處理 (OpenGL) 的錯誤
description: GluErrorString 函式會捕獲對應于 OpenGL 或 X.GLU 隊錯誤碼的錯誤字串。
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- OpenGL 公用程式 (X.GLU 隊) ，錯誤碼
- X.GLU 隊 (OpenGL 公用程式) ，錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035188"
---
# <a name="handling-errors-opengl"></a>處理 (OpenGL) 的錯誤

**GluErrorString** 函式會捕獲對應于 OPENGL 或 x.glu 隊錯誤碼的錯誤字串。 目前定義的 OpenGL 錯誤碼如 [**glGetError**](glgeterror.md)中所述。 X.GLU 隊錯誤碼列在 [**gluErrorString**](gluerrorstring.md)、 [*gluTessCallback*](glutess.md)、 [*gluQuadricCallback*](gluquadric.md)和 [*gluNurbsCallback*](glunurbs.md)中。

**GluErrorString** 的傳回值是對應于 *errorCode* 參數中所傳遞之 OPENGL、x.glu 隊或 GLX 錯誤號碼的描述性字串指標。 在 *OpenGL 參考手冊* 中，已定義的錯誤碼和可以產生這些錯誤碼的函式或函式相關描述。

 

 




