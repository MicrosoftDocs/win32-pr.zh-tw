---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: GPS. 經度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985342"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="7dae8-103">GPS. 經度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="7dae8-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="7dae8-104">適用于 [system.object](../properties/props-system-gps-longitude.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="7dae8-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7dae8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7dae8-105">PKEY</span></span>

<span data-ttu-id="7dae8-106">PKEY \_ GPS \_ 經度</span><span class="sxs-lookup"><span data-stu-id="7dae8-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="7dae8-107">容器</span><span class="sxs-lookup"><span data-stu-id="7dae8-107">Containers</span></span>

<span data-ttu-id="7dae8-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="7dae8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7dae8-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="7dae8-109">Read-Only</span></span>

<span data-ttu-id="7dae8-110">Yes</span><span class="sxs-lookup"><span data-stu-id="7dae8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7dae8-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="7dae8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7dae8-112">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="7dae8-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7dae8-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="7dae8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="7dae8-114">您可以藉由寫入 LongitudeNumerator 和 LongitudeDenominator 來寫入這個值。</span><span class="sxs-lookup"><span data-stu-id="7dae8-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="7dae8-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="7dae8-115">It cannot be written directly.</span></span> <span data-ttu-id="7dae8-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="7dae8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7dae8-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="7dae8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7dae8-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-118">Read Paths</span></span>



| <span data-ttu-id="7dae8-119">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-119">Order</span></span> | <span data-ttu-id="7dae8-120">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-120">Path</span></span>                     | <span data-ttu-id="7dae8-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7dae8-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="7dae8-122">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-122">1</span></span>     | <span data-ttu-id="7dae8-123">/app1/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="7dae8-124">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-124">2</span></span>     | <span data-ttu-id="7dae8-125">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="7dae8-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-126">Write Paths</span></span>



| <span data-ttu-id="7dae8-127">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-127">Order</span></span> | <span data-ttu-id="7dae8-128">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-128">Path</span></span>                     | <span data-ttu-id="7dae8-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7dae8-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="7dae8-130">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-130">1</span></span>     | <span data-ttu-id="7dae8-131">/app1/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="7dae8-132">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-132">2</span></span>     | <span data-ttu-id="7dae8-133">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7dae8-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-134">Remove Paths</span></span>



| <span data-ttu-id="7dae8-135">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-135">Order</span></span> | <span data-ttu-id="7dae8-136">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="7dae8-137">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-137">1</span></span>     | <span data-ttu-id="7dae8-138">/app1/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="7dae8-139">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-139">2</span></span>     | <span data-ttu-id="7dae8-140">/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="7dae8-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="7dae8-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7dae8-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-142">Read Paths</span></span>



| <span data-ttu-id="7dae8-143">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-143">Order</span></span> | <span data-ttu-id="7dae8-144">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-144">Path</span></span>                       | <span data-ttu-id="7dae8-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7dae8-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="7dae8-146">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-146">1</span></span>     | <span data-ttu-id="7dae8-147">/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="7dae8-148">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-148">2</span></span>     | <span data-ttu-id="7dae8-149">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="7dae8-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-150">Write Paths</span></span>



| <span data-ttu-id="7dae8-151">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-151">Order</span></span> | <span data-ttu-id="7dae8-152">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-152">Path</span></span>                       | <span data-ttu-id="7dae8-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7dae8-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="7dae8-154">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-154">1</span></span>     | <span data-ttu-id="7dae8-155">/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="7dae8-156">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-156">2</span></span>     | <span data-ttu-id="7dae8-157">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7dae8-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-158">Remove Paths</span></span>



| <span data-ttu-id="7dae8-159">單</span><span class="sxs-lookup"><span data-stu-id="7dae8-159">Order</span></span> | <span data-ttu-id="7dae8-160">路徑</span><span class="sxs-lookup"><span data-stu-id="7dae8-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="7dae8-161">1</span><span class="sxs-lookup"><span data-stu-id="7dae8-161">1</span></span>     | <span data-ttu-id="7dae8-162">/ifd/gps/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="7dae8-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="7dae8-163">2</span><span class="sxs-lookup"><span data-stu-id="7dae8-163">2</span></span>     | <span data-ttu-id="7dae8-164">/ifd/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="7dae8-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7dae8-165">備註</span><span class="sxs-lookup"><span data-stu-id="7dae8-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dae8-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dae8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dae8-167">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="7dae8-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
