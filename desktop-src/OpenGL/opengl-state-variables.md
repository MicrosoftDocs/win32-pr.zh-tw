---
title: OpenGL 狀態變數
description: 下列主題列出可查詢的狀態變數名稱
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- OpenGL 狀態變數
- 狀態變數，OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965370"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="f5402-105">OpenGL 狀態變數</span><span class="sxs-lookup"><span data-stu-id="f5402-105">OpenGL State Variables</span></span>

<span data-ttu-id="f5402-106">下列主題列出可查詢的狀態變數名稱：</span><span class="sxs-lookup"><span data-stu-id="f5402-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="f5402-107">**目前值和相關資料的狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="f5402-108">**轉換狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="f5402-109">**著色狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="f5402-110">**光源狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="f5402-111">**柵格化狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="f5402-112">**紋理狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="f5402-113">**圖元作業**</span><span class="sxs-lookup"><span data-stu-id="f5402-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="f5402-114">**畫面格緩衝區控制項狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="f5402-115">**圖元狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="f5402-116">**評估工具狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="f5402-117">**提示狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="f5402-118">**實作為相依狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="f5402-119">**與執行相依的 Pixel-Depth 狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="f5402-120">**其他狀態變數**</span><span class="sxs-lookup"><span data-stu-id="f5402-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="f5402-121">針對每個變數，此主題會列出描述、屬性群組、初始或最小值，以及建議用來取得它的 [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)函數。</span><span class="sxs-lookup"><span data-stu-id="f5402-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="f5402-122">您可以使用 [**glGetBooleanv**](glgetbooleanv.md)、 [**glGetIntegerv**](glgetintegerv.md)、 [**glGetFloatv**](glgetfloatv.md)或 [**glGetDoublev**](glgetdoublev.md) 取得的狀態變數，只會列出其中一個 functionsthe，最適合傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f5402-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="f5402-123">您無法使用 [**glIsEnabled**](glisenabled.md)取得這些狀態變數。</span><span class="sxs-lookup"><span data-stu-id="f5402-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="f5402-124">不過，您可以使用 **glGetBooleanv**、 **glGetIntegerv**、 **glGetFloatv** 和 **glGetDoublev** 取得 **glIsEnabled** 列為查詢函數的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="f5402-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="f5402-125">您可以使用該函式，取得任何其他函式僅列為查詢函數的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="f5402-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="f5402-126">如果未列出任何屬性群組，則變數不屬於任何群組。</span><span class="sxs-lookup"><span data-stu-id="f5402-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="f5402-127">您可以查詢的所有狀態變數（除了執行相依的狀態變數）都有初始值。</span><span class="sxs-lookup"><span data-stu-id="f5402-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="f5402-128">若要判斷未列出任何初始值之變數的初始值，請參閱該變數的參考或</span><span class="sxs-lookup"><span data-stu-id="f5402-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="f5402-129">*OpenGL 參考手冊*。</span><span class="sxs-lookup"><span data-stu-id="f5402-129">*OpenGL Reference Manual*.</span></span>

 

 




