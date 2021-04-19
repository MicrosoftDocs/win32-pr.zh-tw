---
title: 'gluPwlCurve 函式 (X.glu 隊) '
description: GluPwlCurve 函式描述分段線性非統一的有理數 B 曲線 (NURBS) 修剪曲線。
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999818"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="e505b-104">gluPwlCurve 函式</span><span class="sxs-lookup"><span data-stu-id="e505b-104">gluPwlCurve function</span></span>

<span data-ttu-id="e505b-105">**GluPwlCurve** 函式描述分段線性非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 修剪曲線。</span><span class="sxs-lookup"><span data-stu-id="e505b-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="e505b-106">語法</span><span class="sxs-lookup"><span data-stu-id="e505b-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="e505b-107">參數</span><span class="sxs-lookup"><span data-stu-id="e505b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e505b-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="e505b-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="e505b-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="e505b-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e505b-110">*計數*</span><span class="sxs-lookup"><span data-stu-id="e505b-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="e505b-111">曲線上的點數目。</span><span class="sxs-lookup"><span data-stu-id="e505b-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="e505b-112">*array*</span><span class="sxs-lookup"><span data-stu-id="e505b-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="e505b-113">包含曲線點的陣列。</span><span class="sxs-lookup"><span data-stu-id="e505b-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="e505b-114">*大步*</span><span class="sxs-lookup"><span data-stu-id="e505b-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="e505b-115">位移 (在曲線上的點之間) 的單精確度浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="e505b-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="e505b-116">*type*</span><span class="sxs-lookup"><span data-stu-id="e505b-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e505b-117">曲線的類型。</span><span class="sxs-lookup"><span data-stu-id="e505b-117">The type of curve.</span></span> <span data-ttu-id="e505b-118">必須是 X.GLU 隊 \_ MAP1 \_ trim \_ 2 或 x.glu 隊 \_ MAP1 \_ TRIM \_ 3。</span><span class="sxs-lookup"><span data-stu-id="e505b-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e505b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e505b-119">Return value</span></span>

<span data-ttu-id="e505b-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e505b-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e505b-121">備註</span><span class="sxs-lookup"><span data-stu-id="e505b-121">Remarks</span></span>

<span data-ttu-id="e505b-122">**GluPwlCurve** 函數描述 NURBS 表面的分段線性修剪曲線。</span><span class="sxs-lookup"><span data-stu-id="e505b-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="e505b-123">分段線性曲線包含要修剪的 NURBS 介面之參數空間中的點座標清單。</span><span class="sxs-lookup"><span data-stu-id="e505b-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="e505b-124">這些點會與線段連接以形成曲線。</span><span class="sxs-lookup"><span data-stu-id="e505b-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="e505b-125">如果曲線是實際曲線的近似值，則點應該夠接近，如此一來，所產生的路徑就會顯示在應用程式中所使用的解析度上。</span><span class="sxs-lookup"><span data-stu-id="e505b-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="e505b-126">如果 *type* 是 X.glu 隊 \_ MAP1 \_ TRIM \_ 2，則會以二維 (*u* 和 *v*) 參數空間來描述曲線。</span><span class="sxs-lookup"><span data-stu-id="e505b-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="e505b-127">如果它是 X.GLU 隊 \_ MAP1 \_ TRIM \_ 3，則會以二維同質 (*u*、 *v* 和 *w*) 參數空間來描述曲線。</span><span class="sxs-lookup"><span data-stu-id="e505b-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="e505b-128">如需修剪曲線的詳細資訊，請參閱 [**gluBeginTrim**](glubegintrim.md)。</span><span class="sxs-lookup"><span data-stu-id="e505b-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e505b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e505b-129">Requirements</span></span>



| <span data-ttu-id="e505b-130">需求</span><span class="sxs-lookup"><span data-stu-id="e505b-130">Requirement</span></span> | <span data-ttu-id="e505b-131">值</span><span class="sxs-lookup"><span data-stu-id="e505b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e505b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e505b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e505b-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e505b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e505b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e505b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e505b-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e505b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e505b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e505b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e505b-137"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="e505b-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e505b-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="e505b-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e505b-139"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e505b-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e505b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e505b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e505b-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e505b-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e505b-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e505b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e505b-143">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="e505b-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="e505b-144">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="e505b-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="e505b-145">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="e505b-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="e505b-146">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="e505b-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





