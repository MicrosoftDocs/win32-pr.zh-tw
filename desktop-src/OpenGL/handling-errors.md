---
title: 處理 (OpenGL) 的錯誤
description: GluErrorString 函式會捕獲對應于 OpenGL 或 X.GLU 隊錯誤碼的錯誤字串。
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- OpenGL 公用程式 (X.GLU 隊) ，錯誤碼
- X.GLU 隊 (OpenGL 公用程式) ，錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316984"
---
# <a name="handling-errors-opengl"></a><span data-ttu-id="0d4fc-105">處理 (OpenGL) 的錯誤</span><span class="sxs-lookup"><span data-stu-id="0d4fc-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="0d4fc-106">**GluErrorString** 函式會捕獲對應于 OPENGL 或 x.glu 隊錯誤碼的錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="0d4fc-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="0d4fc-107">目前定義的 OpenGL 錯誤碼如 [**glGetError**](glgeterror.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="0d4fc-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="0d4fc-108">X.GLU 隊錯誤碼列在 [**gluErrorString**](gluerrorstring.md)、 [*gluTessCallback*](glutess.md)、 [*gluQuadricCallback*](gluquadric.md)和 [*gluNurbsCallback*](glunurbs.md)中。</span><span class="sxs-lookup"><span data-stu-id="0d4fc-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="0d4fc-109">**GluErrorString** 的傳回值是對應于 *errorCode* 參數中所傳遞之 OPENGL、x.glu 隊或 GLX 錯誤號碼的描述性字串指標。</span><span class="sxs-lookup"><span data-stu-id="0d4fc-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="0d4fc-110">在 *OpenGL 參考手冊* 中，已定義的錯誤碼和可以產生這些錯誤碼的函式或函式相關描述。</span><span class="sxs-lookup"><span data-stu-id="0d4fc-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




