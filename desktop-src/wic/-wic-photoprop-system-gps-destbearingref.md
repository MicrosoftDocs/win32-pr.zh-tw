---
description: DestBearingRef 屬性的相片中繼資料原則。
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: DestBearingRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193558"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="5e2ee-103">DestBearingRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="5e2ee-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="5e2ee-104">[DestBearingRef](../properties/props-system-gps-destbearingref.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="5e2ee-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5e2ee-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5e2ee-105">PKEY</span></span>

<span data-ttu-id="5e2ee-106">PKEY \_ GPS \_ DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="5e2ee-107">容器</span><span class="sxs-lookup"><span data-stu-id="5e2ee-107">Containers</span></span>

<span data-ttu-id="5e2ee-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="5e2ee-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5e2ee-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="5e2ee-109">Read-Only</span></span>

<span data-ttu-id="5e2ee-110">No</span><span class="sxs-lookup"><span data-stu-id="5e2ee-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5e2ee-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="5e2ee-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5e2ee-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5e2ee-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5e2ee-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="5e2ee-113">Input Type</span></span>

<span data-ttu-id="5e2ee-114">字串。</span><span class="sxs-lookup"><span data-stu-id="5e2ee-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5e2ee-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="5e2ee-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5e2ee-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="5e2ee-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="5e2ee-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="5e2ee-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5e2ee-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-118">Read Paths</span></span>



| <span data-ttu-id="5e2ee-119">單</span><span class="sxs-lookup"><span data-stu-id="5e2ee-119">Order</span></span> | <span data-ttu-id="5e2ee-120">路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-120">Path</span></span>                        | <span data-ttu-id="5e2ee-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5e2ee-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="5e2ee-122">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-122">1</span></span>     | <span data-ttu-id="5e2ee-123">/app1/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="5e2ee-124">ascii</span><span class="sxs-lookup"><span data-stu-id="5e2ee-124">ascii</span></span>       |
| <span data-ttu-id="5e2ee-125">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-125">2</span></span>     | <span data-ttu-id="5e2ee-126">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="5e2ee-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="5e2ee-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5e2ee-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-128">Write Paths</span></span>



| <span data-ttu-id="5e2ee-129">單</span><span class="sxs-lookup"><span data-stu-id="5e2ee-129">Order</span></span> | <span data-ttu-id="5e2ee-130">路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-130">Path</span></span>                        | <span data-ttu-id="5e2ee-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5e2ee-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="5e2ee-132">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-132">1</span></span>     | <span data-ttu-id="5e2ee-133">/app1/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="5e2ee-134">ascii</span><span class="sxs-lookup"><span data-stu-id="5e2ee-134">ascii</span></span>       |
| <span data-ttu-id="5e2ee-135">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-135">2</span></span>     | <span data-ttu-id="5e2ee-136">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="5e2ee-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="5e2ee-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5e2ee-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-138">Remove Paths</span></span>



| <span data-ttu-id="5e2ee-139">單</span><span class="sxs-lookup"><span data-stu-id="5e2ee-139">Order</span></span> | <span data-ttu-id="5e2ee-140">路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="5e2ee-141">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-141">1</span></span>     | <span data-ttu-id="5e2ee-142">/app1/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="5e2ee-143">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-143">2</span></span>     | <span data-ttu-id="5e2ee-144">/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="5e2ee-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="5e2ee-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="5e2ee-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5e2ee-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-146">Read Paths</span></span>



| <span data-ttu-id="5e2ee-147">單</span><span class="sxs-lookup"><span data-stu-id="5e2ee-147">Order</span></span> | <span data-ttu-id="5e2ee-148">路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-148">Path</span></span>                            | <span data-ttu-id="5e2ee-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5e2ee-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="5e2ee-150">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-150">1</span></span>     | <span data-ttu-id="5e2ee-151">/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="5e2ee-152">ascii</span><span class="sxs-lookup"><span data-stu-id="5e2ee-152">ascii</span></span>       |
| <span data-ttu-id="5e2ee-153">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-153">2</span></span>     | <span data-ttu-id="5e2ee-154">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="5e2ee-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="5e2ee-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5e2ee-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-156">Write Paths</span></span>



| <span data-ttu-id="5e2ee-157">單</span><span class="sxs-lookup"><span data-stu-id="5e2ee-157">Order</span></span> | <span data-ttu-id="5e2ee-158">路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-158">Path</span></span>                            | <span data-ttu-id="5e2ee-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5e2ee-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="5e2ee-160">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-160">1</span></span>     | <span data-ttu-id="5e2ee-161">/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="5e2ee-162">ascii</span><span class="sxs-lookup"><span data-stu-id="5e2ee-162">ascii</span></span>       |
| <span data-ttu-id="5e2ee-163">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-163">2</span></span>     | <span data-ttu-id="5e2ee-164">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="5e2ee-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="5e2ee-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5e2ee-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="5e2ee-166">Remove Paths</span></span>



| <span data-ttu-id="5e2ee-167">順序</span><span class="sxs-lookup"><span data-stu-id="5e2ee-167">order</span></span> | <span data-ttu-id="5e2ee-168">path</span><span class="sxs-lookup"><span data-stu-id="5e2ee-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="5e2ee-169">1</span><span class="sxs-lookup"><span data-stu-id="5e2ee-169">1</span></span>     | <span data-ttu-id="5e2ee-170">/ifd/gps/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="5e2ee-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="5e2ee-171">2</span><span class="sxs-lookup"><span data-stu-id="5e2ee-171">2</span></span>     | <span data-ttu-id="5e2ee-172">/ifd/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="5e2ee-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5e2ee-173">備註</span><span class="sxs-lookup"><span data-stu-id="5e2ee-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e2ee-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e2ee-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e2ee-175">DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="5e2ee-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
