---
description: '[攝影] 屬性的相片中繼資料原則。'
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: '[攝影相片中繼資料] 原則'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971480"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="7f612-103">[攝影相片中繼資料] 原則</span><span class="sxs-lookup"><span data-stu-id="7f612-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="7f612-104">[[攝影] 屬性的](../properties/props-system-photo-exposuretime.md)相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="7f612-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7f612-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7f612-105">PKEY</span></span>

<span data-ttu-id="7f612-106">PKEY \_ 相片 \_ Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="7f612-107">容器</span><span class="sxs-lookup"><span data-stu-id="7f612-107">Containers</span></span>

<span data-ttu-id="7f612-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="7f612-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7f612-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f612-109">Read-Only</span></span>

<span data-ttu-id="7f612-110">No</span><span class="sxs-lookup"><span data-stu-id="7f612-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7f612-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="7f612-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7f612-112">\_如果來源架構) 為) ，則 vt UI1 (（ \_ 如果來源架構為 UI2，則為 vt (）</span><span class="sxs-lookup"><span data-stu-id="7f612-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="7f612-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="7f612-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="7f612-114">輸入類型</span><span class="sxs-lookup"><span data-stu-id="7f612-114">Input Type</span></span>

<span data-ttu-id="7f612-115">VT \_ UI1、VTUI2、VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="7f612-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="7f612-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="7f612-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7f612-117">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="7f612-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="7f612-118">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="7f612-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7f612-119">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="7f612-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7f612-120">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-120">Read Paths</span></span>



| <span data-ttu-id="7f612-121">單</span><span class="sxs-lookup"><span data-stu-id="7f612-121">Order</span></span> | <span data-ttu-id="7f612-122">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-122">Path</span></span>                             | <span data-ttu-id="7f612-123">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7f612-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="7f612-124">1</span><span class="sxs-lookup"><span data-stu-id="7f612-124">1</span></span>     | <span data-ttu-id="7f612-125">/app1/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="7f612-126">ushort</span><span class="sxs-lookup"><span data-stu-id="7f612-126">ushort</span></span>      |
| <span data-ttu-id="7f612-127">2</span><span class="sxs-lookup"><span data-stu-id="7f612-127">2</span></span>     | <span data-ttu-id="7f612-128">/xmp/ <xmpstruct> exif： Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="7f612-129">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-129">Write Paths</span></span>



| <span data-ttu-id="7f612-130">單</span><span class="sxs-lookup"><span data-stu-id="7f612-130">Order</span></span> | <span data-ttu-id="7f612-131">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-131">Path</span></span>                             | <span data-ttu-id="7f612-132">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7f612-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="7f612-133">1</span><span class="sxs-lookup"><span data-stu-id="7f612-133">1</span></span>     | <span data-ttu-id="7f612-134">/app1/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="7f612-135">ushort</span><span class="sxs-lookup"><span data-stu-id="7f612-135">ushort</span></span>      |
| <span data-ttu-id="7f612-136">2</span><span class="sxs-lookup"><span data-stu-id="7f612-136">2</span></span>     | <span data-ttu-id="7f612-137">/xmp/ <xmpstruct> exif： Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7f612-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-138">Remove Paths</span></span>



| <span data-ttu-id="7f612-139">單</span><span class="sxs-lookup"><span data-stu-id="7f612-139">Order</span></span> | <span data-ttu-id="7f612-140">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="7f612-141">1</span><span class="sxs-lookup"><span data-stu-id="7f612-141">1</span></span>     | <span data-ttu-id="7f612-142">/app1/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="7f612-143">2</span><span class="sxs-lookup"><span data-stu-id="7f612-143">2</span></span>     | <span data-ttu-id="7f612-144">/xmp/ <xmpstruct> exif： flash</span><span class="sxs-lookup"><span data-stu-id="7f612-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="7f612-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="7f612-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7f612-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-146">Read Paths</span></span>



| <span data-ttu-id="7f612-147">單</span><span class="sxs-lookup"><span data-stu-id="7f612-147">Order</span></span> | <span data-ttu-id="7f612-148">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-148">Path</span></span>                                 | <span data-ttu-id="7f612-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7f612-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="7f612-150">1</span><span class="sxs-lookup"><span data-stu-id="7f612-150">1</span></span>     | <span data-ttu-id="7f612-151">/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="7f612-152">ushort</span><span class="sxs-lookup"><span data-stu-id="7f612-152">ushort</span></span>      |
| <span data-ttu-id="7f612-153">2</span><span class="sxs-lookup"><span data-stu-id="7f612-153">2</span></span>     | <span data-ttu-id="7f612-154">/ifd/xmp/ <xmpstruct> exif： Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="7f612-155">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-155">Write Paths</span></span>



| <span data-ttu-id="7f612-156">單</span><span class="sxs-lookup"><span data-stu-id="7f612-156">Order</span></span> | <span data-ttu-id="7f612-157">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-157">Path</span></span>                                 | <span data-ttu-id="7f612-158">磁片格式</span><span class="sxs-lookup"><span data-stu-id="7f612-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="7f612-159">1</span><span class="sxs-lookup"><span data-stu-id="7f612-159">1</span></span>     | <span data-ttu-id="7f612-160">/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="7f612-161">ushort</span><span class="sxs-lookup"><span data-stu-id="7f612-161">ushort</span></span>      |
| <span data-ttu-id="7f612-162">2</span><span class="sxs-lookup"><span data-stu-id="7f612-162">2</span></span>     | <span data-ttu-id="7f612-163">/ifd/xmp/ <xmpstruct> exif： Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7f612-164">移除路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-164">Remove Paths</span></span>



| <span data-ttu-id="7f612-165">單</span><span class="sxs-lookup"><span data-stu-id="7f612-165">Order</span></span> | <span data-ttu-id="7f612-166">路徑</span><span class="sxs-lookup"><span data-stu-id="7f612-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="7f612-167">1</span><span class="sxs-lookup"><span data-stu-id="7f612-167">1</span></span>     | <span data-ttu-id="7f612-168">/ifd/exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="7f612-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="7f612-169">2</span><span class="sxs-lookup"><span data-stu-id="7f612-169">2</span></span>     | <span data-ttu-id="7f612-170">/ifd/xmp/ <xmpstruct> exif： flash</span><span class="sxs-lookup"><span data-stu-id="7f612-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f612-171">備註</span><span class="sxs-lookup"><span data-stu-id="7f612-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f612-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f612-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f612-173">： Flash</span><span class="sxs-lookup"><span data-stu-id="7f612-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
