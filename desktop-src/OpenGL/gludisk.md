---
title: 'gluDisk 函式 (X.glu 隊) '
description: GluDisk 函式會繪製磁片。
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025064"
---
# <a name="gludisk-function"></a><span data-ttu-id="129f2-104">gluDisk 函式</span><span class="sxs-lookup"><span data-stu-id="129f2-104">gluDisk function</span></span>

<span data-ttu-id="129f2-105">**GluDisk** 函式會繪製磁片。</span><span class="sxs-lookup"><span data-stu-id="129f2-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="129f2-106">語法</span><span class="sxs-lookup"><span data-stu-id="129f2-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="129f2-107">參數</span><span class="sxs-lookup"><span data-stu-id="129f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129f2-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="129f2-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="129f2-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="129f2-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="129f2-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="129f2-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="129f2-111">磁片 (的內部半徑可能是零) 。</span><span class="sxs-lookup"><span data-stu-id="129f2-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="129f2-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="129f2-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="129f2-113">磁片的外部半徑。</span><span class="sxs-lookup"><span data-stu-id="129f2-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="129f2-114">*片*</span><span class="sxs-lookup"><span data-stu-id="129f2-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="129f2-115">圍繞 Z 軸的細分數目。</span><span class="sxs-lookup"><span data-stu-id="129f2-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="129f2-116">*迴圈*</span><span class="sxs-lookup"><span data-stu-id="129f2-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="129f2-117">磁片正在細分之來源的同心圓環形數目。</span><span class="sxs-lookup"><span data-stu-id="129f2-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129f2-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="129f2-118">Return value</span></span>

<span data-ttu-id="129f2-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="129f2-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="129f2-120">備註</span><span class="sxs-lookup"><span data-stu-id="129f2-120">Remarks</span></span>

<span data-ttu-id="129f2-121">**GluDisk** 函式會在 *z* = 0 平面上呈現磁片。</span><span class="sxs-lookup"><span data-stu-id="129f2-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="129f2-122">磁片的半徑為 *outerRadius*，並包含半徑為 *innerRadius* 的同心圓圓形孔。</span><span class="sxs-lookup"><span data-stu-id="129f2-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="129f2-123">如果 *innerRadius* 為0，則不會產生任何漏洞。</span><span class="sxs-lookup"><span data-stu-id="129f2-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="129f2-124">磁片會以 Z 軸的形式細分為配量 (例如比薩配量) 以及依配量和 *迴圈* 所 *指定的環形* (，分別) 。</span><span class="sxs-lookup"><span data-stu-id="129f2-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="129f2-125">相對於方向，磁片的正 *z* 端會被視為 *外部* (請參閱 [**gluQuadricOrientation**](gluquadricorientation.md)) 。</span><span class="sxs-lookup"><span data-stu-id="129f2-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="129f2-126">這表示，如果方向設定為 \_ 外部 x.glu 隊，則為沿著正 Z 軸的任何法線產生點。</span><span class="sxs-lookup"><span data-stu-id="129f2-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="129f2-127">如果 (使用 [**gluQuadricTexture**](gluquadrictexture.md)) 來開啟紋理座標，則會以線性方式產生紋理座標，使 *r*  =  *outerRadius*、在 (*r*、0、0) 的值是 (1、0.5) ; 在 (0、 *r*、0)  (0.5、1) 、在 (-r *、* 0、0) ， (0、-r *、* 0)  (0.5，0) 。0。5</span><span class="sxs-lookup"><span data-stu-id="129f2-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="129f2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="129f2-128">Requirements</span></span>



| <span data-ttu-id="129f2-129">需求</span><span class="sxs-lookup"><span data-stu-id="129f2-129">Requirement</span></span> | <span data-ttu-id="129f2-130">值</span><span class="sxs-lookup"><span data-stu-id="129f2-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="129f2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="129f2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="129f2-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="129f2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="129f2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="129f2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="129f2-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="129f2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="129f2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="129f2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="129f2-136"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="129f2-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="129f2-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="129f2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="129f2-138"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="129f2-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="129f2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="129f2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="129f2-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="129f2-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="129f2-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="129f2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129f2-142">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="129f2-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="129f2-143">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="129f2-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="129f2-144">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="129f2-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="129f2-145">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="129f2-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="129f2-146">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="129f2-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="129f2-147">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="129f2-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





