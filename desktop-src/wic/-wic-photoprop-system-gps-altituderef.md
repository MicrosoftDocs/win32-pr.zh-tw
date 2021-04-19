---
description: AltitudeRef 屬性的相片中繼資料原則。
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: AltitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980502"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="1d244-103">AltitudeRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="1d244-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="1d244-104">[AltitudeRef](../properties/props-system-gps-altituderef.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="1d244-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1d244-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1d244-105">PKEY</span></span>

<span data-ttu-id="1d244-106">PKEY \_ GPS \_ AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="1d244-107">Description</span><span class="sxs-lookup"><span data-stu-id="1d244-107">Description</span></span>

<span data-ttu-id="1d244-108">表示用來做為參考高度的高度。</span><span class="sxs-lookup"><span data-stu-id="1d244-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="1d244-109">值為0表示海拔超過海平面。</span><span class="sxs-lookup"><span data-stu-id="1d244-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="1d244-110">值為1時，表示低於海平面的高度。</span><span class="sxs-lookup"><span data-stu-id="1d244-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="1d244-111">容器</span><span class="sxs-lookup"><span data-stu-id="1d244-111">Containers</span></span>

<span data-ttu-id="1d244-112">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="1d244-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1d244-113">唯讀</span><span class="sxs-lookup"><span data-stu-id="1d244-113">Read-Only</span></span>

<span data-ttu-id="1d244-114">No</span><span class="sxs-lookup"><span data-stu-id="1d244-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1d244-115">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="1d244-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1d244-116">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="1d244-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="1d244-117">輸入類型</span><span class="sxs-lookup"><span data-stu-id="1d244-117">Input Type</span></span>

<span data-ttu-id="1d244-118">位元組。</span><span class="sxs-lookup"><span data-stu-id="1d244-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1d244-119">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="1d244-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="1d244-120">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="1d244-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="1d244-121">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="1d244-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1d244-122">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-122">Read Paths</span></span>



| <span data-ttu-id="1d244-123">單</span><span class="sxs-lookup"><span data-stu-id="1d244-123">Order</span></span> | <span data-ttu-id="1d244-124">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-124">Path</span></span>                     | <span data-ttu-id="1d244-125">磁片格式</span><span class="sxs-lookup"><span data-stu-id="1d244-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1d244-126">1</span><span class="sxs-lookup"><span data-stu-id="1d244-126">1</span></span>     | <span data-ttu-id="1d244-127">/app1/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="1d244-128">byte</span><span class="sxs-lookup"><span data-stu-id="1d244-128">byte</span></span>        |
| <span data-ttu-id="1d244-129">2</span><span class="sxs-lookup"><span data-stu-id="1d244-129">2</span></span>     | <span data-ttu-id="1d244-130">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1d244-131">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d244-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1d244-132">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-132">Write Paths</span></span>



| <span data-ttu-id="1d244-133">單</span><span class="sxs-lookup"><span data-stu-id="1d244-133">Order</span></span> | <span data-ttu-id="1d244-134">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-134">Path</span></span>                     | <span data-ttu-id="1d244-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="1d244-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1d244-136">1</span><span class="sxs-lookup"><span data-stu-id="1d244-136">1</span></span>     | <span data-ttu-id="1d244-137">/app1/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="1d244-138">byte</span><span class="sxs-lookup"><span data-stu-id="1d244-138">byte</span></span>        |
| <span data-ttu-id="1d244-139">2</span><span class="sxs-lookup"><span data-stu-id="1d244-139">2</span></span>     | <span data-ttu-id="1d244-140">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1d244-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d244-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1d244-142">移除路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-142">Remove Paths</span></span>



| <span data-ttu-id="1d244-143">單</span><span class="sxs-lookup"><span data-stu-id="1d244-143">Order</span></span> | <span data-ttu-id="1d244-144">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1d244-145">1</span><span class="sxs-lookup"><span data-stu-id="1d244-145">1</span></span>     | <span data-ttu-id="1d244-146">/app1/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="1d244-147">2</span><span class="sxs-lookup"><span data-stu-id="1d244-147">2</span></span>     | <span data-ttu-id="1d244-148">/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="1d244-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="1d244-149">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="1d244-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1d244-150">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-150">Read Paths</span></span>



| <span data-ttu-id="1d244-151">單</span><span class="sxs-lookup"><span data-stu-id="1d244-151">Order</span></span> | <span data-ttu-id="1d244-152">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-152">Path</span></span>                         | <span data-ttu-id="1d244-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="1d244-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="1d244-154">1</span><span class="sxs-lookup"><span data-stu-id="1d244-154">1</span></span>     | <span data-ttu-id="1d244-155">/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="1d244-156">byte</span><span class="sxs-lookup"><span data-stu-id="1d244-156">byte</span></span>        |
| <span data-ttu-id="1d244-157">2</span><span class="sxs-lookup"><span data-stu-id="1d244-157">2</span></span>     | <span data-ttu-id="1d244-158">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1d244-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d244-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1d244-160">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-160">Write Paths</span></span>



| <span data-ttu-id="1d244-161">單</span><span class="sxs-lookup"><span data-stu-id="1d244-161">Order</span></span> | <span data-ttu-id="1d244-162">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-162">Path</span></span>                         | <span data-ttu-id="1d244-163">磁片格式</span><span class="sxs-lookup"><span data-stu-id="1d244-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="1d244-164">1</span><span class="sxs-lookup"><span data-stu-id="1d244-164">1</span></span>     | <span data-ttu-id="1d244-165">/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="1d244-166">byte</span><span class="sxs-lookup"><span data-stu-id="1d244-166">byte</span></span>        |
| <span data-ttu-id="1d244-167">2</span><span class="sxs-lookup"><span data-stu-id="1d244-167">2</span></span>     | <span data-ttu-id="1d244-168">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1d244-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d244-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1d244-170">移除路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-170">Remove Paths</span></span>



| <span data-ttu-id="1d244-171">單</span><span class="sxs-lookup"><span data-stu-id="1d244-171">Order</span></span> | <span data-ttu-id="1d244-172">路徑</span><span class="sxs-lookup"><span data-stu-id="1d244-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="1d244-173">1</span><span class="sxs-lookup"><span data-stu-id="1d244-173">1</span></span>     | <span data-ttu-id="1d244-174">/ifd/gps/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1d244-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="1d244-175">2</span><span class="sxs-lookup"><span data-stu-id="1d244-175">2</span></span>     | <span data-ttu-id="1d244-176">/ifd/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="1d244-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1d244-177">備註</span><span class="sxs-lookup"><span data-stu-id="1d244-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d244-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d244-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d244-179">AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1d244-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
