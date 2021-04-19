---
description: WhiteBalance 屬性的相片中繼資料原則。
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: WhiteBalance 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001738"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="f70b5-103">WhiteBalance 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f70b5-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="f70b5-104">[WhiteBalance](../properties/props-system-photo-whitebalance.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f70b5-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f70b5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f70b5-105">PKEY</span></span>

<span data-ttu-id="f70b5-106">PKEY \_ 相片 \_ WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="f70b5-107">容器</span><span class="sxs-lookup"><span data-stu-id="f70b5-107">Containers</span></span>

<span data-ttu-id="f70b5-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f70b5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f70b5-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f70b5-109">Read-Only</span></span>

<span data-ttu-id="f70b5-110">No</span><span class="sxs-lookup"><span data-stu-id="f70b5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f70b5-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f70b5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f70b5-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f70b5-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="f70b5-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="f70b5-113">Input Type</span></span>

<span data-ttu-id="f70b5-114">UShort</span><span class="sxs-lookup"><span data-stu-id="f70b5-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f70b5-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f70b5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f70b5-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="f70b5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f70b5-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="f70b5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f70b5-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-118">Read Paths</span></span>



| <span data-ttu-id="f70b5-119">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-119">Order</span></span> | <span data-ttu-id="f70b5-120">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-120">Path</span></span>                          | <span data-ttu-id="f70b5-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f70b5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f70b5-122">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-122">1</span></span>     | <span data-ttu-id="f70b5-123">/app1/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="f70b5-124">ushort</span><span class="sxs-lookup"><span data-stu-id="f70b5-124">ushort</span></span>      |
| <span data-ttu-id="f70b5-125">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-125">2</span></span>     | <span data-ttu-id="f70b5-126">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="f70b5-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f70b5-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f70b5-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-128">Write Paths</span></span>



| <span data-ttu-id="f70b5-129">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-129">Order</span></span> | <span data-ttu-id="f70b5-130">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-130">Path</span></span>                          | <span data-ttu-id="f70b5-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f70b5-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f70b5-132">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-132">1</span></span>     | <span data-ttu-id="f70b5-133">/app1/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="f70b5-134">ushort</span><span class="sxs-lookup"><span data-stu-id="f70b5-134">ushort</span></span>      |
| <span data-ttu-id="f70b5-135">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-135">2</span></span>     | <span data-ttu-id="f70b5-136">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="f70b5-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f70b5-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f70b5-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-138">Remove Paths</span></span>



| <span data-ttu-id="f70b5-139">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-139">Order</span></span> | <span data-ttu-id="f70b5-140">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f70b5-141">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-141">1</span></span>     | <span data-ttu-id="f70b5-142">/app1/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="f70b5-143">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-143">2</span></span>     | <span data-ttu-id="f70b5-144">/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="f70b5-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="f70b5-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f70b5-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-146">Read Paths</span></span>



| <span data-ttu-id="f70b5-147">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-147">Order</span></span> | <span data-ttu-id="f70b5-148">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-148">Path</span></span>                       | <span data-ttu-id="f70b5-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f70b5-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="f70b5-150">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-150">1</span></span>     | <span data-ttu-id="f70b5-151">/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="f70b5-152">ushort</span><span class="sxs-lookup"><span data-stu-id="f70b5-152">ushort</span></span>      |
| <span data-ttu-id="f70b5-153">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-153">2</span></span>     | <span data-ttu-id="f70b5-154">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="f70b5-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="f70b5-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f70b5-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-156">Write Paths</span></span>



| <span data-ttu-id="f70b5-157">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-157">Order</span></span> | <span data-ttu-id="f70b5-158">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-158">Path</span></span>                       | <span data-ttu-id="f70b5-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f70b5-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="f70b5-160">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-160">1</span></span>     | <span data-ttu-id="f70b5-161">/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="f70b5-162">ushort</span><span class="sxs-lookup"><span data-stu-id="f70b5-162">ushort</span></span>      |
| <span data-ttu-id="f70b5-163">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-163">2</span></span>     | <span data-ttu-id="f70b5-164">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="f70b5-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="f70b5-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f70b5-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-166">Remove Paths</span></span>



| <span data-ttu-id="f70b5-167">單</span><span class="sxs-lookup"><span data-stu-id="f70b5-167">Order</span></span> | <span data-ttu-id="f70b5-168">路徑</span><span class="sxs-lookup"><span data-stu-id="f70b5-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="f70b5-169">1</span><span class="sxs-lookup"><span data-stu-id="f70b5-169">1</span></span>     | <span data-ttu-id="f70b5-170">/ifd/exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="f70b5-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="f70b5-171">2</span><span class="sxs-lookup"><span data-stu-id="f70b5-171">2</span></span>     | <span data-ttu-id="f70b5-172">/ifd/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f70b5-173">備註</span><span class="sxs-lookup"><span data-stu-id="f70b5-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f70b5-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="f70b5-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f70b5-175">WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="f70b5-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
