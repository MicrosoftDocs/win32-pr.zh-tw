---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: System.servicemodel. 速度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988344"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="a6628-103">System.servicemodel. 速度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="a6628-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="a6628-104">System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-gps-speed.md)</span><span class="sxs-lookup"><span data-stu-id="a6628-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a6628-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a6628-105">PKEY</span></span>

<span data-ttu-id="a6628-106">PKEY \_ GPS \_ 速度</span><span class="sxs-lookup"><span data-stu-id="a6628-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="a6628-107">容器</span><span class="sxs-lookup"><span data-stu-id="a6628-107">Containers</span></span>

<span data-ttu-id="a6628-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="a6628-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a6628-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="a6628-109">Read-Only</span></span>

<span data-ttu-id="a6628-110">Yes</span><span class="sxs-lookup"><span data-stu-id="a6628-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a6628-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a6628-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a6628-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a6628-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a6628-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="a6628-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a6628-114">這個值是從 SpeedNumerator 和 SpeedDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="a6628-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="a6628-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="a6628-115">It cannot be written directly.</span></span> <span data-ttu-id="a6628-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="a6628-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a6628-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="a6628-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a6628-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-118">Read Paths</span></span>



| <span data-ttu-id="a6628-119">單</span><span class="sxs-lookup"><span data-stu-id="a6628-119">Order</span></span> | <span data-ttu-id="a6628-120">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-120">Path</span></span>                      | <span data-ttu-id="a6628-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a6628-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a6628-122">1</span><span class="sxs-lookup"><span data-stu-id="a6628-122">1</span></span>     | <span data-ttu-id="a6628-123">/app1/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="a6628-124">2</span><span class="sxs-lookup"><span data-stu-id="a6628-124">2</span></span>     | <span data-ttu-id="a6628-125">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="a6628-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="a6628-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-126">Write Paths</span></span>



| <span data-ttu-id="a6628-127">單</span><span class="sxs-lookup"><span data-stu-id="a6628-127">Order</span></span> | <span data-ttu-id="a6628-128">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-128">Path</span></span>                      | <span data-ttu-id="a6628-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a6628-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a6628-130">1</span><span class="sxs-lookup"><span data-stu-id="a6628-130">1</span></span>     | <span data-ttu-id="a6628-131">/app1/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="a6628-132">2</span><span class="sxs-lookup"><span data-stu-id="a6628-132">2</span></span>     | <span data-ttu-id="a6628-133">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="a6628-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a6628-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-134">Remove Paths</span></span>



| <span data-ttu-id="a6628-135">單</span><span class="sxs-lookup"><span data-stu-id="a6628-135">Order</span></span> | <span data-ttu-id="a6628-136">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a6628-137">1</span><span class="sxs-lookup"><span data-stu-id="a6628-137">1</span></span>     | <span data-ttu-id="a6628-138">/app1/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="a6628-139">2</span><span class="sxs-lookup"><span data-stu-id="a6628-139">2</span></span>     | <span data-ttu-id="a6628-140">/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="a6628-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="a6628-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="a6628-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a6628-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-142">Read Paths</span></span>



| <span data-ttu-id="a6628-143">單</span><span class="sxs-lookup"><span data-stu-id="a6628-143">Order</span></span> | <span data-ttu-id="a6628-144">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-144">Path</span></span>                   | <span data-ttu-id="a6628-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a6628-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a6628-146">1</span><span class="sxs-lookup"><span data-stu-id="a6628-146">1</span></span>     | <span data-ttu-id="a6628-147">/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="a6628-148">2</span><span class="sxs-lookup"><span data-stu-id="a6628-148">2</span></span>     | <span data-ttu-id="a6628-149">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="a6628-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a6628-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-150">Write Paths</span></span>



| <span data-ttu-id="a6628-151">單</span><span class="sxs-lookup"><span data-stu-id="a6628-151">Order</span></span> | <span data-ttu-id="a6628-152">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-152">Path</span></span>                   | <span data-ttu-id="a6628-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a6628-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a6628-154">1</span><span class="sxs-lookup"><span data-stu-id="a6628-154">1</span></span>     | <span data-ttu-id="a6628-155">/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="a6628-156">2</span><span class="sxs-lookup"><span data-stu-id="a6628-156">2</span></span>     | <span data-ttu-id="a6628-157">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="a6628-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a6628-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-158">Remove Paths</span></span>



| <span data-ttu-id="a6628-159">單</span><span class="sxs-lookup"><span data-stu-id="a6628-159">Order</span></span> | <span data-ttu-id="a6628-160">路徑</span><span class="sxs-lookup"><span data-stu-id="a6628-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="a6628-161">1</span><span class="sxs-lookup"><span data-stu-id="a6628-161">1</span></span>     | <span data-ttu-id="a6628-162">/ifd/gps/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="a6628-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="a6628-163">2</span><span class="sxs-lookup"><span data-stu-id="a6628-163">2</span></span>     | <span data-ttu-id="a6628-164">/ifd/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="a6628-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6628-165">備註</span><span class="sxs-lookup"><span data-stu-id="a6628-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6628-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6628-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6628-167">GPS. 速度</span><span class="sxs-lookup"><span data-stu-id="a6628-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
