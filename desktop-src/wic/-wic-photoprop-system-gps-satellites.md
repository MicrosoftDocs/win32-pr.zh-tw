---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: 系統 GPS. 衛星相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969384"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="38f32-103">系統 GPS. 衛星相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="38f32-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="38f32-104">適用于 [system.object](../properties/props-system-gps-satellites.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="38f32-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="38f32-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="38f32-105">PKEY</span></span>

<span data-ttu-id="38f32-106">PKEY \_ GPS \_ 衛星</span><span class="sxs-lookup"><span data-stu-id="38f32-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="38f32-107">容器</span><span class="sxs-lookup"><span data-stu-id="38f32-107">Containers</span></span>

<span data-ttu-id="38f32-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="38f32-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="38f32-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="38f32-109">Read-Only</span></span>

<span data-ttu-id="38f32-110">No</span><span class="sxs-lookup"><span data-stu-id="38f32-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="38f32-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="38f32-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="38f32-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="38f32-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="38f32-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="38f32-113">Input Type</span></span>

<span data-ttu-id="38f32-114">字串。</span><span class="sxs-lookup"><span data-stu-id="38f32-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="38f32-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="38f32-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="38f32-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="38f32-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="38f32-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="38f32-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="38f32-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-118">Read Paths</span></span>



| <span data-ttu-id="38f32-119">單</span><span class="sxs-lookup"><span data-stu-id="38f32-119">Order</span></span> | <span data-ttu-id="38f32-120">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-120">Path</span></span>                     | <span data-ttu-id="38f32-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38f32-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="38f32-122">1</span><span class="sxs-lookup"><span data-stu-id="38f32-122">1</span></span>     | <span data-ttu-id="38f32-123">/app1/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="38f32-124">ascii</span><span class="sxs-lookup"><span data-stu-id="38f32-124">ascii</span></span>       |
| <span data-ttu-id="38f32-125">2</span><span class="sxs-lookup"><span data-stu-id="38f32-125">2</span></span>     | <span data-ttu-id="38f32-126">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="38f32-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="38f32-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="38f32-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-128">Write Paths</span></span>



| <span data-ttu-id="38f32-129">單</span><span class="sxs-lookup"><span data-stu-id="38f32-129">Order</span></span> | <span data-ttu-id="38f32-130">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-130">Path</span></span>                     | <span data-ttu-id="38f32-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38f32-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="38f32-132">1</span><span class="sxs-lookup"><span data-stu-id="38f32-132">1</span></span>     | <span data-ttu-id="38f32-133">/app1/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="38f32-134">ascii</span><span class="sxs-lookup"><span data-stu-id="38f32-134">ascii</span></span>       |
| <span data-ttu-id="38f32-135">2</span><span class="sxs-lookup"><span data-stu-id="38f32-135">2</span></span>     | <span data-ttu-id="38f32-136">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="38f32-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="38f32-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="38f32-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-138">Remove Paths</span></span>



| <span data-ttu-id="38f32-139">單</span><span class="sxs-lookup"><span data-stu-id="38f32-139">Order</span></span> | <span data-ttu-id="38f32-140">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="38f32-141">1</span><span class="sxs-lookup"><span data-stu-id="38f32-141">1</span></span>     | <span data-ttu-id="38f32-142">/app1/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="38f32-143">2</span><span class="sxs-lookup"><span data-stu-id="38f32-143">2</span></span>     | <span data-ttu-id="38f32-144">/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="38f32-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="38f32-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="38f32-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-146">Read Paths</span></span>



| <span data-ttu-id="38f32-147">單</span><span class="sxs-lookup"><span data-stu-id="38f32-147">Order</span></span> | <span data-ttu-id="38f32-148">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-148">Path</span></span>                        | <span data-ttu-id="38f32-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38f32-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="38f32-150">1</span><span class="sxs-lookup"><span data-stu-id="38f32-150">1</span></span>     | <span data-ttu-id="38f32-151">/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="38f32-152">ascii</span><span class="sxs-lookup"><span data-stu-id="38f32-152">ascii</span></span>       |
| <span data-ttu-id="38f32-153">2</span><span class="sxs-lookup"><span data-stu-id="38f32-153">2</span></span>     | <span data-ttu-id="38f32-154">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="38f32-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="38f32-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="38f32-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-156">Write Paths</span></span>



| <span data-ttu-id="38f32-157">單</span><span class="sxs-lookup"><span data-stu-id="38f32-157">Order</span></span> | <span data-ttu-id="38f32-158">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-158">Path</span></span>                        | <span data-ttu-id="38f32-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="38f32-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="38f32-160">1</span><span class="sxs-lookup"><span data-stu-id="38f32-160">1</span></span>     | <span data-ttu-id="38f32-161">/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="38f32-162">ascii</span><span class="sxs-lookup"><span data-stu-id="38f32-162">ascii</span></span>       |
| <span data-ttu-id="38f32-163">2</span><span class="sxs-lookup"><span data-stu-id="38f32-163">2</span></span>     | <span data-ttu-id="38f32-164">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="38f32-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="38f32-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="38f32-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-166">Remove Paths</span></span>



| <span data-ttu-id="38f32-167">單</span><span class="sxs-lookup"><span data-stu-id="38f32-167">Order</span></span> | <span data-ttu-id="38f32-168">路徑</span><span class="sxs-lookup"><span data-stu-id="38f32-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="38f32-169">1</span><span class="sxs-lookup"><span data-stu-id="38f32-169">1</span></span>     | <span data-ttu-id="38f32-170">/ifd/gps/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="38f32-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="38f32-171">2</span><span class="sxs-lookup"><span data-stu-id="38f32-171">2</span></span>     | <span data-ttu-id="38f32-172">/ifd/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="38f32-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38f32-173">備註</span><span class="sxs-lookup"><span data-stu-id="38f32-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="38f32-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="38f32-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f32-175">系統 GPS</span><span class="sxs-lookup"><span data-stu-id="38f32-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
