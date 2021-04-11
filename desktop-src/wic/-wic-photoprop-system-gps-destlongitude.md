---
description: DestLongitude 屬性的相片中繼資料原則。
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: DestLongitude 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027270"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="e0595-103">DestLongitude 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="e0595-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="e0595-104">[DestLongitude](../properties/props-system-gps-destlongitude.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="e0595-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e0595-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e0595-105">PKEY</span></span>

<span data-ttu-id="e0595-106">PKEY \_ GPS \_ DestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="e0595-107">容器</span><span class="sxs-lookup"><span data-stu-id="e0595-107">Containers</span></span>

<span data-ttu-id="e0595-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="e0595-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e0595-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="e0595-109">Read-Only</span></span>

<span data-ttu-id="e0595-110">Yes</span><span class="sxs-lookup"><span data-stu-id="e0595-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e0595-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="e0595-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e0595-112">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="e0595-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e0595-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="e0595-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e0595-114">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="e0595-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e0595-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="e0595-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e0595-116">這個值是從 DestLongitudeNumerator 和 DestLongitudeDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="e0595-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="e0595-117">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="e0595-117">It cannot be written directly.</span></span> <span data-ttu-id="e0595-118">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="e0595-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e0595-119">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="e0595-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e0595-120">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-120">Read Paths</span></span>



| <span data-ttu-id="e0595-121">單</span><span class="sxs-lookup"><span data-stu-id="e0595-121">Order</span></span> | <span data-ttu-id="e0595-122">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-122">Path</span></span>                       | <span data-ttu-id="e0595-123">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e0595-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e0595-124">1</span><span class="sxs-lookup"><span data-stu-id="e0595-124">1</span></span>     | <span data-ttu-id="e0595-125">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="e0595-126">2</span><span class="sxs-lookup"><span data-stu-id="e0595-126">2</span></span>     | <span data-ttu-id="e0595-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e0595-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-128">Write Paths</span></span>



| <span data-ttu-id="e0595-129">單</span><span class="sxs-lookup"><span data-stu-id="e0595-129">Order</span></span> | <span data-ttu-id="e0595-130">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-130">Path</span></span>                       | <span data-ttu-id="e0595-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e0595-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e0595-132">1</span><span class="sxs-lookup"><span data-stu-id="e0595-132">1</span></span>     | <span data-ttu-id="e0595-133">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="e0595-134">2</span><span class="sxs-lookup"><span data-stu-id="e0595-134">2</span></span>     | <span data-ttu-id="e0595-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e0595-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-136">Remove Paths</span></span>



| <span data-ttu-id="e0595-137">單</span><span class="sxs-lookup"><span data-stu-id="e0595-137">Order</span></span> | <span data-ttu-id="e0595-138">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="e0595-139">1</span><span class="sxs-lookup"><span data-stu-id="e0595-139">1</span></span>     | <span data-ttu-id="e0595-140">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="e0595-141">2</span><span class="sxs-lookup"><span data-stu-id="e0595-141">2</span></span>     | <span data-ttu-id="e0595-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="e0595-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="e0595-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e0595-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-144">Read Paths</span></span>



| <span data-ttu-id="e0595-145">單</span><span class="sxs-lookup"><span data-stu-id="e0595-145">Order</span></span> | <span data-ttu-id="e0595-146">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-146">Path</span></span>                           | <span data-ttu-id="e0595-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e0595-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e0595-148">1</span><span class="sxs-lookup"><span data-stu-id="e0595-148">1</span></span>     | <span data-ttu-id="e0595-149">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="e0595-150">2</span><span class="sxs-lookup"><span data-stu-id="e0595-150">2</span></span>     | <span data-ttu-id="e0595-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e0595-152">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-152">Write Paths</span></span>



| <span data-ttu-id="e0595-153">單</span><span class="sxs-lookup"><span data-stu-id="e0595-153">Order</span></span> | <span data-ttu-id="e0595-154">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-154">Path</span></span>                           | <span data-ttu-id="e0595-155">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e0595-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e0595-156">1</span><span class="sxs-lookup"><span data-stu-id="e0595-156">1</span></span>     | <span data-ttu-id="e0595-157">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="e0595-158">2</span><span class="sxs-lookup"><span data-stu-id="e0595-158">2</span></span>     | <span data-ttu-id="e0595-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e0595-160">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-160">Remove Paths</span></span>



| <span data-ttu-id="e0595-161">單</span><span class="sxs-lookup"><span data-stu-id="e0595-161">Order</span></span> | <span data-ttu-id="e0595-162">路徑</span><span class="sxs-lookup"><span data-stu-id="e0595-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="e0595-163">1</span><span class="sxs-lookup"><span data-stu-id="e0595-163">1</span></span>     | <span data-ttu-id="e0595-164">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="e0595-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="e0595-165">2</span><span class="sxs-lookup"><span data-stu-id="e0595-165">2</span></span>     | <span data-ttu-id="e0595-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e0595-167">備註</span><span class="sxs-lookup"><span data-stu-id="e0595-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0595-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0595-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0595-169">DestLongitude</span><span class="sxs-lookup"><span data-stu-id="e0595-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
