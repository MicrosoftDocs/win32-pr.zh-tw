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
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="ce4af-103">DestLongitude 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="ce4af-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="ce4af-104">[DestLongitude](../properties/props-system-gps-destlongitude.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="ce4af-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ce4af-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ce4af-105">PKEY</span></span>

<span data-ttu-id="ce4af-106">PKEY \_ GPS \_ DestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="ce4af-107">容器</span><span class="sxs-lookup"><span data-stu-id="ce4af-107">Containers</span></span>

<span data-ttu-id="ce4af-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="ce4af-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ce4af-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="ce4af-109">Read-Only</span></span>

<span data-ttu-id="ce4af-110">Yes</span><span class="sxs-lookup"><span data-stu-id="ce4af-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ce4af-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ce4af-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ce4af-112">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="ce4af-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="ce4af-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ce4af-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="ce4af-114">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="ce4af-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ce4af-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="ce4af-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ce4af-116">這個值是從 DestLongitudeNumerator 和 DestLongitudeDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="ce4af-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="ce4af-117">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="ce4af-117">It cannot be written directly.</span></span> <span data-ttu-id="ce4af-118">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="ce4af-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ce4af-119">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="ce4af-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce4af-120">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-120">Read Paths</span></span>



| <span data-ttu-id="ce4af-121">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-121">Order</span></span> | <span data-ttu-id="ce4af-122">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-122">Path</span></span>                       | <span data-ttu-id="ce4af-123">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce4af-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="ce4af-124">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-124">1</span></span>     | <span data-ttu-id="ce4af-125">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="ce4af-126">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-126">2</span></span>     | <span data-ttu-id="ce4af-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ce4af-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-128">Write Paths</span></span>



| <span data-ttu-id="ce4af-129">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-129">Order</span></span> | <span data-ttu-id="ce4af-130">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-130">Path</span></span>                       | <span data-ttu-id="ce4af-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce4af-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="ce4af-132">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-132">1</span></span>     | <span data-ttu-id="ce4af-133">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="ce4af-134">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-134">2</span></span>     | <span data-ttu-id="ce4af-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ce4af-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-136">Remove Paths</span></span>



| <span data-ttu-id="ce4af-137">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-137">Order</span></span> | <span data-ttu-id="ce4af-138">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="ce4af-139">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-139">1</span></span>     | <span data-ttu-id="ce4af-140">/app1/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="ce4af-141">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-141">2</span></span>     | <span data-ttu-id="ce4af-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ce4af-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="ce4af-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce4af-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-144">Read Paths</span></span>



| <span data-ttu-id="ce4af-145">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-145">Order</span></span> | <span data-ttu-id="ce4af-146">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-146">Path</span></span>                           | <span data-ttu-id="ce4af-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce4af-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="ce4af-148">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-148">1</span></span>     | <span data-ttu-id="ce4af-149">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="ce4af-150">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-150">2</span></span>     | <span data-ttu-id="ce4af-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ce4af-152">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-152">Write Paths</span></span>



| <span data-ttu-id="ce4af-153">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-153">Order</span></span> | <span data-ttu-id="ce4af-154">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-154">Path</span></span>                           | <span data-ttu-id="ce4af-155">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce4af-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="ce4af-156">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-156">1</span></span>     | <span data-ttu-id="ce4af-157">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="ce4af-158">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-158">2</span></span>     | <span data-ttu-id="ce4af-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ce4af-160">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-160">Remove Paths</span></span>



| <span data-ttu-id="ce4af-161">單</span><span class="sxs-lookup"><span data-stu-id="ce4af-161">Order</span></span> | <span data-ttu-id="ce4af-162">路徑</span><span class="sxs-lookup"><span data-stu-id="ce4af-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="ce4af-163">1</span><span class="sxs-lookup"><span data-stu-id="ce4af-163">1</span></span>     | <span data-ttu-id="ce4af-164">/ifd/gps/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="ce4af-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="ce4af-165">2</span><span class="sxs-lookup"><span data-stu-id="ce4af-165">2</span></span>     | <span data-ttu-id="ce4af-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ce4af-167">備註</span><span class="sxs-lookup"><span data-stu-id="ce4af-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce4af-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce4af-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce4af-169">DestLongitude</span><span class="sxs-lookup"><span data-stu-id="ce4af-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
