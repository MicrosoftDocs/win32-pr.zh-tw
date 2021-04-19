---
description: CompressedBitsPerPixel 屬性的相片中繼資料原則。
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: CompressedBitsPerPixel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988834"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a><span data-ttu-id="32050-103">CompressedBitsPerPixel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="32050-103">System.Image.CompressedBitsPerPixel Photo Metadata Policy</span></span>

<span data-ttu-id="32050-104">[CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="32050-104">The photo metadata policy for the [System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="32050-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="32050-105">PKEY</span></span>

<span data-ttu-id="32050-106">PKEY \_ 影像 \_ CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="32050-106">PKEY\_Image\_CompressedBitsPerPixel</span></span>

### <a name="containers"></a><span data-ttu-id="32050-107">容器</span><span class="sxs-lookup"><span data-stu-id="32050-107">Containers</span></span>

<span data-ttu-id="32050-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="32050-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="32050-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="32050-109">Read-Only</span></span>

<span data-ttu-id="32050-110">Yes</span><span class="sxs-lookup"><span data-stu-id="32050-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="32050-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="32050-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="32050-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="32050-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="32050-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="32050-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="32050-114">這個值是從 CompressedBitsPerPixelNumerator 和 CompressedBitsPerPixelDenominator 產生的。</span><span class="sxs-lookup"><span data-stu-id="32050-114">This value is generated from System.Image.CompressedBitsPerPixelNumerator and System.Image.CompressedBitsPerPixelDenominator.</span></span> <span data-ttu-id="32050-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="32050-115">It cannot be written directly.</span></span> <span data-ttu-id="32050-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="32050-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="32050-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="32050-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="32050-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="32050-118">Read Paths</span></span>



| <span data-ttu-id="32050-119">單</span><span class="sxs-lookup"><span data-stu-id="32050-119">Order</span></span> | <span data-ttu-id="32050-120">路徑</span><span class="sxs-lookup"><span data-stu-id="32050-120">Path</span></span>                             | <span data-ttu-id="32050-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="32050-121">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="32050-122">1</span><span class="sxs-lookup"><span data-stu-id="32050-122">1</span></span>     | <span data-ttu-id="32050-123">/app1/ifd/exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="32050-123">/app1/ifd/exif/{ushort=37122}</span></span>    |             |
| <span data-ttu-id="32050-124">2</span><span class="sxs-lookup"><span data-stu-id="32050-124">2</span></span>     | <span data-ttu-id="32050-125">/xmp/exif:CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="32050-125">/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="32050-126">移除路徑</span><span class="sxs-lookup"><span data-stu-id="32050-126">Remove Paths</span></span>



| <span data-ttu-id="32050-127">單</span><span class="sxs-lookup"><span data-stu-id="32050-127">Order</span></span> | <span data-ttu-id="32050-128">路徑</span><span class="sxs-lookup"><span data-stu-id="32050-128">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="32050-129">1</span><span class="sxs-lookup"><span data-stu-id="32050-129">1</span></span>     | <span data-ttu-id="32050-130">/app1/ifd/exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="32050-130">/app1/ifd/exif/{ushort=37122}</span></span>    |
| <span data-ttu-id="32050-131">2</span><span class="sxs-lookup"><span data-stu-id="32050-131">2</span></span>     | <span data-ttu-id="32050-132">/xmp/exif:compressedbitsperpixel</span><span class="sxs-lookup"><span data-stu-id="32050-132">/xmp/exif:compressedbitsperpixel</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="32050-133">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="32050-133">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="32050-134">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="32050-134">Read Paths</span></span>



| <span data-ttu-id="32050-135">單</span><span class="sxs-lookup"><span data-stu-id="32050-135">Order</span></span> | <span data-ttu-id="32050-136">路徑</span><span class="sxs-lookup"><span data-stu-id="32050-136">Path</span></span>                                 | <span data-ttu-id="32050-137">磁片格式</span><span class="sxs-lookup"><span data-stu-id="32050-137">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="32050-138">1</span><span class="sxs-lookup"><span data-stu-id="32050-138">1</span></span>     | <span data-ttu-id="32050-139">/ifd/exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="32050-139">/ifd/exif/{ushort=37122}</span></span>             |             |
| <span data-ttu-id="32050-140">2</span><span class="sxs-lookup"><span data-stu-id="32050-140">2</span></span>     | <span data-ttu-id="32050-141">/ifd/xmp/exif:CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="32050-141">/ifd/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="32050-142">移除路徑</span><span class="sxs-lookup"><span data-stu-id="32050-142">Remove Paths</span></span>



| <span data-ttu-id="32050-143">單</span><span class="sxs-lookup"><span data-stu-id="32050-143">Order</span></span> | <span data-ttu-id="32050-144">路徑</span><span class="sxs-lookup"><span data-stu-id="32050-144">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="32050-145">1</span><span class="sxs-lookup"><span data-stu-id="32050-145">1</span></span>     | <span data-ttu-id="32050-146">/ifd/exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="32050-146">/ifd/exif/{ushort=37122}</span></span>             |
| <span data-ttu-id="32050-147">2</span><span class="sxs-lookup"><span data-stu-id="32050-147">2</span></span>     | <span data-ttu-id="32050-148">/ifd/xmp/exif:compressedbitsperpixel</span><span class="sxs-lookup"><span data-stu-id="32050-148">/ifd/xmp/exif:compressedbitsperpixel</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="32050-149">備註</span><span class="sxs-lookup"><span data-stu-id="32050-149">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="32050-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="32050-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32050-151">CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="32050-151">System.Image.CompressedBitsPerPixel</span></span>](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
