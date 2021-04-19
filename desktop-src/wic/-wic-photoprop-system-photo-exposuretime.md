---
description: ExposureTime 屬性的相片中繼資料原則。
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: ExposureTime 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987669"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="bcfb2-103">ExposureTime 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="bcfb2-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="bcfb2-104">[ExposureTime](../properties/props-system-photo-exposuretime.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="bcfb2-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bcfb2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bcfb2-105">PKEY</span></span>

<span data-ttu-id="bcfb2-106">PKEY \_ 相片 \_ ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="bcfb2-107">容器</span><span class="sxs-lookup"><span data-stu-id="bcfb2-107">Containers</span></span>

<span data-ttu-id="bcfb2-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="bcfb2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bcfb2-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="bcfb2-109">Read-Only</span></span>

<span data-ttu-id="bcfb2-110">Yes</span><span class="sxs-lookup"><span data-stu-id="bcfb2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bcfb2-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="bcfb2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bcfb2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="bcfb2-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bcfb2-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="bcfb2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bcfb2-114">系統會從 ExposureTimeNumerator 和 ExposureTimeDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="bcfb2-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="bcfb2-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="bcfb2-115">It cannot be written directly.</span></span> <span data-ttu-id="bcfb2-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="bcfb2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bcfb2-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="bcfb2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bcfb2-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-118">Read Paths</span></span>



| <span data-ttu-id="bcfb2-119">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-119">Order</span></span> | <span data-ttu-id="bcfb2-120">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-120">Path</span></span>                          | <span data-ttu-id="bcfb2-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bcfb2-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bcfb2-122">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-122">1</span></span>     | <span data-ttu-id="bcfb2-123">/app1/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="bcfb2-124">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-124">2</span></span>     | <span data-ttu-id="bcfb2-125">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="bcfb2-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-126">Write Paths</span></span>



| <span data-ttu-id="bcfb2-127">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-127">Order</span></span> | <span data-ttu-id="bcfb2-128">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-128">Path</span></span>                          | <span data-ttu-id="bcfb2-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bcfb2-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bcfb2-130">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-130">1</span></span>     | <span data-ttu-id="bcfb2-131">/app1/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="bcfb2-132">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-132">2</span></span>     | <span data-ttu-id="bcfb2-133">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bcfb2-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-134">Remove Paths</span></span>



| <span data-ttu-id="bcfb2-135">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-135">Order</span></span> | <span data-ttu-id="bcfb2-136">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bcfb2-137">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-137">1</span></span>     | <span data-ttu-id="bcfb2-138">/app1/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="bcfb2-139">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-139">2</span></span>     | <span data-ttu-id="bcfb2-140">/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="bcfb2-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="bcfb2-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bcfb2-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-142">Read Paths</span></span>



| <span data-ttu-id="bcfb2-143">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-143">Order</span></span> | <span data-ttu-id="bcfb2-144">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-144">Path</span></span>                       | <span data-ttu-id="bcfb2-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bcfb2-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="bcfb2-146">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-146">1</span></span>     | <span data-ttu-id="bcfb2-147">/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="bcfb2-148">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-148">2</span></span>     | <span data-ttu-id="bcfb2-149">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bcfb2-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-150">Write Paths</span></span>



| <span data-ttu-id="bcfb2-151">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-151">Order</span></span> | <span data-ttu-id="bcfb2-152">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-152">Path</span></span>                       | <span data-ttu-id="bcfb2-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bcfb2-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="bcfb2-154">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-154">1</span></span>     | <span data-ttu-id="bcfb2-155">/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="bcfb2-156">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-156">2</span></span>     | <span data-ttu-id="bcfb2-157">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bcfb2-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-158">Remove Paths</span></span>



| <span data-ttu-id="bcfb2-159">單</span><span class="sxs-lookup"><span data-stu-id="bcfb2-159">Order</span></span> | <span data-ttu-id="bcfb2-160">路徑</span><span class="sxs-lookup"><span data-stu-id="bcfb2-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="bcfb2-161">1</span><span class="sxs-lookup"><span data-stu-id="bcfb2-161">1</span></span>     | <span data-ttu-id="bcfb2-162">/ifd/exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="bcfb2-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="bcfb2-163">2</span><span class="sxs-lookup"><span data-stu-id="bcfb2-163">2</span></span>     | <span data-ttu-id="bcfb2-164">/ifd/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bcfb2-165">備註</span><span class="sxs-lookup"><span data-stu-id="bcfb2-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcfb2-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="bcfb2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcfb2-167">ExposureTime</span><span class="sxs-lookup"><span data-stu-id="bcfb2-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
