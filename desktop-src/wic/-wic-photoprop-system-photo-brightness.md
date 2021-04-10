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
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="fe4f6-103">系統相片亮度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="fe4f6-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="fe4f6-104">適用于 [ [亮度](../properties/props-system-photo-aperture.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="fe4f6-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fe4f6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="fe4f6-105">PKEY</span></span>

<span data-ttu-id="fe4f6-106">PKEY \_ 相片 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="fe4f6-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="fe4f6-107">容器</span><span class="sxs-lookup"><span data-stu-id="fe4f6-107">Containers</span></span>

<span data-ttu-id="fe4f6-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="fe4f6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fe4f6-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="fe4f6-109">Read-Only</span></span>

<span data-ttu-id="fe4f6-110">Yes</span><span class="sxs-lookup"><span data-stu-id="fe4f6-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="fe4f6-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="fe4f6-111">Input Type</span></span>

<span data-ttu-id="fe4f6-112">Double</span><span class="sxs-lookup"><span data-stu-id="fe4f6-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fe4f6-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="fe4f6-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="fe4f6-114">系統會從 ApertureNumerator 和 ApertureDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="fe4f6-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="fe4f6-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="fe4f6-115">It cannot be written directly.</span></span> <span data-ttu-id="fe4f6-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="fe4f6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fe4f6-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="fe4f6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fe4f6-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-118">Read Paths</span></span>



| <span data-ttu-id="fe4f6-119">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-119">Order</span></span> | <span data-ttu-id="fe4f6-120">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-120">Path</span></span>                          | <span data-ttu-id="fe4f6-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fe4f6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fe4f6-122">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-122">1</span></span>     | <span data-ttu-id="fe4f6-123">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="fe4f6-124">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-124">2</span></span>     | <span data-ttu-id="fe4f6-125">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="fe4f6-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-126">Write Paths</span></span>



| <span data-ttu-id="fe4f6-127">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-127">Order</span></span> | <span data-ttu-id="fe4f6-128">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-128">Path</span></span>                          | <span data-ttu-id="fe4f6-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fe4f6-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fe4f6-130">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-130">1</span></span>     | <span data-ttu-id="fe4f6-131">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="fe4f6-132">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-132">2</span></span>     | <span data-ttu-id="fe4f6-133">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fe4f6-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-134">Remove Paths</span></span>



| <span data-ttu-id="fe4f6-135">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-135">Order</span></span> | <span data-ttu-id="fe4f6-136">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="fe4f6-137">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-137">1</span></span>     | <span data-ttu-id="fe4f6-138">/app1/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="fe4f6-139">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-139">2</span></span>     | <span data-ttu-id="fe4f6-140">/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="fe4f6-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="fe4f6-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fe4f6-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-142">Read Paths</span></span>



| <span data-ttu-id="fe4f6-143">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-143">Order</span></span> | <span data-ttu-id="fe4f6-144">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-144">Path</span></span>                          | <span data-ttu-id="fe4f6-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fe4f6-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fe4f6-146">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-146">1</span></span>     | <span data-ttu-id="fe4f6-147">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="fe4f6-148">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-148">2</span></span>     | <span data-ttu-id="fe4f6-149">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fe4f6-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-150">Write Paths</span></span>



| <span data-ttu-id="fe4f6-151">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-151">Order</span></span> | <span data-ttu-id="fe4f6-152">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-152">Path</span></span>                          | <span data-ttu-id="fe4f6-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fe4f6-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="fe4f6-154">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-154">1</span></span>     | <span data-ttu-id="fe4f6-155">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="fe4f6-156">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-156">2</span></span>     | <span data-ttu-id="fe4f6-157">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fe4f6-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-158">Remove Paths</span></span>



| <span data-ttu-id="fe4f6-159">單</span><span class="sxs-lookup"><span data-stu-id="fe4f6-159">Order</span></span> | <span data-ttu-id="fe4f6-160">路徑</span><span class="sxs-lookup"><span data-stu-id="fe4f6-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="fe4f6-161">1</span><span class="sxs-lookup"><span data-stu-id="fe4f6-161">1</span></span>     | <span data-ttu-id="fe4f6-162">/ifd/exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="fe4f6-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="fe4f6-163">2</span><span class="sxs-lookup"><span data-stu-id="fe4f6-163">2</span></span>     | <span data-ttu-id="fe4f6-164">/ifd/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="fe4f6-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fe4f6-165">備註</span><span class="sxs-lookup"><span data-stu-id="fe4f6-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe4f6-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe4f6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4f6-167">系統相片。亮度</span><span class="sxs-lookup"><span data-stu-id="fe4f6-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
