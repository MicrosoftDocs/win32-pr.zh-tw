---
description: CameraModel 屬性的相片中繼資料原則。
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: CameraModel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851888"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="218c7-103">CameraModel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="218c7-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="218c7-104">[CameraModel](../properties/props-system-photo-cameramodel.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="218c7-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="218c7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="218c7-105">PKEY</span></span>

<span data-ttu-id="218c7-106">PKEY \_ 相片 \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="218c7-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="218c7-107">容器</span><span class="sxs-lookup"><span data-stu-id="218c7-107">Containers</span></span>

<span data-ttu-id="218c7-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="218c7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="218c7-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="218c7-109">Read-Only</span></span>

<span data-ttu-id="218c7-110">No</span><span class="sxs-lookup"><span data-stu-id="218c7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="218c7-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="218c7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="218c7-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="218c7-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="218c7-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="218c7-113">Input Type</span></span>

<span data-ttu-id="218c7-114">字串。</span><span class="sxs-lookup"><span data-stu-id="218c7-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="218c7-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="218c7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="218c7-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="218c7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="218c7-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="218c7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="218c7-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-118">Read Paths</span></span>



| <span data-ttu-id="218c7-119">單</span><span class="sxs-lookup"><span data-stu-id="218c7-119">Order</span></span> | <span data-ttu-id="218c7-120">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-120">Path</span></span>                   | <span data-ttu-id="218c7-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="218c7-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="218c7-122">1</span><span class="sxs-lookup"><span data-stu-id="218c7-122">1</span></span>     | <span data-ttu-id="218c7-123">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="218c7-124">ascii</span><span class="sxs-lookup"><span data-stu-id="218c7-124">ascii</span></span>       |
| <span data-ttu-id="218c7-125">2</span><span class="sxs-lookup"><span data-stu-id="218c7-125">2</span></span>     | <span data-ttu-id="218c7-126">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="218c7-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-127">unicode</span></span>     |
| <span data-ttu-id="218c7-128">3</span><span class="sxs-lookup"><span data-stu-id="218c7-128">3</span></span>     | <span data-ttu-id="218c7-129">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="218c7-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="218c7-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-131">Write Paths</span></span>



| <span data-ttu-id="218c7-132">單</span><span class="sxs-lookup"><span data-stu-id="218c7-132">Order</span></span> | <span data-ttu-id="218c7-133">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-133">Path</span></span>                   | <span data-ttu-id="218c7-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="218c7-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="218c7-135">1</span><span class="sxs-lookup"><span data-stu-id="218c7-135">1</span></span>     | <span data-ttu-id="218c7-136">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="218c7-137">ascii</span><span class="sxs-lookup"><span data-stu-id="218c7-137">ascii</span></span>       |
| <span data-ttu-id="218c7-138">2</span><span class="sxs-lookup"><span data-stu-id="218c7-138">2</span></span>     | <span data-ttu-id="218c7-139">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="218c7-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-140">unicode</span></span>     |
| <span data-ttu-id="218c7-141">3</span><span class="sxs-lookup"><span data-stu-id="218c7-141">3</span></span>     | <span data-ttu-id="218c7-142">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="218c7-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="218c7-144">移除路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-144">Remove Paths</span></span>



| <span data-ttu-id="218c7-145">單</span><span class="sxs-lookup"><span data-stu-id="218c7-145">Order</span></span> | <span data-ttu-id="218c7-146">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="218c7-147">1</span><span class="sxs-lookup"><span data-stu-id="218c7-147">1</span></span>     | <span data-ttu-id="218c7-148">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="218c7-149">2</span><span class="sxs-lookup"><span data-stu-id="218c7-149">2</span></span>     | <span data-ttu-id="218c7-150">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="218c7-151">3</span><span class="sxs-lookup"><span data-stu-id="218c7-151">3</span></span>     | <span data-ttu-id="218c7-152">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="218c7-153">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="218c7-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="218c7-154">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-154">Read Paths</span></span>



| <span data-ttu-id="218c7-155">單</span><span class="sxs-lookup"><span data-stu-id="218c7-155">Order</span></span> | <span data-ttu-id="218c7-156">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-156">Path</span></span>                | <span data-ttu-id="218c7-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="218c7-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="218c7-158">1</span><span class="sxs-lookup"><span data-stu-id="218c7-158">1</span></span>     | <span data-ttu-id="218c7-159">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="218c7-160">ascii</span><span class="sxs-lookup"><span data-stu-id="218c7-160">ascii</span></span>       |
| <span data-ttu-id="218c7-161">2</span><span class="sxs-lookup"><span data-stu-id="218c7-161">2</span></span>     | <span data-ttu-id="218c7-162">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="218c7-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-163">unicode</span></span>     |
| <span data-ttu-id="218c7-164">3</span><span class="sxs-lookup"><span data-stu-id="218c7-164">3</span></span>     | <span data-ttu-id="218c7-165">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="218c7-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="218c7-167">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-167">Write Paths</span></span>



| <span data-ttu-id="218c7-168">單</span><span class="sxs-lookup"><span data-stu-id="218c7-168">Order</span></span> | <span data-ttu-id="218c7-169">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-169">Path</span></span>                | <span data-ttu-id="218c7-170">磁片格式</span><span class="sxs-lookup"><span data-stu-id="218c7-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="218c7-171">1</span><span class="sxs-lookup"><span data-stu-id="218c7-171">1</span></span>     | <span data-ttu-id="218c7-172">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="218c7-173">ascii</span><span class="sxs-lookup"><span data-stu-id="218c7-173">ascii</span></span>       |
| <span data-ttu-id="218c7-174">2</span><span class="sxs-lookup"><span data-stu-id="218c7-174">2</span></span>     | <span data-ttu-id="218c7-175">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="218c7-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-176">unicode</span></span>     |
| <span data-ttu-id="218c7-177">3</span><span class="sxs-lookup"><span data-stu-id="218c7-177">3</span></span>     | <span data-ttu-id="218c7-178">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="218c7-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="218c7-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="218c7-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-180">Remove Paths</span></span>



| <span data-ttu-id="218c7-181">單</span><span class="sxs-lookup"><span data-stu-id="218c7-181">Order</span></span> | <span data-ttu-id="218c7-182">路徑</span><span class="sxs-lookup"><span data-stu-id="218c7-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="218c7-183">1</span><span class="sxs-lookup"><span data-stu-id="218c7-183">1</span></span>     | <span data-ttu-id="218c7-184">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="218c7-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="218c7-185">2</span><span class="sxs-lookup"><span data-stu-id="218c7-185">2</span></span>     | <span data-ttu-id="218c7-186">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="218c7-187">3</span><span class="sxs-lookup"><span data-stu-id="218c7-187">3</span></span>     | <span data-ttu-id="218c7-188">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="218c7-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="218c7-189">備註</span><span class="sxs-lookup"><span data-stu-id="218c7-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="218c7-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="218c7-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="218c7-191">CameraModel</span><span class="sxs-lookup"><span data-stu-id="218c7-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
