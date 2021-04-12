---
description: '[System. Comment] 屬性的相片中繼資料原則。'
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: System. 批註相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320415"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="477ad-103">System. 批註相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="477ad-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="477ad-104">[ [System. Comment](../properties/props-system-comment.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="477ad-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="477ad-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="477ad-105">PKEY</span></span>

<span data-ttu-id="477ad-106">PKEY \_ 批註</span><span class="sxs-lookup"><span data-stu-id="477ad-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="477ad-107">容器</span><span class="sxs-lookup"><span data-stu-id="477ad-107">Containers</span></span>

<span data-ttu-id="477ad-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="477ad-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="477ad-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="477ad-109">Read-Only</span></span>

<span data-ttu-id="477ad-110">No</span><span class="sxs-lookup"><span data-stu-id="477ad-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="477ad-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="477ad-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="477ad-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="477ad-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="477ad-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="477ad-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="477ad-114">VT \_ LPWSTR 或 vt \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="477ad-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="477ad-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="477ad-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="477ad-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="477ad-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="477ad-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="477ad-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="477ad-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-118">Read Paths</span></span>



| <span data-ttu-id="477ad-119">單</span><span class="sxs-lookup"><span data-stu-id="477ad-119">Order</span></span> | <span data-ttu-id="477ad-120">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-120">Path</span></span>                                | <span data-ttu-id="477ad-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="477ad-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="477ad-122">1</span><span class="sxs-lookup"><span data-stu-id="477ad-122">1</span></span>     | <span data-ttu-id="477ad-123">/app1/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="477ad-124">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="477ad-124">unicode\_bytes</span></span> |
| <span data-ttu-id="477ad-125">2</span><span class="sxs-lookup"><span data-stu-id="477ad-125">2</span></span>     | <span data-ttu-id="477ad-126">/app1/ifd/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="477ad-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="477ad-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="477ad-127">unicode</span></span>        |
| <span data-ttu-id="477ad-128">3</span><span class="sxs-lookup"><span data-stu-id="477ad-128">3</span></span>     | <span data-ttu-id="477ad-129">/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="477ad-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="477ad-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="477ad-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="477ad-131">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-131">Write Paths</span></span>



| <span data-ttu-id="477ad-132">單</span><span class="sxs-lookup"><span data-stu-id="477ad-132">Order</span></span> | <span data-ttu-id="477ad-133">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-133">Path</span></span>                     | <span data-ttu-id="477ad-134">磁片格式</span><span class="sxs-lookup"><span data-stu-id="477ad-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="477ad-135">1</span><span class="sxs-lookup"><span data-stu-id="477ad-135">1</span></span>     | <span data-ttu-id="477ad-136">/app1/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="477ad-137">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="477ad-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="477ad-138">移除路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-138">Remove Paths</span></span>



| <span data-ttu-id="477ad-139">單</span><span class="sxs-lookup"><span data-stu-id="477ad-139">Order</span></span> | <span data-ttu-id="477ad-140">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="477ad-141">1</span><span class="sxs-lookup"><span data-stu-id="477ad-141">1</span></span>     | <span data-ttu-id="477ad-142">/app1/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="477ad-143">2</span><span class="sxs-lookup"><span data-stu-id="477ad-143">2</span></span>     | <span data-ttu-id="477ad-144">/app1/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="477ad-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="477ad-145">3</span><span class="sxs-lookup"><span data-stu-id="477ad-145">3</span></span>     | <span data-ttu-id="477ad-146">/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="477ad-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="477ad-147">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="477ad-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="477ad-148">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-148">Read Paths</span></span>



| <span data-ttu-id="477ad-149">單</span><span class="sxs-lookup"><span data-stu-id="477ad-149">Order</span></span> | <span data-ttu-id="477ad-150">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-150">Path</span></span>                                    | <span data-ttu-id="477ad-151">磁片格式</span><span class="sxs-lookup"><span data-stu-id="477ad-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="477ad-152">1</span><span class="sxs-lookup"><span data-stu-id="477ad-152">1</span></span>     | <span data-ttu-id="477ad-153">/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="477ad-154">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="477ad-154">unicode\_bytes</span></span> |
| <span data-ttu-id="477ad-155">2</span><span class="sxs-lookup"><span data-stu-id="477ad-155">2</span></span>     | <span data-ttu-id="477ad-156">/ifd/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="477ad-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="477ad-157">Unicode</span><span class="sxs-lookup"><span data-stu-id="477ad-157">unicode</span></span>        |
| <span data-ttu-id="477ad-158">3</span><span class="sxs-lookup"><span data-stu-id="477ad-158">3</span></span>     | <span data-ttu-id="477ad-159">/ifd/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="477ad-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="477ad-160">Unicode</span><span class="sxs-lookup"><span data-stu-id="477ad-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="477ad-161">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-161">Write Paths</span></span>



| <span data-ttu-id="477ad-162">單</span><span class="sxs-lookup"><span data-stu-id="477ad-162">Order</span></span> | <span data-ttu-id="477ad-163">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-163">Path</span></span>                | <span data-ttu-id="477ad-164">磁片格式</span><span class="sxs-lookup"><span data-stu-id="477ad-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="477ad-165">1</span><span class="sxs-lookup"><span data-stu-id="477ad-165">1</span></span>     | <span data-ttu-id="477ad-166">/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="477ad-167">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="477ad-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="477ad-168">移除路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-168">Remove Paths</span></span>



| <span data-ttu-id="477ad-169">單</span><span class="sxs-lookup"><span data-stu-id="477ad-169">Order</span></span> | <span data-ttu-id="477ad-170">路徑</span><span class="sxs-lookup"><span data-stu-id="477ad-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="477ad-171">1</span><span class="sxs-lookup"><span data-stu-id="477ad-171">1</span></span>     | <span data-ttu-id="477ad-172">/ifd/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="477ad-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="477ad-173">2</span><span class="sxs-lookup"><span data-stu-id="477ad-173">2</span></span>     | <span data-ttu-id="477ad-174">/ifd/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="477ad-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="477ad-175">3</span><span class="sxs-lookup"><span data-stu-id="477ad-175">3</span></span>     | <span data-ttu-id="477ad-176">/ifd/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="477ad-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="477ad-177">備註</span><span class="sxs-lookup"><span data-stu-id="477ad-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="477ad-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="477ad-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="477ad-179">System. Comment</span><span class="sxs-lookup"><span data-stu-id="477ad-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
