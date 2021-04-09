---
description: 適用于 [亮度] 屬性的相片中繼資料原則。
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: 系統相片亮度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945076"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="89c7a-103">系統相片亮度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="89c7a-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="89c7a-104">適用于 [ [亮度](../properties/props-system-photo-aperture.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="89c7a-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="89c7a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="89c7a-105">PKEY</span></span>

<span data-ttu-id="89c7a-106">PKEY \_ 相片 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="89c7a-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="89c7a-107">容器</span><span class="sxs-lookup"><span data-stu-id="89c7a-107">Containers</span></span>

<span data-ttu-id="89c7a-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="89c7a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="89c7a-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="89c7a-109">Read-Only</span></span>

<span data-ttu-id="89c7a-110">Yes</span><span class="sxs-lookup"><span data-stu-id="89c7a-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="89c7a-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="89c7a-111">Input Type</span></span>

<span data-ttu-id="89c7a-112">Double</span><span class="sxs-lookup"><span data-stu-id="89c7a-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="89c7a-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="89c7a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="89c7a-114">系統會從 ApertureNumerator 和 ApertureDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="89c7a-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="89c7a-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="89c7a-115">It cannot be written directly.</span></span> <span data-ttu-id="89c7a-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="89c7a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="89c7a-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="89c7a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="89c7a-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-118">Read Paths</span></span>



| <span data-ttu-id="89c7a-119">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-119">Order</span></span> | <span data-ttu-id="89c7a-120">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-120">Path</span></span>                          | <span data-ttu-id="89c7a-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="89c7a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="89c7a-122">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-122">1</span></span>     | <span data-ttu-id="89c7a-123">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="89c7a-124">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-124">2</span></span>     | <span data-ttu-id="89c7a-125">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="89c7a-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="89c7a-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-126">Write Paths</span></span>



| <span data-ttu-id="89c7a-127">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-127">Order</span></span> | <span data-ttu-id="89c7a-128">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-128">Path</span></span>                          | <span data-ttu-id="89c7a-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="89c7a-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="89c7a-130">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-130">1</span></span>     | <span data-ttu-id="89c7a-131">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="89c7a-132">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-132">2</span></span>     | <span data-ttu-id="89c7a-133">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="89c7a-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="89c7a-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-134">Remove Paths</span></span>



| <span data-ttu-id="89c7a-135">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-135">Order</span></span> | <span data-ttu-id="89c7a-136">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="89c7a-137">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-137">1</span></span>     | <span data-ttu-id="89c7a-138">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="89c7a-139">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-139">2</span></span>     | <span data-ttu-id="89c7a-140">/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="89c7a-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="89c7a-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="89c7a-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="89c7a-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-142">Read Paths</span></span>



| <span data-ttu-id="89c7a-143">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-143">Order</span></span> | <span data-ttu-id="89c7a-144">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-144">Path</span></span>                          | <span data-ttu-id="89c7a-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="89c7a-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="89c7a-146">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-146">1</span></span>     | <span data-ttu-id="89c7a-147">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="89c7a-148">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-148">2</span></span>     | <span data-ttu-id="89c7a-149">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="89c7a-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="89c7a-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-150">Write Paths</span></span>



| <span data-ttu-id="89c7a-151">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-151">Order</span></span> | <span data-ttu-id="89c7a-152">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-152">Path</span></span>                          | <span data-ttu-id="89c7a-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="89c7a-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="89c7a-154">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-154">1</span></span>     | <span data-ttu-id="89c7a-155">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="89c7a-156">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-156">2</span></span>     | <span data-ttu-id="89c7a-157">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="89c7a-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="89c7a-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-158">Remove Paths</span></span>



| <span data-ttu-id="89c7a-159">單</span><span class="sxs-lookup"><span data-stu-id="89c7a-159">Order</span></span> | <span data-ttu-id="89c7a-160">路徑</span><span class="sxs-lookup"><span data-stu-id="89c7a-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="89c7a-161">1</span><span class="sxs-lookup"><span data-stu-id="89c7a-161">1</span></span>     | <span data-ttu-id="89c7a-162">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="89c7a-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="89c7a-163">2</span><span class="sxs-lookup"><span data-stu-id="89c7a-163">2</span></span>     | <span data-ttu-id="89c7a-164">/ifd/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="89c7a-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="89c7a-165">備註</span><span class="sxs-lookup"><span data-stu-id="89c7a-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="89c7a-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="89c7a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89c7a-167">系統相片。亮度</span><span class="sxs-lookup"><span data-stu-id="89c7a-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
