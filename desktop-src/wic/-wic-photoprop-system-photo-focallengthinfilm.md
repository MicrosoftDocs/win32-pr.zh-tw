---
description: FocalLengthInFilm 屬性的相片中繼資料原則。
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: FocalLengthInFilm 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469437"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="65d50-103">FocalLengthInFilm 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="65d50-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="65d50-104">[FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="65d50-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="65d50-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="65d50-105">PKEY</span></span>

<span data-ttu-id="65d50-106">PKEY \_ FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="65d50-107">容器</span><span class="sxs-lookup"><span data-stu-id="65d50-107">Containers</span></span>

<span data-ttu-id="65d50-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="65d50-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="65d50-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="65d50-109">Read-Only</span></span>

<span data-ttu-id="65d50-110">No</span><span class="sxs-lookup"><span data-stu-id="65d50-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="65d50-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="65d50-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="65d50-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="65d50-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="65d50-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="65d50-113">Input Type</span></span>

<span data-ttu-id="65d50-114">UShort</span><span class="sxs-lookup"><span data-stu-id="65d50-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="65d50-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="65d50-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="65d50-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="65d50-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="65d50-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="65d50-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="65d50-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-118">Read Paths</span></span>



| <span data-ttu-id="65d50-119">單</span><span class="sxs-lookup"><span data-stu-id="65d50-119">Order</span></span> | <span data-ttu-id="65d50-120">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-120">Path</span></span>                            | <span data-ttu-id="65d50-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="65d50-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="65d50-122">1</span><span class="sxs-lookup"><span data-stu-id="65d50-122">1</span></span>     | <span data-ttu-id="65d50-123">/app1/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="65d50-124">ushort</span><span class="sxs-lookup"><span data-stu-id="65d50-124">ushort</span></span>      |
| <span data-ttu-id="65d50-125">2</span><span class="sxs-lookup"><span data-stu-id="65d50-125">2</span></span>     | <span data-ttu-id="65d50-126">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="65d50-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="65d50-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="65d50-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-128">Write Paths</span></span>



| <span data-ttu-id="65d50-129">單</span><span class="sxs-lookup"><span data-stu-id="65d50-129">Order</span></span> | <span data-ttu-id="65d50-130">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-130">Path</span></span>                            | <span data-ttu-id="65d50-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="65d50-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="65d50-132">1</span><span class="sxs-lookup"><span data-stu-id="65d50-132">1</span></span>     | <span data-ttu-id="65d50-133">/app1/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="65d50-134">ushort</span><span class="sxs-lookup"><span data-stu-id="65d50-134">ushort</span></span>      |
| <span data-ttu-id="65d50-135">2</span><span class="sxs-lookup"><span data-stu-id="65d50-135">2</span></span>     | <span data-ttu-id="65d50-136">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="65d50-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="65d50-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="65d50-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-138">Remove Paths</span></span>



| <span data-ttu-id="65d50-139">單</span><span class="sxs-lookup"><span data-stu-id="65d50-139">Order</span></span> | <span data-ttu-id="65d50-140">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="65d50-141">1</span><span class="sxs-lookup"><span data-stu-id="65d50-141">1</span></span>     | <span data-ttu-id="65d50-142">/app1/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="65d50-143">2</span><span class="sxs-lookup"><span data-stu-id="65d50-143">2</span></span>     | <span data-ttu-id="65d50-144">/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="65d50-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="65d50-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="65d50-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="65d50-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-146">Read Paths</span></span>



| <span data-ttu-id="65d50-147">單</span><span class="sxs-lookup"><span data-stu-id="65d50-147">Order</span></span> | <span data-ttu-id="65d50-148">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-148">Path</span></span>                                | <span data-ttu-id="65d50-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="65d50-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="65d50-150">1</span><span class="sxs-lookup"><span data-stu-id="65d50-150">1</span></span>     | <span data-ttu-id="65d50-151">/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="65d50-152">ushort</span><span class="sxs-lookup"><span data-stu-id="65d50-152">ushort</span></span>      |
| <span data-ttu-id="65d50-153">2</span><span class="sxs-lookup"><span data-stu-id="65d50-153">2</span></span>     | <span data-ttu-id="65d50-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="65d50-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="65d50-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="65d50-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-156">Write Paths</span></span>



| <span data-ttu-id="65d50-157">單</span><span class="sxs-lookup"><span data-stu-id="65d50-157">Order</span></span> | <span data-ttu-id="65d50-158">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-158">Path</span></span>                                | <span data-ttu-id="65d50-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="65d50-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="65d50-160">1</span><span class="sxs-lookup"><span data-stu-id="65d50-160">1</span></span>     | <span data-ttu-id="65d50-161">/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="65d50-162">ushort</span><span class="sxs-lookup"><span data-stu-id="65d50-162">ushort</span></span>      |
| <span data-ttu-id="65d50-163">2</span><span class="sxs-lookup"><span data-stu-id="65d50-163">2</span></span>     | <span data-ttu-id="65d50-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="65d50-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="65d50-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="65d50-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-166">Remove Paths</span></span>



| <span data-ttu-id="65d50-167">單</span><span class="sxs-lookup"><span data-stu-id="65d50-167">Order</span></span> | <span data-ttu-id="65d50-168">路徑</span><span class="sxs-lookup"><span data-stu-id="65d50-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="65d50-169">1</span><span class="sxs-lookup"><span data-stu-id="65d50-169">1</span></span>     | <span data-ttu-id="65d50-170">/ifd/exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="65d50-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="65d50-171">2</span><span class="sxs-lookup"><span data-stu-id="65d50-171">2</span></span>     | <span data-ttu-id="65d50-172">/ifd/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="65d50-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="65d50-173">備註</span><span class="sxs-lookup"><span data-stu-id="65d50-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="65d50-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="65d50-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d50-175">FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="65d50-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
