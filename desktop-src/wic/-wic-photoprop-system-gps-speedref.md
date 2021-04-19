---
description: SpeedRef 屬性的相片中繼資料原則。
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: SpeedRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985024"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="18954-103">SpeedRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="18954-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="18954-104">[SpeedRef](../properties/props-system-gps-speedref.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="18954-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="18954-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="18954-105">PKEY</span></span>

<span data-ttu-id="18954-106">PKEY \_ GPS \_ SpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="18954-107">容器</span><span class="sxs-lookup"><span data-stu-id="18954-107">Containers</span></span>

<span data-ttu-id="18954-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="18954-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="18954-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="18954-109">Read-Only</span></span>

<span data-ttu-id="18954-110">No</span><span class="sxs-lookup"><span data-stu-id="18954-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="18954-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="18954-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="18954-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="18954-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="18954-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="18954-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="18954-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="18954-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="18954-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="18954-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="18954-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="18954-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="18954-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="18954-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="18954-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="18954-118">Read Paths</span></span>



| <span data-ttu-id="18954-119">單</span><span class="sxs-lookup"><span data-stu-id="18954-119">Order</span></span> | <span data-ttu-id="18954-120">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-120">Path</span></span>                      | <span data-ttu-id="18954-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="18954-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="18954-122">1</span><span class="sxs-lookup"><span data-stu-id="18954-122">1</span></span>     | <span data-ttu-id="18954-123">/app1/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="18954-124">ascii</span><span class="sxs-lookup"><span data-stu-id="18954-124">ascii</span></span>       |
| <span data-ttu-id="18954-125">2</span><span class="sxs-lookup"><span data-stu-id="18954-125">2</span></span>     | <span data-ttu-id="18954-126">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="18954-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="18954-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="18954-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="18954-128">Write Paths</span></span>



| <span data-ttu-id="18954-129">單</span><span class="sxs-lookup"><span data-stu-id="18954-129">Order</span></span> | <span data-ttu-id="18954-130">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-130">Path</span></span>                      | <span data-ttu-id="18954-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="18954-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="18954-132">1</span><span class="sxs-lookup"><span data-stu-id="18954-132">1</span></span>     | <span data-ttu-id="18954-133">/app1/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="18954-134">ascii</span><span class="sxs-lookup"><span data-stu-id="18954-134">ascii</span></span>       |
| <span data-ttu-id="18954-135">2</span><span class="sxs-lookup"><span data-stu-id="18954-135">2</span></span>     | <span data-ttu-id="18954-136">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="18954-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="18954-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="18954-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="18954-138">Remove Paths</span></span>



| <span data-ttu-id="18954-139">單</span><span class="sxs-lookup"><span data-stu-id="18954-139">Order</span></span> | <span data-ttu-id="18954-140">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-140">Path</span></span>                      | <span data-ttu-id="18954-141">磁碟格式</span><span class="sxs-lookup"><span data-stu-id="18954-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="18954-142">1</span><span class="sxs-lookup"><span data-stu-id="18954-142">1</span></span>     | <span data-ttu-id="18954-143">/app1/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="18954-144">2</span><span class="sxs-lookup"><span data-stu-id="18954-144">2</span></span>     | <span data-ttu-id="18954-145">/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="18954-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="18954-146">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="18954-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="18954-147">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="18954-147">Read Paths</span></span>



| <span data-ttu-id="18954-148">單</span><span class="sxs-lookup"><span data-stu-id="18954-148">Order</span></span> | <span data-ttu-id="18954-149">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="18954-150">1</span><span class="sxs-lookup"><span data-stu-id="18954-150">1</span></span>     | <span data-ttu-id="18954-151">/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="18954-152">ascii</span><span class="sxs-lookup"><span data-stu-id="18954-152">ascii</span></span>   |
| <span data-ttu-id="18954-153">2</span><span class="sxs-lookup"><span data-stu-id="18954-153">2</span></span>     | <span data-ttu-id="18954-154">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="18954-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="18954-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="18954-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="18954-156">Write Paths</span></span>



| <span data-ttu-id="18954-157">單</span><span class="sxs-lookup"><span data-stu-id="18954-157">Order</span></span> | <span data-ttu-id="18954-158">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-158">Path</span></span>                      | <span data-ttu-id="18954-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="18954-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="18954-160">1</span><span class="sxs-lookup"><span data-stu-id="18954-160">1</span></span>     | <span data-ttu-id="18954-161">/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="18954-162">ascii</span><span class="sxs-lookup"><span data-stu-id="18954-162">ascii</span></span>       |
| <span data-ttu-id="18954-163">2</span><span class="sxs-lookup"><span data-stu-id="18954-163">2</span></span>     | <span data-ttu-id="18954-164">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="18954-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="18954-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="18954-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="18954-166">Remove Paths</span></span>



| <span data-ttu-id="18954-167">單</span><span class="sxs-lookup"><span data-stu-id="18954-167">Order</span></span> | <span data-ttu-id="18954-168">路徑</span><span class="sxs-lookup"><span data-stu-id="18954-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="18954-169">1</span><span class="sxs-lookup"><span data-stu-id="18954-169">1</span></span>     | <span data-ttu-id="18954-170">/ifd/gps/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="18954-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="18954-171">2</span><span class="sxs-lookup"><span data-stu-id="18954-171">2</span></span>     | <span data-ttu-id="18954-172">/ifd/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="18954-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18954-173">備註</span><span class="sxs-lookup"><span data-stu-id="18954-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="18954-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="18954-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18954-175">SpeedRef</span><span class="sxs-lookup"><span data-stu-id="18954-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
