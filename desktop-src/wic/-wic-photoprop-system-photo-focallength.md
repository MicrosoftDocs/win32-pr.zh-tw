---
description: FocalLength 屬性的相片中繼資料原則。
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: FocalLength 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979811"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="bf9d2-103">FocalLength 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="bf9d2-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="bf9d2-104">[FocalLength](../properties/props-system-photo-focallength.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="bf9d2-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bf9d2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bf9d2-105">PKEY</span></span>

<span data-ttu-id="bf9d2-106">PKEY \_ 相片 \_ FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="bf9d2-107">容器</span><span class="sxs-lookup"><span data-stu-id="bf9d2-107">Containers</span></span>

<span data-ttu-id="bf9d2-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="bf9d2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bf9d2-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="bf9d2-109">Read-Only</span></span>

<span data-ttu-id="bf9d2-110">Yes</span><span class="sxs-lookup"><span data-stu-id="bf9d2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bf9d2-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="bf9d2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bf9d2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="bf9d2-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bf9d2-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="bf9d2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bf9d2-114">系統會從 FocalLengthNumerator 和 FocalLengthDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="bf9d2-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="bf9d2-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="bf9d2-115">It cannot be written directly.</span></span> <span data-ttu-id="bf9d2-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="bf9d2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bf9d2-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="bf9d2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bf9d2-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-118">Read Paths</span></span>



| <span data-ttu-id="bf9d2-119">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-119">Order</span></span> | <span data-ttu-id="bf9d2-120">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-120">Path</span></span>                          | <span data-ttu-id="bf9d2-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf9d2-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bf9d2-122">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-122">1</span></span>     | <span data-ttu-id="bf9d2-123">/app1/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="bf9d2-124">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-124">2</span></span>     | <span data-ttu-id="bf9d2-125">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="bf9d2-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-126">Write Paths</span></span>



| <span data-ttu-id="bf9d2-127">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-127">Order</span></span> | <span data-ttu-id="bf9d2-128">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-128">Path</span></span>                          | <span data-ttu-id="bf9d2-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf9d2-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bf9d2-130">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-130">1</span></span>     | <span data-ttu-id="bf9d2-131">/app1/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="bf9d2-132">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-132">2</span></span>     | <span data-ttu-id="bf9d2-133">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bf9d2-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-134">Remove Paths</span></span>



| <span data-ttu-id="bf9d2-135">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-135">Order</span></span> | <span data-ttu-id="bf9d2-136">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bf9d2-137">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-137">1</span></span>     | <span data-ttu-id="bf9d2-138">/app1/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="bf9d2-139">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-139">2</span></span>     | <span data-ttu-id="bf9d2-140">/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="bf9d2-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="bf9d2-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bf9d2-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-142">Read Paths</span></span>



| <span data-ttu-id="bf9d2-143">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-143">Order</span></span> | <span data-ttu-id="bf9d2-144">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-144">Path</span></span>                      | <span data-ttu-id="bf9d2-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf9d2-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="bf9d2-146">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-146">1</span></span>     | <span data-ttu-id="bf9d2-147">/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="bf9d2-148">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-148">2</span></span>     | <span data-ttu-id="bf9d2-149">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bf9d2-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-150">Write Paths</span></span>



| <span data-ttu-id="bf9d2-151">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-151">Order</span></span> | <span data-ttu-id="bf9d2-152">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-152">Path</span></span>                      | <span data-ttu-id="bf9d2-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="bf9d2-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="bf9d2-154">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-154">1</span></span>     | <span data-ttu-id="bf9d2-155">/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="bf9d2-156">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-156">2</span></span>     | <span data-ttu-id="bf9d2-157">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bf9d2-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-158">Remove Paths</span></span>



| <span data-ttu-id="bf9d2-159">單</span><span class="sxs-lookup"><span data-stu-id="bf9d2-159">Order</span></span> | <span data-ttu-id="bf9d2-160">路徑</span><span class="sxs-lookup"><span data-stu-id="bf9d2-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="bf9d2-161">1</span><span class="sxs-lookup"><span data-stu-id="bf9d2-161">1</span></span>     | <span data-ttu-id="bf9d2-162">/ifd/exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="bf9d2-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="bf9d2-163">2</span><span class="sxs-lookup"><span data-stu-id="bf9d2-163">2</span></span>     | <span data-ttu-id="bf9d2-164">/ifd/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf9d2-165">備註</span><span class="sxs-lookup"><span data-stu-id="bf9d2-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf9d2-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf9d2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9d2-167">FocalLength</span><span class="sxs-lookup"><span data-stu-id="bf9d2-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
