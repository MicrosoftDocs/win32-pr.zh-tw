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
# <a name="using-the-query-functions"></a><span data-ttu-id="27408-105">使用查詢函數</span><span class="sxs-lookup"><span data-stu-id="27408-105">Using the Query Functions</span></span>

<span data-ttu-id="27408-106">有四個查詢函式可用來取得簡單狀態變數，另一個用於判斷是否啟用或停用特定狀態：</span><span class="sxs-lookup"><span data-stu-id="27408-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="27408-107">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="27408-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="27408-108">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="27408-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="27408-109">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="27408-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="27408-110">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="27408-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="27408-111">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="27408-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="27408-112">查詢函式的原型如下：</span><span class="sxs-lookup"><span data-stu-id="27408-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="27408-113">**void** **glGetBooleanv** (**GLenum** *pname* ， **GLboolean \*** *params* ) ;</span><span class="sxs-lookup"><span data-stu-id="27408-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="27408-114">**void** **glGetIntegerv** (**GLenum** *pname* ， **GLint \*** *params* ) ;</span><span class="sxs-lookup"><span data-stu-id="27408-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="27408-115">**void** **glGetFloatv** (**GLenum** *pname* ， **GLfloat \*** *params* ) ;</span><span class="sxs-lookup"><span data-stu-id="27408-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="27408-116">**void** **glGetDoublev** (**GLenum** *pname* ， **GLdouble \*** *params* ) ;</span><span class="sxs-lookup"><span data-stu-id="27408-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="27408-117">查詢函數會分別取得布林值、整數、浮點數或雙精確度狀態變數。</span><span class="sxs-lookup"><span data-stu-id="27408-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="27408-118">*Pname* 參數是一個符號常數，表示要傳回的狀態變數，而 *params* 是指向所指定類型陣列的指標，以放置傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="27408-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="27408-119">*Pname* 的可能值會列在 [OpenGL 狀態變數](opengl-state-variables.md)中。</span><span class="sxs-lookup"><span data-stu-id="27408-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="27408-120">如果需要傳回所需的變數做為要求的資料類型，則會執行類型轉換。</span><span class="sxs-lookup"><span data-stu-id="27408-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="27408-121">[**GlIsEnabled**](glisenabled.md)的原型是：</span><span class="sxs-lookup"><span data-stu-id="27408-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="27408-122">**GLboolean** **glIsEnabled** (GLenum *cap* ) ;</span><span class="sxs-lookup"><span data-stu-id="27408-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="27408-123">如果已啟用 *cap* 所指定的模式， **GLISENABLED** 會傳回 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="27408-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="27408-124">如果 *端點* 指定的模式已停用， **GLISENABLED** 會傳回 GL \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="27408-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="27408-125">*上限* 的可能值會列在 [OpenGL 狀態變數](opengl-state-variables.md)中。</span><span class="sxs-lookup"><span data-stu-id="27408-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="27408-126">其他特製化函數會傳回特定狀態變數。</span><span class="sxs-lookup"><span data-stu-id="27408-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="27408-127">若要瞭解使用這些函數的時機，請參閱 OpenGL 狀態變數和 *Opengl 參考手冊*。</span><span class="sxs-lookup"><span data-stu-id="27408-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="27408-128">如需 OpenGL 的錯誤處理功能和 **glGetError** 函式的詳細資訊，請參閱 [錯誤處理](error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="27408-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="27408-129">傳回特定狀態變數的函式為：</span><span class="sxs-lookup"><span data-stu-id="27408-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="27408-130">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="27408-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="27408-131">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="27408-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="27408-132">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="27408-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="27408-133">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="27408-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="27408-134">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="27408-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="27408-135">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="27408-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="27408-136">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="27408-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="27408-137">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="27408-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="27408-138">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="27408-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="27408-139">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="27408-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="27408-140">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="27408-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="27408-141">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="27408-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="27408-142">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="27408-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




