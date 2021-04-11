---
description: RelatedSoundFile 屬性的相片中繼資料原則。
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: RelatedSoundFile 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944859"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a><span data-ttu-id="bf26c-103">RelatedSoundFile 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="bf26c-103">System.Photo.RelatedSoundFile Photo Metadata Policy</span></span>

<span data-ttu-id="bf26c-104">[RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="bf26c-104">The photo metadata policy for the [System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bf26c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bf26c-105">PKEY</span></span>

<span data-ttu-id="bf26c-106">PKEY \_ 相片 \_ RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-106">PKEY\_Photo\_RelatedSoundFile</span></span>

### <a name="containers"></a><span data-ttu-id="bf26c-107">容器</span><span class="sxs-lookup"><span data-stu-id="bf26c-107">Containers</span></span>

<span data-ttu-id="bf26c-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="bf26c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bf26c-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="bf26c-109">Read-Only</span></span>

<span data-ttu-id="bf26c-110">No</span><span class="sxs-lookup"><span data-stu-id="bf26c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bf26c-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="bf26c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bf26c-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="bf26c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="bf26c-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="bf26c-113">Input Type</span></span>

<span data-ttu-id="bf26c-114">字串。</span><span class="sxs-lookup"><span data-stu-id="bf26c-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bf26c-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="bf26c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="bf26c-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="bf26c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bf26c-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="bf26c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bf26c-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-118">Read Paths</span></span>



| <span data-ttu-id="bf26c-119">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-119">Order</span></span> | <span data-ttu-id="bf26c-120">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-120">Path</span></span>                          | <span data-ttu-id="bf26c-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf26c-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bf26c-122">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-122">1</span></span>     | <span data-ttu-id="bf26c-123">/app1/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-123">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="bf26c-124">ascii</span><span class="sxs-lookup"><span data-stu-id="bf26c-124">ascii</span></span>       |
| <span data-ttu-id="bf26c-125">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-125">2</span></span>     | <span data-ttu-id="bf26c-126">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-126">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="bf26c-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf26c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bf26c-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-128">Write Paths</span></span>



| <span data-ttu-id="bf26c-129">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-129">Order</span></span> | <span data-ttu-id="bf26c-130">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-130">Path</span></span>                          | <span data-ttu-id="bf26c-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf26c-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bf26c-132">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-132">1</span></span>     | <span data-ttu-id="bf26c-133">/app1/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-133">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="bf26c-134">ascii</span><span class="sxs-lookup"><span data-stu-id="bf26c-134">ascii</span></span>       |
| <span data-ttu-id="bf26c-135">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-135">2</span></span>     | <span data-ttu-id="bf26c-136">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-136">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="bf26c-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf26c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bf26c-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-138">Remove Paths</span></span>



| <span data-ttu-id="bf26c-139">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-139">Order</span></span> | <span data-ttu-id="bf26c-140">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bf26c-141">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-141">1</span></span>     | <span data-ttu-id="bf26c-142">/app1/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-142">/app1/ifd/exif/{ushort=40964}</span></span> |
| <span data-ttu-id="bf26c-143">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-143">2</span></span>     | <span data-ttu-id="bf26c-144">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-144">/xmp/exif:RelatedSoundFile</span></span>    |



 

### <a name="tiff-policy"></a><span data-ttu-id="bf26c-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="bf26c-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bf26c-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-146">Read Paths</span></span>



| <span data-ttu-id="bf26c-147">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-147">Order</span></span> | <span data-ttu-id="bf26c-148">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-148">Path</span></span>                           | <span data-ttu-id="bf26c-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf26c-149">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="bf26c-150">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-150">1</span></span>     | <span data-ttu-id="bf26c-151">/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-151">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="bf26c-152">ascii</span><span class="sxs-lookup"><span data-stu-id="bf26c-152">ascii</span></span>       |
| <span data-ttu-id="bf26c-153">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-153">2</span></span>     | <span data-ttu-id="bf26c-154">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-154">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="bf26c-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf26c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bf26c-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-156">Write Paths</span></span>



| <span data-ttu-id="bf26c-157">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-157">Order</span></span> | <span data-ttu-id="bf26c-158">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-158">Path</span></span>                           | <span data-ttu-id="bf26c-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf26c-159">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="bf26c-160">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-160">1</span></span>     | <span data-ttu-id="bf26c-161">/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-161">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="bf26c-162">ascii</span><span class="sxs-lookup"><span data-stu-id="bf26c-162">ascii</span></span>       |
| <span data-ttu-id="bf26c-163">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-163">2</span></span>     | <span data-ttu-id="bf26c-164">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-164">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="bf26c-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf26c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bf26c-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-166">Remove Paths</span></span>



| <span data-ttu-id="bf26c-167">單</span><span class="sxs-lookup"><span data-stu-id="bf26c-167">Order</span></span> | <span data-ttu-id="bf26c-168">路徑</span><span class="sxs-lookup"><span data-stu-id="bf26c-168">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="bf26c-169">1</span><span class="sxs-lookup"><span data-stu-id="bf26c-169">1</span></span>     | <span data-ttu-id="bf26c-170">/ifd/exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="bf26c-170">/ifd/exif/{ushort=40964}</span></span>       |
| <span data-ttu-id="bf26c-171">2</span><span class="sxs-lookup"><span data-stu-id="bf26c-171">2</span></span>     | <span data-ttu-id="bf26c-172">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-172">/ifd/xmp/exif:RelatedSoundFile</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf26c-173">備註</span><span class="sxs-lookup"><span data-stu-id="bf26c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf26c-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf26c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf26c-175">RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="bf26c-175">System.Photo.RelatedSoundFile</span></span>](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
