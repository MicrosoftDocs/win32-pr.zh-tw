---
description: SimpleRating 屬性的相片中繼資料原則。
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: SimpleRating 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027260"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="e2547-103">SimpleRating 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="e2547-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="e2547-104">[SimpleRating](../properties/props-system-simplerating.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="e2547-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e2547-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e2547-105">PKEY</span></span>

<span data-ttu-id="e2547-106">PKEY \_ SimpleRating</span><span class="sxs-lookup"><span data-stu-id="e2547-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="e2547-107">容器</span><span class="sxs-lookup"><span data-stu-id="e2547-107">Containers</span></span>

<span data-ttu-id="e2547-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="e2547-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e2547-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="e2547-109">Read-Only</span></span>

<span data-ttu-id="e2547-110">No</span><span class="sxs-lookup"><span data-stu-id="e2547-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e2547-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="e2547-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e2547-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e2547-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e2547-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="e2547-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e2547-114">可能是 VT \_ UI1、vt \_ UI2 或 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="e2547-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="e2547-115">整數值的範圍可以從0到5。</span><span class="sxs-lookup"><span data-stu-id="e2547-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e2547-116">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="e2547-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="e2547-117">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="e2547-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e2547-118">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="e2547-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2547-119">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-119">Read Paths</span></span>



| <span data-ttu-id="e2547-120">單</span><span class="sxs-lookup"><span data-stu-id="e2547-120">Order</span></span> | <span data-ttu-id="e2547-121">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-121">Path</span></span>                     | <span data-ttu-id="e2547-122">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e2547-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e2547-123">1</span><span class="sxs-lookup"><span data-stu-id="e2547-123">1</span></span>     | <span data-ttu-id="e2547-124">/app1/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="e2547-125">ushort</span><span class="sxs-lookup"><span data-stu-id="e2547-125">ushort</span></span>      |
| <span data-ttu-id="e2547-126">2</span><span class="sxs-lookup"><span data-stu-id="e2547-126">2</span></span>     | <span data-ttu-id="e2547-127">/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="e2547-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2547-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e2547-129">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-129">Write Paths</span></span>



| <span data-ttu-id="e2547-130">單</span><span class="sxs-lookup"><span data-stu-id="e2547-130">Order</span></span> | <span data-ttu-id="e2547-131">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-131">Path</span></span>                     | <span data-ttu-id="e2547-132">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e2547-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e2547-133">1</span><span class="sxs-lookup"><span data-stu-id="e2547-133">1</span></span>     | <span data-ttu-id="e2547-134">/app1/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="e2547-135">ushort</span><span class="sxs-lookup"><span data-stu-id="e2547-135">ushort</span></span>      |
| <span data-ttu-id="e2547-136">2</span><span class="sxs-lookup"><span data-stu-id="e2547-136">2</span></span>     | <span data-ttu-id="e2547-137">/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="e2547-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2547-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e2547-139">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-139">Remove Paths</span></span>



| <span data-ttu-id="e2547-140">單</span><span class="sxs-lookup"><span data-stu-id="e2547-140">Order</span></span> | <span data-ttu-id="e2547-141">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e2547-142">1</span><span class="sxs-lookup"><span data-stu-id="e2547-142">1</span></span>     | <span data-ttu-id="e2547-143">/app1/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="e2547-144">2</span><span class="sxs-lookup"><span data-stu-id="e2547-144">2</span></span>     | <span data-ttu-id="e2547-145">/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="e2547-146">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="e2547-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2547-147">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-147">Read Paths</span></span>



| <span data-ttu-id="e2547-148">單</span><span class="sxs-lookup"><span data-stu-id="e2547-148">Order</span></span> | <span data-ttu-id="e2547-149">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-149">Path</span></span>                | <span data-ttu-id="e2547-150">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e2547-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="e2547-151">1</span><span class="sxs-lookup"><span data-stu-id="e2547-151">1</span></span>     | <span data-ttu-id="e2547-152">/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="e2547-153">ushort</span><span class="sxs-lookup"><span data-stu-id="e2547-153">ushort</span></span>      |
| <span data-ttu-id="e2547-154">2</span><span class="sxs-lookup"><span data-stu-id="e2547-154">2</span></span>     | <span data-ttu-id="e2547-155">/ifd/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="e2547-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2547-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e2547-157">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-157">Write Paths</span></span>



| <span data-ttu-id="e2547-158">單</span><span class="sxs-lookup"><span data-stu-id="e2547-158">Order</span></span> | <span data-ttu-id="e2547-159">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-159">Path</span></span>                | <span data-ttu-id="e2547-160">磁片格式</span><span class="sxs-lookup"><span data-stu-id="e2547-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="e2547-161">1</span><span class="sxs-lookup"><span data-stu-id="e2547-161">1</span></span>     | <span data-ttu-id="e2547-162">/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="e2547-163">ushort</span><span class="sxs-lookup"><span data-stu-id="e2547-163">ushort</span></span>      |
| <span data-ttu-id="e2547-164">2</span><span class="sxs-lookup"><span data-stu-id="e2547-164">2</span></span>     | <span data-ttu-id="e2547-165">/ifd/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="e2547-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2547-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e2547-167">移除路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-167">Remove Paths</span></span>



| <span data-ttu-id="e2547-168">單</span><span class="sxs-lookup"><span data-stu-id="e2547-168">Order</span></span> | <span data-ttu-id="e2547-169">路徑</span><span class="sxs-lookup"><span data-stu-id="e2547-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="e2547-170">1</span><span class="sxs-lookup"><span data-stu-id="e2547-170">1</span></span>     | <span data-ttu-id="e2547-171">/ifd/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="e2547-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="e2547-172">2</span><span class="sxs-lookup"><span data-stu-id="e2547-172">2</span></span>     | <span data-ttu-id="e2547-173">/ifd/xmp/xmp：評等</span><span class="sxs-lookup"><span data-stu-id="e2547-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2547-174">備註</span><span class="sxs-lookup"><span data-stu-id="e2547-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2547-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2547-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2547-176">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="e2547-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
