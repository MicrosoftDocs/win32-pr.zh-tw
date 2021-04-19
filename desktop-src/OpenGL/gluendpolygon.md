---
title: 'gluEndPolygon 函式 (X.glu 隊) '
description: 'GluBeginPolygon 和 gluEndPolygon 函數會分隔多邊形描述。 |gluEndPolygon 函式 (X.glu 隊) '
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- gluEndPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993819"
---
# <a name="gluendpolygon-function"></a><span data-ttu-id="f833c-105">gluEndPolygon 函式</span><span class="sxs-lookup"><span data-stu-id="f833c-105">gluEndPolygon function</span></span>

<span data-ttu-id="f833c-106">\[**GluEndPolygon** 函式已過時，而且只為了回溯相容性而提供。</span><span class="sxs-lookup"><span data-stu-id="f833c-106">\[The **gluEndPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="f833c-107">**GluEndPolygon** 函式會對應到 **gluTessEndPolygon** ，後面接著 **gluTessEndContour**。\]</span><span class="sxs-lookup"><span data-stu-id="f833c-107">The **gluEndPolygon** function is mapped to **gluTessEndPolygon** followed by **gluTessEndContour**.\]</span></span>

<span data-ttu-id="f833c-108">[**GluBeginPolygon**](glubeginpolygon.md)和 **gluEndPolygon** 函數會分隔多邊形描述。</span><span class="sxs-lookup"><span data-stu-id="f833c-108">The [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f833c-109">語法</span><span class="sxs-lookup"><span data-stu-id="f833c-109">Syntax</span></span>


```C++
void gluEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="f833c-110">參數</span><span class="sxs-lookup"><span data-stu-id="f833c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f833c-111">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="f833c-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f833c-112">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="f833c-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f833c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f833c-113">Return value</span></span>

<span data-ttu-id="f833c-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f833c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f833c-115">備註</span><span class="sxs-lookup"><span data-stu-id="f833c-115">Remarks</span></span>

<span data-ttu-id="f833c-116">使用 [**gluBeginPolygon**](glubeginpolygon.md) 和 **gluEndPolygon** 來分隔 nonconvex 多邊形的定義。</span><span class="sxs-lookup"><span data-stu-id="f833c-116">Use [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="f833c-117">呼叫 **gluBeginPolygon**。</span><span class="sxs-lookup"><span data-stu-id="f833c-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="f833c-118">藉由呼叫每個頂點的 [**gluTessVertex**](glutessvertex.md) 和 [**gluNextContour**](glunextcontour.md) 來開始每個新的分佈，以定義多邊形的輪廓。</span><span class="sxs-lookup"><span data-stu-id="f833c-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="f833c-119">呼叫 **gluEndPolygon** 以發出定義的結尾。</span><span class="sxs-lookup"><span data-stu-id="f833c-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="f833c-120">一旦呼叫 **gluEndPolygon** ，就會鑲嵌多邊形，並透過回呼來描述所產生的三角形。</span><span class="sxs-lookup"><span data-stu-id="f833c-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="f833c-121">如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。</span><span class="sxs-lookup"><span data-stu-id="f833c-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f833c-122">範例</span><span class="sxs-lookup"><span data-stu-id="f833c-122">Examples</span></span>

<span data-ttu-id="f833c-123">下列範例說明具有三角形孔的四邊形：</span><span class="sxs-lookup"><span data-stu-id="f833c-123">The following example describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="f833c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f833c-124">Requirements</span></span>



| <span data-ttu-id="f833c-125">需求</span><span class="sxs-lookup"><span data-stu-id="f833c-125">Requirement</span></span> | <span data-ttu-id="f833c-126">值</span><span class="sxs-lookup"><span data-stu-id="f833c-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f833c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f833c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f833c-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f833c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f833c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f833c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f833c-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f833c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f833c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f833c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f833c-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="f833c-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f833c-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="f833c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f833c-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f833c-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f833c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f833c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f833c-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f833c-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f833c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f833c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f833c-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f833c-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f833c-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="f833c-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="f833c-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="f833c-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="f833c-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f833c-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f833c-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f833c-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="f833c-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f833c-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





