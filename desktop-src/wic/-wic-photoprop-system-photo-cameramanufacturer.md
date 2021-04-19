---
description: CameraManufacturer 屬性的相片中繼資料原則。
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: CameraManufacturer 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971575"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a><span data-ttu-id="b2719-103">CameraManufacturer 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="b2719-103">System.Photo.CameraManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="b2719-104">[CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="b2719-104">The photo metadata policy for the [System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b2719-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b2719-105">PKEY</span></span>

<span data-ttu-id="b2719-106">PKEY \_ 相片 \_ CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="b2719-106">PKEY\_Photo\_CameraManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="b2719-107">容器</span><span class="sxs-lookup"><span data-stu-id="b2719-107">Containers</span></span>

<span data-ttu-id="b2719-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="b2719-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b2719-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="b2719-109">Read-Only</span></span>

<span data-ttu-id="b2719-110">No</span><span class="sxs-lookup"><span data-stu-id="b2719-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b2719-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="b2719-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b2719-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b2719-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b2719-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="b2719-113">Input Type</span></span>

<span data-ttu-id="b2719-114">字串。</span><span class="sxs-lookup"><span data-stu-id="b2719-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b2719-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="b2719-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b2719-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="b2719-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b2719-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="b2719-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b2719-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-118">Read Paths</span></span>



| <span data-ttu-id="b2719-119">單</span><span class="sxs-lookup"><span data-stu-id="b2719-119">Order</span></span> | <span data-ttu-id="b2719-120">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-120">Path</span></span>                   | <span data-ttu-id="b2719-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="b2719-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b2719-122">1</span><span class="sxs-lookup"><span data-stu-id="b2719-122">1</span></span>     | <span data-ttu-id="b2719-123">/app1/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-123">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="b2719-124">ascii</span><span class="sxs-lookup"><span data-stu-id="b2719-124">ascii</span></span>       |
| <span data-ttu-id="b2719-125">2</span><span class="sxs-lookup"><span data-stu-id="b2719-125">2</span></span>     | <span data-ttu-id="b2719-126">/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-126">/xmp/tiff:Make</span></span>         | <span data-ttu-id="b2719-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-127">unicode</span></span>     |
| <span data-ttu-id="b2719-128">3</span><span class="sxs-lookup"><span data-stu-id="b2719-128">3</span></span>     | <span data-ttu-id="b2719-129">/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-129">/xmp/tiff:make</span></span>         | <span data-ttu-id="b2719-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b2719-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-131">Write Paths</span></span>



| <span data-ttu-id="b2719-132">單</span><span class="sxs-lookup"><span data-stu-id="b2719-132">Order</span></span> | <span data-ttu-id="b2719-133">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-133">Path</span></span>                   | <span data-ttu-id="b2719-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="b2719-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b2719-135">1</span><span class="sxs-lookup"><span data-stu-id="b2719-135">1</span></span>     | <span data-ttu-id="b2719-136">/app1/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-136">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="b2719-137">ascii</span><span class="sxs-lookup"><span data-stu-id="b2719-137">ascii</span></span>       |
| <span data-ttu-id="b2719-138">2</span><span class="sxs-lookup"><span data-stu-id="b2719-138">2</span></span>     | <span data-ttu-id="b2719-139">/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-139">/xmp/tiff:Make</span></span>         | <span data-ttu-id="b2719-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-140">unicode</span></span>     |
| <span data-ttu-id="b2719-141">3</span><span class="sxs-lookup"><span data-stu-id="b2719-141">3</span></span>     | <span data-ttu-id="b2719-142">/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-142">/xmp/tiff:make</span></span>         | <span data-ttu-id="b2719-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b2719-144">移除路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-144">Remove Paths</span></span>



