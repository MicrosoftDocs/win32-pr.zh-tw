---
description: ImgDirectionRef 屬性的相片中繼資料原則。
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: ImgDirectionRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194775"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="38b01-103">ImgDirectionRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="38b01-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="38b01-104">[ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="38b01-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="38b01-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="38b01-105">PKEY</span></span>

<span data-ttu-id="38b01-106">PKEY \_ GPS。ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="38b01-107">容器</span><span class="sxs-lookup"><span data-stu-id="38b01-107">Containers</span></span>

<span data-ttu-id="38b01-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="38b01-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="38b01-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="38b01-109">Read-Only</span></span>

<span data-ttu-id="38b01-110">No</span><span class="sxs-lookup"><span data-stu-id="38b01-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="38b01-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="38b01-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="38b01-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="38b01-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="38b01-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="38b01-113">Input Type</span></span>

<span data-ttu-id="38b01-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="38b01-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="38b01-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="38b01-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="38b01-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="38b01-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="38b01-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="38b01-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="38b01-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-118">Read Paths</span></span>



| <span data-ttu-id="38b01-119">單</span><span class="sxs-lookup"><span data-stu-id="38b01-119">Order</span></span> | <span data-ttu-id="38b01-120">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-120">Path</span></span>                         | <span data-ttu-id="38b01-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38b01-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="38b01-122">1</span><span class="sxs-lookup"><span data-stu-id="38b01-122">1</span></span>     | <span data-ttu-id="38b01-123">/app1/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="38b01-124">ascii</span><span class="sxs-lookup"><span data-stu-id="38b01-124">ascii</span></span>       |
| <span data-ttu-id="38b01-125">2</span><span class="sxs-lookup"><span data-stu-id="38b01-125">2</span></span>     | <span data-ttu-id="38b01-126">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="38b01-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="38b01-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="38b01-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-128">Write Paths</span></span>



| <span data-ttu-id="38b01-129">單</span><span class="sxs-lookup"><span data-stu-id="38b01-129">Order</span></span> | <span data-ttu-id="38b01-130">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-130">Path</span></span>                         | <span data-ttu-id="38b01-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38b01-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="38b01-132">1</span><span class="sxs-lookup"><span data-stu-id="38b01-132">1</span></span>     | <span data-ttu-id="38b01-133">/app1/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="38b01-134">ascii</span><span class="sxs-lookup"><span data-stu-id="38b01-134">ascii</span></span>       |
| <span data-ttu-id="38b01-135">2</span><span class="sxs-lookup"><span data-stu-id="38b01-135">2</span></span>     | <span data-ttu-id="38b01-136">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="38b01-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="38b01-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="38b01-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-138">Remove Paths</span></span>



| <span data-ttu-id="38b01-139">單</span><span class="sxs-lookup"><span data-stu-id="38b01-139">Order</span></span> | <span data-ttu-id="38b01-140">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="38b01-141">1</span><span class="sxs-lookup"><span data-stu-id="38b01-141">1</span></span>     | <span data-ttu-id="38b01-142">/app1/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="38b01-143">2</span><span class="sxs-lookup"><span data-stu-id="38b01-143">2</span></span>     | <span data-ttu-id="38b01-144">/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="38b01-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="38b01-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="38b01-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="38b01-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-146">Read Paths</span></span>



| <span data-ttu-id="38b01-147">單</span><span class="sxs-lookup"><span data-stu-id="38b01-147">Order</span></span> | <span data-ttu-id="38b01-148">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-148">Path</span></span>                             | <span data-ttu-id="38b01-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38b01-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="38b01-150">1</span><span class="sxs-lookup"><span data-stu-id="38b01-150">1</span></span>     | <span data-ttu-id="38b01-151">/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="38b01-152">ascii</span><span class="sxs-lookup"><span data-stu-id="38b01-152">ascii</span></span>       |
| <span data-ttu-id="38b01-153">2</span><span class="sxs-lookup"><span data-stu-id="38b01-153">2</span></span>     | <span data-ttu-id="38b01-154">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="38b01-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="38b01-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="38b01-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-156">Write Paths</span></span>



| <span data-ttu-id="38b01-157">單</span><span class="sxs-lookup"><span data-stu-id="38b01-157">Order</span></span> | <span data-ttu-id="38b01-158">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-158">Path</span></span>                             | <span data-ttu-id="38b01-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38b01-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="38b01-160">1</span><span class="sxs-lookup"><span data-stu-id="38b01-160">1</span></span>     | <span data-ttu-id="38b01-161">/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="38b01-162">ascii</span><span class="sxs-lookup"><span data-stu-id="38b01-162">ascii</span></span>       |
| <span data-ttu-id="38b01-163">2</span><span class="sxs-lookup"><span data-stu-id="38b01-163">2</span></span>     | <span data-ttu-id="38b01-164">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="38b01-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="38b01-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="38b01-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-166">Remove Paths</span></span>



| <span data-ttu-id="38b01-167">單</span><span class="sxs-lookup"><span data-stu-id="38b01-167">Order</span></span> | <span data-ttu-id="38b01-168">路徑</span><span class="sxs-lookup"><span data-stu-id="38b01-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="38b01-169">1</span><span class="sxs-lookup"><span data-stu-id="38b01-169">1</span></span>     | <span data-ttu-id="38b01-170">/ifd/gps/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="38b01-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="38b01-171">2</span><span class="sxs-lookup"><span data-stu-id="38b01-171">2</span></span>     | <span data-ttu-id="38b01-172">/ifd/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="38b01-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38b01-173">備註</span><span class="sxs-lookup"><span data-stu-id="38b01-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="38b01-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="38b01-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b01-175">ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="38b01-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
