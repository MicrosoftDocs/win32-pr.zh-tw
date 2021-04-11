---
title: 'gluEndTrim 函式 (X.glu 隊) '
description: 'GluBeginTrim 和 gluEndTrim 函式會分隔非統一的有理數 B 曲線 (NURBS) 修剪迴圈定義。 |gluEndTrim 函式 (X.glu 隊) '
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- gluEndTrim 函式 OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035270"
---
# <a name="gluendtrim-function"></a><span data-ttu-id="75683-105">gluEndTrim 函式</span><span class="sxs-lookup"><span data-stu-id="75683-105">gluEndTrim function</span></span>

<span data-ttu-id="75683-106">[**GluBeginTrim**](glubegintrim.md)和 **gluEndTrim** 函式會分隔非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 修剪迴圈定義。</span><span class="sxs-lookup"><span data-stu-id="75683-106">The [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="75683-107">語法</span><span class="sxs-lookup"><span data-stu-id="75683-107">Syntax</span></span>


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="75683-108">參數</span><span class="sxs-lookup"><span data-stu-id="75683-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75683-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="75683-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="75683-110">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="75683-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75683-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="75683-111">Return value</span></span>

<span data-ttu-id="75683-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="75683-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75683-113">備註</span><span class="sxs-lookup"><span data-stu-id="75683-113">Remarks</span></span>

<span data-ttu-id="75683-114">使用 [**gluBeginTrim**](glubegintrim.md) 來標示修剪迴圈的開頭，並使用 **gluEndTrim** 來標記修剪迴圈的結尾。</span><span class="sxs-lookup"><span data-stu-id="75683-114">Use [**gluBeginTrim**](glubegintrim.md) to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="75683-115">修剪迴圈是一組面向的曲線線段， (形成封閉曲線) ，以定義 NURBS 表面的界限。</span><span class="sxs-lookup"><span data-stu-id="75683-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="75683-116">您可以在 [**gluBeginSurface**](glubeginsurface.md) 和 [**gluEndSurface**](gluendsurface.md)的呼叫之間，將這些修剪迴圈包含在 NURBS 介面的定義中。</span><span class="sxs-lookup"><span data-stu-id="75683-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="75683-117">NURBS 介面的定義可以包含許多修剪迴圈。</span><span class="sxs-lookup"><span data-stu-id="75683-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="75683-118">例如，如果您撰寫的 NURBS 介面定義類似于帶有打孔的矩形，則定義會包含兩個修剪迴圈。</span><span class="sxs-lookup"><span data-stu-id="75683-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="75683-119">一個迴圈會定義矩形的外部邊緣;另一個則會定義「穿孔」孔。</span><span class="sxs-lookup"><span data-stu-id="75683-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="75683-120">這些修剪迴圈的定義會以 [**gluBeginTrim**](glubegintrim.md)  /  **gluEndTrim** 配對括住。</span><span class="sxs-lookup"><span data-stu-id="75683-120">The definitions of each of these trimming loops would be bracketed by a [**gluBeginTrim**](glubegintrim.md) / **gluEndTrim** pair.</span></span>

<span data-ttu-id="75683-121">單一封閉修剪迴圈的定義可以由多個曲線區段所組成，每個線段都是形成線性曲線的一連串直線線段， (查看 [**gluPwlCurve**](glupwlcurve.md)) ，例如單一 NURBS 曲線 ([**查看) ，**](glunurbscurve.md) 或是以任何順序結合兩者。</span><span class="sxs-lookup"><span data-stu-id="75683-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="75683-122">唯一可出現在 [**gluBeginTrim**](glubegintrim.md) 和 **gluEndTrim**) 呼叫 (之間的程式庫呼叫，就是 **gluPwlCurve** 和 **gluNurbsCurve**。</span><span class="sxs-lookup"><span data-stu-id="75683-122">The only library calls that can appear in a trimming-loop definition (between the calls to [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="75683-123">NURBS 表面的顯示區域是當曲線參數增加時，在修剪曲線左邊的定義域中的區域。</span><span class="sxs-lookup"><span data-stu-id="75683-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="75683-124">因此，NURBS 表面的保留區域是在逆時針修剪迴圈內，而非順向修剪迴圈外部。</span><span class="sxs-lookup"><span data-stu-id="75683-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="75683-125">針對稍早所述的矩形，矩形外部邊緣的修剪迴圈會以逆時針的方向執行，而向外執行的修剪迴圈則以順時針方向執行。</span><span class="sxs-lookup"><span data-stu-id="75683-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="75683-126">如果您使用多個曲線來定義單一修剪迴圈，則曲線線段必須形成封閉迴圈 (也就是說，每個曲線的端點都必須是下一個曲線的起點，而最後曲線的端點必須是第一個曲線) 的起點。</span><span class="sxs-lookup"><span data-stu-id="75683-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="75683-127">如果曲線的端點足以緊密地關閉，但不完全一致，則會強制它們相符。</span><span class="sxs-lookup"><span data-stu-id="75683-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="75683-128">如果端點未足夠關閉，則會產生錯誤結果 (查看 [*gluNurbsCallback*](glunurbs.md)) 。</span><span class="sxs-lookup"><span data-stu-id="75683-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="75683-129">如果修剪迴圈定義包含多個曲線，則曲線的方向必須是一致的 (也就是說，內部必須位於所有曲線的左邊) 。</span><span class="sxs-lookup"><span data-stu-id="75683-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="75683-130">只要曲線方向的替代正確，您就可以使用嵌套修剪迴圈。</span><span class="sxs-lookup"><span data-stu-id="75683-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="75683-131">修剪曲線無法自我相交，也不能彼此相交 (或錯誤結果) 。</span><span class="sxs-lookup"><span data-stu-id="75683-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="75683-132">如果未針對 NURBS 表面提供修剪資訊，則會繪製整個表面。</span><span class="sxs-lookup"><span data-stu-id="75683-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="75683-133">範例</span><span class="sxs-lookup"><span data-stu-id="75683-133">Examples</span></span>

<span data-ttu-id="75683-134">這個程式碼片段會定義一個修剪迴圈，其中包含一個分段線性曲線和兩個 NURBS 曲線：</span><span class="sxs-lookup"><span data-stu-id="75683-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="75683-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="75683-135">Requirements</span></span>



| <span data-ttu-id="75683-136">需求</span><span class="sxs-lookup"><span data-stu-id="75683-136">Requirement</span></span> | <span data-ttu-id="75683-137">值</span><span class="sxs-lookup"><span data-stu-id="75683-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75683-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75683-138">Minimum supported client</span></span><br/> | <span data-ttu-id="75683-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75683-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75683-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75683-140">Minimum supported server</span></span><br/> | <span data-ttu-id="75683-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75683-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75683-142">標頭</span><span class="sxs-lookup"><span data-stu-id="75683-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="75683-143"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="75683-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="75683-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="75683-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="75683-145"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75683-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="75683-146">DLL</span><span class="sxs-lookup"><span data-stu-id="75683-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75683-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75683-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75683-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75683-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75683-149">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="75683-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="75683-150">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="75683-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="75683-151">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="75683-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="75683-152">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="75683-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="75683-153">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="75683-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="75683-154">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="75683-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





