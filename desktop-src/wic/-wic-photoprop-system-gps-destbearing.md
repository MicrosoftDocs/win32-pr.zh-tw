---
description: DestBearing 屬性的相片中繼資料原則。
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: DestBearing 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320411"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="ba9d2-103">DestBearing 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="ba9d2-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="ba9d2-104">[DestBearing](../properties/props-system-gps-destbearing.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="ba9d2-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ba9d2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ba9d2-105">PKEY</span></span>

<span data-ttu-id="ba9d2-106">PKEY \_ GPS \_ DestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="ba9d2-107">容器</span><span class="sxs-lookup"><span data-stu-id="ba9d2-107">Containers</span></span>

<span data-ttu-id="ba9d2-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="ba9d2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ba9d2-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="ba9d2-109">Read-Only</span></span>

<span data-ttu-id="ba9d2-110">Yes</span><span class="sxs-lookup"><span data-stu-id="ba9d2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ba9d2-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ba9d2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ba9d2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ba9d2-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ba9d2-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="ba9d2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="ba9d2-114">您可以藉由寫入 DestBearingNumerator 和 DestBearingDenominator 來寫入這個值。</span><span class="sxs-lookup"><span data-stu-id="ba9d2-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="ba9d2-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="ba9d2-115">It cannot be written directly.</span></span> <span data-ttu-id="ba9d2-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="ba9d2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ba9d2-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="ba9d2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ba9d2-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-118">Read Paths</span></span>



| <span data-ttu-id="ba9d2-119">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-119">Order</span></span> | <span data-ttu-id="ba9d2-120">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-120">Path</span></span>                      | <span data-ttu-id="ba9d2-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ba9d2-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ba9d2-122">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-122">1</span></span>     | <span data-ttu-id="ba9d2-123">/app1/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="ba9d2-124">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-124">2</span></span>     | <span data-ttu-id="ba9d2-125">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="ba9d2-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-126">Write Paths</span></span>



| <span data-ttu-id="ba9d2-127">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-127">Order</span></span> | <span data-ttu-id="ba9d2-128">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-128">Path</span></span>                      | <span data-ttu-id="ba9d2-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ba9d2-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ba9d2-130">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-130">1</span></span>     | <span data-ttu-id="ba9d2-131">/app1/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="ba9d2-132">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-132">2</span></span>     | <span data-ttu-id="ba9d2-133">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ba9d2-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-134">Remove Paths</span></span>



| <span data-ttu-id="ba9d2-135">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-135">Order</span></span> | <span data-ttu-id="ba9d2-136">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-136">Path</span></span>                      | <span data-ttu-id="ba9d2-137">磁碟格式</span><span class="sxs-lookup"><span data-stu-id="ba9d2-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ba9d2-138">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-138">1</span></span>     | <span data-ttu-id="ba9d2-139">/app1/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="ba9d2-140">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-140">2</span></span>     | <span data-ttu-id="ba9d2-141">/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="ba9d2-142">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="ba9d2-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ba9d2-143">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-143">Read Paths</span></span>



| <span data-ttu-id="ba9d2-144">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-144">Order</span></span> | <span data-ttu-id="ba9d2-145">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-145">Path</span></span>                         | <span data-ttu-id="ba9d2-146">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ba9d2-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ba9d2-147">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-147">1</span></span>     | <span data-ttu-id="ba9d2-148">/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="ba9d2-149">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-149">2</span></span>     | <span data-ttu-id="ba9d2-150">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ba9d2-151">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-151">Write Paths</span></span>



| <span data-ttu-id="ba9d2-152">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-152">Order</span></span> | <span data-ttu-id="ba9d2-153">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-153">Path</span></span>                         | <span data-ttu-id="ba9d2-154">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ba9d2-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ba9d2-155">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-155">1</span></span>     | <span data-ttu-id="ba9d2-156">/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="ba9d2-157">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-157">2</span></span>     | <span data-ttu-id="ba9d2-158">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ba9d2-159">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-159">Remove Paths</span></span>



| <span data-ttu-id="ba9d2-160">單</span><span class="sxs-lookup"><span data-stu-id="ba9d2-160">Order</span></span> | <span data-ttu-id="ba9d2-161">路徑</span><span class="sxs-lookup"><span data-stu-id="ba9d2-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="ba9d2-162">1</span><span class="sxs-lookup"><span data-stu-id="ba9d2-162">1</span></span>     | <span data-ttu-id="ba9d2-163">/ifd/gps/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="ba9d2-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="ba9d2-164">2</span><span class="sxs-lookup"><span data-stu-id="ba9d2-164">2</span></span>     | <span data-ttu-id="ba9d2-165">/ifd/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ba9d2-166">備註</span><span class="sxs-lookup"><span data-stu-id="ba9d2-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba9d2-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba9d2-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba9d2-168">DestBearing</span><span class="sxs-lookup"><span data-stu-id="ba9d2-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
