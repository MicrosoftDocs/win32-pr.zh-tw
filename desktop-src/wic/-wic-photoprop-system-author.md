---
description: System. Author 屬性的相片中繼資料原則。
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: System. 作者相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971597"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="04c87-103">System. 作者相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="04c87-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="04c87-104">[System. Author](../properties/props-system-author.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="04c87-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="04c87-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="04c87-105">PKEY</span></span>

<span data-ttu-id="04c87-106">PKEY \_ 作者</span><span class="sxs-lookup"><span data-stu-id="04c87-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="04c87-107">容器</span><span class="sxs-lookup"><span data-stu-id="04c87-107">Containers</span></span>

<span data-ttu-id="04c87-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="04c87-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="04c87-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="04c87-109">Read-Only</span></span>

<span data-ttu-id="04c87-110">No</span><span class="sxs-lookup"><span data-stu-id="04c87-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="04c87-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="04c87-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="04c87-112">VT \_ 向量 \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="04c87-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="04c87-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="04c87-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="04c87-114">偏好以 VT \_ 向量 \| VT \_ LPWSTR，但 \_ 也接受 vt LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="04c87-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="04c87-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="04c87-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="04c87-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="04c87-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="04c87-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="04c87-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="04c87-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-118">Read Paths</span></span>



| <span data-ttu-id="04c87-119">單</span><span class="sxs-lookup"><span data-stu-id="04c87-119">Order</span></span> | <span data-ttu-id="04c87-120">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-120">Path</span></span>                             | <span data-ttu-id="04c87-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="04c87-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="04c87-122">1</span><span class="sxs-lookup"><span data-stu-id="04c87-122">1</span></span>     | <span data-ttu-id="04c87-123">/app1/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="04c87-124">ascii</span><span class="sxs-lookup"><span data-stu-id="04c87-124">ascii</span></span>          |
| <span data-ttu-id="04c87-125">2</span><span class="sxs-lookup"><span data-stu-id="04c87-125">2</span></span>     | <span data-ttu-id="04c87-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="04c87-127">3</span><span class="sxs-lookup"><span data-stu-id="04c87-127">3</span></span>     | <span data-ttu-id="04c87-128">/xmp/ <xmpseq> dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="04c87-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-129">unicode</span></span>        |
| <span data-ttu-id="04c87-130">4</span><span class="sxs-lookup"><span data-stu-id="04c87-130">4</span></span>     | <span data-ttu-id="04c87-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="04c87-132">5</span><span class="sxs-lookup"><span data-stu-id="04c87-132">5</span></span>     | <span data-ttu-id="04c87-133">/app1/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="04c87-134">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="04c87-134">unicode\_bytes</span></span> |
| <span data-ttu-id="04c87-135">6</span><span class="sxs-lookup"><span data-stu-id="04c87-135">6</span></span>     | <span data-ttu-id="04c87-136">/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="04c87-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="04c87-138">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-138">Write Paths</span></span>



| <span data-ttu-id="04c87-139">單</span><span class="sxs-lookup"><span data-stu-id="04c87-139">Order</span></span> | <span data-ttu-id="04c87-140">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-140">Path</span></span>                             | <span data-ttu-id="04c87-141">磁片格式</span><span class="sxs-lookup"><span data-stu-id="04c87-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="04c87-142">1</span><span class="sxs-lookup"><span data-stu-id="04c87-142">1</span></span>     | <span data-ttu-id="04c87-143">/xmp/ <xmpseq> dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="04c87-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-144">unicode</span></span>        |
| <span data-ttu-id="04c87-145">2</span><span class="sxs-lookup"><span data-stu-id="04c87-145">2</span></span>     | <span data-ttu-id="04c87-146">/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="04c87-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-147">unicode</span></span>        |
| <span data-ttu-id="04c87-148">3</span><span class="sxs-lookup"><span data-stu-id="04c87-148">3</span></span>     | <span data-ttu-id="04c87-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="04c87-150">4</span><span class="sxs-lookup"><span data-stu-id="04c87-150">4</span></span>     | <span data-ttu-id="04c87-151">/app1/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="04c87-152">ascii</span><span class="sxs-lookup"><span data-stu-id="04c87-152">ascii</span></span>          |
| <span data-ttu-id="04c87-153">5</span><span class="sxs-lookup"><span data-stu-id="04c87-153">5</span></span>     | <span data-ttu-id="04c87-154">/app1/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="04c87-155">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="04c87-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="04c87-156">移除路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-156">Remove Paths</span></span>



| <span data-ttu-id="04c87-157">單</span><span class="sxs-lookup"><span data-stu-id="04c87-157">Order</span></span> | <span data-ttu-id="04c87-158">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="04c87-159">1</span><span class="sxs-lookup"><span data-stu-id="04c87-159">1</span></span>     | <span data-ttu-id="04c87-160">/xmp/dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="04c87-161">2</span><span class="sxs-lookup"><span data-stu-id="04c87-161">2</span></span>     | <span data-ttu-id="04c87-162">/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="04c87-163">3</span><span class="sxs-lookup"><span data-stu-id="04c87-163">3</span></span>     | <span data-ttu-id="04c87-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="04c87-165">4</span><span class="sxs-lookup"><span data-stu-id="04c87-165">4</span></span>     | <span data-ttu-id="04c87-166">/app1/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="04c87-167">5</span><span class="sxs-lookup"><span data-stu-id="04c87-167">5</span></span>     | <span data-ttu-id="04c87-168">/app1/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="04c87-169">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="04c87-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="04c87-170">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-170">Read Paths</span></span>



| <span data-ttu-id="04c87-171">單</span><span class="sxs-lookup"><span data-stu-id="04c87-171">Order</span></span> | <span data-ttu-id="04c87-172">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-172">Path</span></span>                              | <span data-ttu-id="04c87-173">磁片格式</span><span class="sxs-lookup"><span data-stu-id="04c87-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="04c87-174">1</span><span class="sxs-lookup"><span data-stu-id="04c87-174">1</span></span>     | <span data-ttu-id="04c87-175">/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="04c87-176">ascii</span><span class="sxs-lookup"><span data-stu-id="04c87-176">ascii</span></span>          |
| <span data-ttu-id="04c87-177">2</span><span class="sxs-lookup"><span data-stu-id="04c87-177">2</span></span>     | <span data-ttu-id="04c87-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="04c87-179">3</span><span class="sxs-lookup"><span data-stu-id="04c87-179">3</span></span>     | <span data-ttu-id="04c87-180">/ifd/xmp/ <xmpseq> dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="04c87-181">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-181">unicode</span></span>        |
| <span data-ttu-id="04c87-182">4</span><span class="sxs-lookup"><span data-stu-id="04c87-182">4</span></span>     | <span data-ttu-id="04c87-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="04c87-184">5</span><span class="sxs-lookup"><span data-stu-id="04c87-184">5</span></span>     | <span data-ttu-id="04c87-185">/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="04c87-186">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="04c87-186">unicode\_bytes</span></span> |
| <span data-ttu-id="04c87-187">6</span><span class="sxs-lookup"><span data-stu-id="04c87-187">6</span></span>     | <span data-ttu-id="04c87-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="04c87-189">7</span><span class="sxs-lookup"><span data-stu-id="04c87-189">7</span></span>     | <span data-ttu-id="04c87-190">/ifd/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="04c87-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="04c87-192">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-192">Write Paths</span></span>



| <span data-ttu-id="04c87-193">單</span><span class="sxs-lookup"><span data-stu-id="04c87-193">Order</span></span> | <span data-ttu-id="04c87-194">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-194">Path</span></span>                              | <span data-ttu-id="04c87-195">磁片格式</span><span class="sxs-lookup"><span data-stu-id="04c87-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="04c87-196">1</span><span class="sxs-lookup"><span data-stu-id="04c87-196">1</span></span>     | <span data-ttu-id="04c87-197">/ifd/xmp/ <xmpseq> dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="04c87-198">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-198">unicode</span></span>        |
| <span data-ttu-id="04c87-199">2</span><span class="sxs-lookup"><span data-stu-id="04c87-199">2</span></span>     | <span data-ttu-id="04c87-200">/ifd/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="04c87-201">Unicode</span><span class="sxs-lookup"><span data-stu-id="04c87-201">unicode</span></span>        |
| <span data-ttu-id="04c87-202">3</span><span class="sxs-lookup"><span data-stu-id="04c87-202">3</span></span>     | <span data-ttu-id="04c87-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="04c87-204">4</span><span class="sxs-lookup"><span data-stu-id="04c87-204">4</span></span>     | <span data-ttu-id="04c87-205">/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="04c87-206">ascii \_ 向量</span><span class="sxs-lookup"><span data-stu-id="04c87-206">ascii\_vector</span></span>  |
| <span data-ttu-id="04c87-207">5</span><span class="sxs-lookup"><span data-stu-id="04c87-207">5</span></span>     | <span data-ttu-id="04c87-208">/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="04c87-209">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="04c87-209">unicode\_bytes</span></span> |
| <span data-ttu-id="04c87-210">6</span><span class="sxs-lookup"><span data-stu-id="04c87-210">6</span></span>     | <span data-ttu-id="04c87-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="04c87-212">移除路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-212">Remove Paths</span></span>



| <span data-ttu-id="04c87-213">單</span><span class="sxs-lookup"><span data-stu-id="04c87-213">Order</span></span> | <span data-ttu-id="04c87-214">路徑</span><span class="sxs-lookup"><span data-stu-id="04c87-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="04c87-215">1</span><span class="sxs-lookup"><span data-stu-id="04c87-215">1</span></span>     | <span data-ttu-id="04c87-216">/ifd/xmp/dc： creator</span><span class="sxs-lookup"><span data-stu-id="04c87-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="04c87-217">2</span><span class="sxs-lookup"><span data-stu-id="04c87-217">2</span></span>     | <span data-ttu-id="04c87-218">/ifd/xmp/tiff：演出者</span><span class="sxs-lookup"><span data-stu-id="04c87-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="04c87-219">3</span><span class="sxs-lookup"><span data-stu-id="04c87-219">3</span></span>     | <span data-ttu-id="04c87-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="04c87-221">4</span><span class="sxs-lookup"><span data-stu-id="04c87-221">4</span></span>     | <span data-ttu-id="04c87-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="04c87-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="04c87-223">5</span><span class="sxs-lookup"><span data-stu-id="04c87-223">5</span></span>     | <span data-ttu-id="04c87-224">/ifd/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="04c87-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="04c87-225">6</span><span class="sxs-lookup"><span data-stu-id="04c87-225">6</span></span>     | <span data-ttu-id="04c87-226">/ifd/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="04c87-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="04c87-227">備註</span><span class="sxs-lookup"><span data-stu-id="04c87-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="04c87-228">相關主題</span><span class="sxs-lookup"><span data-stu-id="04c87-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c87-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="04c87-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
