---
description: 適用于 [追蹤] 屬性的相片中繼資料原則。
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: GPS：追蹤相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994570"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="68157-103">GPS：追蹤相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="68157-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="68157-104">適用于 [ [追蹤](../properties/props-system-gps-track.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="68157-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="68157-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="68157-105">PKEY</span></span>

<span data-ttu-id="68157-106">PKEY \_ GPS \_ 軌</span><span class="sxs-lookup"><span data-stu-id="68157-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="68157-107">容器</span><span class="sxs-lookup"><span data-stu-id="68157-107">Containers</span></span>

<span data-ttu-id="68157-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="68157-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="68157-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="68157-109">Read-Only</span></span>

<span data-ttu-id="68157-110">Yes</span><span class="sxs-lookup"><span data-stu-id="68157-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="68157-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="68157-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="68157-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="68157-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="68157-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="68157-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="68157-114">這個值是從 TrackNumerator 和 TrackDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="68157-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="68157-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="68157-115">It cannot be written directly.</span></span> <span data-ttu-id="68157-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="68157-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="68157-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="68157-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="68157-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="68157-118">Read Paths</span></span>



| <span data-ttu-id="68157-119">單</span><span class="sxs-lookup"><span data-stu-id="68157-119">Order</span></span> | <span data-ttu-id="68157-120">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-120">Path</span></span>                      | <span data-ttu-id="68157-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="68157-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="68157-122">1</span><span class="sxs-lookup"><span data-stu-id="68157-122">1</span></span>     | <span data-ttu-id="68157-123">/app1/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="68157-124">2</span><span class="sxs-lookup"><span data-stu-id="68157-124">2</span></span>     | <span data-ttu-id="68157-125">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="68157-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="68157-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="68157-126">Write Paths</span></span>



| <span data-ttu-id="68157-127">單</span><span class="sxs-lookup"><span data-stu-id="68157-127">Order</span></span> | <span data-ttu-id="68157-128">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-128">Path</span></span>                      | <span data-ttu-id="68157-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="68157-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="68157-130">1</span><span class="sxs-lookup"><span data-stu-id="68157-130">1</span></span>     | <span data-ttu-id="68157-131">/app1/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="68157-132">2</span><span class="sxs-lookup"><span data-stu-id="68157-132">2</span></span>     | <span data-ttu-id="68157-133">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="68157-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="68157-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="68157-134">Remove Paths</span></span>



| <span data-ttu-id="68157-135">單</span><span class="sxs-lookup"><span data-stu-id="68157-135">Order</span></span> | <span data-ttu-id="68157-136">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="68157-137">1</span><span class="sxs-lookup"><span data-stu-id="68157-137">1</span></span>     | <span data-ttu-id="68157-138">/app1/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="68157-139">2</span><span class="sxs-lookup"><span data-stu-id="68157-139">2</span></span>     | <span data-ttu-id="68157-140">/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="68157-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="68157-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="68157-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="68157-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="68157-142">Read Paths</span></span>



| <span data-ttu-id="68157-143">單</span><span class="sxs-lookup"><span data-stu-id="68157-143">Order</span></span> | <span data-ttu-id="68157-144">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-144">Path</span></span>                   | <span data-ttu-id="68157-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="68157-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="68157-146">1</span><span class="sxs-lookup"><span data-stu-id="68157-146">1</span></span>     | <span data-ttu-id="68157-147">/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="68157-148">2</span><span class="sxs-lookup"><span data-stu-id="68157-148">2</span></span>     | <span data-ttu-id="68157-149">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="68157-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="68157-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="68157-150">Write Paths</span></span>



| <span data-ttu-id="68157-151">單</span><span class="sxs-lookup"><span data-stu-id="68157-151">Order</span></span> | <span data-ttu-id="68157-152">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-152">Path</span></span>                   | <span data-ttu-id="68157-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="68157-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="68157-154">1</span><span class="sxs-lookup"><span data-stu-id="68157-154">1</span></span>     | <span data-ttu-id="68157-155">/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="68157-156">2</span><span class="sxs-lookup"><span data-stu-id="68157-156">2</span></span>     | <span data-ttu-id="68157-157">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="68157-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="68157-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="68157-158">Remove Paths</span></span>



| <span data-ttu-id="68157-159">單</span><span class="sxs-lookup"><span data-stu-id="68157-159">Order</span></span> | <span data-ttu-id="68157-160">路徑</span><span class="sxs-lookup"><span data-stu-id="68157-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="68157-161">1</span><span class="sxs-lookup"><span data-stu-id="68157-161">1</span></span>     | <span data-ttu-id="68157-162">/ifd/gps/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="68157-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="68157-163">2</span><span class="sxs-lookup"><span data-stu-id="68157-163">2</span></span>     | <span data-ttu-id="68157-164">/ifd/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="68157-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="68157-165">備註</span><span class="sxs-lookup"><span data-stu-id="68157-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="68157-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="68157-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68157-167">GPS. 追蹤</span><span class="sxs-lookup"><span data-stu-id="68157-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
