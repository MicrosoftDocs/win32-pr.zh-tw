---
description: AreaInformation 屬性的相片中繼資料原則。
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: AreaInformation 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319543"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="53a29-103">AreaInformation 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="53a29-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="53a29-104">[AreaInformation](../properties/props-system-gps-areainformation.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="53a29-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="53a29-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="53a29-105">PKEY</span></span>

<span data-ttu-id="53a29-106">PKEY \_ GPS \_ AreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="53a29-107">容器</span><span class="sxs-lookup"><span data-stu-id="53a29-107">Containers</span></span>

<span data-ttu-id="53a29-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="53a29-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="53a29-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-109">Read-Only</span></span>

<span data-ttu-id="53a29-110">No</span><span class="sxs-lookup"><span data-stu-id="53a29-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="53a29-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="53a29-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="53a29-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="53a29-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="53a29-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="53a29-113">Input Type</span></span>

<span data-ttu-id="53a29-114">字串。</span><span class="sxs-lookup"><span data-stu-id="53a29-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="53a29-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="53a29-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="53a29-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="53a29-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="53a29-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="53a29-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="53a29-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-118">Read Paths</span></span>



| <span data-ttu-id="53a29-119">單</span><span class="sxs-lookup"><span data-stu-id="53a29-119">Order</span></span> | <span data-ttu-id="53a29-120">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-120">Path</span></span>                         | <span data-ttu-id="53a29-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="53a29-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="53a29-122">1</span><span class="sxs-lookup"><span data-stu-id="53a29-122">1</span></span>     | <span data-ttu-id="53a29-123">/app1/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="53a29-124">2</span><span class="sxs-lookup"><span data-stu-id="53a29-124">2</span></span>     | <span data-ttu-id="53a29-125">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="53a29-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="53a29-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="53a29-127">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-127">Write Paths</span></span>



| <span data-ttu-id="53a29-128">單</span><span class="sxs-lookup"><span data-stu-id="53a29-128">Order</span></span> | <span data-ttu-id="53a29-129">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-129">Path</span></span>                         | <span data-ttu-id="53a29-130">磁片格式</span><span class="sxs-lookup"><span data-stu-id="53a29-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="53a29-131">1</span><span class="sxs-lookup"><span data-stu-id="53a29-131">1</span></span>     | <span data-ttu-id="53a29-132">/app1/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="53a29-133">2</span><span class="sxs-lookup"><span data-stu-id="53a29-133">2</span></span>     | <span data-ttu-id="53a29-134">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="53a29-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="53a29-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="53a29-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-136">Remove Paths</span></span>



| <span data-ttu-id="53a29-137">單</span><span class="sxs-lookup"><span data-stu-id="53a29-137">Order</span></span> | <span data-ttu-id="53a29-138">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="53a29-139">1</span><span class="sxs-lookup"><span data-stu-id="53a29-139">1</span></span>     | <span data-ttu-id="53a29-140">/app1/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="53a29-141">2</span><span class="sxs-lookup"><span data-stu-id="53a29-141">2</span></span>     | <span data-ttu-id="53a29-142">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="53a29-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="53a29-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="53a29-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-144">Read Paths</span></span>



| <span data-ttu-id="53a29-145">單</span><span class="sxs-lookup"><span data-stu-id="53a29-145">Order</span></span> | <span data-ttu-id="53a29-146">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-146">Path</span></span>                             | <span data-ttu-id="53a29-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="53a29-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="53a29-148">1</span><span class="sxs-lookup"><span data-stu-id="53a29-148">1</span></span>     | <span data-ttu-id="53a29-149">/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="53a29-150">2</span><span class="sxs-lookup"><span data-stu-id="53a29-150">2</span></span>     | <span data-ttu-id="53a29-151">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="53a29-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="53a29-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="53a29-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-153">Write Paths</span></span>



| <span data-ttu-id="53a29-154">單</span><span class="sxs-lookup"><span data-stu-id="53a29-154">Order</span></span> | <span data-ttu-id="53a29-155">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-155">Path</span></span>                             | <span data-ttu-id="53a29-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="53a29-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="53a29-157">1</span><span class="sxs-lookup"><span data-stu-id="53a29-157">1</span></span>     | <span data-ttu-id="53a29-158">/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="53a29-159">2</span><span class="sxs-lookup"><span data-stu-id="53a29-159">2</span></span>     | <span data-ttu-id="53a29-160">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="53a29-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="53a29-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="53a29-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-162">Remove Paths</span></span>



| <span data-ttu-id="53a29-163">單</span><span class="sxs-lookup"><span data-stu-id="53a29-163">Order</span></span> | <span data-ttu-id="53a29-164">路徑</span><span class="sxs-lookup"><span data-stu-id="53a29-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="53a29-165">1</span><span class="sxs-lookup"><span data-stu-id="53a29-165">1</span></span>     | <span data-ttu-id="53a29-166">/ifd/gps/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="53a29-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="53a29-167">2</span><span class="sxs-lookup"><span data-stu-id="53a29-167">2</span></span>     | <span data-ttu-id="53a29-168">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="53a29-169">備註</span><span class="sxs-lookup"><span data-stu-id="53a29-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="53a29-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="53a29-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a29-171">AreaInformation</span><span class="sxs-lookup"><span data-stu-id="53a29-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
