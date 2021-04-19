---
description: ResolutionUnit 屬性的相片中繼資料原則。
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: ResolutionUnit 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974301"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a><span data-ttu-id="88e45-103">ResolutionUnit 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="88e45-103">System.Image.ResolutionUnit Photo Metadata Policy</span></span>

<span data-ttu-id="88e45-104">[ResolutionUnit](../properties/props-system-image-resolutionunit.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="88e45-104">The photo metadata policy for the [System.Image.ResolutionUnit](../properties/props-system-image-resolutionunit.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="88e45-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="88e45-105">PKEY</span></span>

<span data-ttu-id="88e45-106">PKEY \_ 影像 \_ ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-106">PKEY\_Image\_ResolutionUnit</span></span>

### <a name="containers"></a><span data-ttu-id="88e45-107">容器</span><span class="sxs-lookup"><span data-stu-id="88e45-107">Containers</span></span>

<span data-ttu-id="88e45-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="88e45-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="88e45-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="88e45-109">Read-Only</span></span>

<span data-ttu-id="88e45-110">是。</span><span class="sxs-lookup"><span data-stu-id="88e45-110">Yes.</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="88e45-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="88e45-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="88e45-112">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="88e45-112">VT\_I2</span></span>

### <a name="input-type"></a><span data-ttu-id="88e45-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="88e45-113">Input Type</span></span>

<span data-ttu-id="88e45-114">UShort</span><span class="sxs-lookup"><span data-stu-id="88e45-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="88e45-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="88e45-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="88e45-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="88e45-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="88e45-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="88e45-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="88e45-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-118">Read Paths</span></span>



| <span data-ttu-id="88e45-119">單</span><span class="sxs-lookup"><span data-stu-id="88e45-119">Order</span></span> | <span data-ttu-id="88e45-120">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-120">Path</span></span>                     | <span data-ttu-id="88e45-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="88e45-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="88e45-122">1</span><span class="sxs-lookup"><span data-stu-id="88e45-122">1</span></span>     | <span data-ttu-id="88e45-123">/app1/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-123">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="88e45-124">ushort</span><span class="sxs-lookup"><span data-stu-id="88e45-124">ushort</span></span>      |
| <span data-ttu-id="88e45-125">2</span><span class="sxs-lookup"><span data-stu-id="88e45-125">2</span></span>     | <span data-ttu-id="88e45-126">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-126">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="88e45-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="88e45-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="88e45-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-128">Write Paths</span></span>



| <span data-ttu-id="88e45-129">單</span><span class="sxs-lookup"><span data-stu-id="88e45-129">Order</span></span> | <span data-ttu-id="88e45-130">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-130">Path</span></span>                     | <span data-ttu-id="88e45-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="88e45-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="88e45-132">1</span><span class="sxs-lookup"><span data-stu-id="88e45-132">1</span></span>     | <span data-ttu-id="88e45-133">/app1/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-133">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="88e45-134">ushort</span><span class="sxs-lookup"><span data-stu-id="88e45-134">ushort</span></span>      |
| <span data-ttu-id="88e45-135">2</span><span class="sxs-lookup"><span data-stu-id="88e45-135">2</span></span>     | <span data-ttu-id="88e45-136">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-136">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="88e45-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="88e45-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="88e45-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-138">Remove Paths</span></span>



| <span data-ttu-id="88e45-139">單</span><span class="sxs-lookup"><span data-stu-id="88e45-139">Order</span></span> | <span data-ttu-id="88e45-140">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="88e45-141">1</span><span class="sxs-lookup"><span data-stu-id="88e45-141">1</span></span>     | <span data-ttu-id="88e45-142">/app1/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-142">/app1/ifd/{ushort=296}</span></span>   |
| <span data-ttu-id="88e45-143">2</span><span class="sxs-lookup"><span data-stu-id="88e45-143">2</span></span>     | <span data-ttu-id="88e45-144">/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="88e45-144">/xmp/tiff:resolutionunit</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="88e45-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="88e45-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="88e45-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-146">Read Paths</span></span>



| <span data-ttu-id="88e45-147">單</span><span class="sxs-lookup"><span data-stu-id="88e45-147">Order</span></span> | <span data-ttu-id="88e45-148">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-148">Path</span></span>                         | <span data-ttu-id="88e45-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="88e45-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="88e45-150">1</span><span class="sxs-lookup"><span data-stu-id="88e45-150">1</span></span>     | <span data-ttu-id="88e45-151">/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-151">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="88e45-152">ushort</span><span class="sxs-lookup"><span data-stu-id="88e45-152">ushort</span></span>      |
| <span data-ttu-id="88e45-153">2</span><span class="sxs-lookup"><span data-stu-id="88e45-153">2</span></span>     | <span data-ttu-id="88e45-154">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-154">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="88e45-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="88e45-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="88e45-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-156">Write Paths</span></span>



| <span data-ttu-id="88e45-157">單</span><span class="sxs-lookup"><span data-stu-id="88e45-157">Order</span></span> | <span data-ttu-id="88e45-158">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-158">Path</span></span>                         | <span data-ttu-id="88e45-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="88e45-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="88e45-160">1</span><span class="sxs-lookup"><span data-stu-id="88e45-160">1</span></span>     | <span data-ttu-id="88e45-161">/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-161">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="88e45-162">ushort</span><span class="sxs-lookup"><span data-stu-id="88e45-162">ushort</span></span>      |
| <span data-ttu-id="88e45-163">2</span><span class="sxs-lookup"><span data-stu-id="88e45-163">2</span></span>     | <span data-ttu-id="88e45-164">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-164">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="88e45-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="88e45-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="88e45-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-166">Remove Paths</span></span>



| <span data-ttu-id="88e45-167">單</span><span class="sxs-lookup"><span data-stu-id="88e45-167">Order</span></span> | <span data-ttu-id="88e45-168">路徑</span><span class="sxs-lookup"><span data-stu-id="88e45-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="88e45-169">1</span><span class="sxs-lookup"><span data-stu-id="88e45-169">1</span></span>     | <span data-ttu-id="88e45-170">/ifd/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="88e45-170">/ifd/{ushort=296}</span></span>            |
| <span data-ttu-id="88e45-171">2</span><span class="sxs-lookup"><span data-stu-id="88e45-171">2</span></span>     | <span data-ttu-id="88e45-172">/ifd/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="88e45-172">/ifd/xmp/tiff:resolutionunit</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="88e45-173">備註</span><span class="sxs-lookup"><span data-stu-id="88e45-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e45-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="88e45-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e45-175">ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="88e45-175">System.Image.ResolutionUnit</span></span>](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
