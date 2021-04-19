---
description: DestDistanceRef 屬性的相片中繼資料原則。
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: DestDistanceRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978146"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="abc66-103">DestDistanceRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="abc66-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="abc66-104">[DestDistanceRef](../properties/props-system-gps-destdistanceref.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="abc66-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="abc66-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="abc66-105">PKEY</span></span>

<span data-ttu-id="abc66-106">PKEY \_ DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="abc66-107">容器</span><span class="sxs-lookup"><span data-stu-id="abc66-107">Containers</span></span>

<span data-ttu-id="abc66-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="abc66-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="abc66-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="abc66-109">Read-Only</span></span>

<span data-ttu-id="abc66-110">No</span><span class="sxs-lookup"><span data-stu-id="abc66-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="abc66-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="abc66-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="abc66-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="abc66-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="abc66-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="abc66-113">Input Type</span></span>

<span data-ttu-id="abc66-114">\_接受 vt LPWSTR 或 vt \_ LPSTR。</span><span class="sxs-lookup"><span data-stu-id="abc66-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="abc66-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="abc66-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="abc66-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="abc66-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="abc66-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="abc66-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="abc66-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-118">Read Paths</span></span>



| <span data-ttu-id="abc66-119">單</span><span class="sxs-lookup"><span data-stu-id="abc66-119">Order</span></span> | <span data-ttu-id="abc66-120">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-120">Path</span></span>                         | <span data-ttu-id="abc66-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="abc66-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="abc66-122">1</span><span class="sxs-lookup"><span data-stu-id="abc66-122">1</span></span>     | <span data-ttu-id="abc66-123">/app1/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="abc66-124">ascii</span><span class="sxs-lookup"><span data-stu-id="abc66-124">ascii</span></span>       |
| <span data-ttu-id="abc66-125">2</span><span class="sxs-lookup"><span data-stu-id="abc66-125">2</span></span>     | <span data-ttu-id="abc66-126">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="abc66-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="abc66-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="abc66-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-128">Write Paths</span></span>



| <span data-ttu-id="abc66-129">單</span><span class="sxs-lookup"><span data-stu-id="abc66-129">Order</span></span> | <span data-ttu-id="abc66-130">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-130">Path</span></span>                         | <span data-ttu-id="abc66-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="abc66-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="abc66-132">1</span><span class="sxs-lookup"><span data-stu-id="abc66-132">1</span></span>     | <span data-ttu-id="abc66-133">/app1/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="abc66-134">ascii</span><span class="sxs-lookup"><span data-stu-id="abc66-134">ascii</span></span>       |
| <span data-ttu-id="abc66-135">2</span><span class="sxs-lookup"><span data-stu-id="abc66-135">2</span></span>     | <span data-ttu-id="abc66-136">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="abc66-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="abc66-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="abc66-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-138">Remove Paths</span></span>



| <span data-ttu-id="abc66-139">單</span><span class="sxs-lookup"><span data-stu-id="abc66-139">Order</span></span> | <span data-ttu-id="abc66-140">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="abc66-141">1</span><span class="sxs-lookup"><span data-stu-id="abc66-141">1</span></span>     | <span data-ttu-id="abc66-142">/app1/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="abc66-143">2</span><span class="sxs-lookup"><span data-stu-id="abc66-143">2</span></span>     | <span data-ttu-id="abc66-144">/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="abc66-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="abc66-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="abc66-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="abc66-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-146">Read Paths</span></span>



| <span data-ttu-id="abc66-147">單</span><span class="sxs-lookup"><span data-stu-id="abc66-147">Order</span></span> | <span data-ttu-id="abc66-148">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-148">Path</span></span>                             | <span data-ttu-id="abc66-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="abc66-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="abc66-150">1</span><span class="sxs-lookup"><span data-stu-id="abc66-150">1</span></span>     | <span data-ttu-id="abc66-151">/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="abc66-152">ascii</span><span class="sxs-lookup"><span data-stu-id="abc66-152">ascii</span></span>       |
| <span data-ttu-id="abc66-153">2</span><span class="sxs-lookup"><span data-stu-id="abc66-153">2</span></span>     | <span data-ttu-id="abc66-154">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="abc66-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="abc66-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="abc66-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-156">Write Paths</span></span>



| <span data-ttu-id="abc66-157">單</span><span class="sxs-lookup"><span data-stu-id="abc66-157">Order</span></span> | <span data-ttu-id="abc66-158">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-158">Path</span></span>                             | <span data-ttu-id="abc66-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="abc66-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="abc66-160">1</span><span class="sxs-lookup"><span data-stu-id="abc66-160">1</span></span>     | <span data-ttu-id="abc66-161">/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="abc66-162">ascii</span><span class="sxs-lookup"><span data-stu-id="abc66-162">ascii</span></span>       |
| <span data-ttu-id="abc66-163">2</span><span class="sxs-lookup"><span data-stu-id="abc66-163">2</span></span>     | <span data-ttu-id="abc66-164">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="abc66-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="abc66-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="abc66-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-166">Remove Paths</span></span>



| <span data-ttu-id="abc66-167">單</span><span class="sxs-lookup"><span data-stu-id="abc66-167">Order</span></span> | <span data-ttu-id="abc66-168">路徑</span><span class="sxs-lookup"><span data-stu-id="abc66-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="abc66-169">1</span><span class="sxs-lookup"><span data-stu-id="abc66-169">1</span></span>     | <span data-ttu-id="abc66-170">/ifd/gps/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="abc66-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="abc66-171">2</span><span class="sxs-lookup"><span data-stu-id="abc66-171">2</span></span>     | <span data-ttu-id="abc66-172">/ifd/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="abc66-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="abc66-173">備註</span><span class="sxs-lookup"><span data-stu-id="abc66-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="abc66-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="abc66-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abc66-175">DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="abc66-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
