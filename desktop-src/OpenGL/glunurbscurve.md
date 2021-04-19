---
title: 'gluNurbsCurve 函式 (X.glu 隊) '
description: GluNurbsCurve 函式會定義非統一有理數 B 曲線 (NURBS) 曲線的形狀。
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967726"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="eeec5-104">gluNurbsCurve 函式</span><span class="sxs-lookup"><span data-stu-id="eeec5-104">gluNurbsCurve function</span></span>

<span data-ttu-id="eeec5-105">**GluNurbsCurve** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 曲線的形狀。</span><span class="sxs-lookup"><span data-stu-id="eeec5-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeec5-106">語法</span><span class="sxs-lookup"><span data-stu-id="eeec5-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="eeec5-107">參數</span><span class="sxs-lookup"><span data-stu-id="eeec5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeec5-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="eeec5-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="eeec5-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-110">*nknots*</span><span class="sxs-lookup"><span data-stu-id="eeec5-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-111">*節點* 中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="eeec5-111">The number of knots in *knot*.</span></span> <span data-ttu-id="eeec5-112">*Nknots* 參數等於控制點的數目加上順序。</span><span class="sxs-lookup"><span data-stu-id="eeec5-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-113">*結*</span><span class="sxs-lookup"><span data-stu-id="eeec5-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-114">*Nknots* nondecreasing 節點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="eeec5-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-115">*大步*</span><span class="sxs-lookup"><span data-stu-id="eeec5-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-116">位移 (為連續曲線控制點之間) 的單精確度浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="eeec5-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="eeec5-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-118">指向控制點陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="eeec5-118">A pointer to an array of control points.</span></span> <span data-ttu-id="eeec5-119">座標必須與 *類型* 一致。</span><span class="sxs-lookup"><span data-stu-id="eeec5-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-120">*order*</span><span class="sxs-lookup"><span data-stu-id="eeec5-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-121">NURBS 曲線的順序。</span><span class="sxs-lookup"><span data-stu-id="eeec5-121">The order of the NURBS curve.</span></span> <span data-ttu-id="eeec5-122">*Order* 參數等於度數 + 1;因此，三曲線的順序為4。</span><span class="sxs-lookup"><span data-stu-id="eeec5-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="eeec5-123">*type*</span><span class="sxs-lookup"><span data-stu-id="eeec5-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec5-124">曲線的型別。</span><span class="sxs-lookup"><span data-stu-id="eeec5-124">The type of the curve.</span></span> <span data-ttu-id="eeec5-125">如果此曲線定義在 [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md)配對內，則該類型可以是任何有效的一維評估工具類型 (例如 GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ COLOR \_ 4) 。</span><span class="sxs-lookup"><span data-stu-id="eeec5-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="eeec5-126">在 [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md)配對之間，唯一有效的類型為 x.glu 隊 \_ MAP1 \_ TRIM \_ 2 和 x.glu 隊 \_ MAP1 \_ TRIM \_ 3。</span><span class="sxs-lookup"><span data-stu-id="eeec5-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeec5-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeec5-127">Return value</span></span>

<span data-ttu-id="eeec5-128">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eeec5-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeec5-129">備註</span><span class="sxs-lookup"><span data-stu-id="eeec5-129">Remarks</span></span>

<span data-ttu-id="eeec5-130">當 **gluNurbsCurve** 出現在 **gluBeginCurve** / **gluEndCurve** 配對之間時，它會描述要呈現的曲線。</span><span class="sxs-lookup"><span data-stu-id="eeec5-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="eeec5-131">您可以建立位置、材質和色彩座標的關聯，方法是將它們呈現為 **gluBeginCurve** / **gluEndCurve** 配對之間個別的 gluNurbsCurve。</span><span class="sxs-lookup"><span data-stu-id="eeec5-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="eeec5-132">請勿對單一 **gluBeginCurve** gluEndCurve 配對內的色彩、位置和材質資料進行一個以上的 **gluNurbsCurve** 呼叫 /  。</span><span class="sxs-lookup"><span data-stu-id="eeec5-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="eeec5-133">進行精確的呼叫，以描述曲線的位置 (一 *種* gl \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4) 。</span><span class="sxs-lookup"><span data-stu-id="eeec5-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="eeec5-134">當 **gluNurbsCurve** 出現在 [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md)配對之間時，它會描述 NURBS 表面上的修剪曲線。</span><span class="sxs-lookup"><span data-stu-id="eeec5-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="eeec5-135">如果 *type* 是 X.glu 隊 \_ MAP1 \_ TRIM \_ 2，則會以二維 (*u* 和 *v*) 參數空間來描述曲線。</span><span class="sxs-lookup"><span data-stu-id="eeec5-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="eeec5-136">如果它是 X.GLU 隊 \_ MAP1 \_ TRIM \_ 3，則會以二維同質 (*u*、 *v* 和 *w*) 參數空間來描述曲線。</span><span class="sxs-lookup"><span data-stu-id="eeec5-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="eeec5-137">如需修剪曲線的詳細討論，請參閱 **gluBeginTrim**。</span><span class="sxs-lookup"><span data-stu-id="eeec5-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="eeec5-138">範例</span><span class="sxs-lookup"><span data-stu-id="eeec5-138">Examples</span></span>

<span data-ttu-id="eeec5-139">下列函式會以法線呈現有紋理的 NURBS 曲線：</span><span class="sxs-lookup"><span data-stu-id="eeec5-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="eeec5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeec5-140">Requirements</span></span>



| <span data-ttu-id="eeec5-141">需求</span><span class="sxs-lookup"><span data-stu-id="eeec5-141">Requirement</span></span> | <span data-ttu-id="eeec5-142">值</span><span class="sxs-lookup"><span data-stu-id="eeec5-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eeec5-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeec5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eeec5-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeec5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eeec5-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeec5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eeec5-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeec5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eeec5-147">標頭</span><span class="sxs-lookup"><span data-stu-id="eeec5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeec5-148"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeec5-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="eeec5-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="eeec5-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="eeec5-150"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeec5-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eeec5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="eeec5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeec5-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeec5-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeec5-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeec5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeec5-154">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="eeec5-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="eeec5-155">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="eeec5-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="eeec5-156">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="eeec5-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="eeec5-157">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="eeec5-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="eeec5-158">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="eeec5-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="eeec5-159">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="eeec5-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





