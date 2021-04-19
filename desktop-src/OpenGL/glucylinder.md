---
title: 'gluCylinder 函式 (X.glu 隊) '
description: GluCylinder 函式會繪製圓柱。
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder 函式 OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969597"
---
# <a name="glucylinder-function"></a><span data-ttu-id="0c4eb-104">gluCylinder 函式</span><span class="sxs-lookup"><span data-stu-id="0c4eb-104">gluCylinder function</span></span>

<span data-ttu-id="0c4eb-105">**GluCylinder** 函式會繪製圓柱。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4eb-106">語法</span><span class="sxs-lookup"><span data-stu-id="0c4eb-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="0c4eb-107">參數</span><span class="sxs-lookup"><span data-stu-id="0c4eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4eb-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="0c4eb-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0c4eb-110">*baseRadius*</span><span class="sxs-lookup"><span data-stu-id="0c4eb-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-111">位於 *z* = 0 之圓柱的半徑。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="0c4eb-112">*topRadius*</span><span class="sxs-lookup"><span data-stu-id="0c4eb-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-113">以 *z* 高度為圓柱的半徑半徑  =  \*\*。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="0c4eb-114">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="0c4eb-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-115">圓柱的高度。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="0c4eb-116">*片*</span><span class="sxs-lookup"><span data-stu-id="0c4eb-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-117">圍繞 Z 軸的細分數目。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0c4eb-118">*棧*</span><span class="sxs-lookup"><span data-stu-id="0c4eb-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4eb-119">沿著 Z 軸的子分割數目。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4eb-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c4eb-120">Return value</span></span>

<span data-ttu-id="0c4eb-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4eb-122">備註</span><span class="sxs-lookup"><span data-stu-id="0c4eb-122">Remarks</span></span>

<span data-ttu-id="0c4eb-123">**GluCylinder** 函式會繪製沿著 Z 軸方向的圓柱。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="0c4eb-124">圓柱的基底位於 *z* = 0，而頂端是 *z*  =  *高度*。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="0c4eb-125">如同球體，圓柱會以 Z 軸的形式細分為配量，並沿著 Z 軸細分為堆疊。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="0c4eb-126">請注意，如果 *topRadius* 設為零，則此常式會產生一個錐形。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="0c4eb-127">如果方向設定為 \_ 使用 [**gluQuadricOrientation**](gluquadricorientation.md))  (外部 x.glu 隊，則任何產生的法線點都不會出現在 Z 軸上。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="0c4eb-128">否則，它們會指向 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="0c4eb-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="0c4eb-129">如果使用 [**gluQuadricTexture**](gluquadrictexture.md)) 開啟 (的紋理：系統會產生紋理座標，讓 *t* 範圍從0.0 （以 *z 為單位*）到1.0 （以 *z*  =  *高度* 為單位），以及從位於正 y 軸的0.0 到位於正 y 軸的0.25、從正 y 軸到、從正 y 軸到0.5、在負 y 軸的0.75，以及從正 y 軸回到1.0。 </span><span class="sxs-lookup"><span data-stu-id="0c4eb-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4eb-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c4eb-130">Requirements</span></span>



| <span data-ttu-id="0c4eb-131">需求</span><span class="sxs-lookup"><span data-stu-id="0c4eb-131">Requirement</span></span> | <span data-ttu-id="0c4eb-132">值</span><span class="sxs-lookup"><span data-stu-id="0c4eb-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4eb-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c4eb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4eb-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c4eb-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0c4eb-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c4eb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4eb-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c4eb-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0c4eb-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0c4eb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c4eb-138"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c4eb-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0c4eb-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c4eb-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c4eb-140"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c4eb-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c4eb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0c4eb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c4eb-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c4eb-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4eb-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c4eb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4eb-144">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="0c4eb-145">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="0c4eb-146">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="0c4eb-147">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="0c4eb-148">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="0c4eb-149">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="0c4eb-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





