---
title: 'glEvalMesh2 函式 (Gl) '
description: 計算點或線條的二維方格。
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685700"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="0eba1-104">glEvalMesh2 函式</span><span class="sxs-lookup"><span data-stu-id="0eba1-104">glEvalMesh2 function</span></span>

<span data-ttu-id="0eba1-105">計算點或線條的二維方格。</span><span class="sxs-lookup"><span data-stu-id="0eba1-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eba1-106">語法</span><span class="sxs-lookup"><span data-stu-id="0eba1-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="0eba1-107">參數</span><span class="sxs-lookup"><span data-stu-id="0eba1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eba1-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="0eba1-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="0eba1-109">值，指定是否要計算點、線條或多邊形的二維網格。</span><span class="sxs-lookup"><span data-stu-id="0eba1-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="0eba1-110">接受下列符號常數： GL \_ 點、gl \_ 線路和 gl \_ 填滿。</span><span class="sxs-lookup"><span data-stu-id="0eba1-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="0eba1-111">*i1*</span><span class="sxs-lookup"><span data-stu-id="0eba1-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="0eba1-112">方格網域變數 i 的第一個整數值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="0eba1-113">*i2*</span><span class="sxs-lookup"><span data-stu-id="0eba1-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="0eba1-114">方格網域變數 i 的最後一個整數值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="0eba1-115">*j1*</span><span class="sxs-lookup"><span data-stu-id="0eba1-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="0eba1-116">方格網域變數 j 的第一個整數值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="0eba1-117">*j2*</span><span class="sxs-lookup"><span data-stu-id="0eba1-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="0eba1-118">方格網域變數 j 的最後一個整數值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eba1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0eba1-119">Return value</span></span>

<span data-ttu-id="0eba1-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0eba1-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0eba1-121">Error codes</span></span>

<span data-ttu-id="0eba1-122">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0eba1-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0eba1-123">Name</span><span class="sxs-lookup"><span data-stu-id="0eba1-123">Name</span></span>                                                                                                  | <span data-ttu-id="0eba1-124">意義</span><span class="sxs-lookup"><span data-stu-id="0eba1-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0eba1-125"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="0eba1-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0eba1-126">表示 *模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="0eba1-127"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0eba1-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0eba1-128">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="0eba1-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="0eba1-129">備註</span><span class="sxs-lookup"><span data-stu-id="0eba1-129">Remarks</span></span>

