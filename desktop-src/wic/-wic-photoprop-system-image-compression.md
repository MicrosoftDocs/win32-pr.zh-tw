---
description: 適用于 [壓縮] 屬性的相片中繼資料原則。
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: 系統映射。壓縮相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992467"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="3b653-103">系統映射。壓縮相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="3b653-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="3b653-104">適用于 [ [壓縮](../properties/props-system-image-compression.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="3b653-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3b653-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3b653-105">PKEY</span></span>

<span data-ttu-id="3b653-106">PKEY \_ 影像 \_ 壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="3b653-107">容器</span><span class="sxs-lookup"><span data-stu-id="3b653-107">Containers</span></span>

<span data-ttu-id="3b653-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="3b653-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3b653-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="3b653-109">Read-Only</span></span>

<span data-ttu-id="3b653-110">Yes</span><span class="sxs-lookup"><span data-stu-id="3b653-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3b653-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="3b653-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3b653-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="3b653-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="3b653-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="3b653-113">Input Type</span></span>

<span data-ttu-id="3b653-114">UShort</span><span class="sxs-lookup"><span data-stu-id="3b653-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3b653-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="3b653-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3b653-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="3b653-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3b653-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="3b653-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3b653-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-118">Read Paths</span></span>



| <span data-ttu-id="3b653-119">單</span><span class="sxs-lookup"><span data-stu-id="3b653-119">Order</span></span> | <span data-ttu-id="3b653-120">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-120">Path</span></span>                   | <span data-ttu-id="3b653-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b653-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3b653-122">1</span><span class="sxs-lookup"><span data-stu-id="3b653-122">1</span></span>     | <span data-ttu-id="3b653-123">/app1/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="3b653-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3b653-124">ushort</span></span>      |
| <span data-ttu-id="3b653-125">2</span><span class="sxs-lookup"><span data-stu-id="3b653-125">2</span></span>     | <span data-ttu-id="3b653-126">/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="3b653-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b653-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3b653-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-128">Write Paths</span></span>



| <span data-ttu-id="3b653-129">單</span><span class="sxs-lookup"><span data-stu-id="3b653-129">Order</span></span> | <span data-ttu-id="3b653-130">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-130">Path</span></span>                   | <span data-ttu-id="3b653-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b653-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3b653-132">1</span><span class="sxs-lookup"><span data-stu-id="3b653-132">1</span></span>     | <span data-ttu-id="3b653-133">/app1/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="3b653-134">ushort</span><span class="sxs-lookup"><span data-stu-id="3b653-134">ushort</span></span>      |
| <span data-ttu-id="3b653-135">2</span><span class="sxs-lookup"><span data-stu-id="3b653-135">2</span></span>     | <span data-ttu-id="3b653-136">/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="3b653-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b653-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3b653-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-138">Remove Paths</span></span>



| <span data-ttu-id="3b653-139">單</span><span class="sxs-lookup"><span data-stu-id="3b653-139">Order</span></span> | <span data-ttu-id="3b653-140">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="3b653-141">1</span><span class="sxs-lookup"><span data-stu-id="3b653-141">1</span></span>     | <span data-ttu-id="3b653-142">/app1/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="3b653-143">2</span><span class="sxs-lookup"><span data-stu-id="3b653-143">2</span></span>     | <span data-ttu-id="3b653-144">/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="3b653-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="3b653-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3b653-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-146">Read Paths</span></span>



| <span data-ttu-id="3b653-147">單</span><span class="sxs-lookup"><span data-stu-id="3b653-147">Order</span></span> | <span data-ttu-id="3b653-148">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-148">Path</span></span>                      | <span data-ttu-id="3b653-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b653-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3b653-150">1</span><span class="sxs-lookup"><span data-stu-id="3b653-150">1</span></span>     | <span data-ttu-id="3b653-151">/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="3b653-152">ushort</span><span class="sxs-lookup"><span data-stu-id="3b653-152">ushort</span></span>      |
| <span data-ttu-id="3b653-153">2</span><span class="sxs-lookup"><span data-stu-id="3b653-153">2</span></span>     | <span data-ttu-id="3b653-154">/ifd/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="3b653-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b653-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3b653-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-156">Write Paths</span></span>



| <span data-ttu-id="3b653-157">單</span><span class="sxs-lookup"><span data-stu-id="3b653-157">Order</span></span> | <span data-ttu-id="3b653-158">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-158">Path</span></span>                      | <span data-ttu-id="3b653-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b653-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3b653-160">1</span><span class="sxs-lookup"><span data-stu-id="3b653-160">1</span></span>     | <span data-ttu-id="3b653-161">/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="3b653-162">ushort</span><span class="sxs-lookup"><span data-stu-id="3b653-162">ushort</span></span>      |
| <span data-ttu-id="3b653-163">2</span><span class="sxs-lookup"><span data-stu-id="3b653-163">2</span></span>     | <span data-ttu-id="3b653-164">/ifd/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="3b653-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b653-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3b653-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-166">Remove Paths</span></span>



| <span data-ttu-id="3b653-167">單</span><span class="sxs-lookup"><span data-stu-id="3b653-167">Order</span></span> | <span data-ttu-id="3b653-168">路徑</span><span class="sxs-lookup"><span data-stu-id="3b653-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3b653-169">1</span><span class="sxs-lookup"><span data-stu-id="3b653-169">1</span></span>     | <span data-ttu-id="3b653-170">/ifd/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="3b653-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="3b653-171">2</span><span class="sxs-lookup"><span data-stu-id="3b653-171">2</span></span>     | <span data-ttu-id="3b653-172">/ifd/xmp/tiff：壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3b653-173">備註</span><span class="sxs-lookup"><span data-stu-id="3b653-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b653-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b653-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b653-175">系統映射壓縮</span><span class="sxs-lookup"><span data-stu-id="3b653-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
