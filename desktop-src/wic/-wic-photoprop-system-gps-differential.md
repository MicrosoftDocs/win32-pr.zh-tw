---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: 系統 GPS. 差異相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320407"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="69e94-103">系統 GPS. 差異相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="69e94-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="69e94-104">適用于 [system.object](../properties/props-system-gps-differential.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="69e94-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="69e94-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="69e94-105">PKEY</span></span>

<span data-ttu-id="69e94-106">PKEY \_ GPS \_ 差異</span><span class="sxs-lookup"><span data-stu-id="69e94-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="69e94-107">容器</span><span class="sxs-lookup"><span data-stu-id="69e94-107">Containers</span></span>

<span data-ttu-id="69e94-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="69e94-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="69e94-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="69e94-109">Read-Only</span></span>

<span data-ttu-id="69e94-110">No</span><span class="sxs-lookup"><span data-stu-id="69e94-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="69e94-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="69e94-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="69e94-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="69e94-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="69e94-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="69e94-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="69e94-114">VT \_ UI1、vt \_ UI2 和 vt \_ UI4 全都接受。</span><span class="sxs-lookup"><span data-stu-id="69e94-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="69e94-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="69e94-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="69e94-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="69e94-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="69e94-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="69e94-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="69e94-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-118">Read Paths</span></span>



| <span data-ttu-id="69e94-119">單</span><span class="sxs-lookup"><span data-stu-id="69e94-119">Order</span></span> | <span data-ttu-id="69e94-120">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-120">Path</span></span>                      | <span data-ttu-id="69e94-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="69e94-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="69e94-122">1</span><span class="sxs-lookup"><span data-stu-id="69e94-122">1</span></span>     | <span data-ttu-id="69e94-123">/app1/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="69e94-124">ushort</span><span class="sxs-lookup"><span data-stu-id="69e94-124">ushort</span></span>      |
| <span data-ttu-id="69e94-125">2</span><span class="sxs-lookup"><span data-stu-id="69e94-125">2</span></span>     | <span data-ttu-id="69e94-126">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="69e94-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="69e94-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="69e94-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-128">Write Paths</span></span>



| <span data-ttu-id="69e94-129">單</span><span class="sxs-lookup"><span data-stu-id="69e94-129">Order</span></span> | <span data-ttu-id="69e94-130">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-130">Path</span></span>                      | <span data-ttu-id="69e94-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="69e94-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="69e94-132">1</span><span class="sxs-lookup"><span data-stu-id="69e94-132">1</span></span>     | <span data-ttu-id="69e94-133">/app1/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="69e94-134">ushort</span><span class="sxs-lookup"><span data-stu-id="69e94-134">ushort</span></span>      |
| <span data-ttu-id="69e94-135">2</span><span class="sxs-lookup"><span data-stu-id="69e94-135">2</span></span>     | <span data-ttu-id="69e94-136">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="69e94-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="69e94-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="69e94-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-138">Remove Paths</span></span>



| <span data-ttu-id="69e94-139">單</span><span class="sxs-lookup"><span data-stu-id="69e94-139">Order</span></span> | <span data-ttu-id="69e94-140">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="69e94-141">1</span><span class="sxs-lookup"><span data-stu-id="69e94-141">1</span></span>     | <span data-ttu-id="69e94-142">/app1/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="69e94-143">2</span><span class="sxs-lookup"><span data-stu-id="69e94-143">2</span></span>     | <span data-ttu-id="69e94-144">/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="69e94-145">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="69e94-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="69e94-146">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-146">Read Paths</span></span>



| <span data-ttu-id="69e94-147">單</span><span class="sxs-lookup"><span data-stu-id="69e94-147">Order</span></span> | <span data-ttu-id="69e94-148">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-148">Path</span></span>                          | <span data-ttu-id="69e94-149">磁片格式</span><span class="sxs-lookup"><span data-stu-id="69e94-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="69e94-150">1</span><span class="sxs-lookup"><span data-stu-id="69e94-150">1</span></span>     | <span data-ttu-id="69e94-151">/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="69e94-152">ushort</span><span class="sxs-lookup"><span data-stu-id="69e94-152">ushort</span></span>      |
| <span data-ttu-id="69e94-153">2</span><span class="sxs-lookup"><span data-stu-id="69e94-153">2</span></span>     | <span data-ttu-id="69e94-154">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="69e94-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="69e94-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="69e94-156">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-156">Write Paths</span></span>



| <span data-ttu-id="69e94-157">單</span><span class="sxs-lookup"><span data-stu-id="69e94-157">Order</span></span> | <span data-ttu-id="69e94-158">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-158">Path</span></span>                          | <span data-ttu-id="69e94-159">磁片格式</span><span class="sxs-lookup"><span data-stu-id="69e94-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="69e94-160">1</span><span class="sxs-lookup"><span data-stu-id="69e94-160">1</span></span>     | <span data-ttu-id="69e94-161">/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="69e94-162">ushort</span><span class="sxs-lookup"><span data-stu-id="69e94-162">ushort</span></span>      |
| <span data-ttu-id="69e94-163">2</span><span class="sxs-lookup"><span data-stu-id="69e94-163">2</span></span>     | <span data-ttu-id="69e94-164">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="69e94-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="69e94-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="69e94-166">移除路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-166">Remove Paths</span></span>



| <span data-ttu-id="69e94-167">單</span><span class="sxs-lookup"><span data-stu-id="69e94-167">Order</span></span> | <span data-ttu-id="69e94-168">路徑</span><span class="sxs-lookup"><span data-stu-id="69e94-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="69e94-169">1</span><span class="sxs-lookup"><span data-stu-id="69e94-169">1</span></span>     | <span data-ttu-id="69e94-170">/ifd/gps/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="69e94-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="69e94-171">2</span><span class="sxs-lookup"><span data-stu-id="69e94-171">2</span></span>     | <span data-ttu-id="69e94-172">/ifd/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="69e94-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="69e94-173">備註</span><span class="sxs-lookup"><span data-stu-id="69e94-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="69e94-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="69e94-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69e94-175">系統 GPS</span><span class="sxs-lookup"><span data-stu-id="69e94-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
