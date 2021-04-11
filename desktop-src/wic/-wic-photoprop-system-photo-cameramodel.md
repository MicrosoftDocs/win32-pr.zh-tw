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
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="f03ff-103">CameraModel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f03ff-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="f03ff-104">[CameraModel](../properties/props-system-photo-cameramodel.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f03ff-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f03ff-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f03ff-105">PKEY</span></span>

<span data-ttu-id="f03ff-106">PKEY \_ 相片 \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="f03ff-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="f03ff-107">容器</span><span class="sxs-lookup"><span data-stu-id="f03ff-107">Containers</span></span>

<span data-ttu-id="f03ff-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f03ff-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f03ff-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f03ff-109">Read-Only</span></span>

<span data-ttu-id="f03ff-110">No</span><span class="sxs-lookup"><span data-stu-id="f03ff-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f03ff-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f03ff-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f03ff-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f03ff-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f03ff-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="f03ff-113">Input Type</span></span>

<span data-ttu-id="f03ff-114">字串。</span><span class="sxs-lookup"><span data-stu-id="f03ff-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f03ff-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f03ff-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f03ff-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="f03ff-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f03ff-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="f03ff-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f03ff-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-118">Read Paths</span></span>



| <span data-ttu-id="f03ff-119">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-119">Order</span></span> | <span data-ttu-id="f03ff-120">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-120">Path</span></span>                   | <span data-ttu-id="f03ff-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f03ff-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f03ff-122">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-122">1</span></span>     | <span data-ttu-id="f03ff-123">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="f03ff-124">ascii</span><span class="sxs-lookup"><span data-stu-id="f03ff-124">ascii</span></span>       |
| <span data-ttu-id="f03ff-125">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-125">2</span></span>     | <span data-ttu-id="f03ff-126">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="f03ff-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-127">unicode</span></span>     |
| <span data-ttu-id="f03ff-128">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-128">3</span></span>     | <span data-ttu-id="f03ff-129">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="f03ff-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f03ff-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-131">Write Paths</span></span>



| <span data-ttu-id="f03ff-132">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-132">Order</span></span> | <span data-ttu-id="f03ff-133">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-133">Path</span></span>                   | <span data-ttu-id="f03ff-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f03ff-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f03ff-135">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-135">1</span></span>     | <span data-ttu-id="f03ff-136">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="f03ff-137">ascii</span><span class="sxs-lookup"><span data-stu-id="f03ff-137">ascii</span></span>       |
| <span data-ttu-id="f03ff-138">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-138">2</span></span>     | <span data-ttu-id="f03ff-139">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="f03ff-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-140">unicode</span></span>     |
| <span data-ttu-id="f03ff-141">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-141">3</span></span>     | <span data-ttu-id="f03ff-142">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="f03ff-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f03ff-144">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-144">Remove Paths</span></span>



| <span data-ttu-id="f03ff-145">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-145">Order</span></span> | <span data-ttu-id="f03ff-146">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="f03ff-147">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-147">1</span></span>     | <span data-ttu-id="f03ff-148">/app1/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="f03ff-149">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-149">2</span></span>     | <span data-ttu-id="f03ff-150">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="f03ff-151">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-151">3</span></span>     | <span data-ttu-id="f03ff-152">/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="f03ff-153">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="f03ff-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f03ff-154">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-154">Read Paths</span></span>



| <span data-ttu-id="f03ff-155">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-155">Order</span></span> | <span data-ttu-id="f03ff-156">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-156">Path</span></span>                | <span data-ttu-id="f03ff-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f03ff-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="f03ff-158">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-158">1</span></span>     | <span data-ttu-id="f03ff-159">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="f03ff-160">ascii</span><span class="sxs-lookup"><span data-stu-id="f03ff-160">ascii</span></span>       |
| <span data-ttu-id="f03ff-161">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-161">2</span></span>     | <span data-ttu-id="f03ff-162">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="f03ff-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-163">unicode</span></span>     |
| <span data-ttu-id="f03ff-164">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-164">3</span></span>     | <span data-ttu-id="f03ff-165">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="f03ff-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f03ff-167">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-167">Write Paths</span></span>



| <span data-ttu-id="f03ff-168">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-168">Order</span></span> | <span data-ttu-id="f03ff-169">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-169">Path</span></span>                | <span data-ttu-id="f03ff-170">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f03ff-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="f03ff-171">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-171">1</span></span>     | <span data-ttu-id="f03ff-172">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="f03ff-173">ascii</span><span class="sxs-lookup"><span data-stu-id="f03ff-173">ascii</span></span>       |
| <span data-ttu-id="f03ff-174">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-174">2</span></span>     | <span data-ttu-id="f03ff-175">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="f03ff-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-176">unicode</span></span>     |
| <span data-ttu-id="f03ff-177">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-177">3</span></span>     | <span data-ttu-id="f03ff-178">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="f03ff-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="f03ff-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f03ff-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-180">Remove Paths</span></span>



| <span data-ttu-id="f03ff-181">單</span><span class="sxs-lookup"><span data-stu-id="f03ff-181">Order</span></span> | <span data-ttu-id="f03ff-182">路徑</span><span class="sxs-lookup"><span data-stu-id="f03ff-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="f03ff-183">1</span><span class="sxs-lookup"><span data-stu-id="f03ff-183">1</span></span>     | <span data-ttu-id="f03ff-184">/ifd/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="f03ff-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="f03ff-185">2</span><span class="sxs-lookup"><span data-stu-id="f03ff-185">2</span></span>     | <span data-ttu-id="f03ff-186">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="f03ff-187">3</span><span class="sxs-lookup"><span data-stu-id="f03ff-187">3</span></span>     | <span data-ttu-id="f03ff-188">/ifd/xmp/tiff：模型</span><span class="sxs-lookup"><span data-stu-id="f03ff-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f03ff-189">備註</span><span class="sxs-lookup"><span data-stu-id="f03ff-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f03ff-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="f03ff-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f03ff-191">CameraModel</span><span class="sxs-lookup"><span data-stu-id="f03ff-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
