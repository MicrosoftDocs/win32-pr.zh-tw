---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: '[攝影] 相片中繼資料原則'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980638"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="54b26-103">[攝影] 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="54b26-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="54b26-104">適用于 [system.object](../properties/props-system-photo-aperture.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="54b26-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="54b26-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="54b26-105">PKEY</span></span>

<span data-ttu-id="54b26-106">PKEY \_ 相片 \_ 口徑</span><span class="sxs-lookup"><span data-stu-id="54b26-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="54b26-107">容器</span><span class="sxs-lookup"><span data-stu-id="54b26-107">Containers</span></span>

<span data-ttu-id="54b26-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="54b26-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="54b26-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="54b26-109">Read-Only</span></span>

<span data-ttu-id="54b26-110">Yes</span><span class="sxs-lookup"><span data-stu-id="54b26-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="54b26-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="54b26-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="54b26-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="54b26-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="54b26-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="54b26-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="54b26-114">系統會從 ApertureNumerator 和 ApertureDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="54b26-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="54b26-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="54b26-115">It cannot be written directly.</span></span> <span data-ttu-id="54b26-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="54b26-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="54b26-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="54b26-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="54b26-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-118">Read Paths</span></span>



| <span data-ttu-id="54b26-119">單</span><span class="sxs-lookup"><span data-stu-id="54b26-119">Order</span></span> | <span data-ttu-id="54b26-120">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-120">Path</span></span>                          | <span data-ttu-id="54b26-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54b26-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="54b26-122">1</span><span class="sxs-lookup"><span data-stu-id="54b26-122">1</span></span>     | <span data-ttu-id="54b26-123">/app1/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="54b26-124">2</span><span class="sxs-lookup"><span data-stu-id="54b26-124">2</span></span>     | <span data-ttu-id="54b26-125">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="54b26-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="54b26-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-126">Write Paths</span></span>



| <span data-ttu-id="54b26-127">單</span><span class="sxs-lookup"><span data-stu-id="54b26-127">Order</span></span> | <span data-ttu-id="54b26-128">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-128">Path</span></span>                          | <span data-ttu-id="54b26-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54b26-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="54b26-130">1</span><span class="sxs-lookup"><span data-stu-id="54b26-130">1</span></span>     | <span data-ttu-id="54b26-131">/app1/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="54b26-132">2</span><span class="sxs-lookup"><span data-stu-id="54b26-132">2</span></span>     | <span data-ttu-id="54b26-133">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="54b26-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="54b26-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-134">Remove Paths</span></span>



| <span data-ttu-id="54b26-135">單</span><span class="sxs-lookup"><span data-stu-id="54b26-135">Order</span></span> | <span data-ttu-id="54b26-136">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="54b26-137">1</span><span class="sxs-lookup"><span data-stu-id="54b26-137">1</span></span>     | <span data-ttu-id="54b26-138">/app1/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="54b26-139">2</span><span class="sxs-lookup"><span data-stu-id="54b26-139">2</span></span>     | <span data-ttu-id="54b26-140">/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="54b26-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="54b26-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="54b26-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="54b26-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-142">Read Paths</span></span>



| <span data-ttu-id="54b26-143">單</span><span class="sxs-lookup"><span data-stu-id="54b26-143">Order</span></span> | <span data-ttu-id="54b26-144">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-144">Path</span></span>                        | <span data-ttu-id="54b26-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54b26-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="54b26-146">1</span><span class="sxs-lookup"><span data-stu-id="54b26-146">1</span></span>     | <span data-ttu-id="54b26-147">/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="54b26-148">2</span><span class="sxs-lookup"><span data-stu-id="54b26-148">2</span></span>     | <span data-ttu-id="54b26-149">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="54b26-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="54b26-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-150">Write Paths</span></span>



| <span data-ttu-id="54b26-151">單</span><span class="sxs-lookup"><span data-stu-id="54b26-151">Order</span></span> | <span data-ttu-id="54b26-152">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-152">Path</span></span>                        | <span data-ttu-id="54b26-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="54b26-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="54b26-154">1</span><span class="sxs-lookup"><span data-stu-id="54b26-154">1</span></span>     | <span data-ttu-id="54b26-155">/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="54b26-156">2</span><span class="sxs-lookup"><span data-stu-id="54b26-156">2</span></span>     | <span data-ttu-id="54b26-157">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="54b26-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="54b26-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-158">Remove Paths</span></span>



| <span data-ttu-id="54b26-159">單</span><span class="sxs-lookup"><span data-stu-id="54b26-159">Order</span></span> | <span data-ttu-id="54b26-160">路徑</span><span class="sxs-lookup"><span data-stu-id="54b26-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="54b26-161">1</span><span class="sxs-lookup"><span data-stu-id="54b26-161">1</span></span>     | <span data-ttu-id="54b26-162">/ifd/exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="54b26-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="54b26-163">2</span><span class="sxs-lookup"><span data-stu-id="54b26-163">2</span></span>     | <span data-ttu-id="54b26-164">/ifd/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="54b26-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54b26-165">備註</span><span class="sxs-lookup"><span data-stu-id="54b26-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="54b26-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="54b26-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54b26-167">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="54b26-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
