---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: 沖印相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981020"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="33565-103">沖印相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="33565-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="33565-104">適用于 [system.object](../properties/props-system-photo-sharpness.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="33565-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="33565-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="33565-105">PKEY</span></span>

<span data-ttu-id="33565-106">PKEY \_ 相片 \_ 清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="33565-107">容器</span><span class="sxs-lookup"><span data-stu-id="33565-107">Containers</span></span>

<span data-ttu-id="33565-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="33565-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="33565-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="33565-109">Read-Only</span></span>

<span data-ttu-id="33565-110">No</span><span class="sxs-lookup"><span data-stu-id="33565-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="33565-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="33565-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="33565-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="33565-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="33565-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="33565-113">Input Type</span></span>

<span data-ttu-id="33565-114">UShort</span><span class="sxs-lookup"><span data-stu-id="33565-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="33565-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="33565-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="33565-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="33565-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="33565-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="33565-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="33565-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="33565-118">Read Paths</span></span>



| <span data-ttu-id="33565-119">單</span><span class="sxs-lookup"><span data-stu-id="33565-119">Order</span></span> | <span data-ttu-id="33565-120">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-120">Path</span></span>                          | <span data-ttu-id="33565-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="33565-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="33565-122">1</span><span class="sxs-lookup"><span data-stu-id="33565-122">1</span></span>     | <span data-ttu-id="33565-123">/app1/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="33565-124">ushort</span><span class="sxs-lookup"><span data-stu-id="33565-124">ushort</span></span>      |
| <span data-ttu-id="33565-125">2</span><span class="sxs-lookup"><span data-stu-id="33565-125">2</span></span>     | <span data-ttu-id="33565-126">/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="33565-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="33565-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="33565-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="33565-128">Write Paths</span></span>



| <span data-ttu-id="33565-129">單</span><span class="sxs-lookup"><span data-stu-id="33565-129">Order</span></span> | <span data-ttu-id="33565-130">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-130">Path</span></span>                          | <span data-ttu-id="33565-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="33565-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="33565-132">1</span><span class="sxs-lookup"><span data-stu-id="33565-132">1</span></span>     | <span data-ttu-id="33565-133">/app1/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="33565-134">ushort</span><span class="sxs-lookup"><span data-stu-id="33565-134">ushort</span></span>      |
| <span data-ttu-id="33565-135">2</span><span class="sxs-lookup"><span data-stu-id="33565-135">2</span></span>     | <span data-ttu-id="33565-136">/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="33565-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="33565-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="33565-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="33565-138">Remove Paths</span></span>



| <span data-ttu-id="33565-139">單</span><span class="sxs-lookup"><span data-stu-id="33565-139">Order</span></span> | <span data-ttu-id="33565-140">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="33565-141">1</span><span class="sxs-lookup"><span data-stu-id="33565-141">1</span></span>     | <span data-ttu-id="33565-142">/app1/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="33565-143">2</span><span class="sxs-lookup"><span data-stu-id="33565-143">2</span></span>     | <span data-ttu-id="33565-144">/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="33565-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="33565-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="33565-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="33565-146">Read Paths</span></span>



| <span data-ttu-id="33565-147">單</span><span class="sxs-lookup"><span data-stu-id="33565-147">Order</span></span> | <span data-ttu-id="33565-148">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-148">Path</span></span>                     | <span data-ttu-id="33565-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="33565-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="33565-150">1</span><span class="sxs-lookup"><span data-stu-id="33565-150">1</span></span>     | <span data-ttu-id="33565-151">/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="33565-152">ushort</span><span class="sxs-lookup"><span data-stu-id="33565-152">ushort</span></span>      |
| <span data-ttu-id="33565-153">2</span><span class="sxs-lookup"><span data-stu-id="33565-153">2</span></span>     | <span data-ttu-id="33565-154">/ifd/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="33565-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="33565-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="33565-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="33565-156">Write Paths</span></span>



| <span data-ttu-id="33565-157">單</span><span class="sxs-lookup"><span data-stu-id="33565-157">Order</span></span> | <span data-ttu-id="33565-158">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-158">Path</span></span>                     | <span data-ttu-id="33565-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="33565-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="33565-160">1</span><span class="sxs-lookup"><span data-stu-id="33565-160">1</span></span>     | <span data-ttu-id="33565-161">/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="33565-162">ushort</span><span class="sxs-lookup"><span data-stu-id="33565-162">ushort</span></span>      |
| <span data-ttu-id="33565-163">2</span><span class="sxs-lookup"><span data-stu-id="33565-163">2</span></span>     | <span data-ttu-id="33565-164">/ifd/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="33565-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="33565-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="33565-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="33565-166">Remove Paths</span></span>



| <span data-ttu-id="33565-167">單</span><span class="sxs-lookup"><span data-stu-id="33565-167">Order</span></span> | <span data-ttu-id="33565-168">路徑</span><span class="sxs-lookup"><span data-stu-id="33565-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="33565-169">1</span><span class="sxs-lookup"><span data-stu-id="33565-169">1</span></span>     | <span data-ttu-id="33565-170">/ifd/exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="33565-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="33565-171">2</span><span class="sxs-lookup"><span data-stu-id="33565-171">2</span></span>     | <span data-ttu-id="33565-172">/ifd/xmp/exif：清晰度</span><span class="sxs-lookup"><span data-stu-id="33565-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="33565-173">備註</span><span class="sxs-lookup"><span data-stu-id="33565-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="33565-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="33565-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33565-175">System.string</span><span class="sxs-lookup"><span data-stu-id="33565-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
