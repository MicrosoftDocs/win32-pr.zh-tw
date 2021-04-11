---
description: FNumber 屬性的相片中繼資料原則。
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: FNumber 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193554"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="d6320-103">FNumber 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="d6320-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="d6320-104">[FNumber](../properties/props-system-photo-fnumber.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="d6320-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d6320-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d6320-105">PKEY</span></span>

<span data-ttu-id="d6320-106">PKEY \_ 相片 \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="d6320-107">容器</span><span class="sxs-lookup"><span data-stu-id="d6320-107">Containers</span></span>

<span data-ttu-id="d6320-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="d6320-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d6320-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6320-109">Read-Only</span></span>

<span data-ttu-id="d6320-110">Yes</span><span class="sxs-lookup"><span data-stu-id="d6320-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d6320-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="d6320-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d6320-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="d6320-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d6320-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="d6320-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="d6320-114">系統會從 FNumberNumerator 和 FNumberDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="d6320-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="d6320-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="d6320-115">It cannot be written directly.</span></span> <span data-ttu-id="d6320-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="d6320-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d6320-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="d6320-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d6320-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-118">Read Paths</span></span>



| <span data-ttu-id="d6320-119">單</span><span class="sxs-lookup"><span data-stu-id="d6320-119">Order</span></span> | <span data-ttu-id="d6320-120">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-120">Path</span></span>                          | <span data-ttu-id="d6320-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d6320-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d6320-122">1</span><span class="sxs-lookup"><span data-stu-id="d6320-122">1</span></span>     | <span data-ttu-id="d6320-123">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="d6320-124">2</span><span class="sxs-lookup"><span data-stu-id="d6320-124">2</span></span>     | <span data-ttu-id="d6320-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="d6320-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="d6320-127">單</span><span class="sxs-lookup"><span data-stu-id="d6320-127">Order</span></span> | <span data-ttu-id="d6320-128">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-128">Path</span></span>                          | <span data-ttu-id="d6320-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d6320-129">Disk Format</span></span> |     |
| <span data-ttu-id="d6320-130">1</span><span class="sxs-lookup"><span data-stu-id="d6320-130">1</span></span>     | <span data-ttu-id="d6320-131">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="d6320-132">2</span><span class="sxs-lookup"><span data-stu-id="d6320-132">2</span></span>     | <span data-ttu-id="d6320-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="d6320-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-134">Remove Paths</span></span>



| <span data-ttu-id="d6320-135">單</span><span class="sxs-lookup"><span data-stu-id="d6320-135">Order</span></span> | <span data-ttu-id="d6320-136">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d6320-137">1</span><span class="sxs-lookup"><span data-stu-id="d6320-137">1</span></span>     | <span data-ttu-id="d6320-138">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="d6320-139">2</span><span class="sxs-lookup"><span data-stu-id="d6320-139">2</span></span>     | <span data-ttu-id="d6320-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="d6320-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="d6320-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="d6320-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d6320-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-142">Read Paths</span></span>



| <span data-ttu-id="d6320-143">單</span><span class="sxs-lookup"><span data-stu-id="d6320-143">Order</span></span> | <span data-ttu-id="d6320-144">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-144">Path</span></span>                     | <span data-ttu-id="d6320-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d6320-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d6320-146">1</span><span class="sxs-lookup"><span data-stu-id="d6320-146">1</span></span>     | <span data-ttu-id="d6320-147">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="d6320-148">2</span><span class="sxs-lookup"><span data-stu-id="d6320-148">2</span></span>     | <span data-ttu-id="d6320-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="d6320-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-150">Write Paths</span></span>



| <span data-ttu-id="d6320-151">單</span><span class="sxs-lookup"><span data-stu-id="d6320-151">Order</span></span> | <span data-ttu-id="d6320-152">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-152">Path</span></span>                     | <span data-ttu-id="d6320-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d6320-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d6320-154">1</span><span class="sxs-lookup"><span data-stu-id="d6320-154">1</span></span>     | <span data-ttu-id="d6320-155">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="d6320-156">2</span><span class="sxs-lookup"><span data-stu-id="d6320-156">2</span></span>     | <span data-ttu-id="d6320-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d6320-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-158">Remove Paths</span></span>



| <span data-ttu-id="d6320-159">單</span><span class="sxs-lookup"><span data-stu-id="d6320-159">Order</span></span> | <span data-ttu-id="d6320-160">路徑</span><span class="sxs-lookup"><span data-stu-id="d6320-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="d6320-161">1</span><span class="sxs-lookup"><span data-stu-id="d6320-161">1</span></span>     | <span data-ttu-id="d6320-162">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="d6320-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="d6320-163">2</span><span class="sxs-lookup"><span data-stu-id="d6320-163">2</span></span>     | <span data-ttu-id="d6320-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="d6320-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="d6320-165">備註</span><span class="sxs-lookup"><span data-stu-id="d6320-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6320-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6320-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6320-167">FNumber</span><span class="sxs-lookup"><span data-stu-id="d6320-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
