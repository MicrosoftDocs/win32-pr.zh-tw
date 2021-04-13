---
title: 'gluTessEndContour 函式 (X.glu 隊) '
description: 'GluTessBeginContour 和 gluTessEndContour 函式會分隔分佈描述。 |gluTessEndContour 函式 (X.glu 隊) '
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321992"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="956cb-105">gluTessEndContour 函式</span><span class="sxs-lookup"><span data-stu-id="956cb-105">gluTessEndContour function</span></span>

<span data-ttu-id="956cb-106">[**GluTessBeginContour**](glutessbegincontour.md)和 **gluTessEndContour** 函式會分隔分佈描述。</span><span class="sxs-lookup"><span data-stu-id="956cb-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="956cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="956cb-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="956cb-108">參數</span><span class="sxs-lookup"><span data-stu-id="956cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956cb-109">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="956cb-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="956cb-110">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="956cb-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956cb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="956cb-111">Return value</span></span>

<span data-ttu-id="956cb-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="956cb-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="956cb-113">備註</span><span class="sxs-lookup"><span data-stu-id="956cb-113">Remarks</span></span>

<span data-ttu-id="956cb-114">[**GluTessBeginContour**](glutessbegincontour.md)和 **gluTessEndContour** 函數會分隔多邊形輪廓的定義。</span><span class="sxs-lookup"><span data-stu-id="956cb-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="956cb-115">在每個 **gluTessBeginContour** / **gluTessEndContour** 配對中，可能會有零或多個對 [**gluTessVertex**](glutessvertex.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="956cb-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="956cb-116">頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。</span><span class="sxs-lookup"><span data-stu-id="956cb-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="956cb-117">您只能在 [**gluTessBeginPolygon**](glutessbeginpolygon.md)和 [**GluTessEndPolygon**](glutessendpolygon.md)之間呼叫 **gluTessBeginContour** 。</span><span class="sxs-lookup"><span data-stu-id="956cb-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="956cb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="956cb-118">Requirements</span></span>



| <span data-ttu-id="956cb-119">需求</span><span class="sxs-lookup"><span data-stu-id="956cb-119">Requirement</span></span> | <span data-ttu-id="956cb-120">值</span><span class="sxs-lookup"><span data-stu-id="956cb-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="956cb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="956cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="956cb-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956cb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="956cb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="956cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="956cb-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956cb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="956cb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="956cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="956cb-126"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="956cb-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="956cb-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="956cb-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="956cb-128"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="956cb-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="956cb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="956cb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="956cb-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="956cb-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956cb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="956cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956cb-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="956cb-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="956cb-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="956cb-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="956cb-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="956cb-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="956cb-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="956cb-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="956cb-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="956cb-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="956cb-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="956cb-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="956cb-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="956cb-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





