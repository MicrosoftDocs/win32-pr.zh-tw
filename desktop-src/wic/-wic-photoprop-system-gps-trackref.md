---
description: TrackRef 屬性的相片中繼資料原則。
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: TrackRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195313"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="448e1-103">TrackRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="448e1-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="448e1-104">[TrackRef](../properties/props-system-gps-trackref.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="448e1-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="448e1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="448e1-105">PKEY</span></span>

<span data-ttu-id="448e1-106">PKEY \_ GPS \_ TrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="448e1-107">容器</span><span class="sxs-lookup"><span data-stu-id="448e1-107">Containers</span></span>

<span data-ttu-id="448e1-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="448e1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="448e1-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="448e1-109">Read-Only</span></span>

<span data-ttu-id="448e1-110">No</span><span class="sxs-lookup"><span data-stu-id="448e1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="448e1-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="448e1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="448e1-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="448e1-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="448e1-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="448e1-113">Input Type</span></span>

<span data-ttu-id="448e1-114">String</span><span class="sxs-lookup"><span data-stu-id="448e1-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="448e1-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="448e1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="448e1-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="448e1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="448e1-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="448e1-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="448e1-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-118">Read Paths</span></span>



| <span data-ttu-id="448e1-119">單</span><span class="sxs-lookup"><span data-stu-id="448e1-119">Order</span></span> | <span data-ttu-id="448e1-120">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-120">Path</span></span>                      | <span data-ttu-id="448e1-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="448e1-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="448e1-122">1</span><span class="sxs-lookup"><span data-stu-id="448e1-122">1</span></span>     | <span data-ttu-id="448e1-123">/app1/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="448e1-124">ascii</span><span class="sxs-lookup"><span data-stu-id="448e1-124">ascii</span></span>       |
| <span data-ttu-id="448e1-125">2</span><span class="sxs-lookup"><span data-stu-id="448e1-125">2</span></span>     | <span data-ttu-id="448e1-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="448e1-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="448e1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="448e1-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-128">Write Paths</span></span>



| <span data-ttu-id="448e1-129">單</span><span class="sxs-lookup"><span data-stu-id="448e1-129">Order</span></span> | <span data-ttu-id="448e1-130">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-130">Path</span></span>                      | <span data-ttu-id="448e1-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="448e1-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="448e1-132">1</span><span class="sxs-lookup"><span data-stu-id="448e1-132">1</span></span>     | <span data-ttu-id="448e1-133">/app1/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="448e1-134">ascii</span><span class="sxs-lookup"><span data-stu-id="448e1-134">ascii</span></span>       |
| <span data-ttu-id="448e1-135">2</span><span class="sxs-lookup"><span data-stu-id="448e1-135">2</span></span>     | <span data-ttu-id="448e1-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="448e1-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="448e1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="448e1-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-138">Remove Paths</span></span>



| <span data-ttu-id="448e1-139">單</span><span class="sxs-lookup"><span data-stu-id="448e1-139">Order</span></span> | <span data-ttu-id="448e1-140">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="448e1-141">1</span><span class="sxs-lookup"><span data-stu-id="448e1-141">1</span></span>     | <span data-ttu-id="448e1-142">/app1/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="448e1-143">2</span><span class="sxs-lookup"><span data-stu-id="448e1-143">2</span></span>     | <span data-ttu-id="448e1-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="448e1-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="448e1-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="448e1-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="448e1-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-146">Read Paths</span></span>



| <span data-ttu-id="448e1-147">單</span><span class="sxs-lookup"><span data-stu-id="448e1-147">Order</span></span> | <span data-ttu-id="448e1-148">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-148">Path</span></span>                      | <span data-ttu-id="448e1-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="448e1-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="448e1-150">1</span><span class="sxs-lookup"><span data-stu-id="448e1-150">1</span></span>     | <span data-ttu-id="448e1-151">/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="448e1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="448e1-152">ascii</span></span>       |
| <span data-ttu-id="448e1-153">2</span><span class="sxs-lookup"><span data-stu-id="448e1-153">2</span></span>     | <span data-ttu-id="448e1-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="448e1-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="448e1-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="448e1-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-156">Write Paths</span></span>



| <span data-ttu-id="448e1-157">單</span><span class="sxs-lookup"><span data-stu-id="448e1-157">Order</span></span> | <span data-ttu-id="448e1-158">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-158">Path</span></span>                      | <span data-ttu-id="448e1-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="448e1-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="448e1-160">1</span><span class="sxs-lookup"><span data-stu-id="448e1-160">1</span></span>     | <span data-ttu-id="448e1-161">/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="448e1-162">ascii</span><span class="sxs-lookup"><span data-stu-id="448e1-162">ascii</span></span>       |
| <span data-ttu-id="448e1-163">2</span><span class="sxs-lookup"><span data-stu-id="448e1-163">2</span></span>     | <span data-ttu-id="448e1-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="448e1-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="448e1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="448e1-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-166">Remove Paths</span></span>



| <span data-ttu-id="448e1-167">單</span><span class="sxs-lookup"><span data-stu-id="448e1-167">Order</span></span> | <span data-ttu-id="448e1-168">路徑</span><span class="sxs-lookup"><span data-stu-id="448e1-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="448e1-169">1</span><span class="sxs-lookup"><span data-stu-id="448e1-169">1</span></span>     | <span data-ttu-id="448e1-170">/ifd/gps/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="448e1-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="448e1-171">2</span><span class="sxs-lookup"><span data-stu-id="448e1-171">2</span></span>     | <span data-ttu-id="448e1-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="448e1-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="448e1-173">備註</span><span class="sxs-lookup"><span data-stu-id="448e1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="448e1-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="448e1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="448e1-175">TrackRef</span><span class="sxs-lookup"><span data-stu-id="448e1-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
