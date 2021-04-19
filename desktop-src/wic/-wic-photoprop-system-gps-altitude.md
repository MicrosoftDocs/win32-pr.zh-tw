---
description: 適用于 [海拔] 屬性的相片中繼資料原則。
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: 系統 GPS. 高度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987364"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="8f5c0-103">系統 GPS. 高度相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="8f5c0-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="8f5c0-104">適用于 [ [海拔](../properties/props-system-gps-altitude.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8f5c0-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8f5c0-105">PKEY</span></span>

<span data-ttu-id="8f5c0-106">PKEY \_ GPS \_ 高度</span><span class="sxs-lookup"><span data-stu-id="8f5c0-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="8f5c0-107">Description</span><span class="sxs-lookup"><span data-stu-id="8f5c0-107">Description</span></span>

<span data-ttu-id="8f5c0-108">高度會表示為計量中參考的絕對值。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="8f5c0-109">容器</span><span class="sxs-lookup"><span data-stu-id="8f5c0-109">Containers</span></span>

<span data-ttu-id="8f5c0-110">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="8f5c0-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8f5c0-111">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f5c0-111">Read-Only</span></span>

<span data-ttu-id="8f5c0-112">Yes</span><span class="sxs-lookup"><span data-stu-id="8f5c0-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8f5c0-113">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8f5c0-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8f5c0-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="8f5c0-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8f5c0-115">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8f5c0-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8f5c0-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="8f5c0-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8f5c0-117">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="8f5c0-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="8f5c0-118">您可以藉由寫入 system.string 和 system.servicemodel，來寫入這個值的值。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="8f5c0-119">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-119">It cannot be written directly.</span></span> <span data-ttu-id="8f5c0-120">下表中的寫入路徑指出值在產生時可儲存的位置，而不是直接寫入時。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="8f5c0-121">當讀取此值時，會協調來自不同架構的值。</span><span class="sxs-lookup"><span data-stu-id="8f5c0-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8f5c0-122">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="8f5c0-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8f5c0-123">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-123">Read Paths</span></span>



| <span data-ttu-id="8f5c0-124">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-124">Order</span></span> | <span data-ttu-id="8f5c0-125">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-125">Path</span></span>                     | <span data-ttu-id="8f5c0-126">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8f5c0-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8f5c0-127">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-127">1</span></span>     | <span data-ttu-id="8f5c0-128">/app1/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="8f5c0-129">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-129">2</span></span>     | <span data-ttu-id="8f5c0-130">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="8f5c0-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-131">Write Paths</span></span>



| <span data-ttu-id="8f5c0-132">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-132">Order</span></span> | <span data-ttu-id="8f5c0-133">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-133">Path</span></span>                     | <span data-ttu-id="8f5c0-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8f5c0-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8f5c0-135">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-135">1</span></span>     | <span data-ttu-id="8f5c0-136">/app1/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="8f5c0-137">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-137">2</span></span>     | <span data-ttu-id="8f5c0-138">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8f5c0-139">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-139">Remove Paths</span></span>



| <span data-ttu-id="8f5c0-140">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-140">Order</span></span> | <span data-ttu-id="8f5c0-141">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="8f5c0-142">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-142">1</span></span>     | <span data-ttu-id="8f5c0-143">/app1/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="8f5c0-144">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-144">2</span></span>     | <span data-ttu-id="8f5c0-145">/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="8f5c0-146">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="8f5c0-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8f5c0-147">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-147">Read Paths</span></span>



| <span data-ttu-id="8f5c0-148">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-148">Order</span></span> | <span data-ttu-id="8f5c0-149">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-149">Path</span></span>                      | <span data-ttu-id="8f5c0-150">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8f5c0-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8f5c0-151">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-151">1</span></span>     | <span data-ttu-id="8f5c0-152">/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="8f5c0-153">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-153">2</span></span>     | <span data-ttu-id="8f5c0-154">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8f5c0-155">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-155">Write Paths</span></span>



| <span data-ttu-id="8f5c0-156">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-156">Order</span></span> | <span data-ttu-id="8f5c0-157">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-157">Path</span></span>                      | <span data-ttu-id="8f5c0-158">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8f5c0-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8f5c0-159">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-159">1</span></span>     | <span data-ttu-id="8f5c0-160">/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="8f5c0-161">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-161">2</span></span>     | <span data-ttu-id="8f5c0-162">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8f5c0-163">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-163">Remove Paths</span></span>



| <span data-ttu-id="8f5c0-164">單</span><span class="sxs-lookup"><span data-stu-id="8f5c0-164">Order</span></span> | <span data-ttu-id="8f5c0-165">路徑</span><span class="sxs-lookup"><span data-stu-id="8f5c0-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="8f5c0-166">1</span><span class="sxs-lookup"><span data-stu-id="8f5c0-166">1</span></span>     | <span data-ttu-id="8f5c0-167">/ifd/gps/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="8f5c0-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="8f5c0-168">2</span><span class="sxs-lookup"><span data-stu-id="8f5c0-168">2</span></span>     | <span data-ttu-id="8f5c0-169">/ifd/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="8f5c0-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="8f5c0-170">備註</span><span class="sxs-lookup"><span data-stu-id="8f5c0-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f5c0-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f5c0-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5c0-172">GPS</span><span class="sxs-lookup"><span data-stu-id="8f5c0-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
