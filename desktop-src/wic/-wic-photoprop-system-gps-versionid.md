---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: System.servicemodel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983523"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="c4b2c-103">System.servicemodel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="c4b2c-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="c4b2c-104">System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-gps-versionid.md)</span><span class="sxs-lookup"><span data-stu-id="c4b2c-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c4b2c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c4b2c-105">PKEY</span></span>

<span data-ttu-id="c4b2c-106">PKEY \_ GPS \_ VersionID</span><span class="sxs-lookup"><span data-stu-id="c4b2c-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="c4b2c-107">容器</span><span class="sxs-lookup"><span data-stu-id="c4b2c-107">Containers</span></span>

<span data-ttu-id="c4b2c-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="c4b2c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c4b2c-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="c4b2c-109">Read-Only</span></span>

<span data-ttu-id="c4b2c-110">No</span><span class="sxs-lookup"><span data-stu-id="c4b2c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c4b2c-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="c4b2c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c4b2c-112">VT \_ 向量 \| VT \_ UI</span><span class="sxs-lookup"><span data-stu-id="c4b2c-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="c4b2c-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="c4b2c-113">Input Type</span></span>

<span data-ttu-id="c4b2c-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="c4b2c-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c4b2c-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="c4b2c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c4b2c-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="c4b2c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c4b2c-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="c4b2c-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c4b2c-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-118">Read Paths</span></span>



| <span data-ttu-id="c4b2c-119">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-119">Order</span></span> | <span data-ttu-id="c4b2c-120">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-120">Path</span></span>                     | <span data-ttu-id="c4b2c-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c4b2c-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c4b2c-122">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-122">1</span></span>     | <span data-ttu-id="c4b2c-123">/app1/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="c4b2c-124">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-124">2</span></span>     | <span data-ttu-id="c4b2c-125">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="c4b2c-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="c4b2c-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="c4b2c-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c4b2c-127">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-127">Write Paths</span></span>



| <span data-ttu-id="c4b2c-128">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-128">Order</span></span> | <span data-ttu-id="c4b2c-129">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-129">Path</span></span>                     | <span data-ttu-id="c4b2c-130">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c4b2c-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c4b2c-131">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-131">1</span></span>     | <span data-ttu-id="c4b2c-132">/app1/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="c4b2c-133">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-133">2</span></span>     | <span data-ttu-id="c4b2c-134">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="c4b2c-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="c4b2c-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="c4b2c-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c4b2c-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-136">Remove Paths</span></span>



| <span data-ttu-id="c4b2c-137">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-137">Order</span></span> | <span data-ttu-id="c4b2c-138">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c4b2c-139">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-139">1</span></span>     | <span data-ttu-id="c4b2c-140">/app1/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="c4b2c-141">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-141">2</span></span>     | <span data-ttu-id="c4b2c-142">/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="c4b2c-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="c4b2c-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="c4b2c-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c4b2c-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-144">Read Paths</span></span>



| <span data-ttu-id="c4b2c-145">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-145">Order</span></span> | <span data-ttu-id="c4b2c-146">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-146">Path</span></span>                       | <span data-ttu-id="c4b2c-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c4b2c-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c4b2c-148">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-148">1</span></span>     | <span data-ttu-id="c4b2c-149">/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="c4b2c-150">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-150">2</span></span>     | <span data-ttu-id="c4b2c-151">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="c4b2c-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="c4b2c-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="c4b2c-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c4b2c-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-153">Write Paths</span></span>



| <span data-ttu-id="c4b2c-154">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-154">Order</span></span> | <span data-ttu-id="c4b2c-155">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-155">Path</span></span>                       | <span data-ttu-id="c4b2c-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c4b2c-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c4b2c-157">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-157">1</span></span>     | <span data-ttu-id="c4b2c-158">/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="c4b2c-159">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-159">2</span></span>     | <span data-ttu-id="c4b2c-160">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="c4b2c-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="c4b2c-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="c4b2c-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c4b2c-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-162">Remove Paths</span></span>



| <span data-ttu-id="c4b2c-163">單</span><span class="sxs-lookup"><span data-stu-id="c4b2c-163">Order</span></span> | <span data-ttu-id="c4b2c-164">路徑</span><span class="sxs-lookup"><span data-stu-id="c4b2c-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="c4b2c-165">1</span><span class="sxs-lookup"><span data-stu-id="c4b2c-165">1</span></span>     | <span data-ttu-id="c4b2c-166">/ifd/gps/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="c4b2c-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="c4b2c-167">2</span><span class="sxs-lookup"><span data-stu-id="c4b2c-167">2</span></span>     | <span data-ttu-id="c4b2c-168">/ifd/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="c4b2c-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c4b2c-169">備註</span><span class="sxs-lookup"><span data-stu-id="c4b2c-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4b2c-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4b2c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b2c-171">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="c4b2c-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
