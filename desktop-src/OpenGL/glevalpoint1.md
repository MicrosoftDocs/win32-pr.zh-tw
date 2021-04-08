---
title: 'glEvalPoint1 函式 (Gl) '
description: 'GlEvalPoint1 和 glEvalPoint2 函數會產生和評估網格中的單一點。 |glEvalPoint1 函式 (Gl) '
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853888"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="803d9-105">glEvalPoint1 函式</span><span class="sxs-lookup"><span data-stu-id="803d9-105">glEvalPoint1 function</span></span>

<span data-ttu-id="803d9-106">[**GlEvalPoint1**](glevalpoint.md)和 **glEvalPoint2** 函數會產生和評估網格中的單一點。</span><span class="sxs-lookup"><span data-stu-id="803d9-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="803d9-107">語法</span><span class="sxs-lookup"><span data-stu-id="803d9-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="803d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="803d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803d9-109">*i*</span><span class="sxs-lookup"><span data-stu-id="803d9-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="803d9-110">方格網域變數 *i* 的整數值。</span><span class="sxs-lookup"><span data-stu-id="803d9-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803d9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="803d9-111">Return value</span></span>

<span data-ttu-id="803d9-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="803d9-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="803d9-113">備註</span><span class="sxs-lookup"><span data-stu-id="803d9-113">Remarks</span></span>

<span data-ttu-id="803d9-114">[**GlMapGrid**](glmapgrid-functions.md)和 [**glEvalMesh**](glevalmesh-functions.md)函式會以串聯方式使用，以有效率地產生和評估一連串的平均地圖定義域值。</span><span class="sxs-lookup"><span data-stu-id="803d9-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="803d9-115">您可以使用 **glEvalPoint** 來評估 **glEvalMesh** 所進行的相同 gridspace 中的單一方格點。</span><span class="sxs-lookup"><span data-stu-id="803d9-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="803d9-116">呼叫 [**glEvalPoint1**](glevalpoint.md) 相當於呼叫</span><span class="sxs-lookup"><span data-stu-id="803d9-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="803d9-117">**glEvalCoord1** (*i* ？*u*  +*u* 1 ) ;</span><span class="sxs-lookup"><span data-stu-id="803d9-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="803d9-118">其中</span><span class="sxs-lookup"><span data-stu-id="803d9-118">where</span></span>

<span data-ttu-id="803d9-119">?*u* = (*u* 2 *u* 1 ) /*n*</span><span class="sxs-lookup"><span data-stu-id="803d9-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="803d9-120">和 *n*、 *u* 1 和 *u* 2 是最近 **glMapGrid1** 函數的引數。</span><span class="sxs-lookup"><span data-stu-id="803d9-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="803d9-121">其中一個絕對數值需求是，如果 *我* 是  =  *n*，則會從 (*i* 計算值？*u* + u1 ) 剛好是 *u* 2。</span><span class="sxs-lookup"><span data-stu-id="803d9-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="803d9-122">在二維案例中， **glEvalPoint2**，let</span><span class="sxs-lookup"><span data-stu-id="803d9-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="803d9-123">?*u* = (*u* 2 *u* 1 ) /*n*</span><span class="sxs-lookup"><span data-stu-id="803d9-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="803d9-124">?*v* = (*v* 2 *v* 1 ) /*m*</span><span class="sxs-lookup"><span data-stu-id="803d9-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="803d9-125">其中 *n*、 *u* 1、 *u* 2、 *m*、 *v* 1 和 *v* 2 是最新 **glMapGrid2** 函式的引數。</span><span class="sxs-lookup"><span data-stu-id="803d9-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="803d9-126">然後， **glEvalPoint2** 函式相當於呼叫</span><span class="sxs-lookup"><span data-stu-id="803d9-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="803d9-127">**glEvalCoord2** (*i* ？*u*  + *u* 1、 *j* ？*v*  + *v* 1 ) ;</span><span class="sxs-lookup"><span data-stu-id="803d9-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="803d9-128">唯一的絕對數值需求是，如果 *我* 是 = *n*，則會從 (*i* 計算值？*u*  +  *u* 1 ) 完全是 u2，如果是 *j*  =  *m*，則是從 (*j* 計算的值？*v v*  +  \*\* 1 ) 正好是 *v* 2。</span><span class="sxs-lookup"><span data-stu-id="803d9-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="803d9-129">下列函式會取得 [**glEvalPoint1**](glevalpoint.md) 和 **glEvalPoint2** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="803d9-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="803d9-130">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="803d9-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="803d9-131">具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="803d9-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="803d9-132">具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="803d9-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="803d9-133">具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="803d9-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="803d9-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="803d9-134">Requirements</span></span>



| <span data-ttu-id="803d9-135">需求</span><span class="sxs-lookup"><span data-stu-id="803d9-135">Requirement</span></span> | <span data-ttu-id="803d9-136">值</span><span class="sxs-lookup"><span data-stu-id="803d9-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="803d9-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="803d9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="803d9-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="803d9-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="803d9-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="803d9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="803d9-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="803d9-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="803d9-141">標頭</span><span class="sxs-lookup"><span data-stu-id="803d9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="803d9-142"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="803d9-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="803d9-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="803d9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="803d9-144"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="803d9-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="803d9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="803d9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="803d9-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803d9-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803d9-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="803d9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803d9-148">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="803d9-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="803d9-149">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="803d9-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="803d9-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="803d9-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="803d9-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="803d9-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="803d9-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="803d9-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="803d9-153">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="803d9-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





