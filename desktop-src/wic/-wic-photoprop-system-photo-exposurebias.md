---
description: ExposureBias 屬性的相片中繼資料原則。
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: ExposureBias 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992060"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="e1741-103">ExposureBias 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="e1741-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="e1741-104">[ExposureBias](../properties/props-system-photo-exposurebias.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="e1741-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e1741-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e1741-105">PKEY</span></span>

<span data-ttu-id="e1741-106">PKEY \_ 相片 \_ ExposureBias</span><span class="sxs-lookup"><span data-stu-id="e1741-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="e1741-107">容器</span><span class="sxs-lookup"><span data-stu-id="e1741-107">Containers</span></span>

<span data-ttu-id="e1741-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="e1741-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e1741-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="e1741-109">Read-Only</span></span>

<span data-ttu-id="e1741-110">Yes</span><span class="sxs-lookup"><span data-stu-id="e1741-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e1741-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="e1741-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e1741-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e1741-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e1741-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="e1741-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e1741-114">系統會從 ExposureBiasNumerator 和 ExposureBiasDenominator 產生此值。</span><span class="sxs-lookup"><span data-stu-id="e1741-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="e1741-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="e1741-115">It cannot be written directly.</span></span> <span data-ttu-id="e1741-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="e1741-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e1741-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="e1741-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e1741-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-118">Read Paths</span></span>



| <span data-ttu-id="e1741-119">單</span><span class="sxs-lookup"><span data-stu-id="e1741-119">Order</span></span> | <span data-ttu-id="e1741-120">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-120">Path</span></span>                          | <span data-ttu-id="e1741-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e1741-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e1741-122">1</span><span class="sxs-lookup"><span data-stu-id="e1741-122">1</span></span>     | <span data-ttu-id="e1741-123">/app1/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="e1741-124">2</span><span class="sxs-lookup"><span data-stu-id="e1741-124">2</span></span>     | <span data-ttu-id="e1741-125">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="e1741-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="e1741-126">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-126">Write Paths</span></span>



| <span data-ttu-id="e1741-127">單</span><span class="sxs-lookup"><span data-stu-id="e1741-127">Order</span></span> | <span data-ttu-id="e1741-128">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-128">Path</span></span>                          | <span data-ttu-id="e1741-129">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e1741-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e1741-130">1</span><span class="sxs-lookup"><span data-stu-id="e1741-130">1</span></span>     | <span data-ttu-id="e1741-131">/app1/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="e1741-132">2</span><span class="sxs-lookup"><span data-stu-id="e1741-132">2</span></span>     | <span data-ttu-id="e1741-133">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="e1741-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e1741-134">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-134">Remove Paths</span></span>



| <span data-ttu-id="e1741-135">單</span><span class="sxs-lookup"><span data-stu-id="e1741-135">Order</span></span> | <span data-ttu-id="e1741-136">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e1741-137">1</span><span class="sxs-lookup"><span data-stu-id="e1741-137">1</span></span>     | <span data-ttu-id="e1741-138">/app1/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="e1741-139">2</span><span class="sxs-lookup"><span data-stu-id="e1741-139">2</span></span>     | <span data-ttu-id="e1741-140">/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="e1741-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="e1741-141">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="e1741-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e1741-142">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-142">Read Paths</span></span>



| <span data-ttu-id="e1741-143">單</span><span class="sxs-lookup"><span data-stu-id="e1741-143">Order</span></span> | <span data-ttu-id="e1741-144">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-144">Path</span></span>                            | <span data-ttu-id="e1741-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e1741-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e1741-146">1</span><span class="sxs-lookup"><span data-stu-id="e1741-146">1</span></span>     | <span data-ttu-id="e1741-147">/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="e1741-148">2</span><span class="sxs-lookup"><span data-stu-id="e1741-148">2</span></span>     | <span data-ttu-id="e1741-149">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="e1741-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e1741-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-150">Write Paths</span></span>



| <span data-ttu-id="e1741-151">單</span><span class="sxs-lookup"><span data-stu-id="e1741-151">Order</span></span> | <span data-ttu-id="e1741-152">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-152">Path</span></span>                            | <span data-ttu-id="e1741-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e1741-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e1741-154">1</span><span class="sxs-lookup"><span data-stu-id="e1741-154">1</span></span>     | <span data-ttu-id="e1741-155">/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="e1741-156">2</span><span class="sxs-lookup"><span data-stu-id="e1741-156">2</span></span>     | <span data-ttu-id="e1741-157">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="e1741-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e1741-158">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-158">Remove Paths</span></span>



| <span data-ttu-id="e1741-159">單</span><span class="sxs-lookup"><span data-stu-id="e1741-159">Order</span></span> | <span data-ttu-id="e1741-160">路徑</span><span class="sxs-lookup"><span data-stu-id="e1741-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="e1741-161">1</span><span class="sxs-lookup"><span data-stu-id="e1741-161">1</span></span>     | <span data-ttu-id="e1741-162">/ifd/exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="e1741-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="e1741-163">2</span><span class="sxs-lookup"><span data-stu-id="e1741-163">2</span></span>     | <span data-ttu-id="e1741-164">/ifd/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="e1741-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1741-165">備註</span><span class="sxs-lookup"><span data-stu-id="e1741-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1741-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1741-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1741-167">ExposureBias</span><span class="sxs-lookup"><span data-stu-id="e1741-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
