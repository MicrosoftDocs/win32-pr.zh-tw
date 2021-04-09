---
title: 'gluTessNormal 函式 (X.glu 隊) '
description: GluTessNormal 函數會指定多邊形的一般。
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934983"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="4ade0-104">gluTessNormal 函式</span><span class="sxs-lookup"><span data-stu-id="4ade0-104">gluTessNormal function</span></span>

<span data-ttu-id="4ade0-105">**GluTessNormal** 函數會指定多邊形的一般。</span><span class="sxs-lookup"><span data-stu-id="4ade0-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ade0-106">語法</span><span class="sxs-lookup"><span data-stu-id="4ade0-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="4ade0-107">參數</span><span class="sxs-lookup"><span data-stu-id="4ade0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ade0-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="4ade0-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="4ade0-109">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="4ade0-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4ade0-110">*x*</span><span class="sxs-lookup"><span data-stu-id="4ade0-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="4ade0-111">一般的 x 座標元件。</span><span class="sxs-lookup"><span data-stu-id="4ade0-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="4ade0-112">*y*</span><span class="sxs-lookup"><span data-stu-id="4ade0-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="4ade0-113">一般的 y 座標元件。</span><span class="sxs-lookup"><span data-stu-id="4ade0-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="4ade0-114">*Z*</span><span class="sxs-lookup"><span data-stu-id="4ade0-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="4ade0-115">一般的 z 座標元件。</span><span class="sxs-lookup"><span data-stu-id="4ade0-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ade0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ade0-116">Return value</span></span>

<span data-ttu-id="4ade0-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ade0-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ade0-118">備註</span><span class="sxs-lookup"><span data-stu-id="4ade0-118">Remarks</span></span>

<span data-ttu-id="4ade0-119">**GluTessNormal** 函式描述您所定義多邊形的一般。</span><span class="sxs-lookup"><span data-stu-id="4ade0-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="4ade0-120">所有輸入資料都會投射在鑲嵌式之前垂直的平面，而且所有輸出三角形都是以逆時針方向進行導向。</span><span class="sxs-lookup"><span data-stu-id="4ade0-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="4ade0-121"> (若要取得順時針方向，請將提供的一般) 的正負號反轉。</span><span class="sxs-lookup"><span data-stu-id="4ade0-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="4ade0-122">例如，如果您知道所有多邊形都位於 x-y 平面中，請在轉譯任何多邊形之前，先呼叫 **gluTessNormal** (tess，0.0，0.0，1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4ade0-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="4ade0-123">如果提供的一般 (0.0、0.0、0.0)  (預設值) ，則會以下列方式決定正常：</span><span class="sxs-lookup"><span data-stu-id="4ade0-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="4ade0-124">標準的方向（最多可到其正負號）是藉由將平面調整到頂點的方式找到，而不考慮頂點的連接方式。</span><span class="sxs-lookup"><span data-stu-id="4ade0-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="4ade0-125">輸入資料應該大約位於平面中;否則，垂直投影的三個座標軸之一可以大幅變更幾何。</span><span class="sxs-lookup"><span data-stu-id="4ade0-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="4ade0-126">選擇 [一般] 的正負號，如此一來，所有輸入等高線的已簽署區域總和都是非負的 (其中的逆時針輪廓具有正區域) 。</span><span class="sxs-lookup"><span data-stu-id="4ade0-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="4ade0-127">提供的一般保存，直到 **gluTessNormal** 的另一個呼叫變更為止。</span><span class="sxs-lookup"><span data-stu-id="4ade0-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ade0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ade0-128">Requirements</span></span>



| <span data-ttu-id="4ade0-129">需求</span><span class="sxs-lookup"><span data-stu-id="4ade0-129">Requirement</span></span> | <span data-ttu-id="4ade0-130">值</span><span class="sxs-lookup"><span data-stu-id="4ade0-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ade0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ade0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ade0-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ade0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4ade0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ade0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ade0-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ade0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4ade0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4ade0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ade0-136"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ade0-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4ade0-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ade0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ade0-138"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ade0-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4ade0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4ade0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ade0-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ade0-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ade0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ade0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ade0-142">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="4ade0-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="4ade0-143">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="4ade0-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="4ade0-144">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="4ade0-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





