---
description: LightSource 屬性的相片中繼資料原則。
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: LightSource 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513952"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="c134e-103">LightSource 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="c134e-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="c134e-104">[LightSource](../properties/props-system-photo-lightsource.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="c134e-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c134e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c134e-105">PKEY</span></span>

<span data-ttu-id="c134e-106">PKEY \_ 相片 \_ LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="c134e-107">容器</span><span class="sxs-lookup"><span data-stu-id="c134e-107">Containers</span></span>

<span data-ttu-id="c134e-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="c134e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c134e-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="c134e-109">Read-Only</span></span>

<span data-ttu-id="c134e-110">No</span><span class="sxs-lookup"><span data-stu-id="c134e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c134e-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="c134e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c134e-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c134e-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="c134e-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="c134e-113">Input Type</span></span>

<span data-ttu-id="c134e-114">UShort</span><span class="sxs-lookup"><span data-stu-id="c134e-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c134e-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="c134e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c134e-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="c134e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c134e-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="c134e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c134e-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-118">Read Paths</span></span>



| <span data-ttu-id="c134e-119">單</span><span class="sxs-lookup"><span data-stu-id="c134e-119">Order</span></span> | <span data-ttu-id="c134e-120">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-120">Path</span></span>                          | <span data-ttu-id="c134e-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c134e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c134e-122">1</span><span class="sxs-lookup"><span data-stu-id="c134e-122">1</span></span>     | <span data-ttu-id="c134e-123">/app1/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="c134e-124">ushort</span><span class="sxs-lookup"><span data-stu-id="c134e-124">ushort</span></span>      |
| <span data-ttu-id="c134e-125">2</span><span class="sxs-lookup"><span data-stu-id="c134e-125">2</span></span>     | <span data-ttu-id="c134e-126">/xmp/exif:LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="c134e-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="c134e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c134e-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-128">Write Paths</span></span>



| <span data-ttu-id="c134e-129">單</span><span class="sxs-lookup"><span data-stu-id="c134e-129">Order</span></span> | <span data-ttu-id="c134e-130">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-130">Path</span></span>                          | <span data-ttu-id="c134e-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c134e-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c134e-132">1</span><span class="sxs-lookup"><span data-stu-id="c134e-132">1</span></span>     | <span data-ttu-id="c134e-133">/app1/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="c134e-134">ushort</span><span class="sxs-lookup"><span data-stu-id="c134e-134">ushort</span></span>      |
| <span data-ttu-id="c134e-135">2</span><span class="sxs-lookup"><span data-stu-id="c134e-135">2</span></span>     | <span data-ttu-id="c134e-136">/xmp/exif:LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="c134e-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="c134e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c134e-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-138">Remove Paths</span></span>



| <span data-ttu-id="c134e-139">單</span><span class="sxs-lookup"><span data-stu-id="c134e-139">Order</span></span> | <span data-ttu-id="c134e-140">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c134e-141">1</span><span class="sxs-lookup"><span data-stu-id="c134e-141">1</span></span>     | <span data-ttu-id="c134e-142">/app1/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="c134e-143">2</span><span class="sxs-lookup"><span data-stu-id="c134e-143">2</span></span>     | <span data-ttu-id="c134e-144">/xmp/exif:lightsource</span><span class="sxs-lookup"><span data-stu-id="c134e-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="c134e-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="c134e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c134e-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-146">Read Paths</span></span>



| <span data-ttu-id="c134e-147">單</span><span class="sxs-lookup"><span data-stu-id="c134e-147">Order</span></span> | <span data-ttu-id="c134e-148">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-148">Path</span></span>                      | <span data-ttu-id="c134e-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c134e-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c134e-150">1</span><span class="sxs-lookup"><span data-stu-id="c134e-150">1</span></span>     | <span data-ttu-id="c134e-151">/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="c134e-152">ushort</span><span class="sxs-lookup"><span data-stu-id="c134e-152">ushort</span></span>      |
| <span data-ttu-id="c134e-153">2</span><span class="sxs-lookup"><span data-stu-id="c134e-153">2</span></span>     | <span data-ttu-id="c134e-154">/ifd/xmp/exif:LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="c134e-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="c134e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c134e-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-156">Write Paths</span></span>



| <span data-ttu-id="c134e-157">單</span><span class="sxs-lookup"><span data-stu-id="c134e-157">Order</span></span> | <span data-ttu-id="c134e-158">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-158">Path</span></span>                      | <span data-ttu-id="c134e-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c134e-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c134e-160">1</span><span class="sxs-lookup"><span data-stu-id="c134e-160">1</span></span>     | <span data-ttu-id="c134e-161">/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="c134e-162">ushort</span><span class="sxs-lookup"><span data-stu-id="c134e-162">ushort</span></span>      |
| <span data-ttu-id="c134e-163">2</span><span class="sxs-lookup"><span data-stu-id="c134e-163">2</span></span>     | <span data-ttu-id="c134e-164">/ifd/xmp/exif:LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="c134e-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="c134e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c134e-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-166">Remove Paths</span></span>



| <span data-ttu-id="c134e-167">單</span><span class="sxs-lookup"><span data-stu-id="c134e-167">Order</span></span> | <span data-ttu-id="c134e-168">路徑</span><span class="sxs-lookup"><span data-stu-id="c134e-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c134e-169">1</span><span class="sxs-lookup"><span data-stu-id="c134e-169">1</span></span>     | <span data-ttu-id="c134e-170">/ifd/exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="c134e-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="c134e-171">2</span><span class="sxs-lookup"><span data-stu-id="c134e-171">2</span></span>     | <span data-ttu-id="c134e-172">/ifd/xmp/exif:lightsource</span><span class="sxs-lookup"><span data-stu-id="c134e-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c134e-173">備註</span><span class="sxs-lookup"><span data-stu-id="c134e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c134e-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="c134e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c134e-175">LightSource</span><span class="sxs-lookup"><span data-stu-id="c134e-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
