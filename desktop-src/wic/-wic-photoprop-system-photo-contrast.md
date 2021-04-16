---
description: '[對比] 屬性的相片中繼資料原則。'
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: 系統相片對比相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514169"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="6882a-103">系統相片對比相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="6882a-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="6882a-104">[ [對比](../properties/props-system-photo-contrast.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="6882a-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6882a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6882a-105">PKEY</span></span>

<span data-ttu-id="6882a-106">PKEY \_ 相片 \_ 對比</span><span class="sxs-lookup"><span data-stu-id="6882a-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="6882a-107">容器</span><span class="sxs-lookup"><span data-stu-id="6882a-107">Containers</span></span>

<span data-ttu-id="6882a-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="6882a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6882a-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="6882a-109">Read-Only</span></span>

<span data-ttu-id="6882a-110">No</span><span class="sxs-lookup"><span data-stu-id="6882a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6882a-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="6882a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6882a-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6882a-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="6882a-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="6882a-113">Input Type</span></span>

<span data-ttu-id="6882a-114">UShort</span><span class="sxs-lookup"><span data-stu-id="6882a-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6882a-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="6882a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6882a-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="6882a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6882a-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="6882a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6882a-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-118">Read Paths</span></span>



| <span data-ttu-id="6882a-119">單</span><span class="sxs-lookup"><span data-stu-id="6882a-119">Order</span></span> | <span data-ttu-id="6882a-120">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-120">Path</span></span>                          | <span data-ttu-id="6882a-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6882a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6882a-122">1</span><span class="sxs-lookup"><span data-stu-id="6882a-122">1</span></span>     | <span data-ttu-id="6882a-123">/app1/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="6882a-124">ushort</span><span class="sxs-lookup"><span data-stu-id="6882a-124">ushort</span></span>      |
| <span data-ttu-id="6882a-125">2</span><span class="sxs-lookup"><span data-stu-id="6882a-125">2</span></span>     | <span data-ttu-id="6882a-126">/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="6882a-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="6882a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6882a-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-128">Write Paths</span></span>



| <span data-ttu-id="6882a-129">單</span><span class="sxs-lookup"><span data-stu-id="6882a-129">Order</span></span> | <span data-ttu-id="6882a-130">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-130">Path</span></span>                          | <span data-ttu-id="6882a-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6882a-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6882a-132">1</span><span class="sxs-lookup"><span data-stu-id="6882a-132">1</span></span>     | <span data-ttu-id="6882a-133">/app1/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="6882a-134">ushort</span><span class="sxs-lookup"><span data-stu-id="6882a-134">ushort</span></span>      |
| <span data-ttu-id="6882a-135">2</span><span class="sxs-lookup"><span data-stu-id="6882a-135">2</span></span>     | <span data-ttu-id="6882a-136">/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="6882a-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="6882a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6882a-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-138">Remove Paths</span></span>



| <span data-ttu-id="6882a-139">單</span><span class="sxs-lookup"><span data-stu-id="6882a-139">Order</span></span> | <span data-ttu-id="6882a-140">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6882a-141">1</span><span class="sxs-lookup"><span data-stu-id="6882a-141">1</span></span>     | <span data-ttu-id="6882a-142">/app1/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="6882a-143">2</span><span class="sxs-lookup"><span data-stu-id="6882a-143">2</span></span>     | <span data-ttu-id="6882a-144">/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="6882a-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="6882a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6882a-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-146">Read Paths</span></span>



| <span data-ttu-id="6882a-147">單</span><span class="sxs-lookup"><span data-stu-id="6882a-147">Order</span></span> | <span data-ttu-id="6882a-148">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-148">Path</span></span>                     | <span data-ttu-id="6882a-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6882a-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6882a-150">1</span><span class="sxs-lookup"><span data-stu-id="6882a-150">1</span></span>     | <span data-ttu-id="6882a-151">/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="6882a-152">ushort</span><span class="sxs-lookup"><span data-stu-id="6882a-152">ushort</span></span>      |
| <span data-ttu-id="6882a-153">2</span><span class="sxs-lookup"><span data-stu-id="6882a-153">2</span></span>     | <span data-ttu-id="6882a-154">/ifd/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="6882a-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="6882a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6882a-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-156">Write Paths</span></span>



| <span data-ttu-id="6882a-157">單</span><span class="sxs-lookup"><span data-stu-id="6882a-157">Order</span></span> | <span data-ttu-id="6882a-158">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-158">Path</span></span>                     | <span data-ttu-id="6882a-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6882a-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6882a-160">1</span><span class="sxs-lookup"><span data-stu-id="6882a-160">1</span></span>     | <span data-ttu-id="6882a-161">/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="6882a-162">ushort</span><span class="sxs-lookup"><span data-stu-id="6882a-162">ushort</span></span>      |
| <span data-ttu-id="6882a-163">2</span><span class="sxs-lookup"><span data-stu-id="6882a-163">2</span></span>     | <span data-ttu-id="6882a-164">/ifd/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="6882a-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="6882a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6882a-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-166">Remove Paths</span></span>



| <span data-ttu-id="6882a-167">單</span><span class="sxs-lookup"><span data-stu-id="6882a-167">Order</span></span> | <span data-ttu-id="6882a-168">路徑</span><span class="sxs-lookup"><span data-stu-id="6882a-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6882a-169">1</span><span class="sxs-lookup"><span data-stu-id="6882a-169">1</span></span>     | <span data-ttu-id="6882a-170">/ifd/exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="6882a-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="6882a-171">2</span><span class="sxs-lookup"><span data-stu-id="6882a-171">2</span></span>     | <span data-ttu-id="6882a-172">/ifd/xmp/exif：對比</span><span class="sxs-lookup"><span data-stu-id="6882a-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="6882a-173">備註</span><span class="sxs-lookup"><span data-stu-id="6882a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6882a-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="6882a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6882a-175">對比</span><span class="sxs-lookup"><span data-stu-id="6882a-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
