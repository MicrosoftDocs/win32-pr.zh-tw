---
description: '[系統狀態] 屬性的相片中繼資料原則。'
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: 系統 GPS。狀態相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993174"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="50a36-103">系統 GPS。狀態相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="50a36-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="50a36-104">[ [系統狀態](../properties/props-system-gps-status.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="50a36-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="50a36-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="50a36-105">PKEY</span></span>

<span data-ttu-id="50a36-106">PKEY \_ GPS \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="50a36-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="50a36-107">容器</span><span class="sxs-lookup"><span data-stu-id="50a36-107">Containers</span></span>

<span data-ttu-id="50a36-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="50a36-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="50a36-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="50a36-109">Read-Only</span></span>

<span data-ttu-id="50a36-110">No</span><span class="sxs-lookup"><span data-stu-id="50a36-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="50a36-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="50a36-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="50a36-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="50a36-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="50a36-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="50a36-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="50a36-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="50a36-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="50a36-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="50a36-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="50a36-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="50a36-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="50a36-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="50a36-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="50a36-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-118">Read Paths</span></span>



| <span data-ttu-id="50a36-119">單</span><span class="sxs-lookup"><span data-stu-id="50a36-119">Order</span></span> | <span data-ttu-id="50a36-120">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-120">Path</span></span>                     | <span data-ttu-id="50a36-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="50a36-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="50a36-122">1</span><span class="sxs-lookup"><span data-stu-id="50a36-122">1</span></span>     | <span data-ttu-id="50a36-123">/app1/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="50a36-124">ascii</span><span class="sxs-lookup"><span data-stu-id="50a36-124">ascii</span></span>       |
| <span data-ttu-id="50a36-125">2</span><span class="sxs-lookup"><span data-stu-id="50a36-125">2</span></span>     | <span data-ttu-id="50a36-126">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="50a36-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="50a36-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="50a36-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="50a36-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-128">Write Paths</span></span>



| <span data-ttu-id="50a36-129">單</span><span class="sxs-lookup"><span data-stu-id="50a36-129">Order</span></span> | <span data-ttu-id="50a36-130">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-130">Path</span></span>                     | <span data-ttu-id="50a36-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="50a36-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="50a36-132">1</span><span class="sxs-lookup"><span data-stu-id="50a36-132">1</span></span>     | <span data-ttu-id="50a36-133">/app1/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="50a36-134">ascii</span><span class="sxs-lookup"><span data-stu-id="50a36-134">ascii</span></span>       |
| <span data-ttu-id="50a36-135">2</span><span class="sxs-lookup"><span data-stu-id="50a36-135">2</span></span>     | <span data-ttu-id="50a36-136">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="50a36-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="50a36-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="50a36-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="50a36-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-138">Remove Paths</span></span>



| <span data-ttu-id="50a36-139">單</span><span class="sxs-lookup"><span data-stu-id="50a36-139">Order</span></span> | <span data-ttu-id="50a36-140">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="50a36-141">1</span><span class="sxs-lookup"><span data-stu-id="50a36-141">1</span></span>     | <span data-ttu-id="50a36-142">/app1/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="50a36-143">2</span><span class="sxs-lookup"><span data-stu-id="50a36-143">2</span></span>     | <span data-ttu-id="50a36-144">/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="50a36-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="50a36-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="50a36-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="50a36-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-146">Read Paths</span></span>



| <span data-ttu-id="50a36-147">單</span><span class="sxs-lookup"><span data-stu-id="50a36-147">Order</span></span> | <span data-ttu-id="50a36-148">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-148">Path</span></span>                    | <span data-ttu-id="50a36-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="50a36-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="50a36-150">1</span><span class="sxs-lookup"><span data-stu-id="50a36-150">1</span></span>     | <span data-ttu-id="50a36-151">/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="50a36-152">ascii</span><span class="sxs-lookup"><span data-stu-id="50a36-152">ascii</span></span>       |
| <span data-ttu-id="50a36-153">2</span><span class="sxs-lookup"><span data-stu-id="50a36-153">2</span></span>     | <span data-ttu-id="50a36-154">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="50a36-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="50a36-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="50a36-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="50a36-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-156">Write Paths</span></span>



| <span data-ttu-id="50a36-157">單</span><span class="sxs-lookup"><span data-stu-id="50a36-157">Order</span></span> | <span data-ttu-id="50a36-158">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-158">Path</span></span>                    | <span data-ttu-id="50a36-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="50a36-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="50a36-160">1</span><span class="sxs-lookup"><span data-stu-id="50a36-160">1</span></span>     | <span data-ttu-id="50a36-161">/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="50a36-162">ascii</span><span class="sxs-lookup"><span data-stu-id="50a36-162">ascii</span></span>       |
| <span data-ttu-id="50a36-163">2</span><span class="sxs-lookup"><span data-stu-id="50a36-163">2</span></span>     | <span data-ttu-id="50a36-164">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="50a36-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="50a36-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="50a36-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="50a36-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-166">Remove Paths</span></span>



| <span data-ttu-id="50a36-167">單</span><span class="sxs-lookup"><span data-stu-id="50a36-167">Order</span></span> | <span data-ttu-id="50a36-168">路徑</span><span class="sxs-lookup"><span data-stu-id="50a36-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="50a36-169">1</span><span class="sxs-lookup"><span data-stu-id="50a36-169">1</span></span>     | <span data-ttu-id="50a36-170">/ifd/gps/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="50a36-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="50a36-171">2</span><span class="sxs-lookup"><span data-stu-id="50a36-171">2</span></span>     | <span data-ttu-id="50a36-172">/ifd/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="50a36-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="50a36-173">備註</span><span class="sxs-lookup"><span data-stu-id="50a36-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="50a36-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="50a36-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50a36-175">系統 GPS。狀態</span><span class="sxs-lookup"><span data-stu-id="50a36-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
