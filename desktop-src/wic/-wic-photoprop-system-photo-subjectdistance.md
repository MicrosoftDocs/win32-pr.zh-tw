---
description: SubjectDistance 屬性的相片中繼資料原則。
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: SubjectDistance 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851212"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="f710d-103">SubjectDistance 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f710d-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="f710d-104">[SubjectDistance](../properties/props-system-photo-subjectdistance.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f710d-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f710d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f710d-105">PKEY</span></span>

<span data-ttu-id="f710d-106">PKEY \_ 相片 \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="f710d-107">容器</span><span class="sxs-lookup"><span data-stu-id="f710d-107">Containers</span></span>

<span data-ttu-id="f710d-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f710d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f710d-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f710d-109">Read-Only</span></span>

<span data-ttu-id="f710d-110">Yes</span><span class="sxs-lookup"><span data-stu-id="f710d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f710d-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f710d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f710d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="f710d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f710d-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f710d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="f710d-114">系統會從 SubjectDistanceNumerator 和 SubjectDistanceDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="f710d-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="f710d-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="f710d-115">It cannot be written directly.</span></span> <span data-ttu-id="f710d-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="f710d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f710d-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="f710d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f710d-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-118">Read Paths</span></span>



| <span data-ttu-id="f710d-119">單</span><span class="sxs-lookup"><span data-stu-id="f710d-119">Order</span></span> | <span data-ttu-id="f710d-120">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-120">Path</span></span>                          | <span data-ttu-id="f710d-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f710d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f710d-122">1</span><span class="sxs-lookup"><span data-stu-id="f710d-122">1</span></span>     | <span data-ttu-id="f710d-123">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="f710d-124">2</span><span class="sxs-lookup"><span data-stu-id="f710d-124">2</span></span>     | <span data-ttu-id="f710d-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="f710d-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-126">Write Paths</span></span>



| <span data-ttu-id="f710d-127">單</span><span class="sxs-lookup"><span data-stu-id="f710d-127">Order</span></span> | <span data-ttu-id="f710d-128">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-128">Path</span></span>                          | <span data-ttu-id="f710d-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f710d-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f710d-130">1</span><span class="sxs-lookup"><span data-stu-id="f710d-130">1</span></span>     | <span data-ttu-id="f710d-131">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="f710d-132">2</span><span class="sxs-lookup"><span data-stu-id="f710d-132">2</span></span>     | <span data-ttu-id="f710d-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f710d-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-134">Remove Paths</span></span>



| <span data-ttu-id="f710d-135">單</span><span class="sxs-lookup"><span data-stu-id="f710d-135">Order</span></span> | <span data-ttu-id="f710d-136">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f710d-137">1</span><span class="sxs-lookup"><span data-stu-id="f710d-137">1</span></span>     | <span data-ttu-id="f710d-138">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="f710d-139">2</span><span class="sxs-lookup"><span data-stu-id="f710d-139">2</span></span>     | <span data-ttu-id="f710d-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="f710d-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="f710d-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="f710d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f710d-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-142">Read Paths</span></span>



| <span data-ttu-id="f710d-143">單</span><span class="sxs-lookup"><span data-stu-id="f710d-143">Order</span></span> | <span data-ttu-id="f710d-144">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-144">Path</span></span>                          | <span data-ttu-id="f710d-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f710d-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f710d-146">1</span><span class="sxs-lookup"><span data-stu-id="f710d-146">1</span></span>     | <span data-ttu-id="f710d-147">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="f710d-148">2</span><span class="sxs-lookup"><span data-stu-id="f710d-148">2</span></span>     | <span data-ttu-id="f710d-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="f710d-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-150">Write Paths</span></span>



| <span data-ttu-id="f710d-151">單</span><span class="sxs-lookup"><span data-stu-id="f710d-151">Order</span></span> | <span data-ttu-id="f710d-152">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-152">Path</span></span>                          | <span data-ttu-id="f710d-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f710d-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f710d-154">1</span><span class="sxs-lookup"><span data-stu-id="f710d-154">1</span></span>     | <span data-ttu-id="f710d-155">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="f710d-156">2</span><span class="sxs-lookup"><span data-stu-id="f710d-156">2</span></span>     | <span data-ttu-id="f710d-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f710d-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-158">Remove Paths</span></span>



| <span data-ttu-id="f710d-159">單</span><span class="sxs-lookup"><span data-stu-id="f710d-159">Order</span></span> | <span data-ttu-id="f710d-160">路徑</span><span class="sxs-lookup"><span data-stu-id="f710d-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f710d-161">1</span><span class="sxs-lookup"><span data-stu-id="f710d-161">1</span></span>     | <span data-ttu-id="f710d-162">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="f710d-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="f710d-163">2</span><span class="sxs-lookup"><span data-stu-id="f710d-163">2</span></span>     | <span data-ttu-id="f710d-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="f710d-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f710d-165">備註</span><span class="sxs-lookup"><span data-stu-id="f710d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f710d-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="f710d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f710d-167">SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="f710d-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
