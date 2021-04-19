---
description: MaxAperture 屬性的相片中繼資料原則。
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: MaxAperture 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987611"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="62871-103">MaxAperture 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="62871-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="62871-104">[MaxAperture](../properties/props-system-photo-maxaperture.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="62871-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="62871-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="62871-105">PKEY</span></span>

<span data-ttu-id="62871-106">PKEY \_ 相片 \_ MaxAperture</span><span class="sxs-lookup"><span data-stu-id="62871-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="62871-107">容器</span><span class="sxs-lookup"><span data-stu-id="62871-107">Containers</span></span>

<span data-ttu-id="62871-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="62871-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="62871-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="62871-109">Read-Only</span></span>

<span data-ttu-id="62871-110">Yes</span><span class="sxs-lookup"><span data-stu-id="62871-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="62871-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="62871-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="62871-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="62871-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="62871-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="62871-113">Input Type</span></span>

<span data-ttu-id="62871-114">Double</span><span class="sxs-lookup"><span data-stu-id="62871-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="62871-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="62871-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="62871-116">系統會從 MaxApertureNumerator 和 MaxApertureDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="62871-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="62871-117">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="62871-117">It cannot be written directly.</span></span> <span data-ttu-id="62871-118">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="62871-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="62871-119">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="62871-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="62871-120">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="62871-120">Read Paths</span></span>



| <span data-ttu-id="62871-121">單</span><span class="sxs-lookup"><span data-stu-id="62871-121">Order</span></span> | <span data-ttu-id="62871-122">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-122">Path</span></span>                          | <span data-ttu-id="62871-123">磁片格式</span><span class="sxs-lookup"><span data-stu-id="62871-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="62871-124">1</span><span class="sxs-lookup"><span data-stu-id="62871-124">1</span></span>     | <span data-ttu-id="62871-125">/app1/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="62871-126">2</span><span class="sxs-lookup"><span data-stu-id="62871-126">2</span></span>     | <span data-ttu-id="62871-127">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="62871-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="62871-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="62871-128">Write Paths</span></span>



| <span data-ttu-id="62871-129">單</span><span class="sxs-lookup"><span data-stu-id="62871-129">Order</span></span> | <span data-ttu-id="62871-130">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-130">Path</span></span>                          | <span data-ttu-id="62871-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="62871-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="62871-132">1</span><span class="sxs-lookup"><span data-stu-id="62871-132">1</span></span>     | <span data-ttu-id="62871-133">/app1/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="62871-134">2</span><span class="sxs-lookup"><span data-stu-id="62871-134">2</span></span>     | <span data-ttu-id="62871-135">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="62871-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62871-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="62871-136">Remove Paths</span></span>



| <span data-ttu-id="62871-137">單</span><span class="sxs-lookup"><span data-stu-id="62871-137">Order</span></span> | <span data-ttu-id="62871-138">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="62871-139">1</span><span class="sxs-lookup"><span data-stu-id="62871-139">1</span></span>     | <span data-ttu-id="62871-140">/app1/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="62871-141">2</span><span class="sxs-lookup"><span data-stu-id="62871-141">2</span></span>     | <span data-ttu-id="62871-142">/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="62871-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="62871-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="62871-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="62871-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="62871-144">Read Paths</span></span>



| <span data-ttu-id="62871-145">單</span><span class="sxs-lookup"><span data-stu-id="62871-145">Order</span></span> | <span data-ttu-id="62871-146">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-146">Path</span></span>                           | <span data-ttu-id="62871-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="62871-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="62871-148">1</span><span class="sxs-lookup"><span data-stu-id="62871-148">1</span></span>     | <span data-ttu-id="62871-149">/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="62871-150">2</span><span class="sxs-lookup"><span data-stu-id="62871-150">2</span></span>     | <span data-ttu-id="62871-151">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="62871-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="62871-152">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="62871-152">Write Paths</span></span>



| <span data-ttu-id="62871-153">單</span><span class="sxs-lookup"><span data-stu-id="62871-153">Order</span></span> | <span data-ttu-id="62871-154">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-154">Path</span></span>                           | <span data-ttu-id="62871-155">磁片格式</span><span class="sxs-lookup"><span data-stu-id="62871-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="62871-156">1</span><span class="sxs-lookup"><span data-stu-id="62871-156">1</span></span>     | <span data-ttu-id="62871-157">/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="62871-158">2</span><span class="sxs-lookup"><span data-stu-id="62871-158">2</span></span>     | <span data-ttu-id="62871-159">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="62871-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62871-160">移除路徑</span><span class="sxs-lookup"><span data-stu-id="62871-160">Remove Paths</span></span>



| <span data-ttu-id="62871-161">單</span><span class="sxs-lookup"><span data-stu-id="62871-161">Order</span></span> | <span data-ttu-id="62871-162">路徑</span><span class="sxs-lookup"><span data-stu-id="62871-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="62871-163">1</span><span class="sxs-lookup"><span data-stu-id="62871-163">1</span></span>     | <span data-ttu-id="62871-164">/ifd/exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="62871-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="62871-165">2</span><span class="sxs-lookup"><span data-stu-id="62871-165">2</span></span>     | <span data-ttu-id="62871-166">/ifd/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="62871-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="62871-167">備註</span><span class="sxs-lookup"><span data-stu-id="62871-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="62871-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="62871-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62871-169">MaxAperture</span><span class="sxs-lookup"><span data-stu-id="62871-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
