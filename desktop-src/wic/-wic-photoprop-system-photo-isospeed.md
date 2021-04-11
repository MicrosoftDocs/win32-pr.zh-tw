---
description: ISOSpeed 屬性的相片中繼資料原則。
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: ISOSpeed 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319616"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="a00cf-103">ISOSpeed 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="a00cf-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="a00cf-104">[ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="a00cf-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a00cf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a00cf-105">PKEY</span></span>

<span data-ttu-id="a00cf-106">PKEY \_ 相片 \_ ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="a00cf-107">容器</span><span class="sxs-lookup"><span data-stu-id="a00cf-107">Containers</span></span>

<span data-ttu-id="a00cf-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="a00cf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a00cf-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="a00cf-109">Read-Only</span></span>

<span data-ttu-id="a00cf-110">No</span><span class="sxs-lookup"><span data-stu-id="a00cf-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a00cf-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a00cf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a00cf-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="a00cf-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="a00cf-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a00cf-113">Input Type</span></span>

<span data-ttu-id="a00cf-114">UShort</span><span class="sxs-lookup"><span data-stu-id="a00cf-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a00cf-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="a00cf-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a00cf-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="a00cf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a00cf-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="a00cf-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a00cf-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-118">Read Paths</span></span>



| <span data-ttu-id="a00cf-119">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-119">Order</span></span> | <span data-ttu-id="a00cf-120">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-120">Path</span></span>                                    | <span data-ttu-id="a00cf-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a00cf-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="a00cf-122">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-122">1</span></span>     | <span data-ttu-id="a00cf-123">/app1/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="a00cf-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a00cf-124">ushort</span></span>      |
| <span data-ttu-id="a00cf-125">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-125">2</span></span>     | <span data-ttu-id="a00cf-126">/xmp/ <xmpseq> exif： ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="a00cf-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="a00cf-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-127">unicode</span></span>     |
| <span data-ttu-id="a00cf-128">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-128">3</span></span>     | <span data-ttu-id="a00cf-129">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="a00cf-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a00cf-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-131">Write Paths</span></span>



| <span data-ttu-id="a00cf-132">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-132">Order</span></span> | <span data-ttu-id="a00cf-133">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-133">Path</span></span>                                    | <span data-ttu-id="a00cf-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a00cf-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="a00cf-135">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-135">1</span></span>     | <span data-ttu-id="a00cf-136">/app1/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="a00cf-137">ushort</span><span class="sxs-lookup"><span data-stu-id="a00cf-137">ushort</span></span>      |
| <span data-ttu-id="a00cf-138">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-138">2</span></span>     | <span data-ttu-id="a00cf-139">/xmp/ <xmpseq> exif： ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="a00cf-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="a00cf-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-140">unicode</span></span>     |
| <span data-ttu-id="a00cf-141">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-141">3</span></span>     | <span data-ttu-id="a00cf-142">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="a00cf-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a00cf-144">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-144">Remove Paths</span></span>



| <span data-ttu-id="a00cf-145">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-145">Order</span></span> | <span data-ttu-id="a00cf-146">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="a00cf-147">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-147">1</span></span>     | <span data-ttu-id="a00cf-148">/app1/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="a00cf-149">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-149">2</span></span>     | <span data-ttu-id="a00cf-150">/xmp/ <xmpseq> exif： isospeedratings</span><span class="sxs-lookup"><span data-stu-id="a00cf-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="a00cf-151">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-151">3</span></span>     | <span data-ttu-id="a00cf-152">/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="a00cf-153">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="a00cf-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a00cf-154">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-154">Read Paths</span></span>



| <span data-ttu-id="a00cf-155">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-155">Order</span></span> | <span data-ttu-id="a00cf-156">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-156">Path</span></span>                                        | <span data-ttu-id="a00cf-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a00cf-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="a00cf-158">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-158">1</span></span>     | <span data-ttu-id="a00cf-159">/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="a00cf-160">ushort</span><span class="sxs-lookup"><span data-stu-id="a00cf-160">ushort</span></span>      |
| <span data-ttu-id="a00cf-161">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-161">2</span></span>     | <span data-ttu-id="a00cf-162">/ifd/xmp/ <xmpseq> exif： ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="a00cf-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="a00cf-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-163">unicode</span></span>     |
| <span data-ttu-id="a00cf-164">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-164">3</span></span>     | <span data-ttu-id="a00cf-165">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="a00cf-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a00cf-167">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-167">Write Paths</span></span>



| <span data-ttu-id="a00cf-168">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-168">Order</span></span> | <span data-ttu-id="a00cf-169">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-169">Path</span></span>                                        | <span data-ttu-id="a00cf-170">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a00cf-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="a00cf-171">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-171">1</span></span>     | <span data-ttu-id="a00cf-172">/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="a00cf-173">ushort</span><span class="sxs-lookup"><span data-stu-id="a00cf-173">ushort</span></span>      |
| <span data-ttu-id="a00cf-174">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-174">2</span></span>     | <span data-ttu-id="a00cf-175">/ifd/xmp/ <xmpseq> exif： ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="a00cf-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="a00cf-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-176">unicode</span></span>     |
| <span data-ttu-id="a00cf-177">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-177">3</span></span>     | <span data-ttu-id="a00cf-178">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="a00cf-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="a00cf-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a00cf-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-180">Remove Paths</span></span>



| <span data-ttu-id="a00cf-181">單</span><span class="sxs-lookup"><span data-stu-id="a00cf-181">Order</span></span> | <span data-ttu-id="a00cf-182">路徑</span><span class="sxs-lookup"><span data-stu-id="a00cf-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="a00cf-183">1</span><span class="sxs-lookup"><span data-stu-id="a00cf-183">1</span></span>     | <span data-ttu-id="a00cf-184">/ifd/exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="a00cf-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="a00cf-185">2</span><span class="sxs-lookup"><span data-stu-id="a00cf-185">2</span></span>     | <span data-ttu-id="a00cf-186">/ifd/xmp/ <xmpseq> exif： isospeedratings</span><span class="sxs-lookup"><span data-stu-id="a00cf-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="a00cf-187">3</span><span class="sxs-lookup"><span data-stu-id="a00cf-187">3</span></span>     | <span data-ttu-id="a00cf-188">/ifd/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="a00cf-189">備註</span><span class="sxs-lookup"><span data-stu-id="a00cf-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a00cf-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="a00cf-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00cf-191">ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="a00cf-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
