---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: 系統 GPS：相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194777"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="54c16-103">系統 GPS：相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="54c16-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="54c16-104">[ [System.object](../properties/props-system-gps-date.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="54c16-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="54c16-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="54c16-105">PKEY</span></span>

<span data-ttu-id="54c16-106">PKEY \_ GPS \_ 日期</span><span class="sxs-lookup"><span data-stu-id="54c16-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="54c16-107">容器</span><span class="sxs-lookup"><span data-stu-id="54c16-107">Containers</span></span>

<span data-ttu-id="54c16-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="54c16-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="54c16-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="54c16-109">Read-Only</span></span>

<span data-ttu-id="54c16-110">No</span><span class="sxs-lookup"><span data-stu-id="54c16-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="54c16-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="54c16-111">Input Type</span></span>

<span data-ttu-id="54c16-112">字串。</span><span class="sxs-lookup"><span data-stu-id="54c16-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="54c16-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="54c16-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="54c16-114">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="54c16-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="54c16-115">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="54c16-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="54c16-116">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-116">Read Paths</span></span>



| <span data-ttu-id="54c16-117">單</span><span class="sxs-lookup"><span data-stu-id="54c16-117">Order</span></span> | <span data-ttu-id="54c16-118">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-118">Path</span></span>                      | <span data-ttu-id="54c16-119">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54c16-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="54c16-120">1</span><span class="sxs-lookup"><span data-stu-id="54c16-120">1</span></span>     | <span data-ttu-id="54c16-121">/app1/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="54c16-122">ascii</span><span class="sxs-lookup"><span data-stu-id="54c16-122">ascii</span></span>       |
| <span data-ttu-id="54c16-123">2</span><span class="sxs-lookup"><span data-stu-id="54c16-123">2</span></span>     | <span data-ttu-id="54c16-124">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="54c16-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="54c16-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="54c16-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-126">Write Paths</span></span>



| <span data-ttu-id="54c16-127">單</span><span class="sxs-lookup"><span data-stu-id="54c16-127">Order</span></span> | <span data-ttu-id="54c16-128">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-128">Path</span></span>                      | <span data-ttu-id="54c16-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54c16-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="54c16-130">1</span><span class="sxs-lookup"><span data-stu-id="54c16-130">1</span></span>     | <span data-ttu-id="54c16-131">/app1/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="54c16-132">ascii</span><span class="sxs-lookup"><span data-stu-id="54c16-132">ascii</span></span>       |
| <span data-ttu-id="54c16-133">2</span><span class="sxs-lookup"><span data-stu-id="54c16-133">2</span></span>     | <span data-ttu-id="54c16-134">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="54c16-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="54c16-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="54c16-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-136">Remove Paths</span></span>



| <span data-ttu-id="54c16-137">單</span><span class="sxs-lookup"><span data-stu-id="54c16-137">Order</span></span> | <span data-ttu-id="54c16-138">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="54c16-139">1</span><span class="sxs-lookup"><span data-stu-id="54c16-139">1</span></span>     | <span data-ttu-id="54c16-140">/app1/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="54c16-141">2</span><span class="sxs-lookup"><span data-stu-id="54c16-141">2</span></span>     | <span data-ttu-id="54c16-142">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="54c16-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="54c16-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="54c16-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-144">Read Paths</span></span>



| <span data-ttu-id="54c16-145">單</span><span class="sxs-lookup"><span data-stu-id="54c16-145">Order</span></span> | <span data-ttu-id="54c16-146">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-146">Path</span></span>                       | <span data-ttu-id="54c16-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54c16-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="54c16-148">1</span><span class="sxs-lookup"><span data-stu-id="54c16-148">1</span></span>     | <span data-ttu-id="54c16-149">/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="54c16-150">ascii</span><span class="sxs-lookup"><span data-stu-id="54c16-150">ascii</span></span>       |
| <span data-ttu-id="54c16-151">2</span><span class="sxs-lookup"><span data-stu-id="54c16-151">2</span></span>     | <span data-ttu-id="54c16-152">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="54c16-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="54c16-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="54c16-154">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-154">Write Paths</span></span>



| <span data-ttu-id="54c16-155">單</span><span class="sxs-lookup"><span data-stu-id="54c16-155">Order</span></span> | <span data-ttu-id="54c16-156">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-156">Path</span></span>                       | <span data-ttu-id="54c16-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54c16-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="54c16-158">1</span><span class="sxs-lookup"><span data-stu-id="54c16-158">1</span></span>     | <span data-ttu-id="54c16-159">/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="54c16-160">ascii</span><span class="sxs-lookup"><span data-stu-id="54c16-160">ascii</span></span>       |
| <span data-ttu-id="54c16-161">2</span><span class="sxs-lookup"><span data-stu-id="54c16-161">2</span></span>     | <span data-ttu-id="54c16-162">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="54c16-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="54c16-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="54c16-164">移除路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-164">Remove Paths</span></span>



| <span data-ttu-id="54c16-165">單</span><span class="sxs-lookup"><span data-stu-id="54c16-165">Order</span></span> | <span data-ttu-id="54c16-166">路徑</span><span class="sxs-lookup"><span data-stu-id="54c16-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="54c16-167">1</span><span class="sxs-lookup"><span data-stu-id="54c16-167">1</span></span>     | <span data-ttu-id="54c16-168">/ifd/gps/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="54c16-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="54c16-169">2</span><span class="sxs-lookup"><span data-stu-id="54c16-169">2</span></span>     | <span data-ttu-id="54c16-170">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="54c16-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54c16-171">備註</span><span class="sxs-lookup"><span data-stu-id="54c16-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="54c16-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="54c16-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c16-173">系統 GPS。 Date</span><span class="sxs-lookup"><span data-stu-id="54c16-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
