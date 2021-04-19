---
title: 'gluTessEndPolygon 函式 (X.glu 隊) '
description: 'GluTessBeginPolygon 和 gluTessEndPolygon 函數會分隔多邊形描述。 |gluTessEndPolygon 函式 (X.glu 隊) '
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- gluTessEndPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989152"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="75d70-105">gluTessEndPolygon 函式</span><span class="sxs-lookup"><span data-stu-id="75d70-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="75d70-106">[**GluTessBeginPolygon**](glutessbeginpolygon.md)和 **gluTessEndPolygon** 函數會分隔多邊形描述。</span><span class="sxs-lookup"><span data-stu-id="75d70-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d70-107">語法</span><span class="sxs-lookup"><span data-stu-id="75d70-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="75d70-108">參數</span><span class="sxs-lookup"><span data-stu-id="75d70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d70-109">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="75d70-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="75d70-110">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="75d70-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="75d70-111">Return value</span></span>

<span data-ttu-id="75d70-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="75d70-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d70-113">備註</span><span class="sxs-lookup"><span data-stu-id="75d70-113">Remarks</span></span>

<span data-ttu-id="75d70-114">[**GluTessBeginPolygon**](glutessbeginpolygon.md)和 **gluTessEndPolygon** 函數會分隔 nonconvex 多邊形的定義。</span><span class="sxs-lookup"><span data-stu-id="75d70-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="75d70-115">在每個 **gluTessBeginPolygon**  /  **gluTessEndPolygon** 配對中，包含一或多個對 [**gluTessBeginContour**](glutessbegincontour.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="75d70-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="75d70-116">在每個分佈中，有零或多個 [**gluTessVertex**](glutessvertex.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="75d70-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="75d70-117">頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。</span><span class="sxs-lookup"><span data-stu-id="75d70-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="75d70-118">*多邊形 \_ 資料* 參數是程式設計人員定義資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="75d70-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="75d70-119">如果指定了適當的回呼 (請參閱 [*gluTessCallback*](glutess.md)) ，此指標會傳回給回呼函式或函式，讓它成為儲存每個多邊形資訊的便利方式。</span><span class="sxs-lookup"><span data-stu-id="75d70-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="75d70-120">當您呼叫 **gluTessEndPolygon** 時，多邊形會是鑲嵌，而產生的三角形會透過回呼來描述。</span><span class="sxs-lookup"><span data-stu-id="75d70-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="75d70-121">如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。</span><span class="sxs-lookup"><span data-stu-id="75d70-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="75d70-122">範例</span><span class="sxs-lookup"><span data-stu-id="75d70-122">Examples</span></span>

<span data-ttu-id="75d70-123">以下說明具有三角形孔的四邊形：</span><span class="sxs-lookup"><span data-stu-id="75d70-123">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="75d70-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="75d70-124">Requirements</span></span>



| <span data-ttu-id="75d70-125">需求</span><span class="sxs-lookup"><span data-stu-id="75d70-125">Requirement</span></span> | <span data-ttu-id="75d70-126">值</span><span class="sxs-lookup"><span data-stu-id="75d70-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75d70-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75d70-127">Minimum supported client</span></span><br/> | <span data-ttu-id="75d70-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75d70-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75d70-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75d70-129">Minimum supported server</span></span><br/> | <span data-ttu-id="75d70-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75d70-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75d70-131">標頭</span><span class="sxs-lookup"><span data-stu-id="75d70-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d70-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="75d70-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="75d70-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="75d70-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="75d70-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75d70-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="75d70-135">DLL</span><span class="sxs-lookup"><span data-stu-id="75d70-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d70-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d70-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d70-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75d70-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d70-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="75d70-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="75d70-139">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="75d70-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="75d70-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="75d70-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="75d70-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="75d70-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="75d70-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="75d70-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="75d70-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="75d70-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="75d70-144">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="75d70-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





