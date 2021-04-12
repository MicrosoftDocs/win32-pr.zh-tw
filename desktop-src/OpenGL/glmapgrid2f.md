---
title: 'glMapGrid2f 函式 (Gl) '
description: '定義一維網格。 |glMapGrid2f 函式 (Gl) '
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- glMapGrid2f 函式 OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087e42aa3d490ec605b4478d5691b256271268f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195883"
---
# <a name="glmapgrid2f-function"></a><span data-ttu-id="fdb61-105">glMapGrid2f 函式</span><span class="sxs-lookup"><span data-stu-id="fdb61-105">glMapGrid2f function</span></span>

<span data-ttu-id="fdb61-106">定義一維網格。</span><span class="sxs-lookup"><span data-stu-id="fdb61-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb61-107">語法</span><span class="sxs-lookup"><span data-stu-id="fdb61-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a><span data-ttu-id="fdb61-108">參數</span><span class="sxs-lookup"><span data-stu-id="fdb61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb61-109">*聯合國*</span><span class="sxs-lookup"><span data-stu-id="fdb61-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-110">方格範圍間隔 u1，u2 的資料分割數目 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="fdb61-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="fdb61-111">這個值必須是正數。</span><span class="sxs-lookup"><span data-stu-id="fdb61-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="fdb61-112">*u1*</span><span class="sxs-lookup"><span data-stu-id="fdb61-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-113">用來當做整數方格定義域值 i = 0 之對應的值。</span><span class="sxs-lookup"><span data-stu-id="fdb61-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="fdb61-114">*u2*</span><span class="sxs-lookup"><span data-stu-id="fdb61-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-115">值，用來當做整數方格定義域值 i = un 的對應。</span><span class="sxs-lookup"><span data-stu-id="fdb61-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="fdb61-116">*vn*</span><span class="sxs-lookup"><span data-stu-id="fdb61-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-117">方格範圍間隔 v1、v2 中的資料分割數目 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="fdb61-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="fdb61-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="fdb61-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-119">用來當做整數方格定義域值 j = 0 對應的值。</span><span class="sxs-lookup"><span data-stu-id="fdb61-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="fdb61-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="fdb61-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="fdb61-121">用來當做整數方格定義域值 j = vn 之對應的值。</span><span class="sxs-lookup"><span data-stu-id="fdb61-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb61-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdb61-122">Return value</span></span>

<span data-ttu-id="fdb61-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fdb61-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fdb61-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fdb61-124">Error codes</span></span>

<span data-ttu-id="fdb61-125">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fdb61-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fdb61-126">Name</span><span class="sxs-lookup"><span data-stu-id="fdb61-126">Name</span></span>                                                                                                  | <span data-ttu-id="fdb61-127">意義</span><span class="sxs-lookup"><span data-stu-id="fdb61-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdb61-128"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="fdb61-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fdb61-129">*Un* 或 *vn* 不是正數。</span><span class="sxs-lookup"><span data-stu-id="fdb61-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="fdb61-130"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="fdb61-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fdb61-131">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="fdb61-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fdb61-132">備註</span><span class="sxs-lookup"><span data-stu-id="fdb61-132">Remarks</span></span>

<span data-ttu-id="fdb61-133">**GlMapGrid** 和 [glEvalMesh](glevalmesh-functions.md)函式會以串聯方式使用，以有效率地產生和評估一連串的平均地圖定義域值。</span><span class="sxs-lookup"><span data-stu-id="fdb61-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="fdb61-134">GlEvalMesh 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md) 和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。</span><span class="sxs-lookup"><span data-stu-id="fdb61-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="fdb61-135">[**GlMapGrid1**](glmapgrid1d.md)和 [**glMapGrid2**](glmapgrid2d.md)函式會指定在 i (或 i 和 j) 整數格線座標之間的線性方格對應、u (或您和 v) 浮點數評估對應座標。</span><span class="sxs-lookup"><span data-stu-id="fdb61-135">The [**glMapGrid1**](glmapgrid1d.md) and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="fdb61-136">如需如何評估您和 v 座標的詳細資訊，請參閱 [**glMap1**](glmap1.md) 和 [**glMap2**](glmap2.md) 。</span><span class="sxs-lookup"><span data-stu-id="fdb61-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="fdb61-137">[**GlMapGrid1**](glmapgrid1d.md)函式會指定單一線性對應，讓整數格線座標0完全對應至 u1，而整數網格 *線座標則* 完全不會對應到 *u2*。</span><span class="sxs-lookup"><span data-stu-id="fdb61-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="fdb61-138">所有其他的整數網格 *線座標都* 有對應，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fdb61-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="fdb61-139">*u = i (u2 u1) /un + u1*</span><span class="sxs-lookup"><span data-stu-id="fdb61-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="fdb61-140">[**GlMapGrid2**](glmapgrid2d.md)函式會指定兩個這類線性對應。</span><span class="sxs-lookup"><span data-stu-id="fdb61-140">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="fdb61-141">一個將整數格線座標 *i = 0* 精確地對應至 *u1*，而整數格線座標 *i =* 完全不是 *u2*。</span><span class="sxs-lookup"><span data-stu-id="fdb61-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="fdb61-142">另一個會將整數格線座標 *j = 0* 精確對應至 *v1*，而整數格線座標 *j = vn* 精確至 *v2*。</span><span class="sxs-lookup"><span data-stu-id="fdb61-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="fdb61-143">其他整數格線座標 i 和 j 會對應到</span><span class="sxs-lookup"><span data-stu-id="fdb61-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="fdb61-144">*u = i (u2 u1) /un + u1*</span><span class="sxs-lookup"><span data-stu-id="fdb61-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="fdb61-145">*v = j (v2 v1) /vn + v1*</span><span class="sxs-lookup"><span data-stu-id="fdb61-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="fdb61-146">[**GlMapGrid**](glmapgrid1d.md)所指定的對應會使用 [glEvalMesh](glevalmesh-functions.md)和 [**glEvalPoint**](glevalpoint.md)的相同方式。</span><span class="sxs-lookup"><span data-stu-id="fdb61-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="fdb61-147">下列函式會取出與 [**glMapGrid**](glmapgrid1d.md)相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="fdb61-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="fdb61-148">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="fdb61-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="fdb61-149">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="fdb61-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="fdb61-150">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="fdb61-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="fdb61-151">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="fdb61-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="fdb61-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdb61-152">Requirements</span></span>



| <span data-ttu-id="fdb61-153">需求</span><span class="sxs-lookup"><span data-stu-id="fdb61-153">Requirement</span></span> | <span data-ttu-id="fdb61-154">值</span><span class="sxs-lookup"><span data-stu-id="fdb61-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb61-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdb61-155">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb61-156">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdb61-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fdb61-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdb61-157">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb61-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdb61-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdb61-159">標頭</span><span class="sxs-lookup"><span data-stu-id="fdb61-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdb61-160"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="fdb61-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fdb61-161">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdb61-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdb61-162"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb61-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fdb61-163">DLL</span><span class="sxs-lookup"><span data-stu-id="fdb61-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdb61-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdb61-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdb61-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdb61-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb61-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fdb61-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fdb61-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fdb61-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fdb61-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="fdb61-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fdb61-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="fdb61-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="fdb61-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="fdb61-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="fdb61-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="fdb61-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="fdb61-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="fdb61-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





