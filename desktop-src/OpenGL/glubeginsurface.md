---
title: 'gluBeginSurface 函式 (X.glu 隊) '
description: 'GluBeginSurface 和 gluEndSurface 函式會分隔非統一的有理 B 曲線 (NURBS) 介面定義。 |gluBeginSurface 函式 (X.glu 隊) '
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976428"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="783c3-105">gluBeginSurface 函式</span><span class="sxs-lookup"><span data-stu-id="783c3-105">gluBeginSurface function</span></span>

<span data-ttu-id="783c3-106">**GluBeginSurface** 和 [**gluEndSurface**](gluendsurface.md)函式會分隔非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 介面定義。</span><span class="sxs-lookup"><span data-stu-id="783c3-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="783c3-107">語法</span><span class="sxs-lookup"><span data-stu-id="783c3-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="783c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="783c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783c3-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="783c3-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="783c3-110">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="783c3-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="783c3-111">Return value</span></span>

<span data-ttu-id="783c3-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="783c3-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="783c3-113">備註</span><span class="sxs-lookup"><span data-stu-id="783c3-113">Remarks</span></span>

<span data-ttu-id="783c3-114">**GluBeginSurface** 和 **gluEndSurface** 函式會標記 NURBS 介面定義的開頭和結尾，這些定義是使用對 **gluNurbsSurface** 的呼叫所定義。</span><span class="sxs-lookup"><span data-stu-id="783c3-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="783c3-115">呼叫 **gluBeginSurface** 以標記 NURBS 介面定義的開頭。</span><span class="sxs-lookup"><span data-stu-id="783c3-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="783c3-116">對 **gluNurbsSurface** 進行一或多個呼叫，以定義介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="783c3-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="783c3-117">只有其中一個 **gluNurbsSurface** 呼叫必須具有 GL \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4 的介面類別型。</span><span class="sxs-lookup"><span data-stu-id="783c3-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="783c3-118">若要標記 NURBS 介面定義的結尾，請呼叫 **gluEndSurface**。</span><span class="sxs-lookup"><span data-stu-id="783c3-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="783c3-119">[**GluBeginTrim**](glubegintrim.md)、 [**gluPwlCurve**](glupwlcurve.md)、 [**GLUNURBSCURVE**](glunurbscurve.md)和 [**gluEndTrim**](gluendtrim.md)函數支援 NURBS 表面的修剪。</span><span class="sxs-lookup"><span data-stu-id="783c3-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="783c3-120">使用 OpenGL 評估工具將 NURBS 表面轉譯為一組多邊形。</span><span class="sxs-lookup"><span data-stu-id="783c3-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="783c3-121">使用 [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) 和 [**glPopAttrib**](glpopattrib.md)在轉譯期間保留評估工具狀態。</span><span class="sxs-lookup"><span data-stu-id="783c3-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="783c3-122">範例</span><span class="sxs-lookup"><span data-stu-id="783c3-122">Examples</span></span>

<span data-ttu-id="783c3-123">下列函式會以法線呈現紋理的 NURBS 介面;材質座標和法線也會描述為 NURBS 表面：</span><span class="sxs-lookup"><span data-stu-id="783c3-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="783c3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="783c3-124">Requirements</span></span>



| <span data-ttu-id="783c3-125">需求</span><span class="sxs-lookup"><span data-stu-id="783c3-125">Requirement</span></span> | <span data-ttu-id="783c3-126">值</span><span class="sxs-lookup"><span data-stu-id="783c3-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="783c3-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="783c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="783c3-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="783c3-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="783c3-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="783c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="783c3-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="783c3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="783c3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="783c3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="783c3-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="783c3-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="783c3-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="783c3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="783c3-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="783c3-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="783c3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="783c3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="783c3-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="783c3-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783c3-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="783c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783c3-138">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="783c3-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="783c3-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="783c3-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="783c3-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="783c3-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="783c3-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="783c3-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="783c3-142">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="783c3-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="783c3-143">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="783c3-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





