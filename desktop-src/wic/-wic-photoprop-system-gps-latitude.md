---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: 系統 GPS. 緯度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985296"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="8350e-103">系統 GPS. 緯度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="8350e-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="8350e-104">適用于 [system.object](../properties/props-system-gps-latitude.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="8350e-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8350e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8350e-105">PKEY</span></span>

<span data-ttu-id="8350e-106">PKEY \_ GPS \_ 緯度</span><span class="sxs-lookup"><span data-stu-id="8350e-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="8350e-107">容器</span><span class="sxs-lookup"><span data-stu-id="8350e-107">Containers</span></span>

<span data-ttu-id="8350e-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="8350e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8350e-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="8350e-109">Read-Only</span></span>

<span data-ttu-id="8350e-110">Yes</span><span class="sxs-lookup"><span data-stu-id="8350e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8350e-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8350e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8350e-112">VT \_ 向量 \| vt \_ R8</span><span class="sxs-lookup"><span data-stu-id="8350e-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8350e-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="8350e-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="8350e-114">您可以藉由寫入 LatitudeNumerator 和 LatitudeDenominator 來寫入這個值。</span><span class="sxs-lookup"><span data-stu-id="8350e-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="8350e-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="8350e-115">It cannot be written directly.</span></span> <span data-ttu-id="8350e-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="8350e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8350e-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="8350e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8350e-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-118">Read Paths</span></span>



| <span data-ttu-id="8350e-119">單</span><span class="sxs-lookup"><span data-stu-id="8350e-119">Order</span></span> | <span data-ttu-id="8350e-120">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-120">Path</span></span>                     | <span data-ttu-id="8350e-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8350e-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8350e-122">1</span><span class="sxs-lookup"><span data-stu-id="8350e-122">1</span></span>     | <span data-ttu-id="8350e-123">/app1/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="8350e-124">2</span><span class="sxs-lookup"><span data-stu-id="8350e-124">2</span></span>     | <span data-ttu-id="8350e-125">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="8350e-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-126">Write Paths</span></span>



| <span data-ttu-id="8350e-127">單</span><span class="sxs-lookup"><span data-stu-id="8350e-127">Order</span></span> | <span data-ttu-id="8350e-128">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-128">Path</span></span>                     | <span data-ttu-id="8350e-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8350e-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8350e-130">1</span><span class="sxs-lookup"><span data-stu-id="8350e-130">1</span></span>     | <span data-ttu-id="8350e-131">/app1/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="8350e-132">2</span><span class="sxs-lookup"><span data-stu-id="8350e-132">2</span></span>     | <span data-ttu-id="8350e-133">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8350e-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-134">Remove Paths</span></span>



| <span data-ttu-id="8350e-135">單</span><span class="sxs-lookup"><span data-stu-id="8350e-135">Order</span></span> | <span data-ttu-id="8350e-136">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="8350e-137">1</span><span class="sxs-lookup"><span data-stu-id="8350e-137">1</span></span>     | <span data-ttu-id="8350e-138">/app1/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="8350e-139">2</span><span class="sxs-lookup"><span data-stu-id="8350e-139">2</span></span>     | <span data-ttu-id="8350e-140">/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="8350e-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="8350e-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8350e-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-142">Read Paths</span></span>



| <span data-ttu-id="8350e-143">單</span><span class="sxs-lookup"><span data-stu-id="8350e-143">Order</span></span> | <span data-ttu-id="8350e-144">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-144">Path</span></span>                      | <span data-ttu-id="8350e-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8350e-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8350e-146">1</span><span class="sxs-lookup"><span data-stu-id="8350e-146">1</span></span>     | <span data-ttu-id="8350e-147">/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="8350e-148">2</span><span class="sxs-lookup"><span data-stu-id="8350e-148">2</span></span>     | <span data-ttu-id="8350e-149">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8350e-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-150">Write Paths</span></span>



| <span data-ttu-id="8350e-151">單</span><span class="sxs-lookup"><span data-stu-id="8350e-151">Order</span></span> | <span data-ttu-id="8350e-152">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-152">Path</span></span>                      | <span data-ttu-id="8350e-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8350e-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8350e-154">1</span><span class="sxs-lookup"><span data-stu-id="8350e-154">1</span></span>     | <span data-ttu-id="8350e-155">/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="8350e-156">2</span><span class="sxs-lookup"><span data-stu-id="8350e-156">2</span></span>     | <span data-ttu-id="8350e-157">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8350e-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-158">Remove Paths</span></span>



| <span data-ttu-id="8350e-159">單</span><span class="sxs-lookup"><span data-stu-id="8350e-159">Order</span></span> | <span data-ttu-id="8350e-160">路徑</span><span class="sxs-lookup"><span data-stu-id="8350e-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8350e-161">1</span><span class="sxs-lookup"><span data-stu-id="8350e-161">1</span></span>     | <span data-ttu-id="8350e-162">/ifd/gps/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="8350e-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="8350e-163">2</span><span class="sxs-lookup"><span data-stu-id="8350e-163">2</span></span>     | <span data-ttu-id="8350e-164">/ifd/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="8350e-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8350e-165">備註</span><span class="sxs-lookup"><span data-stu-id="8350e-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8350e-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="8350e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8350e-167">系統 GPS</span><span class="sxs-lookup"><span data-stu-id="8350e-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
