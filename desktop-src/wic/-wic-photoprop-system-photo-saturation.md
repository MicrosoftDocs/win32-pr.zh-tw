---
description: '[Photo] 屬性的相片中繼資料原則。'
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: 照相相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027264"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="87b11-103">照相相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="87b11-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="87b11-104">[[Photo] 屬性的](../properties/props-system-photo-saturation.md)相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="87b11-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="87b11-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="87b11-105">PKEY</span></span>

<span data-ttu-id="87b11-106">PKEY \_ 相片 \_ 飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="87b11-107">容器</span><span class="sxs-lookup"><span data-stu-id="87b11-107">Containers</span></span>

<span data-ttu-id="87b11-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="87b11-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="87b11-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="87b11-109">Read-Only</span></span>

<span data-ttu-id="87b11-110">No</span><span class="sxs-lookup"><span data-stu-id="87b11-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="87b11-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="87b11-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="87b11-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="87b11-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="87b11-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="87b11-113">Input Type</span></span>

<span data-ttu-id="87b11-114">UShort</span><span class="sxs-lookup"><span data-stu-id="87b11-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="87b11-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="87b11-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="87b11-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="87b11-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="87b11-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="87b11-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="87b11-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-118">Read Paths</span></span>



| <span data-ttu-id="87b11-119">單</span><span class="sxs-lookup"><span data-stu-id="87b11-119">Order</span></span> | <span data-ttu-id="87b11-120">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-120">Path</span></span>                          | <span data-ttu-id="87b11-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="87b11-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="87b11-122">1</span><span class="sxs-lookup"><span data-stu-id="87b11-122">1</span></span>     | <span data-ttu-id="87b11-123">/app1/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="87b11-124">ushort</span><span class="sxs-lookup"><span data-stu-id="87b11-124">ushort</span></span>      |
| <span data-ttu-id="87b11-125">2</span><span class="sxs-lookup"><span data-stu-id="87b11-125">2</span></span>     | <span data-ttu-id="87b11-126">/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="87b11-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="87b11-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="87b11-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-128">Write Paths</span></span>



| <span data-ttu-id="87b11-129">單</span><span class="sxs-lookup"><span data-stu-id="87b11-129">Order</span></span> | <span data-ttu-id="87b11-130">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-130">Path</span></span>                          | <span data-ttu-id="87b11-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="87b11-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="87b11-132">1</span><span class="sxs-lookup"><span data-stu-id="87b11-132">1</span></span>     | <span data-ttu-id="87b11-133">/app1/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="87b11-134">ushort</span><span class="sxs-lookup"><span data-stu-id="87b11-134">ushort</span></span>      |
| <span data-ttu-id="87b11-135">2</span><span class="sxs-lookup"><span data-stu-id="87b11-135">2</span></span>     | <span data-ttu-id="87b11-136">/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="87b11-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="87b11-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="87b11-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-138">Remove Paths</span></span>



| <span data-ttu-id="87b11-139">單</span><span class="sxs-lookup"><span data-stu-id="87b11-139">Order</span></span> | <span data-ttu-id="87b11-140">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="87b11-141">1</span><span class="sxs-lookup"><span data-stu-id="87b11-141">1</span></span>     | <span data-ttu-id="87b11-142">/app1/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="87b11-143">2</span><span class="sxs-lookup"><span data-stu-id="87b11-143">2</span></span>     | <span data-ttu-id="87b11-144">/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="87b11-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="87b11-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="87b11-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-146">Read Paths</span></span>



| <span data-ttu-id="87b11-147">單</span><span class="sxs-lookup"><span data-stu-id="87b11-147">Order</span></span> | <span data-ttu-id="87b11-148">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-148">Path</span></span>                     | <span data-ttu-id="87b11-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="87b11-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="87b11-150">1</span><span class="sxs-lookup"><span data-stu-id="87b11-150">1</span></span>     | <span data-ttu-id="87b11-151">/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="87b11-152">ushort</span><span class="sxs-lookup"><span data-stu-id="87b11-152">ushort</span></span>      |
| <span data-ttu-id="87b11-153">2</span><span class="sxs-lookup"><span data-stu-id="87b11-153">2</span></span>     | <span data-ttu-id="87b11-154">/ifd/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="87b11-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="87b11-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="87b11-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-156">Write Paths</span></span>



| <span data-ttu-id="87b11-157">單</span><span class="sxs-lookup"><span data-stu-id="87b11-157">Order</span></span> | <span data-ttu-id="87b11-158">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-158">Path</span></span>                     | <span data-ttu-id="87b11-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="87b11-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="87b11-160">1</span><span class="sxs-lookup"><span data-stu-id="87b11-160">1</span></span>     | <span data-ttu-id="87b11-161">/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="87b11-162">ushort</span><span class="sxs-lookup"><span data-stu-id="87b11-162">ushort</span></span>      |
| <span data-ttu-id="87b11-163">2</span><span class="sxs-lookup"><span data-stu-id="87b11-163">2</span></span>     | <span data-ttu-id="87b11-164">/ifd/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="87b11-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="87b11-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="87b11-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-166">Remove Paths</span></span>



| <span data-ttu-id="87b11-167">單</span><span class="sxs-lookup"><span data-stu-id="87b11-167">Order</span></span> | <span data-ttu-id="87b11-168">路徑</span><span class="sxs-lookup"><span data-stu-id="87b11-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="87b11-169">1</span><span class="sxs-lookup"><span data-stu-id="87b11-169">1</span></span>     | <span data-ttu-id="87b11-170">/ifd/exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="87b11-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="87b11-171">2</span><span class="sxs-lookup"><span data-stu-id="87b11-171">2</span></span>     | <span data-ttu-id="87b11-172">/ifd/xmp/exif：飽和度</span><span class="sxs-lookup"><span data-stu-id="87b11-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="87b11-173">備註</span><span class="sxs-lookup"><span data-stu-id="87b11-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="87b11-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="87b11-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87b11-175">照相</span><span class="sxs-lookup"><span data-stu-id="87b11-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
