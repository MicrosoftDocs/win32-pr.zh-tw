---
description: DestDistance 屬性的相片中繼資料原則。
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: DestDistance 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983719"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="bb154-103">DestDistance 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="bb154-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="bb154-104">[DestDistance](../properties/props-system-gps-destdistance.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="bb154-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bb154-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bb154-105">PKEY</span></span>

<span data-ttu-id="bb154-106">PKEY \_ GPS \_ DestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="bb154-107">容器</span><span class="sxs-lookup"><span data-stu-id="bb154-107">Containers</span></span>

<span data-ttu-id="bb154-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="bb154-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bb154-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-109">Read-Only</span></span>

<span data-ttu-id="bb154-110">Yes</span><span class="sxs-lookup"><span data-stu-id="bb154-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bb154-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="bb154-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bb154-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="bb154-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bb154-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="bb154-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bb154-114">這個值是從 DestDistanceNumerator 和 DestDistanceDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="bb154-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="bb154-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="bb154-115">It cannot be written directly.</span></span> <span data-ttu-id="bb154-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="bb154-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bb154-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="bb154-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bb154-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-118">Read Paths</span></span>



| <span data-ttu-id="bb154-119">單</span><span class="sxs-lookup"><span data-stu-id="bb154-119">Order</span></span> | <span data-ttu-id="bb154-120">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-120">Path</span></span>                      | <span data-ttu-id="bb154-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bb154-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="bb154-122">1</span><span class="sxs-lookup"><span data-stu-id="bb154-122">1</span></span>     | <span data-ttu-id="bb154-123">/app1/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="bb154-124">2</span><span class="sxs-lookup"><span data-stu-id="bb154-124">2</span></span>     | <span data-ttu-id="bb154-125">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bb154-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-126">Write Paths</span></span>



| <span data-ttu-id="bb154-127">單</span><span class="sxs-lookup"><span data-stu-id="bb154-127">Order</span></span> | <span data-ttu-id="bb154-128">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-128">Path</span></span>                      | <span data-ttu-id="bb154-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bb154-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="bb154-130">1</span><span class="sxs-lookup"><span data-stu-id="bb154-130">1</span></span>     | <span data-ttu-id="bb154-131">/app1/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="bb154-132">2</span><span class="sxs-lookup"><span data-stu-id="bb154-132">2</span></span>     | <span data-ttu-id="bb154-133">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bb154-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-134">Remove Paths</span></span>



| <span data-ttu-id="bb154-135">單</span><span class="sxs-lookup"><span data-stu-id="bb154-135">Order</span></span> | <span data-ttu-id="bb154-136">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="bb154-137">1</span><span class="sxs-lookup"><span data-stu-id="bb154-137">1</span></span>     | <span data-ttu-id="bb154-138">/app1/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="bb154-139">2</span><span class="sxs-lookup"><span data-stu-id="bb154-139">2</span></span>     | <span data-ttu-id="bb154-140">/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="bb154-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="bb154-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="bb154-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bb154-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-142">Read Paths</span></span>



| <span data-ttu-id="bb154-143">單</span><span class="sxs-lookup"><span data-stu-id="bb154-143">Order</span></span> | <span data-ttu-id="bb154-144">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-144">Path</span></span>                          | <span data-ttu-id="bb154-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bb154-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb154-146">1</span><span class="sxs-lookup"><span data-stu-id="bb154-146">1</span></span>     | <span data-ttu-id="bb154-147">/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="bb154-148">2</span><span class="sxs-lookup"><span data-stu-id="bb154-148">2</span></span>     | <span data-ttu-id="bb154-149">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bb154-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-150">Write Paths</span></span>



| <span data-ttu-id="bb154-151">單</span><span class="sxs-lookup"><span data-stu-id="bb154-151">Order</span></span> | <span data-ttu-id="bb154-152">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-152">Path</span></span>                          | <span data-ttu-id="bb154-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bb154-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb154-154">1</span><span class="sxs-lookup"><span data-stu-id="bb154-154">1</span></span>     | <span data-ttu-id="bb154-155">/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="bb154-156">2</span><span class="sxs-lookup"><span data-stu-id="bb154-156">2</span></span>     | <span data-ttu-id="bb154-157">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bb154-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-158">Remove Paths</span></span>



| <span data-ttu-id="bb154-159">單</span><span class="sxs-lookup"><span data-stu-id="bb154-159">Order</span></span> | <span data-ttu-id="bb154-160">路徑</span><span class="sxs-lookup"><span data-stu-id="bb154-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bb154-161">1</span><span class="sxs-lookup"><span data-stu-id="bb154-161">1</span></span>     | <span data-ttu-id="bb154-162">/ifd/gps/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="bb154-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="bb154-163">2</span><span class="sxs-lookup"><span data-stu-id="bb154-163">2</span></span>     | <span data-ttu-id="bb154-164">/ifd/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="bb154-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bb154-165">備註</span><span class="sxs-lookup"><span data-stu-id="bb154-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb154-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb154-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb154-167">DestDistance</span><span class="sxs-lookup"><span data-stu-id="bb154-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
