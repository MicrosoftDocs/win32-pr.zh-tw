---
description: MakerNote 屬性的相片中繼資料原則。
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: MakerNote 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997140"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a><span data-ttu-id="3698e-103">MakerNote 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="3698e-103">System.Photo.MakerNote Photo Metadata Policy</span></span>

<span data-ttu-id="3698e-104">[MakerNote](../properties/props-system-photo-makernote.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="3698e-104">The photo metadata policy for the [System.Photo.MakerNote](../properties/props-system-photo-makernote.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3698e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3698e-105">PKEY</span></span>

<span data-ttu-id="3698e-106">PKEY \_ 相片 \_ MakerNote</span><span class="sxs-lookup"><span data-stu-id="3698e-106">PKEY\_Photo\_MakerNote</span></span>

### <a name="containers"></a><span data-ttu-id="3698e-107">容器</span><span class="sxs-lookup"><span data-stu-id="3698e-107">Containers</span></span>

<span data-ttu-id="3698e-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="3698e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3698e-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="3698e-109">Read-Only</span></span>

<span data-ttu-id="3698e-110">No</span><span class="sxs-lookup"><span data-stu-id="3698e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3698e-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="3698e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3698e-112">VT \_ 向量 \| VTUI1</span><span class="sxs-lookup"><span data-stu-id="3698e-112">VT\_VECTOR \| VTUI1</span></span>

### <a name="input-type"></a><span data-ttu-id="3698e-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="3698e-113">Input Type</span></span>

<span data-ttu-id="3698e-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="3698e-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3698e-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="3698e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3698e-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="3698e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3698e-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="3698e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3698e-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-118">Read Paths</span></span>



| <span data-ttu-id="3698e-119">單</span><span class="sxs-lookup"><span data-stu-id="3698e-119">Order</span></span> | <span data-ttu-id="3698e-120">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-120">Path</span></span>                          | <span data-ttu-id="3698e-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3698e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3698e-122">1</span><span class="sxs-lookup"><span data-stu-id="3698e-122">1</span></span>     | <span data-ttu-id="3698e-123">/app1/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-123">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3698e-124">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-124">Write Paths</span></span>



| <span data-ttu-id="3698e-125">單</span><span class="sxs-lookup"><span data-stu-id="3698e-125">Order</span></span> | <span data-ttu-id="3698e-126">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-126">Path</span></span>                          | <span data-ttu-id="3698e-127">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3698e-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3698e-128">1</span><span class="sxs-lookup"><span data-stu-id="3698e-128">1</span></span>     | <span data-ttu-id="3698e-129">/app1/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-129">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3698e-130">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-130">Remove Paths</span></span>



| <span data-ttu-id="3698e-131">單</span><span class="sxs-lookup"><span data-stu-id="3698e-131">Order</span></span> | <span data-ttu-id="3698e-132">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-132">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="3698e-133">1</span><span class="sxs-lookup"><span data-stu-id="3698e-133">1</span></span>     | <span data-ttu-id="3698e-134">/app1/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-134">/app1/ifd/exif/{ushort=37500}</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="3698e-135">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="3698e-135">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3698e-136">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-136">Read Paths</span></span>



| <span data-ttu-id="3698e-137">單</span><span class="sxs-lookup"><span data-stu-id="3698e-137">Order</span></span> | <span data-ttu-id="3698e-138">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-138">Path</span></span>                     | <span data-ttu-id="3698e-139">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3698e-139">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3698e-140">1</span><span class="sxs-lookup"><span data-stu-id="3698e-140">1</span></span>     | <span data-ttu-id="3698e-141">/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-141">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3698e-142">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-142">Write Paths</span></span>



| <span data-ttu-id="3698e-143">單</span><span class="sxs-lookup"><span data-stu-id="3698e-143">Order</span></span> | <span data-ttu-id="3698e-144">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-144">Path</span></span>                     | <span data-ttu-id="3698e-145">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3698e-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3698e-146">1</span><span class="sxs-lookup"><span data-stu-id="3698e-146">1</span></span>     | <span data-ttu-id="3698e-147">/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-147">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3698e-148">移除路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-148">Remove Paths</span></span>



| <span data-ttu-id="3698e-149">單</span><span class="sxs-lookup"><span data-stu-id="3698e-149">Order</span></span> | <span data-ttu-id="3698e-150">路徑</span><span class="sxs-lookup"><span data-stu-id="3698e-150">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="3698e-151">1</span><span class="sxs-lookup"><span data-stu-id="3698e-151">1</span></span>     | <span data-ttu-id="3698e-152">/ifd/exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="3698e-152">/ifd/exif/{ushort=37500}</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3698e-153">備註</span><span class="sxs-lookup"><span data-stu-id="3698e-153">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3698e-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="3698e-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3698e-155">MakerNote</span><span class="sxs-lookup"><span data-stu-id="3698e-155">System.Photo.MakerNote</span></span>](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
