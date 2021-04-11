---
description: MeasureMode 屬性的相片中繼資料原則。
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: MeasureMode 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944379"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="ea40a-103">MeasureMode 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="ea40a-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="ea40a-104">[MeasureMode](../properties/props-system-gps-measuremode.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="ea40a-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ea40a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ea40a-105">PKEY</span></span>

<span data-ttu-id="ea40a-106">PKEY \_ GPS \_ MeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="ea40a-107">容器</span><span class="sxs-lookup"><span data-stu-id="ea40a-107">Containers</span></span>

<span data-ttu-id="ea40a-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="ea40a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ea40a-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="ea40a-109">Read-Only</span></span>

<span data-ttu-id="ea40a-110">No</span><span class="sxs-lookup"><span data-stu-id="ea40a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ea40a-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ea40a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ea40a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ea40a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="ea40a-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ea40a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="ea40a-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="ea40a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ea40a-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="ea40a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ea40a-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="ea40a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="ea40a-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="ea40a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ea40a-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-118">Read Paths</span></span>



| <span data-ttu-id="ea40a-119">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-119">Order</span></span> | <span data-ttu-id="ea40a-120">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-120">Path</span></span>                      | <span data-ttu-id="ea40a-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ea40a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ea40a-122">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-122">1</span></span>     | <span data-ttu-id="ea40a-123">/app1/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="ea40a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="ea40a-124">ascii</span></span>       |
| <span data-ttu-id="ea40a-125">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-125">2</span></span>     | <span data-ttu-id="ea40a-126">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="ea40a-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="ea40a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ea40a-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-128">Write Paths</span></span>



| <span data-ttu-id="ea40a-129">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-129">Order</span></span> | <span data-ttu-id="ea40a-130">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-130">Path</span></span>                      | <span data-ttu-id="ea40a-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ea40a-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ea40a-132">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-132">1</span></span>     | <span data-ttu-id="ea40a-133">/app1/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="ea40a-134">ascii</span><span class="sxs-lookup"><span data-stu-id="ea40a-134">ascii</span></span>       |
| <span data-ttu-id="ea40a-135">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-135">2</span></span>     | <span data-ttu-id="ea40a-136">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="ea40a-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="ea40a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ea40a-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-138">Remove Paths</span></span>



| <span data-ttu-id="ea40a-139">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-139">Order</span></span> | <span data-ttu-id="ea40a-140">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ea40a-141">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-141">1</span></span>     | <span data-ttu-id="ea40a-142">/app1/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="ea40a-143">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-143">2</span></span>     | <span data-ttu-id="ea40a-144">/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="ea40a-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="ea40a-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="ea40a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ea40a-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-146">Read Paths</span></span>



| <span data-ttu-id="ea40a-147">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-147">Order</span></span> | <span data-ttu-id="ea40a-148">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-148">Path</span></span>                         | <span data-ttu-id="ea40a-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ea40a-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ea40a-150">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-150">1</span></span>     | <span data-ttu-id="ea40a-151">/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="ea40a-152">ascii</span><span class="sxs-lookup"><span data-stu-id="ea40a-152">ascii</span></span>       |
| <span data-ttu-id="ea40a-153">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-153">2</span></span>     | <span data-ttu-id="ea40a-154">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="ea40a-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="ea40a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ea40a-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-156">Write Paths</span></span>



| <span data-ttu-id="ea40a-157">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-157">Order</span></span> | <span data-ttu-id="ea40a-158">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-158">Path</span></span>                         | <span data-ttu-id="ea40a-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ea40a-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ea40a-160">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-160">1</span></span>     | <span data-ttu-id="ea40a-161">/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="ea40a-162">ascii</span><span class="sxs-lookup"><span data-stu-id="ea40a-162">ascii</span></span>       |
| <span data-ttu-id="ea40a-163">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-163">2</span></span>     | <span data-ttu-id="ea40a-164">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="ea40a-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="ea40a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ea40a-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-166">Remove Paths</span></span>



| <span data-ttu-id="ea40a-167">單</span><span class="sxs-lookup"><span data-stu-id="ea40a-167">Order</span></span> | <span data-ttu-id="ea40a-168">路徑</span><span class="sxs-lookup"><span data-stu-id="ea40a-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="ea40a-169">1</span><span class="sxs-lookup"><span data-stu-id="ea40a-169">1</span></span>     | <span data-ttu-id="ea40a-170">/ifd/gps/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ea40a-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="ea40a-171">2</span><span class="sxs-lookup"><span data-stu-id="ea40a-171">2</span></span>     | <span data-ttu-id="ea40a-172">/ifd/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="ea40a-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ea40a-173">備註</span><span class="sxs-lookup"><span data-stu-id="ea40a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea40a-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea40a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea40a-175">MeasureMode</span><span class="sxs-lookup"><span data-stu-id="ea40a-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
