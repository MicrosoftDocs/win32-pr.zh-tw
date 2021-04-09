---
description: ProgramMode 屬性的相片中繼資料原則。
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: ProgramMode 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944860"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="8a297-103">ProgramMode 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="8a297-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="8a297-104">[ProgramMode](../properties/props-system-photo-programmode.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="8a297-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8a297-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8a297-105">PKEY</span></span>

<span data-ttu-id="8a297-106">PKEY \_ 相片 \_ ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="8a297-107">容器</span><span class="sxs-lookup"><span data-stu-id="8a297-107">Containers</span></span>

<span data-ttu-id="8a297-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="8a297-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8a297-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="8a297-109">Read-Only</span></span>

<span data-ttu-id="8a297-110">No</span><span class="sxs-lookup"><span data-stu-id="8a297-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8a297-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="8a297-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8a297-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="8a297-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="8a297-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="8a297-113">Input Type</span></span>

<span data-ttu-id="8a297-114">UShort</span><span class="sxs-lookup"><span data-stu-id="8a297-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8a297-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="8a297-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8a297-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="8a297-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8a297-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="8a297-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8a297-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-118">Read Paths</span></span>



| <span data-ttu-id="8a297-119">單</span><span class="sxs-lookup"><span data-stu-id="8a297-119">Order</span></span> | <span data-ttu-id="8a297-120">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-120">Path</span></span>                          | <span data-ttu-id="8a297-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8a297-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8a297-122">1</span><span class="sxs-lookup"><span data-stu-id="8a297-122">1</span></span>     | <span data-ttu-id="8a297-123">/app1/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="8a297-124">ushort</span><span class="sxs-lookup"><span data-stu-id="8a297-124">ushort</span></span>      |
| <span data-ttu-id="8a297-125">2</span><span class="sxs-lookup"><span data-stu-id="8a297-125">2</span></span>     | <span data-ttu-id="8a297-126">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="8a297-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="8a297-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-127">unicode</span></span>     |
| <span data-ttu-id="8a297-128">3</span><span class="sxs-lookup"><span data-stu-id="8a297-128">3</span></span>     | <span data-ttu-id="8a297-129">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="8a297-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8a297-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-131">Write Paths</span></span>



| <span data-ttu-id="8a297-132">單</span><span class="sxs-lookup"><span data-stu-id="8a297-132">Order</span></span> | <span data-ttu-id="8a297-133">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-133">Path</span></span>                          | <span data-ttu-id="8a297-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8a297-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8a297-135">1</span><span class="sxs-lookup"><span data-stu-id="8a297-135">1</span></span>     | <span data-ttu-id="8a297-136">/app1/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="8a297-137">ushort</span><span class="sxs-lookup"><span data-stu-id="8a297-137">ushort</span></span>      |
| <span data-ttu-id="8a297-138">2</span><span class="sxs-lookup"><span data-stu-id="8a297-138">2</span></span>     | <span data-ttu-id="8a297-139">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="8a297-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="8a297-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-140">unicode</span></span>     |
| <span data-ttu-id="8a297-141">3</span><span class="sxs-lookup"><span data-stu-id="8a297-141">3</span></span>     | <span data-ttu-id="8a297-142">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="8a297-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8a297-144">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-144">Remove Paths</span></span>



| <span data-ttu-id="8a297-145">單</span><span class="sxs-lookup"><span data-stu-id="8a297-145">Order</span></span> | <span data-ttu-id="8a297-146">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8a297-147">1</span><span class="sxs-lookup"><span data-stu-id="8a297-147">1</span></span>     | <span data-ttu-id="8a297-148">/app1/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="8a297-149">2</span><span class="sxs-lookup"><span data-stu-id="8a297-149">2</span></span>     | <span data-ttu-id="8a297-150">/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="8a297-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="8a297-151">3</span><span class="sxs-lookup"><span data-stu-id="8a297-151">3</span></span>     | <span data-ttu-id="8a297-152">/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="8a297-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="8a297-153">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="8a297-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8a297-154">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-154">Read Paths</span></span>



| <span data-ttu-id="8a297-155">單</span><span class="sxs-lookup"><span data-stu-id="8a297-155">Order</span></span> | <span data-ttu-id="8a297-156">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-156">Path</span></span>                          | <span data-ttu-id="8a297-157">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8a297-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8a297-158">1</span><span class="sxs-lookup"><span data-stu-id="8a297-158">1</span></span>     | <span data-ttu-id="8a297-159">/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="8a297-160">ushort</span><span class="sxs-lookup"><span data-stu-id="8a297-160">ushort</span></span>      |
| <span data-ttu-id="8a297-161">2</span><span class="sxs-lookup"><span data-stu-id="8a297-161">2</span></span>     | <span data-ttu-id="8a297-162">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="8a297-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="8a297-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-163">unicode</span></span>     |
| <span data-ttu-id="8a297-164">3</span><span class="sxs-lookup"><span data-stu-id="8a297-164">3</span></span>     | <span data-ttu-id="8a297-165">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="8a297-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8a297-167">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-167">Write Paths</span></span>



| <span data-ttu-id="8a297-168">單</span><span class="sxs-lookup"><span data-stu-id="8a297-168">Order</span></span> | <span data-ttu-id="8a297-169">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-169">Path</span></span>                          | <span data-ttu-id="8a297-170">磁片格式</span><span class="sxs-lookup"><span data-stu-id="8a297-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8a297-171">1</span><span class="sxs-lookup"><span data-stu-id="8a297-171">1</span></span>     | <span data-ttu-id="8a297-172">/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="8a297-173">ushort</span><span class="sxs-lookup"><span data-stu-id="8a297-173">ushort</span></span>      |
| <span data-ttu-id="8a297-174">2</span><span class="sxs-lookup"><span data-stu-id="8a297-174">2</span></span>     | <span data-ttu-id="8a297-175">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="8a297-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="8a297-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-176">unicode</span></span>     |
| <span data-ttu-id="8a297-177">3</span><span class="sxs-lookup"><span data-stu-id="8a297-177">3</span></span>     | <span data-ttu-id="8a297-178">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="8a297-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a297-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8a297-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-180">Remove Paths</span></span>



| <span data-ttu-id="8a297-181">單</span><span class="sxs-lookup"><span data-stu-id="8a297-181">Order</span></span> | <span data-ttu-id="8a297-182">路徑</span><span class="sxs-lookup"><span data-stu-id="8a297-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8a297-183">1</span><span class="sxs-lookup"><span data-stu-id="8a297-183">1</span></span>     | <span data-ttu-id="8a297-184">/ifd/exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="8a297-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="8a297-185">2</span><span class="sxs-lookup"><span data-stu-id="8a297-185">2</span></span>     | <span data-ttu-id="8a297-186">/ifd/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="8a297-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="8a297-187">3</span><span class="sxs-lookup"><span data-stu-id="8a297-187">3</span></span>     | <span data-ttu-id="8a297-188">/ifd/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="8a297-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="8a297-189">備註</span><span class="sxs-lookup"><span data-stu-id="8a297-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a297-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a297-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a297-191">ProgramMode</span><span class="sxs-lookup"><span data-stu-id="8a297-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
