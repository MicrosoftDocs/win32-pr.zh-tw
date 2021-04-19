---
description: ShutterSpeed 屬性的相片中繼資料原則。
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: ShutterSpeed 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980447"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="c7af5-103">ShutterSpeed 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="c7af5-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="c7af5-104">[ShutterSpeed](../properties/props-system-photo-shutterspeed.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="c7af5-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c7af5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c7af5-105">PKEY</span></span>

<span data-ttu-id="c7af5-106">PKEY \_ 相片 \_ ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="c7af5-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="c7af5-107">容器</span><span class="sxs-lookup"><span data-stu-id="c7af5-107">Containers</span></span>

<span data-ttu-id="c7af5-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="c7af5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c7af5-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="c7af5-109">Read-Only</span></span>

<span data-ttu-id="c7af5-110">Yes</span><span class="sxs-lookup"><span data-stu-id="c7af5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c7af5-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="c7af5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c7af5-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="c7af5-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c7af5-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="c7af5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c7af5-114">系統會從 ShutterSpeedNumerator 和 ShutterSpeedDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="c7af5-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="c7af5-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="c7af5-115">It cannot be written directly.</span></span> <span data-ttu-id="c7af5-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="c7af5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c7af5-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="c7af5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c7af5-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-118">Read Paths</span></span>



| <span data-ttu-id="c7af5-119">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-119">Order</span></span> | <span data-ttu-id="c7af5-120">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-120">Path</span></span>                          | <span data-ttu-id="c7af5-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c7af5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c7af5-122">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-122">1</span></span>     | <span data-ttu-id="c7af5-123">/app1/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="c7af5-124">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-124">2</span></span>     | <span data-ttu-id="c7af5-125">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="c7af5-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="c7af5-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-126">Write Paths</span></span>



| <span data-ttu-id="c7af5-127">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-127">Order</span></span> | <span data-ttu-id="c7af5-128">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-128">Path</span></span>                          | <span data-ttu-id="c7af5-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c7af5-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c7af5-130">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-130">1</span></span>     | <span data-ttu-id="c7af5-131">/app1/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="c7af5-132">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-132">2</span></span>     | <span data-ttu-id="c7af5-133">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="c7af5-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c7af5-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-134">Remove Paths</span></span>



| <span data-ttu-id="c7af5-135">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-135">Order</span></span> | <span data-ttu-id="c7af5-136">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c7af5-137">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-137">1</span></span>     | <span data-ttu-id="c7af5-138">/app1/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="c7af5-139">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-139">2</span></span>     | <span data-ttu-id="c7af5-140">/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="c7af5-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="c7af5-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="c7af5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c7af5-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-142">Read Paths</span></span>



| <span data-ttu-id="c7af5-143">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-143">Order</span></span> | <span data-ttu-id="c7af5-144">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-144">Path</span></span>                            | <span data-ttu-id="c7af5-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c7af5-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="c7af5-146">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-146">1</span></span>     | <span data-ttu-id="c7af5-147">/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="c7af5-148">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-148">2</span></span>     | <span data-ttu-id="c7af5-149">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="c7af5-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c7af5-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-150">Write Paths</span></span>



| <span data-ttu-id="c7af5-151">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-151">Order</span></span> | <span data-ttu-id="c7af5-152">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-152">Path</span></span>                            | <span data-ttu-id="c7af5-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c7af5-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="c7af5-154">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-154">1</span></span>     | <span data-ttu-id="c7af5-155">/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="c7af5-156">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-156">2</span></span>     | <span data-ttu-id="c7af5-157">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="c7af5-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c7af5-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-158">Remove Paths</span></span>



| <span data-ttu-id="c7af5-159">單</span><span class="sxs-lookup"><span data-stu-id="c7af5-159">Order</span></span> | <span data-ttu-id="c7af5-160">路徑</span><span class="sxs-lookup"><span data-stu-id="c7af5-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="c7af5-161">1</span><span class="sxs-lookup"><span data-stu-id="c7af5-161">1</span></span>     | <span data-ttu-id="c7af5-162">/ifd/exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="c7af5-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="c7af5-163">2</span><span class="sxs-lookup"><span data-stu-id="c7af5-163">2</span></span>     | <span data-ttu-id="c7af5-164">/ifd/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="c7af5-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c7af5-165">備註</span><span class="sxs-lookup"><span data-stu-id="c7af5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7af5-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7af5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7af5-167">ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="c7af5-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
