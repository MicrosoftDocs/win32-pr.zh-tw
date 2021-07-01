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
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120683"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="e86ec-106">取得狀態資訊</span><span class="sxs-lookup"><span data-stu-id="e86ec-106">Obtaining State Information</span></span>

<span data-ttu-id="e86ec-107">OpenGL 會維護許多會影響許多函數行為的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="e86ec-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="e86ec-108">其中有些變數有專門的查詢函數。</span><span class="sxs-lookup"><span data-stu-id="e86ec-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="e86ec-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="e86ec-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="e86ec-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="e86ec-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="e86ec-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="e86ec-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="e86ec-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="e86ec-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="e86ec-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="e86ec-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="e86ec-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e86ec-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="e86ec-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="e86ec-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="e86ec-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="e86ec-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="e86ec-120">若要取得其他狀態變數的值，請視需要使用 [**glGetBooleanv**](glgetbooleanv.md)、 [**glGetDoublev**](glgetdoublev.md)、 [**glGetFloatv**](glgetfloatv.md)或 [**glGetIntegerv**](glgetintegerv.md)。</span><span class="sxs-lookup"><span data-stu-id="e86ec-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="e86ec-121">如需如何使用這些函數的詳細資訊，請參閱 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 。</span><span class="sxs-lookup"><span data-stu-id="e86ec-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="e86ec-122">您可能想要使用的其他查詢函數包括 [**glGetError**](glgeterror.md)、 [**glGetString**](glgetstring.md)和 [**glIsEnabled**](glisenabled.md)。</span><span class="sxs-lookup"><span data-stu-id="e86ec-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="e86ec-123"> (請參閱 [處理錯誤](handling-errors.md) ，以取得與錯誤處理相關之函式的詳細資訊。 ) 若要儲存和還原狀態變數集，請使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)。</span><span class="sxs-lookup"><span data-stu-id="e86ec-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="e86ec-124">使用查詢函數</span><span class="sxs-lookup"><span data-stu-id="e86ec-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="e86ec-125">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="e86ec-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="e86ec-126">OpenGL 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e86ec-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="e86ec-127">儲存和還原狀態變數集</span><span class="sxs-lookup"><span data-stu-id="e86ec-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="e86ec-128">OpenGL 狀態變數</span><span class="sxs-lookup"><span data-stu-id="e86ec-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="e86ec-129">狀態資訊參考</span><span class="sxs-lookup"><span data-stu-id="e86ec-129">State Information Reference</span></span>](state-information-reference.md)

 

 