| <span data-ttu-id="b2719-145">單</span><span class="sxs-lookup"><span data-stu-id="b2719-145">Order</span></span> | <span data-ttu-id="b2719-146">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="b2719-147">1</span><span class="sxs-lookup"><span data-stu-id="b2719-147">1</span></span>     | <span data-ttu-id="b2719-148">/app1/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-148">/app1/ifd/{ushort=271}</span></span> |
| <span data-ttu-id="b2719-149">2</span><span class="sxs-lookup"><span data-stu-id="b2719-149">2</span></span>     | <span data-ttu-id="b2719-150">/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-150">/xmp/tiff:Make</span></span>         |
| <span data-ttu-id="b2719-151">3</span><span class="sxs-lookup"><span data-stu-id="b2719-151">3</span></span>     | <span data-ttu-id="b2719-152">/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-152">/xmp/tiff:make</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="b2719-153">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="b2719-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b2719-154">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-154">Read Paths</span></span>



| <span data-ttu-id="b2719-155">單</span><span class="sxs-lookup"><span data-stu-id="b2719-155">Order</span></span> | <span data-ttu-id="b2719-156">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-156">Path</span></span>               | <span data-ttu-id="b2719-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="b2719-157">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="b2719-158">1</span><span class="sxs-lookup"><span data-stu-id="b2719-158">1</span></span>     | <span data-ttu-id="b2719-159">/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-159">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="b2719-160">ascii</span><span class="sxs-lookup"><span data-stu-id="b2719-160">ascii</span></span>       |
| <span data-ttu-id="b2719-161">2</span><span class="sxs-lookup"><span data-stu-id="b2719-161">2</span></span>     | <span data-ttu-id="b2719-162">/ifd/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-162">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="b2719-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-163">unicode</span></span>     |
| <span data-ttu-id="b2719-164">3</span><span class="sxs-lookup"><span data-stu-id="b2719-164">3</span></span>     | <span data-ttu-id="b2719-165">/ifd/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-165">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="b2719-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b2719-167">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-167">Write Paths</span></span>



| <span data-ttu-id="b2719-168">單</span><span class="sxs-lookup"><span data-stu-id="b2719-168">Order</span></span> | <span data-ttu-id="b2719-169">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-169">Path</span></span>               | <span data-ttu-id="b2719-170">磁片格式</span><span class="sxs-lookup"><span data-stu-id="b2719-170">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="b2719-171">1</span><span class="sxs-lookup"><span data-stu-id="b2719-171">1</span></span>     | <span data-ttu-id="b2719-172">/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-172">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="b2719-173">ascii</span><span class="sxs-lookup"><span data-stu-id="b2719-173">ascii</span></span>       |
| <span data-ttu-id="b2719-174">2</span><span class="sxs-lookup"><span data-stu-id="b2719-174">2</span></span>     | <span data-ttu-id="b2719-175">/ifd/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-175">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="b2719-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-176">unicode</span></span>     |
| <span data-ttu-id="b2719-177">3</span><span class="sxs-lookup"><span data-stu-id="b2719-177">3</span></span>     | <span data-ttu-id="b2719-178">/ifd/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-178">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="b2719-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="b2719-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b2719-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-180">Remove Paths</span></span>



| <span data-ttu-id="b2719-181">單</span><span class="sxs-lookup"><span data-stu-id="b2719-181">Order</span></span> | <span data-ttu-id="b2719-182">路徑</span><span class="sxs-lookup"><span data-stu-id="b2719-182">Path</span></span>               |
|-------|--------------------|
| <span data-ttu-id="b2719-183">1</span><span class="sxs-lookup"><span data-stu-id="b2719-183">1</span></span>     | <span data-ttu-id="b2719-184">/ifd/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="b2719-184">/ifd/{ushort=271}</span></span>  |
| <span data-ttu-id="b2719-185">2</span><span class="sxs-lookup"><span data-stu-id="b2719-185">2</span></span>     | <span data-ttu-id="b2719-186">/ifd/xmp/tiff： Make</span><span class="sxs-lookup"><span data-stu-id="b2719-186">/ifd/xmp/tiff:Make</span></span> |
| <span data-ttu-id="b2719-187">3</span><span class="sxs-lookup"><span data-stu-id="b2719-187">3</span></span>     | <span data-ttu-id="b2719-188">/ifd/xmp/tiff： make</span><span class="sxs-lookup"><span data-stu-id="b2719-188">/ifd/xmp/tiff:make</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b2719-189">備註</span><span class="sxs-lookup"><span data-stu-id="b2719-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2719-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2719-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2719-191">CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="b2719-191">System.Photo.CameraManufacturer</span></span>](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
