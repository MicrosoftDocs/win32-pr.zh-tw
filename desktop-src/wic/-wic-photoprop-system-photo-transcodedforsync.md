---
description: TranscodedForSync 屬性的相片中繼資料原則。
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: TranscodedForSync 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851211"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="0694d-103">TranscodedForSync 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="0694d-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="0694d-104">[TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="0694d-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0694d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0694d-105">PKEY</span></span>

<span data-ttu-id="0694d-106">PKEY \_ 相片 \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="0694d-107">容器</span><span class="sxs-lookup"><span data-stu-id="0694d-107">Containers</span></span>

<span data-ttu-id="0694d-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="0694d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0694d-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="0694d-109">Read-Only</span></span>

<span data-ttu-id="0694d-110">No</span><span class="sxs-lookup"><span data-stu-id="0694d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0694d-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="0694d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0694d-112">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="0694d-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="0694d-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="0694d-113">Input Type</span></span>

<span data-ttu-id="0694d-114">布林值。</span><span class="sxs-lookup"><span data-stu-id="0694d-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0694d-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="0694d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0694d-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="0694d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0694d-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="0694d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0694d-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-118">Read Paths</span></span>



| <span data-ttu-id="0694d-119">單</span><span class="sxs-lookup"><span data-stu-id="0694d-119">Order</span></span> | <span data-ttu-id="0694d-120">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-120">Path</span></span>                                  | <span data-ttu-id="0694d-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="0694d-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="0694d-122">1</span><span class="sxs-lookup"><span data-stu-id="0694d-122">1</span></span>     | <span data-ttu-id="0694d-123">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="0694d-124">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="0694d-124">bool\_ushort</span></span> |
| <span data-ttu-id="0694d-125">2</span><span class="sxs-lookup"><span data-stu-id="0694d-125">2</span></span>     | <span data-ttu-id="0694d-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="0694d-127">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-127">Write Paths</span></span>



| <span data-ttu-id="0694d-128">單</span><span class="sxs-lookup"><span data-stu-id="0694d-128">Order</span></span> | <span data-ttu-id="0694d-129">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-129">Path</span></span>                                  | <span data-ttu-id="0694d-130">磁片格式</span><span class="sxs-lookup"><span data-stu-id="0694d-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="0694d-131">1</span><span class="sxs-lookup"><span data-stu-id="0694d-131">1</span></span>     | <span data-ttu-id="0694d-132">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="0694d-133">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="0694d-133">bool\_ushort</span></span> |
| <span data-ttu-id="0694d-134">2</span><span class="sxs-lookup"><span data-stu-id="0694d-134">2</span></span>     | <span data-ttu-id="0694d-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="0694d-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-136">Remove Paths</span></span>



| <span data-ttu-id="0694d-137">單</span><span class="sxs-lookup"><span data-stu-id="0694d-137">Order</span></span> | <span data-ttu-id="0694d-138">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="0694d-139">1</span><span class="sxs-lookup"><span data-stu-id="0694d-139">1</span></span>     | <span data-ttu-id="0694d-140">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="0694d-141">2</span><span class="sxs-lookup"><span data-stu-id="0694d-141">2</span></span>     | <span data-ttu-id="0694d-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="0694d-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0694d-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="0694d-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0694d-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-144">Read Paths</span></span>



| <span data-ttu-id="0694d-145">單</span><span class="sxs-lookup"><span data-stu-id="0694d-145">Order</span></span> | <span data-ttu-id="0694d-146">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-146">Path</span></span>                                      | <span data-ttu-id="0694d-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="0694d-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="0694d-148">1</span><span class="sxs-lookup"><span data-stu-id="0694d-148">1</span></span>     | <span data-ttu-id="0694d-149">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="0694d-150">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="0694d-150">bool\_ushort</span></span> |
| <span data-ttu-id="0694d-151">2</span><span class="sxs-lookup"><span data-stu-id="0694d-151">2</span></span>     | <span data-ttu-id="0694d-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="0694d-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-153">Write Paths</span></span>



| <span data-ttu-id="0694d-154">單</span><span class="sxs-lookup"><span data-stu-id="0694d-154">Order</span></span> | <span data-ttu-id="0694d-155">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-155">Path</span></span>                                      | <span data-ttu-id="0694d-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="0694d-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="0694d-157">1</span><span class="sxs-lookup"><span data-stu-id="0694d-157">1</span></span>     | <span data-ttu-id="0694d-158">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="0694d-159">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="0694d-159">bool\_ushort</span></span> |
| <span data-ttu-id="0694d-160">2</span><span class="sxs-lookup"><span data-stu-id="0694d-160">2</span></span>     | <span data-ttu-id="0694d-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="0694d-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-162">Remove Paths</span></span>



| <span data-ttu-id="0694d-163">單</span><span class="sxs-lookup"><span data-stu-id="0694d-163">Order</span></span> | <span data-ttu-id="0694d-164">路徑</span><span class="sxs-lookup"><span data-stu-id="0694d-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="0694d-165">1</span><span class="sxs-lookup"><span data-stu-id="0694d-165">1</span></span>     | <span data-ttu-id="0694d-166">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="0694d-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="0694d-167">2</span><span class="sxs-lookup"><span data-stu-id="0694d-167">2</span></span>     | <span data-ttu-id="0694d-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="0694d-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0694d-169">備註</span><span class="sxs-lookup"><span data-stu-id="0694d-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0694d-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="0694d-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0694d-171">TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="0694d-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
