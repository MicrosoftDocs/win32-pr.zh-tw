---
title: 'gluBeginCurve 函式 (X.glu 隊) '
description: 'GluBeginCurve 和 gluEndCurve 函式會分隔非統一的有理數 B 曲線 (NURBS) 曲線定義。 |gluBeginCurve 函式 (X.glu 隊) '
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- gluBeginCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988571"
---
# <a name="glubegincurve-function"></a><span data-ttu-id="6bb42-105">gluBeginCurve 函式</span><span class="sxs-lookup"><span data-stu-id="6bb42-105">gluBeginCurve function</span></span>

<span data-ttu-id="6bb42-106">**GluBeginCurve** 和 [**gluEndCurve**](gluendcurve.md)函式會分隔非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 曲線定義。</span><span class="sxs-lookup"><span data-stu-id="6bb42-106">The **gluBeginCurve** and [**gluEndCurve**](gluendcurve.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb42-107">語法</span><span class="sxs-lookup"><span data-stu-id="6bb42-107">Syntax</span></span>


```C++
void WINAPI gluBeginCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="6bb42-108">參數</span><span class="sxs-lookup"><span data-stu-id="6bb42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb42-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="6bb42-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb42-110">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="6bb42-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb42-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bb42-111">Return value</span></span>

<span data-ttu-id="6bb42-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6bb42-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb42-113">備註</span><span class="sxs-lookup"><span data-stu-id="6bb42-113">Remarks</span></span>

<span data-ttu-id="6bb42-114">使用 **gluBeginCurve** 來標記 NURBS 曲線定義的開頭。</span><span class="sxs-lookup"><span data-stu-id="6bb42-114">Use **gluBeginCurve** to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="6bb42-115">呼叫 **gluBeginCurve** 之後，請對 [**gluNurbsCurve**](glunurbscurve.md) 進行一或多個呼叫，以定義曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb42-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="6bb42-116">只有其中一個 **gluNurbsCurve** 呼叫必須有 GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4 的曲線類型。</span><span class="sxs-lookup"><span data-stu-id="6bb42-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="6bb42-117">若要標記 NURBS 曲線定義的結尾，請呼叫 [**gluEndCurve**](gluendcurve.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb42-117">To mark the end of the NURBS curve definition, call [**gluEndCurve**](gluendcurve.md).</span></span>

<span data-ttu-id="6bb42-118">OpenGL 評估工具是用來將 NURBS 曲線轉譯成一連串的線段。</span><span class="sxs-lookup"><span data-stu-id="6bb42-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="6bb42-119">使用 [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) 和 [**glPopAttrib**](glpopattrib.md)轉譯時，會保留評估工具狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb42-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="6bb42-120">如需這些呼叫保留之狀態的確切資訊，請參閱 **glPushAttrib**。</span><span class="sxs-lookup"><span data-stu-id="6bb42-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="6bb42-121">範例</span><span class="sxs-lookup"><span data-stu-id="6bb42-121">Examples</span></span>

<span data-ttu-id="6bb42-122">下列函式會以法線呈現有紋理的 NURBS 曲線;紋理座標和法線也會指定為 NURBS 曲線：</span><span class="sxs-lookup"><span data-stu-id="6bb42-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="6bb42-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb42-123">Requirements</span></span>



| <span data-ttu-id="6bb42-124">需求</span><span class="sxs-lookup"><span data-stu-id="6bb42-124">Requirement</span></span> | <span data-ttu-id="6bb42-125">值</span><span class="sxs-lookup"><span data-stu-id="6bb42-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb42-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb42-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb42-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb42-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6bb42-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb42-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb42-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb42-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6bb42-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6bb42-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb42-131"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb42-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6bb42-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="6bb42-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bb42-133"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bb42-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6bb42-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb42-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb42-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb42-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb42-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb42-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb42-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="6bb42-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="6bb42-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="6bb42-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="6bb42-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="6bb42-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="6bb42-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="6bb42-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="6bb42-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="6bb42-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





