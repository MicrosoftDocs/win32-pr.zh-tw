---
description: PhotometricInterpretation 屬性的相片中繼資料原則。
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: PhotometricInterpretation 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980448"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="47fa1-103">PhotometricInterpretation 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="47fa1-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="47fa1-104">[PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="47fa1-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="47fa1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="47fa1-105">PKEY</span></span>

<span data-ttu-id="47fa1-106">PKEY \_ 相片 \_ PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="47fa1-107">容器</span><span class="sxs-lookup"><span data-stu-id="47fa1-107">Containers</span></span>

<span data-ttu-id="47fa1-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="47fa1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="47fa1-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="47fa1-109">Read-Only</span></span>

<span data-ttu-id="47fa1-110">Yes</span><span class="sxs-lookup"><span data-stu-id="47fa1-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="47fa1-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="47fa1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="47fa1-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="47fa1-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="47fa1-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="47fa1-113">Input Type</span></span>

<span data-ttu-id="47fa1-114">UShort</span><span class="sxs-lookup"><span data-stu-id="47fa1-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="47fa1-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="47fa1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="47fa1-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="47fa1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="47fa1-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="47fa1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="47fa1-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-118">Read Paths</span></span>



| <span data-ttu-id="47fa1-119">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-119">Order</span></span> | <span data-ttu-id="47fa1-120">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-120">Path</span></span>                                | <span data-ttu-id="47fa1-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="47fa1-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="47fa1-122">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-122">1</span></span>     | <span data-ttu-id="47fa1-123">/app1/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="47fa1-124">ushort</span><span class="sxs-lookup"><span data-stu-id="47fa1-124">ushort</span></span>      |
| <span data-ttu-id="47fa1-125">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-125">2</span></span>     | <span data-ttu-id="47fa1-126">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="47fa1-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="47fa1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="47fa1-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-128">Write Paths</span></span>



| <span data-ttu-id="47fa1-129">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-129">Order</span></span> | <span data-ttu-id="47fa1-130">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-130">Path</span></span>                                | <span data-ttu-id="47fa1-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="47fa1-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="47fa1-132">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-132">1</span></span>     | <span data-ttu-id="47fa1-133">/app1/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="47fa1-134">ushort</span><span class="sxs-lookup"><span data-stu-id="47fa1-134">ushort</span></span>      |
| <span data-ttu-id="47fa1-135">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-135">2</span></span>     | <span data-ttu-id="47fa1-136">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="47fa1-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="47fa1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="47fa1-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-138">Remove Paths</span></span>



| <span data-ttu-id="47fa1-139">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-139">Order</span></span> | <span data-ttu-id="47fa1-140">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="47fa1-141">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-141">1</span></span>     | <span data-ttu-id="47fa1-142">/app1/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="47fa1-143">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-143">2</span></span>     | <span data-ttu-id="47fa1-144">/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="47fa1-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="47fa1-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="47fa1-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-146">Read Paths</span></span>



| <span data-ttu-id="47fa1-147">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-147">Order</span></span> | <span data-ttu-id="47fa1-148">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-148">Path</span></span>                                    | <span data-ttu-id="47fa1-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="47fa1-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="47fa1-150">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-150">1</span></span>     | <span data-ttu-id="47fa1-151">/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="47fa1-152">ushort</span><span class="sxs-lookup"><span data-stu-id="47fa1-152">ushort</span></span>      |
| <span data-ttu-id="47fa1-153">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-153">2</span></span>     | <span data-ttu-id="47fa1-154">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="47fa1-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="47fa1-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="47fa1-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-156">Write Paths</span></span>



| <span data-ttu-id="47fa1-157">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-157">Order</span></span> | <span data-ttu-id="47fa1-158">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-158">Path</span></span>                                    | <span data-ttu-id="47fa1-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="47fa1-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="47fa1-160">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-160">1</span></span>     | <span data-ttu-id="47fa1-161">/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="47fa1-162">ushort</span><span class="sxs-lookup"><span data-stu-id="47fa1-162">ushort</span></span>      |
| <span data-ttu-id="47fa1-163">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-163">2</span></span>     | <span data-ttu-id="47fa1-164">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="47fa1-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="47fa1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="47fa1-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-166">Remove Paths</span></span>



| <span data-ttu-id="47fa1-167">單</span><span class="sxs-lookup"><span data-stu-id="47fa1-167">Order</span></span> | <span data-ttu-id="47fa1-168">路徑</span><span class="sxs-lookup"><span data-stu-id="47fa1-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="47fa1-169">1</span><span class="sxs-lookup"><span data-stu-id="47fa1-169">1</span></span>     | <span data-ttu-id="47fa1-170">/ifd/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="47fa1-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="47fa1-171">2</span><span class="sxs-lookup"><span data-stu-id="47fa1-171">2</span></span>     | <span data-ttu-id="47fa1-172">/ifd/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="47fa1-173">備註</span><span class="sxs-lookup"><span data-stu-id="47fa1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="47fa1-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="47fa1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fa1-175">PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="47fa1-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
