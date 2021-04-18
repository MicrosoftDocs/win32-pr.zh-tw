---
title: 'gluSphere 函式 (X.glu 隊) '
description: GluSphere 函式會繪製球體。
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere 函式 OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466173"
---
# <a name="glusphere-function"></a><span data-ttu-id="6a668-104">gluSphere 函式</span><span class="sxs-lookup"><span data-stu-id="6a668-104">gluSphere function</span></span>

<span data-ttu-id="6a668-105">**GluSphere** 函式會繪製球體。</span><span class="sxs-lookup"><span data-stu-id="6a668-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a668-106">語法</span><span class="sxs-lookup"><span data-stu-id="6a668-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="6a668-107">參數</span><span class="sxs-lookup"><span data-stu-id="6a668-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a668-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="6a668-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="6a668-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="6a668-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6a668-110">*半徑*</span><span class="sxs-lookup"><span data-stu-id="6a668-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="6a668-111">球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="6a668-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="6a668-112">*片*</span><span class="sxs-lookup"><span data-stu-id="6a668-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="6a668-113">圍繞 Z 軸的線段數 (類似于經度) 。</span><span class="sxs-lookup"><span data-stu-id="6a668-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="6a668-114">*棧*</span><span class="sxs-lookup"><span data-stu-id="6a668-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="6a668-115">沿著 Z 軸的子分割數目 (類似于緯度) 的線條。</span><span class="sxs-lookup"><span data-stu-id="6a668-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a668-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a668-116">Return value</span></span>

<span data-ttu-id="6a668-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6a668-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a668-118">備註</span><span class="sxs-lookup"><span data-stu-id="6a668-118">Remarks</span></span>

<span data-ttu-id="6a668-119">**GluSphere** 函式會繪製以原點為中心之指定半徑的球體。</span><span class="sxs-lookup"><span data-stu-id="6a668-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="6a668-120">球體會以 Z 軸將 Z 軸細分為配量，沿著 Z 軸分割成堆疊 (類似于經度和緯度) 。</span><span class="sxs-lookup"><span data-stu-id="6a668-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="6a668-121">如果方向設定為 [X.GLU 隊 \_ 外部] (**gluQuadricOrientation**) ，則會從球體中央開始的任何法線產生點。</span><span class="sxs-lookup"><span data-stu-id="6a668-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="6a668-122">否則，它們會指向球體的中心。</span><span class="sxs-lookup"><span data-stu-id="6a668-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="6a668-123">如果使用 **gluQuadricTexture**) 來開啟 (的紋理，則會產生材質座標，讓 *t* 範圍從0.0 （z 半徑的 *z* =-*半徑*）到1.0 （ *z*  =  *半徑*） (*t* 在 longitudinal 行之間以線性方式增加) ; 和中的範圍是從0.0 （正 y 軸）到0.25 （正 X 軸）、在負 y 軸的、負 X 軸上的0.75，以及正 y 軸上的1.0。0。5</span><span class="sxs-lookup"><span data-stu-id="6a668-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a668-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a668-124">Requirements</span></span>



| <span data-ttu-id="6a668-125">需求</span><span class="sxs-lookup"><span data-stu-id="6a668-125">Requirement</span></span> | <span data-ttu-id="6a668-126">值</span><span class="sxs-lookup"><span data-stu-id="6a668-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6a668-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a668-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a668-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a668-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6a668-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a668-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a668-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a668-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6a668-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6a668-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a668-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a668-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6a668-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a668-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a668-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a668-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a668-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6a668-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a668-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a668-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a668-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a668-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a668-138">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="6a668-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="6a668-139">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="6a668-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="6a668-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="6a668-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="6a668-141">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="6a668-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="6a668-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="6a668-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="6a668-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="6a668-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