<span data-ttu-id="0eba1-130">使用 [**glMapGrid**](glmapgrid-functions.md) 和 [**glEvalMesh**](glevalmesh-functions.md) ，以便有效率地產生和評估一系列平均間距的地圖定義域值。</span><span class="sxs-lookup"><span data-stu-id="0eba1-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="0eba1-131">**GlEvalMesh** 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md)和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。</span><span class="sxs-lookup"><span data-stu-id="0eba1-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="0eba1-132">Mode 參數會決定產生的頂點是否以點、線條或填滿的多邊形連接。</span><span class="sxs-lookup"><span data-stu-id="0eba1-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="0eba1-133">在二維案例中， **glEvalMesh2**，let</span><span class="sxs-lookup"><span data-stu-id="0eba1-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="0eba1-134">?</span><span class="sxs-lookup"><span data-stu-id="0eba1-134">?</span></span> <span data-ttu-id="0eba1-135">u = (u2 u1) /n</span><span class="sxs-lookup"><span data-stu-id="0eba1-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="0eba1-136">?</span><span class="sxs-lookup"><span data-stu-id="0eba1-136">?</span></span> <span data-ttu-id="0eba1-137">v = (v2 v1) /m，</span><span class="sxs-lookup"><span data-stu-id="0eba1-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="0eba1-138">其中 n、u1、u2、m、v1 和 v2 是最新 [**glMapGrid2**](glmapgrid-functions.md) 函式的引數。</span><span class="sxs-lookup"><span data-stu-id="0eba1-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="0eba1-139">然後，如果 *mode* 是 GL \_ FILL， **glEvalMesh2** 相當於：</span><span class="sxs-lookup"><span data-stu-id="0eba1-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="0eba1-140">若為 (j = j1;j < j2;j + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="0eba1-141">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-141">{</span></span>

<span data-ttu-id="0eba1-142">[**glBegin**](glbegin.md) (GL \_ 四個 \_ 帶) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="0eba1-143">針對 (i = i1;i <= i2;i + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="0eba1-144">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-144">{</span></span>

<span data-ttu-id="0eba1-145">[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1 ( ) ，j？</span><span class="sxs-lookup"><span data-stu-id="0eba1-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="0eba1-146">v + v1) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-146">v + v1);</span></span>

<span data-ttu-id="0eba1-147">[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1 ( ) ， (j + 1) ？</span><span class="sxs-lookup"><span data-stu-id="0eba1-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="0eba1-148">v + v1) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-148">v + v1);</span></span>

<span data-ttu-id="0eba1-149">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-149">}</span></span>

<span data-ttu-id="0eba1-150">[**glEnd**](glend.md) ( ) ;}</span><span class="sxs-lookup"><span data-stu-id="0eba1-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="0eba1-151">如果 *mode* 是 GL \_ 行，則呼叫 **glEvalMesh2** 相當於：</span><span class="sxs-lookup"><span data-stu-id="0eba1-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="0eba1-152">若為 (j = j1;j <= j2;j + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="0eba1-153">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-153">{</span></span>

<span data-ttu-id="0eba1-154">[**glBegin**](glbegin.md) (GL \_ 行 \_ 帶) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="0eba1-155">針對 (i = i1;i <= i2;i + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="0eba1-156">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-156">{</span></span>

<span data-ttu-id="0eba1-157">[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="0eba1-158">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-158">}</span></span>

<span data-ttu-id="0eba1-159">[**glEnd**](glend.md) ( ) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="0eba1-160">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-160">}</span></span>

<span data-ttu-id="0eba1-161">針對 (i = i1;i <= i2;i + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="0eba1-162">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-162">{</span></span>

<span data-ttu-id="0eba1-163">[**glBegin**](glbegin.md) (GL \_ 行 \_ 帶) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="0eba1-164">若為 (j = j1;j <= j1;j + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="0eba1-165">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-165">{</span></span>

<span data-ttu-id="0eba1-166">[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="0eba1-167">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-167">}</span></span>

<span data-ttu-id="0eba1-168">glEnd ( ) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-168">glEnd( );</span></span>

<span data-ttu-id="0eba1-169">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-169">}</span></span>

<span data-ttu-id="0eba1-170">最後，如果 *模式* 是 GL \_ 點，則呼叫 **glEvalMesh2** 相當於：</span><span class="sxs-lookup"><span data-stu-id="0eba1-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="0eba1-171">[**glBegin**](glbegin.md) (GL \_ 點) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="0eba1-172">若為 (j = j1;j <= j2;j + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="0eba1-173">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-173">{</span></span>

<span data-ttu-id="0eba1-174">針對 (i = i1;i <= i2;i + = 1) </span><span class="sxs-lookup"><span data-stu-id="0eba1-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="0eba1-175">{</span><span class="sxs-lookup"><span data-stu-id="0eba1-175">{</span></span>

<span data-ttu-id="0eba1-176">[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="0eba1-177">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-177">}</span></span>

<span data-ttu-id="0eba1-178">}</span><span class="sxs-lookup"><span data-stu-id="0eba1-178">}</span></span>

<span data-ttu-id="0eba1-179">[**glEnd**](glend.md) ( ) ;</span><span class="sxs-lookup"><span data-stu-id="0eba1-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="0eba1-180">在這三種情況下，唯一的絕對數值需求是，如果 i = n，則是從 i 計算的值？u + u1 正好是 u2，如果 j = m，則是從 j 計算的值？v + v1 正好為 v2。</span><span class="sxs-lookup"><span data-stu-id="0eba1-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="0eba1-181">下列函式會取出與 **glEvalMesh** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="0eba1-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="0eba1-182">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="0eba1-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="0eba1-183">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet</span><span class="sxs-lookup"><span data-stu-id="0eba1-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="0eba1-184">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="0eba1-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="0eba1-185">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet</span><span class="sxs-lookup"><span data-stu-id="0eba1-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="0eba1-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="0eba1-186">Requirements</span></span>



| <span data-ttu-id="0eba1-187">需求</span><span class="sxs-lookup"><span data-stu-id="0eba1-187">Requirement</span></span> | <span data-ttu-id="0eba1-188">值</span><span class="sxs-lookup"><span data-stu-id="0eba1-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eba1-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0eba1-189">Minimum supported client</span></span><br/> | <span data-ttu-id="0eba1-190">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0eba1-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0eba1-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0eba1-191">Minimum supported server</span></span><br/> | <span data-ttu-id="0eba1-192">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0eba1-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0eba1-193">標頭</span><span class="sxs-lookup"><span data-stu-id="0eba1-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eba1-194"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0eba1-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0eba1-195">程式庫</span><span class="sxs-lookup"><span data-stu-id="0eba1-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="0eba1-196"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0eba1-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0eba1-197">DLL</span><span class="sxs-lookup"><span data-stu-id="0eba1-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eba1-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eba1-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





