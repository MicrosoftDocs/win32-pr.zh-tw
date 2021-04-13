---
description: '[系統評分] 屬性的相片中繼資料原則。'
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: System. 評分相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319847"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="855cf-103">System. 評分相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="855cf-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="855cf-104">[ [系統評分](../properties/props-system-rating.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="855cf-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="855cf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="855cf-105">PKEY</span></span>

<span data-ttu-id="855cf-106">PKEY \_ 評等</span><span class="sxs-lookup"><span data-stu-id="855cf-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="855cf-107">容器</span><span class="sxs-lookup"><span data-stu-id="855cf-107">Containers</span></span>

<span data-ttu-id="855cf-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="855cf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="855cf-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="855cf-109">Read-Only</span></span>

<span data-ttu-id="855cf-110">No</span><span class="sxs-lookup"><span data-stu-id="855cf-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="855cf-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="855cf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="855cf-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="855cf-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="855cf-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="855cf-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="855cf-114">可能是 VT \_ UI1、vt \_ UI2 或 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="855cf-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="855cf-115">值的範圍可以從0到99。</span><span class="sxs-lookup"><span data-stu-id="855cf-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="855cf-116">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="855cf-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="855cf-117">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="855cf-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="855cf-118">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="855cf-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="855cf-119">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-119">Read Paths</span></span>



| <span data-ttu-id="855cf-120">單</span><span class="sxs-lookup"><span data-stu-id="855cf-120">Order</span></span> | <span data-ttu-id="855cf-121">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-121">Path</span></span>                       | <span data-ttu-id="855cf-122">磁片格式</span><span class="sxs-lookup"><span data-stu-id="855cf-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="855cf-123">1</span><span class="sxs-lookup"><span data-stu-id="855cf-123">1</span></span>     | <span data-ttu-id="855cf-124">/app1/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="855cf-125">ushort</span><span class="sxs-lookup"><span data-stu-id="855cf-125">ushort</span></span>      |
| <span data-ttu-id="855cf-126">2</span><span class="sxs-lookup"><span data-stu-id="855cf-126">2</span></span>     | <span data-ttu-id="855cf-127">/xmp/MicrosoftPhoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="855cf-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="855cf-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="855cf-129">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-129">Write Paths</span></span>



| <span data-ttu-id="855cf-130">單</span><span class="sxs-lookup"><span data-stu-id="855cf-130">Order</span></span> | <span data-ttu-id="855cf-131">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-131">Path</span></span>                       | <span data-ttu-id="855cf-132">磁片格式</span><span class="sxs-lookup"><span data-stu-id="855cf-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="855cf-133">1</span><span class="sxs-lookup"><span data-stu-id="855cf-133">1</span></span>     | <span data-ttu-id="855cf-134">/app1/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="855cf-135">ushort</span><span class="sxs-lookup"><span data-stu-id="855cf-135">ushort</span></span>      |
| <span data-ttu-id="855cf-136">2</span><span class="sxs-lookup"><span data-stu-id="855cf-136">2</span></span>     | <span data-ttu-id="855cf-137">/xmp/MicrosoftPhoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="855cf-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="855cf-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="855cf-139">移除路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-139">Remove Paths</span></span>



| <span data-ttu-id="855cf-140">單</span><span class="sxs-lookup"><span data-stu-id="855cf-140">Order</span></span> | <span data-ttu-id="855cf-141">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="855cf-142">1</span><span class="sxs-lookup"><span data-stu-id="855cf-142">1</span></span>     | <span data-ttu-id="855cf-143">/app1/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="855cf-144">2</span><span class="sxs-lookup"><span data-stu-id="855cf-144">2</span></span>     | <span data-ttu-id="855cf-145">/xmp/microsoftphoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="855cf-146">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="855cf-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="855cf-147">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-147">Read Paths</span></span>



| <span data-ttu-id="855cf-148">單</span><span class="sxs-lookup"><span data-stu-id="855cf-148">Order</span></span> | <span data-ttu-id="855cf-149">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-149">Path</span></span>                           | <span data-ttu-id="855cf-150">磁片格式</span><span class="sxs-lookup"><span data-stu-id="855cf-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="855cf-151">1</span><span class="sxs-lookup"><span data-stu-id="855cf-151">1</span></span>     | <span data-ttu-id="855cf-152">/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="855cf-153">ushort</span><span class="sxs-lookup"><span data-stu-id="855cf-153">ushort</span></span>      |
| <span data-ttu-id="855cf-154">2</span><span class="sxs-lookup"><span data-stu-id="855cf-154">2</span></span>     | <span data-ttu-id="855cf-155">/ifd/xmp/MicrosoftPhoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="855cf-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="855cf-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="855cf-157">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-157">Write Paths</span></span>



| <span data-ttu-id="855cf-158">單</span><span class="sxs-lookup"><span data-stu-id="855cf-158">Order</span></span> | <span data-ttu-id="855cf-159">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-159">Path</span></span>                           | <span data-ttu-id="855cf-160">磁片格式</span><span class="sxs-lookup"><span data-stu-id="855cf-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="855cf-161">1</span><span class="sxs-lookup"><span data-stu-id="855cf-161">1</span></span>     | <span data-ttu-id="855cf-162">/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="855cf-163">ushort</span><span class="sxs-lookup"><span data-stu-id="855cf-163">ushort</span></span>      |
| <span data-ttu-id="855cf-164">2</span><span class="sxs-lookup"><span data-stu-id="855cf-164">2</span></span>     | <span data-ttu-id="855cf-165">/ifd/xmp/MicrosoftPhoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="855cf-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="855cf-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="855cf-167">移除路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-167">Remove Paths</span></span>



| <span data-ttu-id="855cf-168">單</span><span class="sxs-lookup"><span data-stu-id="855cf-168">Order</span></span> | <span data-ttu-id="855cf-169">路徑</span><span class="sxs-lookup"><span data-stu-id="855cf-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="855cf-170">1</span><span class="sxs-lookup"><span data-stu-id="855cf-170">1</span></span>     | <span data-ttu-id="855cf-171">/ifd/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="855cf-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="855cf-172">2</span><span class="sxs-lookup"><span data-stu-id="855cf-172">2</span></span>     | <span data-ttu-id="855cf-173">/ifd/xmp/microsoftphoto：評等</span><span class="sxs-lookup"><span data-stu-id="855cf-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="855cf-174">備註</span><span class="sxs-lookup"><span data-stu-id="855cf-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="855cf-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="855cf-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855cf-176">系統評分</span><span class="sxs-lookup"><span data-stu-id="855cf-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
