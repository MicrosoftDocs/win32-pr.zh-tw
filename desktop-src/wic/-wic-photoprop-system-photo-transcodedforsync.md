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
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="ed702-103">TranscodedForSync 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="ed702-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="ed702-104">[TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="ed702-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed702-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ed702-105">PKEY</span></span>

<span data-ttu-id="ed702-106">PKEY \_ 相片 \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="ed702-107">容器</span><span class="sxs-lookup"><span data-stu-id="ed702-107">Containers</span></span>

<span data-ttu-id="ed702-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="ed702-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed702-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed702-109">Read-Only</span></span>

<span data-ttu-id="ed702-110">No</span><span class="sxs-lookup"><span data-stu-id="ed702-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed702-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ed702-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed702-112">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ed702-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="ed702-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="ed702-113">Input Type</span></span>

<span data-ttu-id="ed702-114">布林值。</span><span class="sxs-lookup"><span data-stu-id="ed702-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed702-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="ed702-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed702-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="ed702-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed702-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="ed702-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed702-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-118">Read Paths</span></span>



| <span data-ttu-id="ed702-119">單</span><span class="sxs-lookup"><span data-stu-id="ed702-119">Order</span></span> | <span data-ttu-id="ed702-120">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-120">Path</span></span>                                  | <span data-ttu-id="ed702-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ed702-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="ed702-122">1</span><span class="sxs-lookup"><span data-stu-id="ed702-122">1</span></span>     | <span data-ttu-id="ed702-123">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="ed702-124">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="ed702-124">bool\_ushort</span></span> |
| <span data-ttu-id="ed702-125">2</span><span class="sxs-lookup"><span data-stu-id="ed702-125">2</span></span>     | <span data-ttu-id="ed702-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="ed702-127">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-127">Write Paths</span></span>



| <span data-ttu-id="ed702-128">單</span><span class="sxs-lookup"><span data-stu-id="ed702-128">Order</span></span> | <span data-ttu-id="ed702-129">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-129">Path</span></span>                                  | <span data-ttu-id="ed702-130">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ed702-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="ed702-131">1</span><span class="sxs-lookup"><span data-stu-id="ed702-131">1</span></span>     | <span data-ttu-id="ed702-132">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="ed702-133">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="ed702-133">bool\_ushort</span></span> |
| <span data-ttu-id="ed702-134">2</span><span class="sxs-lookup"><span data-stu-id="ed702-134">2</span></span>     | <span data-ttu-id="ed702-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="ed702-136">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-136">Remove Paths</span></span>



| <span data-ttu-id="ed702-137">單</span><span class="sxs-lookup"><span data-stu-id="ed702-137">Order</span></span> | <span data-ttu-id="ed702-138">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="ed702-139">1</span><span class="sxs-lookup"><span data-stu-id="ed702-139">1</span></span>     | <span data-ttu-id="ed702-140">/app1/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="ed702-141">2</span><span class="sxs-lookup"><span data-stu-id="ed702-141">2</span></span>     | <span data-ttu-id="ed702-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="ed702-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ed702-143">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="ed702-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed702-144">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-144">Read Paths</span></span>



| <span data-ttu-id="ed702-145">單</span><span class="sxs-lookup"><span data-stu-id="ed702-145">Order</span></span> | <span data-ttu-id="ed702-146">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-146">Path</span></span>                                      | <span data-ttu-id="ed702-147">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ed702-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="ed702-148">1</span><span class="sxs-lookup"><span data-stu-id="ed702-148">1</span></span>     | <span data-ttu-id="ed702-149">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="ed702-150">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="ed702-150">bool\_ushort</span></span> |
| <span data-ttu-id="ed702-151">2</span><span class="sxs-lookup"><span data-stu-id="ed702-151">2</span></span>     | <span data-ttu-id="ed702-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="ed702-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-153">Write Paths</span></span>



| <span data-ttu-id="ed702-154">單</span><span class="sxs-lookup"><span data-stu-id="ed702-154">Order</span></span> | <span data-ttu-id="ed702-155">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-155">Path</span></span>                                      | <span data-ttu-id="ed702-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ed702-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="ed702-157">1</span><span class="sxs-lookup"><span data-stu-id="ed702-157">1</span></span>     | <span data-ttu-id="ed702-158">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="ed702-159">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="ed702-159">bool\_ushort</span></span> |
| <span data-ttu-id="ed702-160">2</span><span class="sxs-lookup"><span data-stu-id="ed702-160">2</span></span>     | <span data-ttu-id="ed702-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="ed702-162">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-162">Remove Paths</span></span>



| <span data-ttu-id="ed702-163">單</span><span class="sxs-lookup"><span data-stu-id="ed702-163">Order</span></span> | <span data-ttu-id="ed702-164">路徑</span><span class="sxs-lookup"><span data-stu-id="ed702-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="ed702-165">1</span><span class="sxs-lookup"><span data-stu-id="ed702-165">1</span></span>     | <span data-ttu-id="ed702-166">/ifd/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="ed702-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="ed702-167">2</span><span class="sxs-lookup"><span data-stu-id="ed702-167">2</span></span>     | <span data-ttu-id="ed702-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="ed702-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed702-169">備註</span><span class="sxs-lookup"><span data-stu-id="ed702-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed702-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed702-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed702-171">TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="ed702-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
