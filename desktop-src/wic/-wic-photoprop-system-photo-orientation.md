---
description: '[列印] 屬性的相片中繼資料原則。'
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: 沖印相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027265"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="3b4bc-103">沖印相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="3b4bc-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="3b4bc-104">[ [列印](../properties/props-system-photo-meteringmode.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="3b4bc-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3b4bc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3b4bc-105">PKEY</span></span>

<span data-ttu-id="3b4bc-106">PKEY \_ 相片 \_ 方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="3b4bc-107">容器</span><span class="sxs-lookup"><span data-stu-id="3b4bc-107">Containers</span></span>

<span data-ttu-id="3b4bc-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="3b4bc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3b4bc-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4bc-109">Read-Only</span></span>

<span data-ttu-id="3b4bc-110">No</span><span class="sxs-lookup"><span data-stu-id="3b4bc-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3b4bc-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="3b4bc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3b4bc-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="3b4bc-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="3b4bc-113">Input Type</span></span>

<span data-ttu-id="3b4bc-114">UShort</span><span class="sxs-lookup"><span data-stu-id="3b4bc-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3b4bc-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="3b4bc-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3b4bc-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="3b4bc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3b4bc-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="3b4bc-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3b4bc-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-118">Read Paths</span></span>



| <span data-ttu-id="3b4bc-119">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-119">Order</span></span> | <span data-ttu-id="3b4bc-120">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-120">Path</span></span>                   | <span data-ttu-id="3b4bc-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b4bc-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3b4bc-122">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-122">1</span></span>     | <span data-ttu-id="3b4bc-123">/app1/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="3b4bc-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3b4bc-124">ushort</span></span>      |
| <span data-ttu-id="3b4bc-125">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-125">2</span></span>     | <span data-ttu-id="3b4bc-126">/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="3b4bc-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b4bc-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3b4bc-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-128">Write Paths</span></span>



| <span data-ttu-id="3b4bc-129">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-129">Order</span></span> | <span data-ttu-id="3b4bc-130">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-130">Path</span></span>                   | <span data-ttu-id="3b4bc-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b4bc-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3b4bc-132">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-132">1</span></span>     | <span data-ttu-id="3b4bc-133">/app1/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="3b4bc-134">ushort</span><span class="sxs-lookup"><span data-stu-id="3b4bc-134">ushort</span></span>      |
| <span data-ttu-id="3b4bc-135">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-135">2</span></span>     | <span data-ttu-id="3b4bc-136">/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="3b4bc-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b4bc-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3b4bc-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-138">Remove Paths</span></span>



| <span data-ttu-id="3b4bc-139">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-139">Order</span></span> | <span data-ttu-id="3b4bc-140">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="3b4bc-141">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-141">1</span></span>     | <span data-ttu-id="3b4bc-142">/app1/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="3b4bc-143">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-143">2</span></span>     | <span data-ttu-id="3b4bc-144">/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="3b4bc-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="3b4bc-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3b4bc-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-146">Read Paths</span></span>



| <span data-ttu-id="3b4bc-147">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-147">Order</span></span> | <span data-ttu-id="3b4bc-148">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-148">Path</span></span>                      | <span data-ttu-id="3b4bc-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b4bc-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3b4bc-150">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-150">1</span></span>     | <span data-ttu-id="3b4bc-151">/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="3b4bc-152">ushort</span><span class="sxs-lookup"><span data-stu-id="3b4bc-152">ushort</span></span>      |
| <span data-ttu-id="3b4bc-153">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-153">2</span></span>     | <span data-ttu-id="3b4bc-154">/ifd/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="3b4bc-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b4bc-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3b4bc-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-156">Write Paths</span></span>



| <span data-ttu-id="3b4bc-157">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-157">Order</span></span> | <span data-ttu-id="3b4bc-158">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-158">Path</span></span>                      | <span data-ttu-id="3b4bc-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3b4bc-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3b4bc-160">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-160">1</span></span>     | <span data-ttu-id="3b4bc-161">/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="3b4bc-162">ushort</span><span class="sxs-lookup"><span data-stu-id="3b4bc-162">ushort</span></span>      |
| <span data-ttu-id="3b4bc-163">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-163">2</span></span>     | <span data-ttu-id="3b4bc-164">/ifd/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="3b4bc-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b4bc-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3b4bc-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-166">Remove Paths</span></span>



| <span data-ttu-id="3b4bc-167">單</span><span class="sxs-lookup"><span data-stu-id="3b4bc-167">Order</span></span> | <span data-ttu-id="3b4bc-168">路徑</span><span class="sxs-lookup"><span data-stu-id="3b4bc-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3b4bc-169">1</span><span class="sxs-lookup"><span data-stu-id="3b4bc-169">1</span></span>     | <span data-ttu-id="3b4bc-170">/ifd/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="3b4bc-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="3b4bc-171">2</span><span class="sxs-lookup"><span data-stu-id="3b4bc-171">2</span></span>     | <span data-ttu-id="3b4bc-172">/ifd/xmp/tiff：方向</span><span class="sxs-lookup"><span data-stu-id="3b4bc-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3b4bc-173">備註</span><span class="sxs-lookup"><span data-stu-id="3b4bc-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b4bc-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b4bc-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3b4bc-175">[[列印]](../properties/props-system-photo-meteringmode.md)</span><span class="sxs-lookup"><span data-stu-id="3b4bc-175">[System.Photo.Orientation](../properties/props-system-photo-meteringmode.md)</span></span>
</dt> </dl>

 

 
