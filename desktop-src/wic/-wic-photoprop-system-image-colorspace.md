---
description: ColorSpace 屬性的相片中繼資料原則。
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: ColorSpace 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979181"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="f2e9f-103">ColorSpace 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f2e9f-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="f2e9f-104">[ColorSpace](../properties/props-system-image-colorspace.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f2e9f-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f2e9f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f2e9f-105">PKEY</span></span>

<span data-ttu-id="f2e9f-106">PKEY \_ 影像 \_ ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="f2e9f-107">容器</span><span class="sxs-lookup"><span data-stu-id="f2e9f-107">Containers</span></span>

<span data-ttu-id="f2e9f-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f2e9f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f2e9f-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f2e9f-109">Read-Only</span></span>

<span data-ttu-id="f2e9f-110">Yes</span><span class="sxs-lookup"><span data-stu-id="f2e9f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f2e9f-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f2e9f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f2e9f-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="f2e9f-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="f2e9f-113">Input Type</span></span>

<span data-ttu-id="f2e9f-114">UShort</span><span class="sxs-lookup"><span data-stu-id="f2e9f-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f2e9f-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f2e9f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f2e9f-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="f2e9f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f2e9f-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="f2e9f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2e9f-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-118">Read Paths</span></span>



| <span data-ttu-id="f2e9f-119">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-119">Order</span></span> | <span data-ttu-id="f2e9f-120">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-120">Path</span></span>                          | <span data-ttu-id="f2e9f-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f2e9f-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2e9f-122">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-122">1</span></span>     | <span data-ttu-id="f2e9f-123">/app1/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="f2e9f-124">ushort</span><span class="sxs-lookup"><span data-stu-id="f2e9f-124">ushort</span></span>      |
| <span data-ttu-id="f2e9f-125">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-125">2</span></span>     | <span data-ttu-id="f2e9f-126">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="f2e9f-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2e9f-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f2e9f-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-128">Write Paths</span></span>



| <span data-ttu-id="f2e9f-129">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-129">Order</span></span> | <span data-ttu-id="f2e9f-130">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-130">Path</span></span>                          | <span data-ttu-id="f2e9f-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f2e9f-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2e9f-132">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-132">1</span></span>     | <span data-ttu-id="f2e9f-133">/app1/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="f2e9f-134">ushort</span><span class="sxs-lookup"><span data-stu-id="f2e9f-134">ushort</span></span>      |
| <span data-ttu-id="f2e9f-135">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-135">2</span></span>     | <span data-ttu-id="f2e9f-136">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="f2e9f-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2e9f-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f2e9f-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-138">Remove Paths</span></span>



| <span data-ttu-id="f2e9f-139">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-139">Order</span></span> | <span data-ttu-id="f2e9f-140">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f2e9f-141">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-141">1</span></span>     | <span data-ttu-id="f2e9f-142">/app1/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="f2e9f-143">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-143">2</span></span>     | <span data-ttu-id="f2e9f-144">/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="f2e9f-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="f2e9f-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2e9f-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-146">Read Paths</span></span>



| <span data-ttu-id="f2e9f-147">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-147">Order</span></span> | <span data-ttu-id="f2e9f-148">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-148">Path</span></span>                     | <span data-ttu-id="f2e9f-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f2e9f-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2e9f-150">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-150">1</span></span>     | <span data-ttu-id="f2e9f-151">/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="f2e9f-152">ushort</span><span class="sxs-lookup"><span data-stu-id="f2e9f-152">ushort</span></span>      |
| <span data-ttu-id="f2e9f-153">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-153">2</span></span>     | <span data-ttu-id="f2e9f-154">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="f2e9f-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2e9f-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f2e9f-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-156">Write Paths</span></span>



| <span data-ttu-id="f2e9f-157">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-157">Order</span></span> | <span data-ttu-id="f2e9f-158">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-158">Path</span></span>                     | <span data-ttu-id="f2e9f-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f2e9f-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2e9f-160">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-160">1</span></span>     | <span data-ttu-id="f2e9f-161">/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="f2e9f-162">ushort</span><span class="sxs-lookup"><span data-stu-id="f2e9f-162">ushort</span></span>      |
| <span data-ttu-id="f2e9f-163">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-163">2</span></span>     | <span data-ttu-id="f2e9f-164">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="f2e9f-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2e9f-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f2e9f-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-166">Remove Paths</span></span>



| <span data-ttu-id="f2e9f-167">單</span><span class="sxs-lookup"><span data-stu-id="f2e9f-167">Order</span></span> | <span data-ttu-id="f2e9f-168">路徑</span><span class="sxs-lookup"><span data-stu-id="f2e9f-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="f2e9f-169">1</span><span class="sxs-lookup"><span data-stu-id="f2e9f-169">1</span></span>     | <span data-ttu-id="f2e9f-170">/ifd/exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="f2e9f-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="f2e9f-171">2</span><span class="sxs-lookup"><span data-stu-id="f2e9f-171">2</span></span>     | <span data-ttu-id="f2e9f-172">/ifd/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f2e9f-173">備註</span><span class="sxs-lookup"><span data-stu-id="f2e9f-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2e9f-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2e9f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e9f-175">ColorSpace</span><span class="sxs-lookup"><span data-stu-id="f2e9f-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
