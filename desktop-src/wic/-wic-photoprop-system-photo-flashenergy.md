---
description: FlashEnergy 屬性的相片中繼資料原則。
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: FlashEnergy 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027406"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="9a6b8-103">FlashEnergy 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="9a6b8-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="9a6b8-104">[FlashEnergy](../properties/props-system-photo-flashenergy.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="9a6b8-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9a6b8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9a6b8-105">PKEY</span></span>

<span data-ttu-id="9a6b8-106">PKEY \_ 相片 \_ FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="9a6b8-107">容器</span><span class="sxs-lookup"><span data-stu-id="9a6b8-107">Containers</span></span>

<span data-ttu-id="9a6b8-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="9a6b8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9a6b8-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="9a6b8-109">Read-Only</span></span>

<span data-ttu-id="9a6b8-110">Yes</span><span class="sxs-lookup"><span data-stu-id="9a6b8-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="9a6b8-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="9a6b8-111">Input Type</span></span>

<span data-ttu-id="9a6b8-112">Double</span><span class="sxs-lookup"><span data-stu-id="9a6b8-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9a6b8-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="9a6b8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9a6b8-114">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="9a6b8-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9a6b8-115">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="9a6b8-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a6b8-116">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-116">Read Paths</span></span>



| <span data-ttu-id="9a6b8-117">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-117">Order</span></span> | <span data-ttu-id="9a6b8-118">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-118">Path</span></span>                          | <span data-ttu-id="9a6b8-119">磁片格式</span><span class="sxs-lookup"><span data-stu-id="9a6b8-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9a6b8-120">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-120">1</span></span>     | <span data-ttu-id="9a6b8-121">/app1/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="9a6b8-122">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-122">2</span></span>     | <span data-ttu-id="9a6b8-123">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="9a6b8-124">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-124">Write Paths</span></span>



| <span data-ttu-id="9a6b8-125">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-125">Order</span></span> | <span data-ttu-id="9a6b8-126">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-126">Path</span></span>                          | <span data-ttu-id="9a6b8-127">磁片格式</span><span class="sxs-lookup"><span data-stu-id="9a6b8-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9a6b8-128">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-128">1</span></span>     | <span data-ttu-id="9a6b8-129">/app1/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="9a6b8-130">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-130">2</span></span>     | <span data-ttu-id="9a6b8-131">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9a6b8-132">移除路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-132">Remove Paths</span></span>



| <span data-ttu-id="9a6b8-133">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-133">Order</span></span> | <span data-ttu-id="9a6b8-134">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9a6b8-135">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-135">1</span></span>     | <span data-ttu-id="9a6b8-136">/app1/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="9a6b8-137">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-137">2</span></span>     | <span data-ttu-id="9a6b8-138">/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="9a6b8-139">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="9a6b8-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a6b8-140">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-140">Read Paths</span></span>



| <span data-ttu-id="9a6b8-141">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-141">Order</span></span> | <span data-ttu-id="9a6b8-142">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-142">Path</span></span>                      | <span data-ttu-id="9a6b8-143">磁片格式</span><span class="sxs-lookup"><span data-stu-id="9a6b8-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a6b8-144">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-144">1</span></span>     | <span data-ttu-id="9a6b8-145">/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="9a6b8-146">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-146">2</span></span>     | <span data-ttu-id="9a6b8-147">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9a6b8-148">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-148">Write Paths</span></span>



| <span data-ttu-id="9a6b8-149">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-149">Order</span></span> | <span data-ttu-id="9a6b8-150">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-150">Path</span></span>                      | <span data-ttu-id="9a6b8-151">磁片格式</span><span class="sxs-lookup"><span data-stu-id="9a6b8-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a6b8-152">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-152">1</span></span>     | <span data-ttu-id="9a6b8-153">/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="9a6b8-154">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-154">2</span></span>     | <span data-ttu-id="9a6b8-155">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9a6b8-156">移除路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-156">Remove Paths</span></span>



| <span data-ttu-id="9a6b8-157">單</span><span class="sxs-lookup"><span data-stu-id="9a6b8-157">Order</span></span> | <span data-ttu-id="9a6b8-158">路徑</span><span class="sxs-lookup"><span data-stu-id="9a6b8-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9a6b8-159">1</span><span class="sxs-lookup"><span data-stu-id="9a6b8-159">1</span></span>     | <span data-ttu-id="9a6b8-160">/ifd/exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9a6b8-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="9a6b8-161">2</span><span class="sxs-lookup"><span data-stu-id="9a6b8-161">2</span></span>     | <span data-ttu-id="9a6b8-162">/ifd/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a6b8-163">備註</span><span class="sxs-lookup"><span data-stu-id="9a6b8-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a6b8-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a6b8-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a6b8-165">FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9a6b8-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
