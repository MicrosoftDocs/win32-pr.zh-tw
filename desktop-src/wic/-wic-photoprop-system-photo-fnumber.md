---
description: FNumber 屬性的相片中繼資料原則。
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: FNumber 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443619"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="a3005-103">FNumber 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="a3005-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="a3005-104">[FNumber](../properties/props-system-photo-fnumber.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="a3005-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a3005-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a3005-105">PKEY</span></span>

<span data-ttu-id="a3005-106">PKEY \_ 相片 \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="a3005-107">容器</span><span class="sxs-lookup"><span data-stu-id="a3005-107">Containers</span></span>

<span data-ttu-id="a3005-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="a3005-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a3005-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="a3005-109">Read-Only</span></span>

<span data-ttu-id="a3005-110">是</span><span class="sxs-lookup"><span data-stu-id="a3005-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a3005-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a3005-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a3005-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a3005-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a3005-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="a3005-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a3005-114">系統會從 FNumberNumerator 和 FNumberDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="a3005-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="a3005-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="a3005-115">It cannot be written directly.</span></span> <span data-ttu-id="a3005-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="a3005-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a3005-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="a3005-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3005-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-118">Read Paths</span></span>



| <span data-ttu-id="a3005-119">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-119">Order</span></span> | <span data-ttu-id="a3005-120">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-120">Path</span></span>                          | <span data-ttu-id="a3005-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a3005-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a3005-122">1</span><span class="sxs-lookup"><span data-stu-id="a3005-122">1</span></span>     | <span data-ttu-id="a3005-123">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="a3005-124">2</span><span class="sxs-lookup"><span data-stu-id="a3005-124">2</span></span>     | <span data-ttu-id="a3005-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="a3005-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-126">Write Paths</span></span>



| <span data-ttu-id="a3005-127">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-127">Order</span></span> | <span data-ttu-id="a3005-128">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-128">Path</span></span>                          | <span data-ttu-id="a3005-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a3005-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a3005-130">1</span><span class="sxs-lookup"><span data-stu-id="a3005-130">1</span></span>     | <span data-ttu-id="a3005-131">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="a3005-132">2</span><span class="sxs-lookup"><span data-stu-id="a3005-132">2</span></span>     | <span data-ttu-id="a3005-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="a3005-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-134">Remove Paths</span></span>



| <span data-ttu-id="a3005-135">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-135">Order</span></span> | <span data-ttu-id="a3005-136">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a3005-137">1</span><span class="sxs-lookup"><span data-stu-id="a3005-137">1</span></span>     | <span data-ttu-id="a3005-138">/app1/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="a3005-139">2</span><span class="sxs-lookup"><span data-stu-id="a3005-139">2</span></span>     | <span data-ttu-id="a3005-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="a3005-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="a3005-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="a3005-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3005-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-142">Read Paths</span></span>



| <span data-ttu-id="a3005-143">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-143">Order</span></span> | <span data-ttu-id="a3005-144">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-144">Path</span></span>                     | <span data-ttu-id="a3005-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a3005-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a3005-146">1</span><span class="sxs-lookup"><span data-stu-id="a3005-146">1</span></span>     | <span data-ttu-id="a3005-147">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="a3005-148">2</span><span class="sxs-lookup"><span data-stu-id="a3005-148">2</span></span>     | <span data-ttu-id="a3005-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="a3005-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-150">Write Paths</span></span>



| <span data-ttu-id="a3005-151">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-151">Order</span></span> | <span data-ttu-id="a3005-152">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-152">Path</span></span>                     | <span data-ttu-id="a3005-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a3005-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a3005-154">1</span><span class="sxs-lookup"><span data-stu-id="a3005-154">1</span></span>     | <span data-ttu-id="a3005-155">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="a3005-156">2</span><span class="sxs-lookup"><span data-stu-id="a3005-156">2</span></span>     | <span data-ttu-id="a3005-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a3005-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-158">Remove Paths</span></span>



| <span data-ttu-id="a3005-159">順序</span><span class="sxs-lookup"><span data-stu-id="a3005-159">Order</span></span> | <span data-ttu-id="a3005-160">路徑</span><span class="sxs-lookup"><span data-stu-id="a3005-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="a3005-161">1</span><span class="sxs-lookup"><span data-stu-id="a3005-161">1</span></span>     | <span data-ttu-id="a3005-162">/ifd/exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="a3005-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="a3005-163">2</span><span class="sxs-lookup"><span data-stu-id="a3005-163">2</span></span>     | <span data-ttu-id="a3005-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="a3005-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="a3005-165">備註</span><span class="sxs-lookup"><span data-stu-id="a3005-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3005-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3005-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3005-167">FNumber</span><span class="sxs-lookup"><span data-stu-id="a3005-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
