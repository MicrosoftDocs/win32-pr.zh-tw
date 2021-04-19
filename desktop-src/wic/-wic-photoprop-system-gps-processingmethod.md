---
description: ProcessingMethod 屬性的相片中繼資料原則。
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: ProcessingMethod 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000335"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="a4eb1-103">ProcessingMethod 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="a4eb1-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="a4eb1-104">[ProcessingMethod](../properties/props-system-gps-processingmethod.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="a4eb1-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a4eb1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a4eb1-105">PKEY</span></span>

<span data-ttu-id="a4eb1-106">PKEY \_ GPS \_ ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="a4eb1-107">容器</span><span class="sxs-lookup"><span data-stu-id="a4eb1-107">Containers</span></span>

<span data-ttu-id="a4eb1-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="a4eb1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a4eb1-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="a4eb1-109">Read-Only</span></span>

<span data-ttu-id="a4eb1-110">No</span><span class="sxs-lookup"><span data-stu-id="a4eb1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a4eb1-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a4eb1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a4eb1-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a4eb1-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="a4eb1-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a4eb1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="a4eb1-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="a4eb1-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a4eb1-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="a4eb1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a4eb1-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="a4eb1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="a4eb1-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="a4eb1-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4eb1-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-118">Read Paths</span></span>



| <span data-ttu-id="a4eb1-119">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-119">Order</span></span> | <span data-ttu-id="a4eb1-120">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-120">Path</span></span>                          | <span data-ttu-id="a4eb1-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a4eb1-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a4eb1-122">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-122">1</span></span>     | <span data-ttu-id="a4eb1-123">/app1/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="a4eb1-124">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-124">2</span></span>     | <span data-ttu-id="a4eb1-125">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="a4eb1-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4eb1-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a4eb1-127">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-127">Write Paths</span></span>



| <span data-ttu-id="a4eb1-128">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-128">Order</span></span> | <span data-ttu-id="a4eb1-129">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-129">Path</span></span>                          | <span data-ttu-id="a4eb1-130">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a4eb1-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a4eb1-131">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-131">1</span></span>     | <span data-ttu-id="a4eb1-132">/app1/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="a4eb1-133">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-133">2</span></span>     | <span data-ttu-id="a4eb1-134">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="a4eb1-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4eb1-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a4eb1-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-136">Remove Paths</span></span>



| <span data-ttu-id="a4eb1-137">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-137">Order</span></span> | <span data-ttu-id="a4eb1-138">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a4eb1-139">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-139">1</span></span>     | <span data-ttu-id="a4eb1-140">/app1/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="a4eb1-141">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-141">2</span></span>     | <span data-ttu-id="a4eb1-142">/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a4eb1-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="a4eb1-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4eb1-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-144">Read Paths</span></span>



| <span data-ttu-id="a4eb1-145">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-145">Order</span></span> | <span data-ttu-id="a4eb1-146">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-146">Path</span></span>                              | <span data-ttu-id="a4eb1-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a4eb1-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="a4eb1-148">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-148">1</span></span>     | <span data-ttu-id="a4eb1-149">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="a4eb1-150">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4eb1-150">unicode</span></span>     |
| <span data-ttu-id="a4eb1-151">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-151">2</span></span>     | <span data-ttu-id="a4eb1-152">/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="a4eb1-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-153">Write Paths</span></span>



| <span data-ttu-id="a4eb1-154">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-154">Order</span></span> | <span data-ttu-id="a4eb1-155">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-155">Path</span></span>                              | <span data-ttu-id="a4eb1-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a4eb1-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="a4eb1-157">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-157">1</span></span>     | <span data-ttu-id="a4eb1-158">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="a4eb1-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4eb1-159">unicode</span></span>     |
| <span data-ttu-id="a4eb1-160">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-160">2</span></span>     | <span data-ttu-id="a4eb1-161">/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a4eb1-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-162">Remove Paths</span></span>



| <span data-ttu-id="a4eb1-163">單</span><span class="sxs-lookup"><span data-stu-id="a4eb1-163">Order</span></span> | <span data-ttu-id="a4eb1-164">路徑</span><span class="sxs-lookup"><span data-stu-id="a4eb1-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="a4eb1-165">1</span><span class="sxs-lookup"><span data-stu-id="a4eb1-165">1</span></span>     | <span data-ttu-id="a4eb1-166">/ifd/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="a4eb1-167">2</span><span class="sxs-lookup"><span data-stu-id="a4eb1-167">2</span></span>     | <span data-ttu-id="a4eb1-168">/ifd/gps/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="a4eb1-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="a4eb1-169">備註</span><span class="sxs-lookup"><span data-stu-id="a4eb1-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4eb1-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4eb1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4eb1-171">ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="a4eb1-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
