---
description: ImageID 屬性的相片中繼資料原則。
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: ImageID 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513508"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="26880-103">ImageID 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="26880-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="26880-104">[ImageID](../properties/props-system-image-imageid.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="26880-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="26880-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="26880-105">PKEY</span></span>

<span data-ttu-id="26880-106">PKEY \_ 影像 \_ ImageID</span><span class="sxs-lookup"><span data-stu-id="26880-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="26880-107">容器</span><span class="sxs-lookup"><span data-stu-id="26880-107">Containers</span></span>

<span data-ttu-id="26880-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="26880-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="26880-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="26880-109">Read-Only</span></span>

<span data-ttu-id="26880-110">No</span><span class="sxs-lookup"><span data-stu-id="26880-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="26880-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="26880-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="26880-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="26880-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="26880-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="26880-113">Input Type</span></span>

<span data-ttu-id="26880-114">字串。</span><span class="sxs-lookup"><span data-stu-id="26880-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="26880-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="26880-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="26880-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="26880-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="26880-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="26880-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="26880-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="26880-118">Read Paths</span></span>



| <span data-ttu-id="26880-119">單</span><span class="sxs-lookup"><span data-stu-id="26880-119">Order</span></span> | <span data-ttu-id="26880-120">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-120">Path</span></span>                          | <span data-ttu-id="26880-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="26880-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="26880-122">1</span><span class="sxs-lookup"><span data-stu-id="26880-122">1</span></span>     | <span data-ttu-id="26880-123">/app1/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="26880-124">ascii</span><span class="sxs-lookup"><span data-stu-id="26880-124">ascii</span></span>       |
| <span data-ttu-id="26880-125">2</span><span class="sxs-lookup"><span data-stu-id="26880-125">2</span></span>     | <span data-ttu-id="26880-126">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="26880-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="26880-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="26880-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="26880-128">Write Paths</span></span>



| <span data-ttu-id="26880-129">單</span><span class="sxs-lookup"><span data-stu-id="26880-129">Order</span></span> | <span data-ttu-id="26880-130">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-130">Path</span></span>                          | <span data-ttu-id="26880-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="26880-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="26880-132">1</span><span class="sxs-lookup"><span data-stu-id="26880-132">1</span></span>     | <span data-ttu-id="26880-133">/app1/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="26880-134">ascii</span><span class="sxs-lookup"><span data-stu-id="26880-134">ascii</span></span>       |
| <span data-ttu-id="26880-135">2</span><span class="sxs-lookup"><span data-stu-id="26880-135">2</span></span>     | <span data-ttu-id="26880-136">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="26880-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="26880-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="26880-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="26880-138">Remove Paths</span></span>



| <span data-ttu-id="26880-139">單</span><span class="sxs-lookup"><span data-stu-id="26880-139">Order</span></span> | <span data-ttu-id="26880-140">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="26880-141">1</span><span class="sxs-lookup"><span data-stu-id="26880-141">1</span></span>     | <span data-ttu-id="26880-142">/app1/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="26880-143">2</span><span class="sxs-lookup"><span data-stu-id="26880-143">2</span></span>     | <span data-ttu-id="26880-144">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="26880-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="26880-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="26880-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="26880-146">Read Paths</span></span>



| <span data-ttu-id="26880-147">單</span><span class="sxs-lookup"><span data-stu-id="26880-147">Order</span></span> | <span data-ttu-id="26880-148">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-148">Path</span></span>                        | <span data-ttu-id="26880-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="26880-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="26880-150">/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="26880-151">ascii</span><span class="sxs-lookup"><span data-stu-id="26880-151">ascii</span></span>       |
|       | <span data-ttu-id="26880-152">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="26880-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="26880-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="26880-154">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="26880-154">Write Paths</span></span>



| <span data-ttu-id="26880-155">單</span><span class="sxs-lookup"><span data-stu-id="26880-155">Order</span></span> | <span data-ttu-id="26880-156">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-156">Path</span></span>                        | <span data-ttu-id="26880-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="26880-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="26880-158">/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="26880-159">ascii</span><span class="sxs-lookup"><span data-stu-id="26880-159">ascii</span></span>       |
|       | <span data-ttu-id="26880-160">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="26880-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="26880-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="26880-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="26880-162">Remove Paths</span></span>



| <span data-ttu-id="26880-163">單</span><span class="sxs-lookup"><span data-stu-id="26880-163">Order</span></span> | <span data-ttu-id="26880-164">路徑</span><span class="sxs-lookup"><span data-stu-id="26880-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="26880-165">/ifd/exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="26880-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="26880-166">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="26880-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="26880-167">備註</span><span class="sxs-lookup"><span data-stu-id="26880-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="26880-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="26880-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26880-169">ImageID</span><span class="sxs-lookup"><span data-stu-id="26880-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
