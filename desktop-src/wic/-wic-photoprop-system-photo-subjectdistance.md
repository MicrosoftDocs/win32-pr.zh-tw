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
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="fd400-103">SubjectDistance 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="fd400-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="fd400-104">[SubjectDistance](../properties/props-system-photo-subjectdistance.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="fd400-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fd400-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="fd400-105">PKEY</span></span>

<span data-ttu-id="fd400-106">PKEY \_ 相片 \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="fd400-107">容器</span><span class="sxs-lookup"><span data-stu-id="fd400-107">Containers</span></span>

<span data-ttu-id="fd400-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="fd400-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fd400-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd400-109">Read-Only</span></span>

<span data-ttu-id="fd400-110">Yes</span><span class="sxs-lookup"><span data-stu-id="fd400-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fd400-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="fd400-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fd400-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="fd400-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fd400-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="fd400-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="fd400-114">系統會從 SubjectDistanceNumerator 和 SubjectDistanceDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="fd400-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="fd400-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="fd400-115">It cannot be written directly.</span></span> <span data-ttu-id="fd400-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="fd400-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fd400-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="fd400-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fd400-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-118">Read Paths</span></span>



| <span data-ttu-id="fd400-119">單</span><span class="sxs-lookup"><span data-stu-id="fd400-119">Order</span></span> | <span data-ttu-id="fd400-120">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-120">Path</span></span>                          | <span data-ttu-id="fd400-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fd400-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fd400-122">1</span><span class="sxs-lookup"><span data-stu-id="fd400-122">1</span></span>     | <span data-ttu-id="fd400-123">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="fd400-124">2</span><span class="sxs-lookup"><span data-stu-id="fd400-124">2</span></span>     | <span data-ttu-id="fd400-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="fd400-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-126">Write Paths</span></span>



| <span data-ttu-id="fd400-127">單</span><span class="sxs-lookup"><span data-stu-id="fd400-127">Order</span></span> | <span data-ttu-id="fd400-128">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-128">Path</span></span>                          | <span data-ttu-id="fd400-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fd400-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fd400-130">1</span><span class="sxs-lookup"><span data-stu-id="fd400-130">1</span></span>     | <span data-ttu-id="fd400-131">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="fd400-132">2</span><span class="sxs-lookup"><span data-stu-id="fd400-132">2</span></span>     | <span data-ttu-id="fd400-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fd400-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-134">Remove Paths</span></span>



| <span data-ttu-id="fd400-135">單</span><span class="sxs-lookup"><span data-stu-id="fd400-135">Order</span></span> | <span data-ttu-id="fd400-136">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="fd400-137">1</span><span class="sxs-lookup"><span data-stu-id="fd400-137">1</span></span>     | <span data-ttu-id="fd400-138">/app1/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="fd400-139">2</span><span class="sxs-lookup"><span data-stu-id="fd400-139">2</span></span>     | <span data-ttu-id="fd400-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="fd400-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="fd400-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="fd400-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fd400-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-142">Read Paths</span></span>



| <span data-ttu-id="fd400-143">單</span><span class="sxs-lookup"><span data-stu-id="fd400-143">Order</span></span> | <span data-ttu-id="fd400-144">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-144">Path</span></span>                          | <span data-ttu-id="fd400-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fd400-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fd400-146">1</span><span class="sxs-lookup"><span data-stu-id="fd400-146">1</span></span>     | <span data-ttu-id="fd400-147">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="fd400-148">2</span><span class="sxs-lookup"><span data-stu-id="fd400-148">2</span></span>     | <span data-ttu-id="fd400-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fd400-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-150">Write Paths</span></span>



| <span data-ttu-id="fd400-151">單</span><span class="sxs-lookup"><span data-stu-id="fd400-151">Order</span></span> | <span data-ttu-id="fd400-152">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-152">Path</span></span>                          | <span data-ttu-id="fd400-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fd400-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fd400-154">1</span><span class="sxs-lookup"><span data-stu-id="fd400-154">1</span></span>     | <span data-ttu-id="fd400-155">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="fd400-156">2</span><span class="sxs-lookup"><span data-stu-id="fd400-156">2</span></span>     | <span data-ttu-id="fd400-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fd400-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-158">Remove Paths</span></span>



| <span data-ttu-id="fd400-159">單</span><span class="sxs-lookup"><span data-stu-id="fd400-159">Order</span></span> | <span data-ttu-id="fd400-160">路徑</span><span class="sxs-lookup"><span data-stu-id="fd400-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="fd400-161">1</span><span class="sxs-lookup"><span data-stu-id="fd400-161">1</span></span>     | <span data-ttu-id="fd400-162">/ifd/exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="fd400-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="fd400-163">2</span><span class="sxs-lookup"><span data-stu-id="fd400-163">2</span></span>     | <span data-ttu-id="fd400-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="fd400-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fd400-165">備註</span><span class="sxs-lookup"><span data-stu-id="fd400-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd400-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd400-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd400-167">SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="fd400-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
