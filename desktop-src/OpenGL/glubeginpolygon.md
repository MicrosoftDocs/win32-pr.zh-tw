---
title: 'gluBeginPolygon 函式 (X.glu 隊) '
description: 'GluBeginPolygon 和 gluEndPolygon 函數會分隔多邊形描述。 |gluBeginPolygon 函式 (X.glu 隊) '
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- gluBeginPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974797"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="c4288-105">gluBeginPolygon 函式</span><span class="sxs-lookup"><span data-stu-id="c4288-105">gluBeginPolygon function</span></span>

<span data-ttu-id="c4288-106">\[**GluBeginPolygon** 函式已過時，而且只為了回溯相容性而提供。</span><span class="sxs-lookup"><span data-stu-id="c4288-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="c4288-107">**GluBeginPolygon** 函式會對應到 [**gluTessBeginPolygon**](glutessbeginpolygon.md) ，後面接著 [**gluTessBeginContour**](glutessbegincontour.md)。\]</span><span class="sxs-lookup"><span data-stu-id="c4288-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="c4288-108">**GluBeginPolygon** 和 [**gluEndPolygon**](gluendpolygon.md)函數會分隔多邊形描述。</span><span class="sxs-lookup"><span data-stu-id="c4288-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4288-109">語法</span><span class="sxs-lookup"><span data-stu-id="c4288-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="c4288-110">參數</span><span class="sxs-lookup"><span data-stu-id="c4288-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4288-111">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="c4288-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="c4288-112">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="c4288-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4288-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4288-113">Return value</span></span>

<span data-ttu-id="c4288-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c4288-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4288-115">備註</span><span class="sxs-lookup"><span data-stu-id="c4288-115">Remarks</span></span>

<span data-ttu-id="c4288-116">使用 **gluBeginPolygon** 和 **gluEndPolygon** 來分隔 nonconvex 多邊形的定義。</span><span class="sxs-lookup"><span data-stu-id="c4288-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="c4288-117">呼叫 **gluBeginPolygon**。</span><span class="sxs-lookup"><span data-stu-id="c4288-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="c4288-118">藉由呼叫每個頂點的 [**gluTessVertex**](glutessvertex.md) 和 [**gluNextContour**](glunextcontour.md) 來開始每個新的分佈，以定義多邊形的輪廓。</span><span class="sxs-lookup"><span data-stu-id="c4288-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="c4288-119">呼叫 **gluEndPolygon** 以發出定義的結尾。</span><span class="sxs-lookup"><span data-stu-id="c4288-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="c4288-120">一旦呼叫 **gluEndPolygon** ，就會鑲嵌多邊形，並透過回呼來描述所產生的三角形。</span><span class="sxs-lookup"><span data-stu-id="c4288-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="c4288-121">如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。</span><span class="sxs-lookup"><span data-stu-id="c4288-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c4288-122">範例</span><span class="sxs-lookup"><span data-stu-id="c4288-122">Examples</span></span>

<span data-ttu-id="c4288-123">下列範例說明具有三角形孔的四邊形：</span><span class="sxs-lookup"><span data-stu-id="c4288-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="c4288-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4288-124">Requirements</span></span>



| <span data-ttu-id="c4288-125">需求</span><span class="sxs-lookup"><span data-stu-id="c4288-125">Requirement</span></span> | <span data-ttu-id="c4288-126">值</span><span class="sxs-lookup"><span data-stu-id="c4288-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4288-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4288-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c4288-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4288-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c4288-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4288-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c4288-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4288-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c4288-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c4288-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4288-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4288-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c4288-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4288-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4288-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4288-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c4288-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c4288-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4288-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4288-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4288-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4288-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4288-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="c4288-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="c4288-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="c4288-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="c4288-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="c4288-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="c4288-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="c4288-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="c4288-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="c4288-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="c4288-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="c4288-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





