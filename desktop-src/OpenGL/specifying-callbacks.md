---
title: 指定回呼
description: 您最多可以為鑲嵌式指定五個回呼函數。
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- " (X.GLU 隊) 的 OpenGL 公用程式，指定回呼函式"
- X.GLU 隊 (OpenGL 公用程式) ，指定回呼函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507409"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="c055e-105">指定回呼</span><span class="sxs-lookup"><span data-stu-id="c055e-105">Specifying Callbacks</span></span>

<span data-ttu-id="c055e-106">您最多可以為鑲嵌式指定五個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c055e-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="c055e-107">您未指定的任何函式都不會在鑲嵌期間呼叫，且您不會取得任何可能傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="c055e-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="c055e-108">您可以使用 [*gluTessCallback*](glutess.md)來指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c055e-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="c055e-109">**GluTessCallback** 函式 *會讓回呼* 函式與鑲嵌式物件 *tessobj* 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c055e-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="c055e-110">回呼的類型取決於參數 *類型*，可以是 **X.glu 隊 \_ BEGIN**、 **X.glu 隊 \_ EDGE \_ 旗** 標、 **x.glu 隊 \_ 頂點**、 **x.glu 隊 \_ END** 或 **x.glu 隊 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="c055e-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="c055e-111">五個可能的回呼函數具有下列原型。</span><span class="sxs-lookup"><span data-stu-id="c055e-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="c055e-112">回呼函數</span><span class="sxs-lookup"><span data-stu-id="c055e-112">Callback function</span></span>   | <span data-ttu-id="c055e-113">原型</span><span class="sxs-lookup"><span data-stu-id="c055e-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="c055e-114">**X.GLU 隊 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="c055e-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="c055e-115">**void** **Begin** ( \**GLenum \* \* \* 類型* ) ;</span><span class="sxs-lookup"><span data-stu-id="c055e-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="c055e-116">**X.GLU 隊 \_ EDGE \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="c055e-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="c055e-117">**void** **EdgeFlag** ( \**GLboolean \* \* \* 旗* 標 ) ;</span><span class="sxs-lookup"><span data-stu-id="c055e-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="c055e-118">**X.GLU 隊 \_ 頂點**</span><span class="sxs-lookup"><span data-stu-id="c055e-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="c055e-119">**void** **頂點** ( \**void \* \* \* \* 資料* ) ;</span><span class="sxs-lookup"><span data-stu-id="c055e-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="c055e-120">**X.GLU 隊 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="c055e-120">**GLU\_END**</span></span>        | <span data-ttu-id="c055e-121">**void** **end** ( *void* ) ;</span><span class="sxs-lookup"><span data-stu-id="c055e-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="c055e-122">**X.GLU 隊 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c055e-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="c055e-123">**void** **Error** ( \**GLenum \* \* \* errno* ) ;</span><span class="sxs-lookup"><span data-stu-id="c055e-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="c055e-124">若要變更回呼函數，請使用新的函式來呼叫 [*gluTessCallback*](glutess.md) 。</span><span class="sxs-lookup"><span data-stu-id="c055e-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="c055e-125">若要消除回呼函式，而不將它取代為新的函式，請針對適當的函式傳遞 **gluTessCallback** 為 null 指標。</span><span class="sxs-lookup"><span data-stu-id="c055e-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="c055e-126">當鑲嵌式進行時，回呼函式的呼叫方式類似于使用 OpenGL 函數 [**glBegin**](glbegin.md)、 [glEdgeFlag](gledgeflag-functions.md)、 [glVertex](glvertex-functions.md)和 [**glEnd**](glend.md)。</span><span class="sxs-lookup"><span data-stu-id="c055e-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="c055e-127">使用三個可能參數中的其中一個來叫用 **X.glu 隊 \_ BEGIN** 回呼函數：</span><span class="sxs-lookup"><span data-stu-id="c055e-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="c055e-128">GL \_ 三角形 \_ 風扇</span><span class="sxs-lookup"><span data-stu-id="c055e-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="c055e-129">GL \_ 三角形 \_ 條紋</span><span class="sxs-lookup"><span data-stu-id="c055e-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="c055e-130">GL \_ 三角形</span><span class="sxs-lookup"><span data-stu-id="c055e-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="c055e-131">呼叫 **X.glu 隊 \_ BEGIN** 回呼函式，並在呼叫與 **x.glu 隊 \_ END** 相關聯的回呼函式之前，會叫用一些 **x.glu 隊 \_ 邊緣 \_ 旗** 標和 **x.glu 隊 \_ 頂點** 回呼的組合。</span><span class="sxs-lookup"><span data-stu-id="c055e-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="c055e-132">相關聯的頂點和邊緣旗標在 **glBegin** (GL \_ 三角形 \_ 風扇) 、 **glBegin** (gl \_ 三角形區域 \_) 或 **glBegin** (gl 三角形 \_ **)** 和相符 **glEnd** 之間，會完全以 OpenGL 來解讀。</span><span class="sxs-lookup"><span data-stu-id="c055e-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="c055e-133">因為邊緣旗標在三角形風扇或三角形區域中沒有任何意義，所以如果有與 **X.glu 隊 \_ edge \_ 旗** 標相關聯的回呼函式，則只會使用 **GL \_ 三角形** 來呼叫 **x.glu 隊 \_ 開始** 回呼。</span><span class="sxs-lookup"><span data-stu-id="c055e-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="c055e-134">**X.glu 隊 \_ EDGE \_ 旗** 標回呼函式可以類似至 OpenGL [glEdgeFlag](gledgeflag-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="c055e-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="c055e-135">如果鑲嵌期間發生錯誤，則會叫用錯誤回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c055e-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="c055e-136">錯誤回呼函式會傳遞 X.GLU 隊錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="c055e-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="c055e-137">您可以使用 [**gluErrorString**](gluerrorstring.md) 函數取得描述錯誤的字元字串。</span><span class="sxs-lookup"><span data-stu-id="c055e-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




