---
description: DigitalZoom 屬性的相片中繼資料原則。
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: DigitalZoom 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319947"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="46713-103">DigitalZoom 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="46713-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="46713-104">[DigitalZoom](../properties/props-system-photo-digitalzoom.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="46713-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="46713-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="46713-105">PKEY</span></span>

<span data-ttu-id="46713-106">PKEY \_ 相片 \_ DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="46713-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="46713-107">容器</span><span class="sxs-lookup"><span data-stu-id="46713-107">Containers</span></span>

<span data-ttu-id="46713-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="46713-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="46713-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="46713-109">Read-Only</span></span>

<span data-ttu-id="46713-110">Yes</span><span class="sxs-lookup"><span data-stu-id="46713-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="46713-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="46713-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="46713-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="46713-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="46713-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="46713-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="46713-114">系統會從 DigitalZoomNumerator 和 DigitalZoomDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="46713-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="46713-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="46713-115">It cannot be written directly.</span></span> <span data-ttu-id="46713-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="46713-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="46713-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="46713-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="46713-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="46713-118">Read Paths</span></span>



| <span data-ttu-id="46713-119">單</span><span class="sxs-lookup"><span data-stu-id="46713-119">Order</span></span> | <span data-ttu-id="46713-120">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-120">Path</span></span>                          | <span data-ttu-id="46713-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46713-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="46713-122">1</span><span class="sxs-lookup"><span data-stu-id="46713-122">1</span></span>     | <span data-ttu-id="46713-123">/app1/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="46713-124">2</span><span class="sxs-lookup"><span data-stu-id="46713-124">2</span></span>     | <span data-ttu-id="46713-125">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="46713-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="46713-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="46713-126">Write Paths</span></span>



| <span data-ttu-id="46713-127">單</span><span class="sxs-lookup"><span data-stu-id="46713-127">Order</span></span> | <span data-ttu-id="46713-128">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-128">Path</span></span>                          | <span data-ttu-id="46713-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46713-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="46713-130">1</span><span class="sxs-lookup"><span data-stu-id="46713-130">1</span></span>     | <span data-ttu-id="46713-131">/app1/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="46713-132">2</span><span class="sxs-lookup"><span data-stu-id="46713-132">2</span></span>     | <span data-ttu-id="46713-133">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="46713-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="46713-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="46713-134">Remove Paths</span></span>



| <span data-ttu-id="46713-135">單</span><span class="sxs-lookup"><span data-stu-id="46713-135">Order</span></span> | <span data-ttu-id="46713-136">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="46713-137">1</span><span class="sxs-lookup"><span data-stu-id="46713-137">1</span></span>     | <span data-ttu-id="46713-138">/app1/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="46713-139">2</span><span class="sxs-lookup"><span data-stu-id="46713-139">2</span></span>     | <span data-ttu-id="46713-140">/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="46713-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="46713-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="46713-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="46713-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="46713-142">Read Paths</span></span>



| <span data-ttu-id="46713-143">單</span><span class="sxs-lookup"><span data-stu-id="46713-143">Order</span></span> | <span data-ttu-id="46713-144">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-144">Path</span></span>                           | <span data-ttu-id="46713-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46713-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="46713-146">1</span><span class="sxs-lookup"><span data-stu-id="46713-146">1</span></span>     | <span data-ttu-id="46713-147">/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="46713-148">2</span><span class="sxs-lookup"><span data-stu-id="46713-148">2</span></span>     | <span data-ttu-id="46713-149">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="46713-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="46713-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="46713-150">Write Paths</span></span>



| <span data-ttu-id="46713-151">單</span><span class="sxs-lookup"><span data-stu-id="46713-151">Order</span></span> | <span data-ttu-id="46713-152">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-152">Path</span></span>                           | <span data-ttu-id="46713-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46713-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="46713-154">1</span><span class="sxs-lookup"><span data-stu-id="46713-154">1</span></span>     | <span data-ttu-id="46713-155">/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="46713-156">2</span><span class="sxs-lookup"><span data-stu-id="46713-156">2</span></span>     | <span data-ttu-id="46713-157">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="46713-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="46713-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="46713-158">Remove Paths</span></span>



| <span data-ttu-id="46713-159">單</span><span class="sxs-lookup"><span data-stu-id="46713-159">Order</span></span> | <span data-ttu-id="46713-160">路徑</span><span class="sxs-lookup"><span data-stu-id="46713-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="46713-161">1</span><span class="sxs-lookup"><span data-stu-id="46713-161">1</span></span>     | <span data-ttu-id="46713-162">/ifd/exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="46713-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="46713-163">2</span><span class="sxs-lookup"><span data-stu-id="46713-163">2</span></span>     | <span data-ttu-id="46713-164">/ifd/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="46713-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="46713-165">備註</span><span class="sxs-lookup"><span data-stu-id="46713-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="46713-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="46713-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46713-167">DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="46713-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
