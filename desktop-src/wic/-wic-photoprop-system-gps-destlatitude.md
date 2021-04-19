---
description: DestLatitude 屬性的相片中繼資料原則。
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: DestLatitude 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994515"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="8e303-103">DestLatitude 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="8e303-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="8e303-104">[DestLatitude](../properties/props-system-gps-destlatitude.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="8e303-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8e303-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8e303-105">PKEY</span></span>

<span data-ttu-id="8e303-106">PKEY \_ GPS \_ DestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="8e303-107">容器</span><span class="sxs-lookup"><span data-stu-id="8e303-107">Containers</span></span>

<span data-ttu-id="8e303-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="8e303-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8e303-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="8e303-109">Read-Only</span></span>

<span data-ttu-id="8e303-110">Yes</span><span class="sxs-lookup"><span data-stu-id="8e303-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8e303-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8e303-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8e303-112">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="8e303-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8e303-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8e303-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8e303-114">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="8e303-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8e303-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="8e303-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8e303-116">這個值是從 DestLatitudeNumerator 和 DestLatitudeDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="8e303-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="8e303-117">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="8e303-117">It cannot be written directly.</span></span> <span data-ttu-id="8e303-118">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="8e303-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8e303-119">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="8e303-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8e303-120">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-120">Read Paths</span></span>



| <span data-ttu-id="8e303-121">單</span><span class="sxs-lookup"><span data-stu-id="8e303-121">Order</span></span> | <span data-ttu-id="8e303-122">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-122">Path</span></span>                      | <span data-ttu-id="8e303-123">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8e303-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8e303-124">1</span><span class="sxs-lookup"><span data-stu-id="8e303-124">1</span></span>     | <span data-ttu-id="8e303-125">/app1/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="8e303-126">2</span><span class="sxs-lookup"><span data-stu-id="8e303-126">2</span></span>     | <span data-ttu-id="8e303-127">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8e303-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-128">Write Paths</span></span>



| <span data-ttu-id="8e303-129">單</span><span class="sxs-lookup"><span data-stu-id="8e303-129">Order</span></span> | <span data-ttu-id="8e303-130">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-130">Path</span></span>                      | <span data-ttu-id="8e303-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8e303-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8e303-132">1</span><span class="sxs-lookup"><span data-stu-id="8e303-132">1</span></span>     | <span data-ttu-id="8e303-133">/app1/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="8e303-134">2</span><span class="sxs-lookup"><span data-stu-id="8e303-134">2</span></span>     | <span data-ttu-id="8e303-135">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8e303-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-136">Remove Paths</span></span>



| <span data-ttu-id="8e303-137">單</span><span class="sxs-lookup"><span data-stu-id="8e303-137">Order</span></span> | <span data-ttu-id="8e303-138">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8e303-139">1</span><span class="sxs-lookup"><span data-stu-id="8e303-139">1</span></span>     | <span data-ttu-id="8e303-140">/app1/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="8e303-141">2</span><span class="sxs-lookup"><span data-stu-id="8e303-141">2</span></span>     | <span data-ttu-id="8e303-142">/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="8e303-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="8e303-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8e303-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-144">Read Paths</span></span>



| <span data-ttu-id="8e303-145">單</span><span class="sxs-lookup"><span data-stu-id="8e303-145">Order</span></span> | <span data-ttu-id="8e303-146">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-146">Path</span></span>                          | <span data-ttu-id="8e303-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8e303-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8e303-148">1</span><span class="sxs-lookup"><span data-stu-id="8e303-148">1</span></span>     | <span data-ttu-id="8e303-149">/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="8e303-150">2</span><span class="sxs-lookup"><span data-stu-id="8e303-150">2</span></span>     | <span data-ttu-id="8e303-151">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8e303-152">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-152">Write Paths</span></span>



| <span data-ttu-id="8e303-153">單</span><span class="sxs-lookup"><span data-stu-id="8e303-153">Order</span></span> | <span data-ttu-id="8e303-154">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-154">Path</span></span>                          | <span data-ttu-id="8e303-155">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8e303-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8e303-156">1</span><span class="sxs-lookup"><span data-stu-id="8e303-156">1</span></span>     | <span data-ttu-id="8e303-157">/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="8e303-158">2</span><span class="sxs-lookup"><span data-stu-id="8e303-158">2</span></span>     | <span data-ttu-id="8e303-159">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8e303-160">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-160">Remove Paths</span></span>



| <span data-ttu-id="8e303-161">單</span><span class="sxs-lookup"><span data-stu-id="8e303-161">Order</span></span> | <span data-ttu-id="8e303-162">路徑</span><span class="sxs-lookup"><span data-stu-id="8e303-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8e303-163">1</span><span class="sxs-lookup"><span data-stu-id="8e303-163">1</span></span>     | <span data-ttu-id="8e303-164">/ifd/gps/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="8e303-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="8e303-165">2</span><span class="sxs-lookup"><span data-stu-id="8e303-165">2</span></span>     | <span data-ttu-id="8e303-166">/ifd/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8e303-167">備註</span><span class="sxs-lookup"><span data-stu-id="8e303-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e303-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e303-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e303-169">DestLatitude</span><span class="sxs-lookup"><span data-stu-id="8e303-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
