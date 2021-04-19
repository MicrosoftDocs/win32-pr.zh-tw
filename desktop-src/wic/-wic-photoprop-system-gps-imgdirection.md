---
description: ImgDirection 屬性的相片中繼資料原則。
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: ImgDirection 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975903"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="4732f-103">ImgDirection 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="4732f-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="4732f-104">[ImgDirection](../properties/props-system-gps-imgdirection.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="4732f-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4732f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4732f-105">PKEY</span></span>

<span data-ttu-id="4732f-106">PKEY \_ GPS \_ ImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="4732f-107">容器</span><span class="sxs-lookup"><span data-stu-id="4732f-107">Containers</span></span>

<span data-ttu-id="4732f-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="4732f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4732f-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="4732f-109">Read-Only</span></span>

<span data-ttu-id="4732f-110">Yes</span><span class="sxs-lookup"><span data-stu-id="4732f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4732f-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="4732f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4732f-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4732f-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4732f-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="4732f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="4732f-114">您可以藉由寫入 ImgDirectionNumerator 和 ImgDirectionDenominator 來寫入這個值。</span><span class="sxs-lookup"><span data-stu-id="4732f-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="4732f-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="4732f-115">It cannot be written directly.</span></span> <span data-ttu-id="4732f-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="4732f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4732f-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="4732f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4732f-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-118">Read Paths</span></span>



| <span data-ttu-id="4732f-119">單</span><span class="sxs-lookup"><span data-stu-id="4732f-119">Order</span></span> | <span data-ttu-id="4732f-120">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-120">Path</span></span>                      | <span data-ttu-id="4732f-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4732f-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4732f-122">1</span><span class="sxs-lookup"><span data-stu-id="4732f-122">1</span></span>     | <span data-ttu-id="4732f-123">/app1/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="4732f-124">2</span><span class="sxs-lookup"><span data-stu-id="4732f-124">2</span></span>     | <span data-ttu-id="4732f-125">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4732f-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-126">Write Paths</span></span>



| <span data-ttu-id="4732f-127">單</span><span class="sxs-lookup"><span data-stu-id="4732f-127">Order</span></span> | <span data-ttu-id="4732f-128">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-128">Path</span></span>                      | <span data-ttu-id="4732f-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4732f-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4732f-130">1</span><span class="sxs-lookup"><span data-stu-id="4732f-130">1</span></span>     | <span data-ttu-id="4732f-131">/app1/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="4732f-132">2</span><span class="sxs-lookup"><span data-stu-id="4732f-132">2</span></span>     | <span data-ttu-id="4732f-133">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4732f-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-134">Remove Paths</span></span>



| <span data-ttu-id="4732f-135">單</span><span class="sxs-lookup"><span data-stu-id="4732f-135">Order</span></span> | <span data-ttu-id="4732f-136">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4732f-137">1</span><span class="sxs-lookup"><span data-stu-id="4732f-137">1</span></span>     | <span data-ttu-id="4732f-138">/app1/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="4732f-139">2</span><span class="sxs-lookup"><span data-stu-id="4732f-139">2</span></span>     | <span data-ttu-id="4732f-140">/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="4732f-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="4732f-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="4732f-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4732f-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-142">Read Paths</span></span>



| <span data-ttu-id="4732f-143">單</span><span class="sxs-lookup"><span data-stu-id="4732f-143">Order</span></span> | <span data-ttu-id="4732f-144">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-144">Path</span></span>                          | <span data-ttu-id="4732f-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4732f-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4732f-146">1</span><span class="sxs-lookup"><span data-stu-id="4732f-146">1</span></span>     | <span data-ttu-id="4732f-147">/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="4732f-148">2</span><span class="sxs-lookup"><span data-stu-id="4732f-148">2</span></span>     | <span data-ttu-id="4732f-149">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4732f-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-150">Write Paths</span></span>



| <span data-ttu-id="4732f-151">單</span><span class="sxs-lookup"><span data-stu-id="4732f-151">Order</span></span> | <span data-ttu-id="4732f-152">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-152">Path</span></span>                          | <span data-ttu-id="4732f-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4732f-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4732f-154">1</span><span class="sxs-lookup"><span data-stu-id="4732f-154">1</span></span>     | <span data-ttu-id="4732f-155">/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="4732f-156">2</span><span class="sxs-lookup"><span data-stu-id="4732f-156">2</span></span>     | <span data-ttu-id="4732f-157">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4732f-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-158">Remove Paths</span></span>



| <span data-ttu-id="4732f-159">單</span><span class="sxs-lookup"><span data-stu-id="4732f-159">Order</span></span> | <span data-ttu-id="4732f-160">路徑</span><span class="sxs-lookup"><span data-stu-id="4732f-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="4732f-161">1</span><span class="sxs-lookup"><span data-stu-id="4732f-161">1</span></span>     | <span data-ttu-id="4732f-162">/ifd/gps/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="4732f-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="4732f-163">2</span><span class="sxs-lookup"><span data-stu-id="4732f-163">2</span></span>     | <span data-ttu-id="4732f-164">/ifd/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="4732f-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4732f-165">備註</span><span class="sxs-lookup"><span data-stu-id="4732f-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4732f-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="4732f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4732f-167">ImgDirection</span><span class="sxs-lookup"><span data-stu-id="4732f-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
