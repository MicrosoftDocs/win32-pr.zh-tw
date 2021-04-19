---
description: PeopleNames 屬性的相片中繼資料原則。
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: PeopleNames 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985682"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="31bf3-103">PeopleNames 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="31bf3-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="31bf3-104">[PeopleNames](../properties/props-system-photo-peoplenames.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="31bf3-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="31bf3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="31bf3-105">PKEY</span></span>

<span data-ttu-id="31bf3-106">PKEY \_ 相片 \_ PeopleNames</span><span class="sxs-lookup"><span data-stu-id="31bf3-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="31bf3-107">容器</span><span class="sxs-lookup"><span data-stu-id="31bf3-107">Containers</span></span>

<span data-ttu-id="31bf3-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="31bf3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="31bf3-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="31bf3-109">Read-Only</span></span>

<span data-ttu-id="31bf3-110">No</span><span class="sxs-lookup"><span data-stu-id="31bf3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="31bf3-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="31bf3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="31bf3-112">VT \_ 向量 \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="31bf3-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="31bf3-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="31bf3-113">Input Type</span></span>

<span data-ttu-id="31bf3-114">StringMulti</span><span class="sxs-lookup"><span data-stu-id="31bf3-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="31bf3-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="31bf3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="31bf3-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="31bf3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="31bf3-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="31bf3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="31bf3-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-118">Read Paths</span></span>



| <span data-ttu-id="31bf3-119">單</span><span class="sxs-lookup"><span data-stu-id="31bf3-119">Order</span></span> | <span data-ttu-id="31bf3-120">路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-120">Path</span></span>                                                           | <span data-ttu-id="31bf3-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="31bf3-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="31bf3-122">1</span><span class="sxs-lookup"><span data-stu-id="31bf3-122">1</span></span>     | <span data-ttu-id="31bf3-123">/xmp/ <xmpstruct> MP： RegionInfo/ <xmpbag> MPRI：區域</span><span class="sxs-lookup"><span data-stu-id="31bf3-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="31bf3-124">ushort</span><span class="sxs-lookup"><span data-stu-id="31bf3-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="31bf3-125">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-125">Write Paths</span></span>

<span data-ttu-id="31bf3-126">無法使用中繼資料原則來寫入這個屬性。</span><span class="sxs-lookup"><span data-stu-id="31bf3-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="31bf3-127">移除路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-127">Remove Paths</span></span>



| <span data-ttu-id="31bf3-128">單</span><span class="sxs-lookup"><span data-stu-id="31bf3-128">Order</span></span> | <span data-ttu-id="31bf3-129">路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="31bf3-130">1</span><span class="sxs-lookup"><span data-stu-id="31bf3-130">1</span></span>     | <span data-ttu-id="31bf3-131">/xmp/ <xmpstruct> MP： RegionInfo</span><span class="sxs-lookup"><span data-stu-id="31bf3-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="31bf3-132">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="31bf3-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="31bf3-133">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-133">Read Paths</span></span>



| <span data-ttu-id="31bf3-134">單</span><span class="sxs-lookup"><span data-stu-id="31bf3-134">Order</span></span> | <span data-ttu-id="31bf3-135">路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-135">Path</span></span>                                                               | <span data-ttu-id="31bf3-136">磁片格式</span><span class="sxs-lookup"><span data-stu-id="31bf3-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="31bf3-137">1</span><span class="sxs-lookup"><span data-stu-id="31bf3-137">1</span></span>     | <span data-ttu-id="31bf3-138">/ifd/xmp/ <xmpstruct> MP： RegionInfo/ <xmpbag> MPRI：區域</span><span class="sxs-lookup"><span data-stu-id="31bf3-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="31bf3-139">ushort</span><span class="sxs-lookup"><span data-stu-id="31bf3-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="31bf3-140">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-140">Write Paths</span></span>

<span data-ttu-id="31bf3-141">無法使用中繼資料原則來寫入這個屬性。</span><span class="sxs-lookup"><span data-stu-id="31bf3-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="31bf3-142">移除路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-142">Remove Paths</span></span>



| <span data-ttu-id="31bf3-143">單</span><span class="sxs-lookup"><span data-stu-id="31bf3-143">Order</span></span> | <span data-ttu-id="31bf3-144">路徑</span><span class="sxs-lookup"><span data-stu-id="31bf3-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="31bf3-145">1</span><span class="sxs-lookup"><span data-stu-id="31bf3-145">1</span></span>     | <span data-ttu-id="31bf3-146">/ifd/xmp/ <xmpstruct> MP： RegionInfo</span><span class="sxs-lookup"><span data-stu-id="31bf3-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="31bf3-147">備註</span><span class="sxs-lookup"><span data-stu-id="31bf3-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="31bf3-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="31bf3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31bf3-149">ProgramMode</span><span class="sxs-lookup"><span data-stu-id="31bf3-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
