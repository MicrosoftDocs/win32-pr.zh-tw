---
title: 'gluTessBeginPolygon 函式 (X.glu 隊) '
description: 'GluTessBeginPolygon 和 gluTessEndPolygon 函數會分隔多邊形描述。 |gluTessBeginPolygon 函式 (X.glu 隊) '
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998572"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="fb108-105">gluTessBeginPolygon 函式</span><span class="sxs-lookup"><span data-stu-id="fb108-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="fb108-106">**GluTessBeginPolygon** 和 [**gluTessEndPolygon**](glutessendpolygon.md)函數會分隔多邊形描述。</span><span class="sxs-lookup"><span data-stu-id="fb108-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb108-107">語法</span><span class="sxs-lookup"><span data-stu-id="fb108-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="fb108-108">參數</span><span class="sxs-lookup"><span data-stu-id="fb108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb108-109">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="fb108-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="fb108-110">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="fb108-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fb108-111">*多邊形 \_ 資料*</span><span class="sxs-lookup"><span data-stu-id="fb108-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="fb108-112">程式設計人員定義多邊形資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fb108-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb108-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb108-113">Return value</span></span>

<span data-ttu-id="fb108-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fb108-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb108-115">備註</span><span class="sxs-lookup"><span data-stu-id="fb108-115">Remarks</span></span>

<span data-ttu-id="fb108-116">**GluTessBeginPolygon** 和 [**gluTessEndPolygon**](glutessendpolygon.md)函數會分隔 nonconvex 多邊形的定義。</span><span class="sxs-lookup"><span data-stu-id="fb108-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="fb108-117">在每個 **gluTessBeginPolygon**  /  **gluTessEndPolygon** 配對中，包含一或多個對 [**gluTessBeginContour**](glutessbegincontour.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb108-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="fb108-118">在每個分佈中，有零或多個 [**gluTessVertex**](glutessvertex.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb108-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="fb108-119">頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。</span><span class="sxs-lookup"><span data-stu-id="fb108-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="fb108-120">*多邊形 \_ 資料* 參數是程式設計人員定義資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fb108-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="fb108-121">如果指定了適當的回呼 (請參閱 [*gluTessCallback*](glutess.md)) ，此指標會傳回給回呼函式或函式，讓它成為儲存每個多邊形資訊的便利方式。</span><span class="sxs-lookup"><span data-stu-id="fb108-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="fb108-122">當您呼叫 [**gluTessEndPolygon**](glutessendpolygon.md)時，多邊形會是鑲嵌，而產生的三角形會透過回呼來描述。</span><span class="sxs-lookup"><span data-stu-id="fb108-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="fb108-123">如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。</span><span class="sxs-lookup"><span data-stu-id="fb108-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb108-124">範例</span><span class="sxs-lookup"><span data-stu-id="fb108-124">Examples</span></span>

<span data-ttu-id="fb108-125">以下說明具有三角形孔的四邊形：</span><span class="sxs-lookup"><span data-stu-id="fb108-125">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="fb108-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb108-126">Requirements</span></span>



| <span data-ttu-id="fb108-127">需求</span><span class="sxs-lookup"><span data-stu-id="fb108-127">Requirement</span></span> | <span data-ttu-id="fb108-128">值</span><span class="sxs-lookup"><span data-stu-id="fb108-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb108-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb108-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb108-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb108-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fb108-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb108-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb108-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb108-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fb108-133">標頭</span><span class="sxs-lookup"><span data-stu-id="fb108-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb108-134"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb108-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fb108-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb108-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb108-136"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb108-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb108-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fb108-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb108-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb108-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb108-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb108-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb108-140">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="fb108-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="fb108-141">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="fb108-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="fb108-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="fb108-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="fb108-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="fb108-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="fb108-144">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="fb108-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="fb108-145">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="fb108-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="fb108-146">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="fb108-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





