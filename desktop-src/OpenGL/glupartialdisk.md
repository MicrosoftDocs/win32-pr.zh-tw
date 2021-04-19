---
title: 'gluPartialDisk 函式 (X.glu 隊) '
description: GluPartialDisk 函式會繪製磁片的弧形。
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968138"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="a53b4-104">gluPartialDisk 函式</span><span class="sxs-lookup"><span data-stu-id="a53b4-104">gluPartialDisk function</span></span>

<span data-ttu-id="a53b4-105">**GluPartialDisk** 函式會繪製磁片的弧形。</span><span class="sxs-lookup"><span data-stu-id="a53b4-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="a53b4-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="a53b4-107">參數</span><span class="sxs-lookup"><span data-stu-id="a53b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53b4-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="a53b4-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-109">使用 [**gluNewQuadric**](glunewquadric.md))  (建立的 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="a53b4-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="a53b4-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-111">部分磁片 (的內部半徑可以是零) 。</span><span class="sxs-lookup"><span data-stu-id="a53b4-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="a53b4-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-113">部分磁片的外部半徑。</span><span class="sxs-lookup"><span data-stu-id="a53b4-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-114">*片*</span><span class="sxs-lookup"><span data-stu-id="a53b4-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-115">圍繞 Z 軸的細分數目。</span><span class="sxs-lookup"><span data-stu-id="a53b4-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-116">*迴圈*</span><span class="sxs-lookup"><span data-stu-id="a53b4-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-117">部分磁片已細分之來源的同心圓環形數目。</span><span class="sxs-lookup"><span data-stu-id="a53b4-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-118">*>startangle*</span><span class="sxs-lookup"><span data-stu-id="a53b4-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-119">磁片部分的起始角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="a53b4-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="a53b4-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="a53b4-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="a53b4-121">磁片部分的掃描角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="a53b4-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53b4-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a53b4-122">Return value</span></span>

<span data-ttu-id="a53b4-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a53b4-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a53b4-124">備註</span><span class="sxs-lookup"><span data-stu-id="a53b4-124">Remarks</span></span>

<span data-ttu-id="a53b4-125">**GluPartialDisk** 函式會在 *z* = 0 平面上呈現部分磁片。</span><span class="sxs-lookup"><span data-stu-id="a53b4-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="a53b4-126">部分磁片類似于完整磁片，不同之處在于只會包含從 *>startangle* 到 *>startangle* sweepAngle 的磁片子集，  +   (其中0度沿著正 y 軸，90度是沿著正 X 軸、180度沿著負 y 軸，而270度則沿著負 X 軸) 。</span><span class="sxs-lookup"><span data-stu-id="a53b4-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="a53b4-127">部分磁片的半徑為 *outerRadius* ，且包含半徑為 *innerRadius* 的同心圓迴圈。</span><span class="sxs-lookup"><span data-stu-id="a53b4-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="a53b4-128">如果 *innerRadius* 為零，則不會產生任何洞。</span><span class="sxs-lookup"><span data-stu-id="a53b4-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="a53b4-129">部分磁片會以 Z 軸的形式細分為配量 (例如) 的比薩配量，也會將 Z 軸分割成環形 (*（依配* 量和 *迴圈* 的指定），分別) 。</span><span class="sxs-lookup"><span data-stu-id="a53b4-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="a53b4-130">相對於方向，部分磁片的正面 z 端會被視為外部 (請參閱 [**gluQuadricOrientation**](gluquadricorientation.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a53b4-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="a53b4-131">這表示，如果方向設定為 \_ 外部 x.glu 隊，則為沿著正 Z 軸的任何法線產生點。</span><span class="sxs-lookup"><span data-stu-id="a53b4-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="a53b4-132">如果您已使用 [**gluQuadricTexture**](gluquadrictexture.md)) 開啟紋理 (， **gluPartialDisk** 會以線性方式產生紋理座標，因此 *r*  =  *outerRadius*、 (*r*、0、0) 的值是 (1、0.5) 、 (0、 *r*、0)  (0.5、1) *、 (* r、0、0)  (r、0、0)  (*r*、0、0)  (0.5，0) 。0。5</span><span class="sxs-lookup"><span data-stu-id="a53b4-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="a53b4-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a53b4-133">Requirements</span></span>



| <span data-ttu-id="a53b4-134">需求</span><span class="sxs-lookup"><span data-stu-id="a53b4-134">Requirement</span></span> | <span data-ttu-id="a53b4-135">值</span><span class="sxs-lookup"><span data-stu-id="a53b4-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a53b4-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a53b4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a53b4-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a53b4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a53b4-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a53b4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a53b4-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a53b4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a53b4-140">標頭</span><span class="sxs-lookup"><span data-stu-id="a53b4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53b4-141"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="a53b4-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a53b4-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="a53b4-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a53b4-143"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a53b4-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a53b4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a53b4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a53b4-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a53b4-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53b4-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a53b4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53b4-147">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="a53b4-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="a53b4-148">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="a53b4-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="a53b4-149">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="a53b4-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="a53b4-150">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="a53b4-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="a53b4-151">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="a53b4-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="a53b4-152">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="a53b4-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





