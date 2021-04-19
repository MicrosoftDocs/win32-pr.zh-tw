---
title: 'gluTessBeginContour 函式 (X.glu 隊) '
description: 'GluTessBeginContour 和 gluTessEndContour 函式會分隔分佈描述。 |gluTessBeginContour 函式 (X.glu 隊) '
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000548"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="72d55-105">gluTessBeginContour 函式</span><span class="sxs-lookup"><span data-stu-id="72d55-105">gluTessBeginContour function</span></span>

<span data-ttu-id="72d55-106">**GluTessBeginContour** 和 [**gluTessEndContour**](glutessendcontour.md)函式會分隔分佈描述。</span><span class="sxs-lookup"><span data-stu-id="72d55-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d55-107">語法</span><span class="sxs-lookup"><span data-stu-id="72d55-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="72d55-108">參數</span><span class="sxs-lookup"><span data-stu-id="72d55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d55-109">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="72d55-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="72d55-110">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="72d55-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d55-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="72d55-111">Return value</span></span>

<span data-ttu-id="72d55-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="72d55-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d55-113">備註</span><span class="sxs-lookup"><span data-stu-id="72d55-113">Remarks</span></span>

<span data-ttu-id="72d55-114">**GluTessBeginContour** 和 [**gluTessEndPolygon**](glutessendpolygon.md)函數會分隔多邊形輪廓的定義。</span><span class="sxs-lookup"><span data-stu-id="72d55-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="72d55-115">在每個 **gluTessBeginContour** / **gluTessEndPolygon** 配對中，可能會有零或多個對 [**gluTessVertex**](glutessvertex.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="72d55-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="72d55-116">頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。</span><span class="sxs-lookup"><span data-stu-id="72d55-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="72d55-117">您只能在 [**gluTessBeginPolygon**](glutessbeginpolygon.md)和 **GluTessEndPolygon** 之間呼叫 **gluTessBeginContour** 。</span><span class="sxs-lookup"><span data-stu-id="72d55-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d55-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="72d55-118">Requirements</span></span>



| <span data-ttu-id="72d55-119">需求</span><span class="sxs-lookup"><span data-stu-id="72d55-119">Requirement</span></span> | <span data-ttu-id="72d55-120">值</span><span class="sxs-lookup"><span data-stu-id="72d55-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72d55-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72d55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="72d55-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d55-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="72d55-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72d55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="72d55-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d55-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="72d55-125">標頭</span><span class="sxs-lookup"><span data-stu-id="72d55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d55-126"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="72d55-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="72d55-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="72d55-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="72d55-128"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="72d55-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="72d55-129">DLL</span><span class="sxs-lookup"><span data-stu-id="72d55-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d55-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d55-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d55-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72d55-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d55-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="72d55-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="72d55-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="72d55-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="72d55-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="72d55-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="72d55-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="72d55-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="72d55-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="72d55-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="72d55-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="72d55-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="72d55-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="72d55-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





