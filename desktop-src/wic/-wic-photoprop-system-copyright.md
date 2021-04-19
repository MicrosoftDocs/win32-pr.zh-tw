---
description: '[系統著作權] 屬性的相片中繼資料原則。'
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: System. 著作權相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977099"
---
# <a name="systemcopyright-photo-metadata-policy"></a><span data-ttu-id="fed4d-103">System. 著作權相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="fed4d-103">System.Copyright Photo Metadata Policy</span></span>

<span data-ttu-id="fed4d-104">[ [系統著作權](../properties/props-system-copyright.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="fed4d-104">The photo metadata policy for the [System.Copyright](../properties/props-system-copyright.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fed4d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="fed4d-105">PKEY</span></span>

<span data-ttu-id="fed4d-106">PKEY \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="fed4d-106">PKEY\_Copyright</span></span>

### <a name="containers"></a><span data-ttu-id="fed4d-107">容器</span><span class="sxs-lookup"><span data-stu-id="fed4d-107">Containers</span></span>

<span data-ttu-id="fed4d-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="fed4d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fed4d-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="fed4d-109">Read-Only</span></span>

<span data-ttu-id="fed4d-110">No</span><span class="sxs-lookup"><span data-stu-id="fed4d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fed4d-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="fed4d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fed4d-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="fed4d-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="fed4d-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="fed4d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="fed4d-114">String</span><span class="sxs-lookup"><span data-stu-id="fed4d-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fed4d-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="fed4d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fed4d-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="fed4d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fed4d-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="fed4d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fed4d-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-118">Read Paths</span></span>



| <span data-ttu-id="fed4d-119">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-119">Order</span></span> | <span data-ttu-id="fed4d-120">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-120">Path</span></span>                                      | <span data-ttu-id="fed4d-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fed4d-121">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="fed4d-122">/app1/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-122">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="fed4d-123">ascii</span><span class="sxs-lookup"><span data-stu-id="fed4d-123">ascii</span></span>       |
|       | <span data-ttu-id="fed4d-124">/app13/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-124">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="fed4d-125">/xmp/ <xmpalt> dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-125">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="fed4d-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-126">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-127">/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-127">/xmp/dc:rights</span></span>                            | <span data-ttu-id="fed4d-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-128">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-129">/app13/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-129">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fed4d-130">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-130">Write Paths</span></span>



| <span data-ttu-id="fed4d-131">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-131">Order</span></span> | <span data-ttu-id="fed4d-132">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-132">Path</span></span>                                      | <span data-ttu-id="fed4d-133">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fed4d-133">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="fed4d-134">/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-134">/xmp/dc:rights</span></span>                            | <span data-ttu-id="fed4d-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-135">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-136">/xmp/ <xmpalt> dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-136">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="fed4d-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-137">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-138">/app13/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-138">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="fed4d-139">/app1/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-139">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="fed4d-140">ascii</span><span class="sxs-lookup"><span data-stu-id="fed4d-140">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="fed4d-141">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-141">Remove Paths</span></span>



| <span data-ttu-id="fed4d-142">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-142">Order</span></span> | <span data-ttu-id="fed4d-143">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-143">Path</span></span>                                      |
|-------|-------------------------------------------|
|       | <span data-ttu-id="fed4d-144">/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-144">/xmp/dc:rights</span></span>                            |
|       | <span data-ttu-id="fed4d-145">/app13/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-145">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="fed4d-146">/app1/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-146">/app1/ifd/{ushort=33432}</span></span>                  |



 

### <a name="tiff-policy"></a><span data-ttu-id="fed4d-147">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="fed4d-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fed4d-148">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-148">Read Paths</span></span>



| <span data-ttu-id="fed4d-149">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-149">Order</span></span> | <span data-ttu-id="fed4d-150">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-150">Path</span></span>                                    | <span data-ttu-id="fed4d-151">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fed4d-151">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="fed4d-152">/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-152">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="fed4d-153">ascii</span><span class="sxs-lookup"><span data-stu-id="fed4d-153">ascii</span></span>       |
|       | <span data-ttu-id="fed4d-154">/ifd/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-154">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="fed4d-155">/ifd/xmp/ <xmpalt> dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-155">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="fed4d-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-156">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-157">/ifd/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-157">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="fed4d-158">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-158">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-159">/ifd/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-159">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="fed4d-160">/ifd/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-160">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fed4d-161">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-161">Write Paths</span></span>



| <span data-ttu-id="fed4d-162">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-162">Order</span></span> | <span data-ttu-id="fed4d-163">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-163">Path</span></span>                                    | <span data-ttu-id="fed4d-164">磁片格式</span><span class="sxs-lookup"><span data-stu-id="fed4d-164">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="fed4d-165">/ifd/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-165">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="fed4d-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-166">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-167">/ifd/xmp/ <xmpalt> dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-167">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="fed4d-168">Unicode</span><span class="sxs-lookup"><span data-stu-id="fed4d-168">unicode</span></span>     |
|       | <span data-ttu-id="fed4d-169">/ifd/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-169">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="fed4d-170">/ifd/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-170">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="fed4d-171">/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-171">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="fed4d-172">ascii</span><span class="sxs-lookup"><span data-stu-id="fed4d-172">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="fed4d-173">移除路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-173">Remove Paths</span></span>



| <span data-ttu-id="fed4d-174">單</span><span class="sxs-lookup"><span data-stu-id="fed4d-174">Order</span></span> | <span data-ttu-id="fed4d-175">路徑</span><span class="sxs-lookup"><span data-stu-id="fed4d-175">Path</span></span>                                    |
|-------|-----------------------------------------|
|       | <span data-ttu-id="fed4d-176">/ifd/xmp/dc：許可權</span><span class="sxs-lookup"><span data-stu-id="fed4d-176">/ifd/xmp/dc:rights</span></span>                      |
|       | <span data-ttu-id="fed4d-177">/ifd/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-177">/ifd/iptc/copyright notice</span></span>              |
|       | <span data-ttu-id="fed4d-178">/ifd/irb/8bimiptc/iptc/copyright 通知</span><span class="sxs-lookup"><span data-stu-id="fed4d-178">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="fed4d-179">/ifd/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="fed4d-179">/ifd/{ushort=33432}</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="fed4d-180">備註</span><span class="sxs-lookup"><span data-stu-id="fed4d-180">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fed4d-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="fed4d-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fed4d-182">系統著作權</span><span class="sxs-lookup"><span data-stu-id="fed4d-182">System.Copyright</span></span>](../properties/props-system-copyright.md)
</dt> </dl>

 

 
