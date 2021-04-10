---
description: EXIFVersion 屬性的相片中繼資料原則。
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: EXIFVersion 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194572"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="4a7f9-103">EXIFVersion 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="4a7f9-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="4a7f9-104">[EXIFVersion](../properties/props-system-photo-exifversion.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="4a7f9-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4a7f9-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4a7f9-105">PKEY</span></span>

<span data-ttu-id="4a7f9-106">PKEY \_ 相片 \_ EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="4a7f9-107">容器</span><span class="sxs-lookup"><span data-stu-id="4a7f9-107">Containers</span></span>

<span data-ttu-id="4a7f9-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="4a7f9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4a7f9-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="4a7f9-109">Read-Only</span></span>

<span data-ttu-id="4a7f9-110">No</span><span class="sxs-lookup"><span data-stu-id="4a7f9-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4a7f9-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="4a7f9-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4a7f9-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4a7f9-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4a7f9-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="4a7f9-113">Input Type</span></span>

<span data-ttu-id="4a7f9-114">字串。</span><span class="sxs-lookup"><span data-stu-id="4a7f9-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4a7f9-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="4a7f9-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4a7f9-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="4a7f9-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4a7f9-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="4a7f9-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a7f9-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-118">Read Paths</span></span>



| <span data-ttu-id="4a7f9-119">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-119">Order</span></span> | <span data-ttu-id="4a7f9-120">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-120">Path</span></span>                          | <span data-ttu-id="4a7f9-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4a7f9-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="4a7f9-122">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-122">1</span></span>     | <span data-ttu-id="4a7f9-123">/app1/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="4a7f9-124">exif \_ 版本</span><span class="sxs-lookup"><span data-stu-id="4a7f9-124">exif\_version</span></span> |
| <span data-ttu-id="4a7f9-125">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-125">2</span></span>     | <span data-ttu-id="4a7f9-126">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="4a7f9-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7f9-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="4a7f9-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-128">Write Paths</span></span>



| <span data-ttu-id="4a7f9-129">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-129">Order</span></span> | <span data-ttu-id="4a7f9-130">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-130">Path</span></span>                          | <span data-ttu-id="4a7f9-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4a7f9-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="4a7f9-132">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-132">1</span></span>     | <span data-ttu-id="4a7f9-133">/app1/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="4a7f9-134">exif \_ 版本</span><span class="sxs-lookup"><span data-stu-id="4a7f9-134">exif\_version</span></span> |
| <span data-ttu-id="4a7f9-135">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-135">2</span></span>     | <span data-ttu-id="4a7f9-136">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="4a7f9-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7f9-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="4a7f9-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-138">Remove Paths</span></span>



| <span data-ttu-id="4a7f9-139">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-139">Order</span></span> | <span data-ttu-id="4a7f9-140">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="4a7f9-141">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-141">1</span></span>     | <span data-ttu-id="4a7f9-142">/app1/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="4a7f9-143">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-143">2</span></span>     | <span data-ttu-id="4a7f9-144">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="4a7f9-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="4a7f9-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a7f9-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-146">Read Paths</span></span>



| <span data-ttu-id="4a7f9-147">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-147">Order</span></span> | <span data-ttu-id="4a7f9-148">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-148">Path</span></span>                      | <span data-ttu-id="4a7f9-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4a7f9-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="4a7f9-150">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-150">1</span></span>     | <span data-ttu-id="4a7f9-151">/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="4a7f9-152">exif \_ 版本</span><span class="sxs-lookup"><span data-stu-id="4a7f9-152">exif\_version</span></span> |
| <span data-ttu-id="4a7f9-153">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-153">2</span></span>     | <span data-ttu-id="4a7f9-154">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="4a7f9-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7f9-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="4a7f9-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-156">Write Paths</span></span>



| <span data-ttu-id="4a7f9-157">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-157">Order</span></span> | <span data-ttu-id="4a7f9-158">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-158">Path</span></span>                      | <span data-ttu-id="4a7f9-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4a7f9-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="4a7f9-160">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-160">1</span></span>     | <span data-ttu-id="4a7f9-161">/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="4a7f9-162">exif \_ 版本</span><span class="sxs-lookup"><span data-stu-id="4a7f9-162">exif\_version</span></span> |
| <span data-ttu-id="4a7f9-163">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-163">2</span></span>     | <span data-ttu-id="4a7f9-164">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="4a7f9-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7f9-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="4a7f9-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-166">Remove Paths</span></span>



| <span data-ttu-id="4a7f9-167">單</span><span class="sxs-lookup"><span data-stu-id="4a7f9-167">Order</span></span> | <span data-ttu-id="4a7f9-168">路徑</span><span class="sxs-lookup"><span data-stu-id="4a7f9-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4a7f9-169">1</span><span class="sxs-lookup"><span data-stu-id="4a7f9-169">1</span></span>     | <span data-ttu-id="4a7f9-170">/ifd/exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="4a7f9-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="4a7f9-171">2</span><span class="sxs-lookup"><span data-stu-id="4a7f9-171">2</span></span>     | <span data-ttu-id="4a7f9-172">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4a7f9-173">備註</span><span class="sxs-lookup"><span data-stu-id="4a7f9-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a7f9-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a7f9-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a7f9-175">EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="4a7f9-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
