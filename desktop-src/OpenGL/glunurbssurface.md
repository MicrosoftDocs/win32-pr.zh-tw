---
title: 'gluNurbsSurface 函式 (X.glu 隊) '
description: GluNurbsSurface 函式會定義非統一有理數 B 曲線 (NURBS) 介面的形狀。
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933890"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="aaec0-104">gluNurbsSurface 函式</span><span class="sxs-lookup"><span data-stu-id="aaec0-104">gluNurbsSurface function</span></span>

<span data-ttu-id="aaec0-105">**GluNurbsSurface** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 介面的形狀。</span><span class="sxs-lookup"><span data-stu-id="aaec0-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaec0-106">語法</span><span class="sxs-lookup"><span data-stu-id="aaec0-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="aaec0-107">參數</span><span class="sxs-lookup"><span data-stu-id="aaec0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaec0-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="aaec0-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="aaec0-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-110">*sknot \_ 計數*</span><span class="sxs-lookup"><span data-stu-id="aaec0-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-111">參數 *u* 方向中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="aaec0-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="aaec0-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-113">*Sknot \_ 計數* 的陣列會以參數 *u* 方向 nondecreasing 節點值。</span><span class="sxs-lookup"><span data-stu-id="aaec0-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-114">*tknot \_ 計數*</span><span class="sxs-lookup"><span data-stu-id="aaec0-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-115">參數化 *v* 方向中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="aaec0-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="aaec0-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-117">*Tknot \_ 計數* 的陣列會 nondecreasing 在參數化 *v* 方向中的節點值。</span><span class="sxs-lookup"><span data-stu-id="aaec0-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-118">*s \_ stride*</span><span class="sxs-lookup"><span data-stu-id="aaec0-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-119">位移 (為 *ctlarray* 中參數 *u* 方向的連續控制點之間的單一 precisionfloating 點) 值。</span><span class="sxs-lookup"><span data-stu-id="aaec0-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-120">*t \_ stride*</span><span class="sxs-lookup"><span data-stu-id="aaec0-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-121">單一 precisionfloating 點值中的位移 (在 *ctlarray* 的參數式 *v* 方向的連續控制點之間) 。</span><span class="sxs-lookup"><span data-stu-id="aaec0-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="aaec0-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-123">陣列，包含 NURBS 表面的控制點。</span><span class="sxs-lookup"><span data-stu-id="aaec0-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="aaec0-124">參數 *u* 和 *v* 方向中連續控制點之間的位移，會由 *s \_ stride* 和 *t \_ stride* 提供。</span><span class="sxs-lookup"><span data-stu-id="aaec0-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="aaec0-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-126">NURBS 介面在參數 *u* 方向的順序。</span><span class="sxs-lookup"><span data-stu-id="aaec0-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="aaec0-127">順序比角度多一點，因此以 *u* 為立方的表面有 *u* 階4。</span><span class="sxs-lookup"><span data-stu-id="aaec0-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-128">*torder*</span><span class="sxs-lookup"><span data-stu-id="aaec0-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-129">NURBS 介面在參數化 *v* 方向的順序。</span><span class="sxs-lookup"><span data-stu-id="aaec0-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="aaec0-130">順序比角度多一點，因此 *v* 中的三個平面的 *v* 順序為4。</span><span class="sxs-lookup"><span data-stu-id="aaec0-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="aaec0-131">*type*</span><span class="sxs-lookup"><span data-stu-id="aaec0-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="aaec0-132">介面的類型。</span><span class="sxs-lookup"><span data-stu-id="aaec0-132">The type of the surface.</span></span> <span data-ttu-id="aaec0-133">*類型* 參數可以是任何有效的二維評估工具類型 (例如 GL \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ COLOR \_ 4) 。</span><span class="sxs-lookup"><span data-stu-id="aaec0-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaec0-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaec0-134">Return value</span></span>

<span data-ttu-id="aaec0-135">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aaec0-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaec0-136">備註</span><span class="sxs-lookup"><span data-stu-id="aaec0-136">Remarks</span></span>

<span data-ttu-id="aaec0-137">在 NURBS 介面定義中使用 **gluNurbsSurface** ，以描述在任何修剪) 之前 (的 nurbs 介面圖形。</span><span class="sxs-lookup"><span data-stu-id="aaec0-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="aaec0-138">若要標記 NURBS 介面定義的開頭，請使用 [**gluBeginSurface**](glubeginsurface.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaec0-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="aaec0-139">若要標記 NURBS 介面定義的結尾，請使用 [**gluEndSurface**](gluendsurface.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaec0-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="aaec0-140">只在 NURBS 介面定義中呼叫 **gluNurbsSurface** 。</span><span class="sxs-lookup"><span data-stu-id="aaec0-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="aaec0-141">您可以將位置、材質和色彩座標與介面產生關聯，方法是在 **gluBeginSurface** gluEndSurface 配對之間呈現個別的 **gluNurbsSurface** /  。</span><span class="sxs-lookup"><span data-stu-id="aaec0-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="aaec0-142">在單一 **gluBeginSurface** / **gluEndSurface** 配對中，您只能對 **gluNurbsSurface** 進行色彩、位置和材質資料的單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="aaec0-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="aaec0-143">只需進行一次呼叫，就能描述 (*類型* 為 gl \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4) 的介面位置。</span><span class="sxs-lookup"><span data-stu-id="aaec0-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="aaec0-144">您可以使用 GluNurbsCurve 和 GluPwlCurve 函式，在對 [**gluBeginTrim**](glubegintrim.md)和 [**gluEndTrim**](gluendtrim.md)的呼叫之間使用 [](glunurbscurve.md)和 [](glupwlcurve.md)函數來修剪 NURBS 介面。</span><span class="sxs-lookup"><span data-stu-id="aaec0-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="aaec0-145">在 *u* 方向中有 *sknot \_ 計數* 節點的 **gluNurbsSurface** ，以及訂單 *sorder* 和 *torder* 的 *v* 方向中的 *tknot \_ 計數* 節點，必須具有 (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) 控制點。</span><span class="sxs-lookup"><span data-stu-id="aaec0-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaec0-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaec0-146">Requirements</span></span>



| <span data-ttu-id="aaec0-147">需求</span><span class="sxs-lookup"><span data-stu-id="aaec0-147">Requirement</span></span> | <span data-ttu-id="aaec0-148">值</span><span class="sxs-lookup"><span data-stu-id="aaec0-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aaec0-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaec0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="aaec0-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaec0-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aaec0-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaec0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="aaec0-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaec0-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aaec0-153">標頭</span><span class="sxs-lookup"><span data-stu-id="aaec0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaec0-154"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="aaec0-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="aaec0-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="aaec0-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="aaec0-156"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaec0-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aaec0-157">DLL</span><span class="sxs-lookup"><span data-stu-id="aaec0-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaec0-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaec0-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaec0-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaec0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaec0-160">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="aaec0-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="aaec0-161">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="aaec0-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="aaec0-162">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="aaec0-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="aaec0-163">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="aaec0-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="aaec0-164">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="aaec0-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="aaec0-165">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="aaec0-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="aaec0-166">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="aaec0-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





