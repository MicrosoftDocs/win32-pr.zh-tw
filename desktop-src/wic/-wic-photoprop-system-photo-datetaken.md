---
description: DateTaken 屬性的相片中繼資料原則。
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: DateTaken 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978183"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="a018e-103">DateTaken 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="a018e-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="a018e-104">[DateTaken](../properties/props-system-photo-datetaken.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="a018e-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a018e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a018e-105">PKEY</span></span>

<span data-ttu-id="a018e-106">PKEY \_ 相片 \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="a018e-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="a018e-107">容器</span><span class="sxs-lookup"><span data-stu-id="a018e-107">Containers</span></span>

<span data-ttu-id="a018e-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="a018e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a018e-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="a018e-109">Read-Only</span></span>

<span data-ttu-id="a018e-110">No</span><span class="sxs-lookup"><span data-stu-id="a018e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a018e-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="a018e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a018e-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="a018e-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="a018e-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a018e-113">Input Type</span></span>

<span data-ttu-id="a018e-114">Datetime</span><span class="sxs-lookup"><span data-stu-id="a018e-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a018e-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="a018e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a018e-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="a018e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a018e-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="a018e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a018e-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-118">Read Paths</span></span>



| <span data-ttu-id="a018e-119">單</span><span class="sxs-lookup"><span data-stu-id="a018e-119">Order</span></span> | <span data-ttu-id="a018e-120">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-120">Path</span></span>                                  | <span data-ttu-id="a018e-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="a018e-122">1</span><span class="sxs-lookup"><span data-stu-id="a018e-122">1</span></span>     | <span data-ttu-id="a018e-123">/app1/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="a018e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-124">ascii</span></span>       |
| <span data-ttu-id="a018e-125">2</span><span class="sxs-lookup"><span data-stu-id="a018e-125">2</span></span>     | <span data-ttu-id="a018e-126">/app13/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a018e-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-127">unicode</span></span>     |
| <span data-ttu-id="a018e-128">3</span><span class="sxs-lookup"><span data-stu-id="a018e-128">3</span></span>     | <span data-ttu-id="a018e-129">/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="a018e-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-130">unicode</span></span>     |
| <span data-ttu-id="a018e-131">4</span><span class="sxs-lookup"><span data-stu-id="a018e-131">4</span></span>     | <span data-ttu-id="a018e-132">/app1/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="a018e-133">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-133">ascii</span></span>       |
| <span data-ttu-id="a018e-134">5</span><span class="sxs-lookup"><span data-stu-id="a018e-134">5</span></span>     | <span data-ttu-id="a018e-135">/app13/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a018e-136">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-136">unicode</span></span>     |
| <span data-ttu-id="a018e-137">6</span><span class="sxs-lookup"><span data-stu-id="a018e-137">6</span></span>     | <span data-ttu-id="a018e-138">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="a018e-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a018e-140">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-140">Write Paths</span></span>



| <span data-ttu-id="a018e-141">單</span><span class="sxs-lookup"><span data-stu-id="a018e-141">Order</span></span> | <span data-ttu-id="a018e-142">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-142">Path</span></span>                                  | <span data-ttu-id="a018e-143">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="a018e-144">1</span><span class="sxs-lookup"><span data-stu-id="a018e-144">1</span></span>     | <span data-ttu-id="a018e-145">/app1/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="a018e-146">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-146">ascii</span></span>       |
| <span data-ttu-id="a018e-147">2</span><span class="sxs-lookup"><span data-stu-id="a018e-147">2</span></span>     | <span data-ttu-id="a018e-148">/app13/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a018e-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-149">unicode</span></span>     |
| <span data-ttu-id="a018e-150">3</span><span class="sxs-lookup"><span data-stu-id="a018e-150">3</span></span>     | <span data-ttu-id="a018e-151">/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="a018e-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-152">unicode</span></span>     |
| <span data-ttu-id="a018e-153">4</span><span class="sxs-lookup"><span data-stu-id="a018e-153">4</span></span>     | <span data-ttu-id="a018e-154">/app1/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="a018e-155">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-155">ascii</span></span>       |
| <span data-ttu-id="a018e-156">5</span><span class="sxs-lookup"><span data-stu-id="a018e-156">5</span></span>     | <span data-ttu-id="a018e-157">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="a018e-158">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a018e-159">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-159">Remove Paths</span></span>



| <span data-ttu-id="a018e-160">單</span><span class="sxs-lookup"><span data-stu-id="a018e-160">Order</span></span> | <span data-ttu-id="a018e-161">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="a018e-162">1</span><span class="sxs-lookup"><span data-stu-id="a018e-162">1</span></span>     | <span data-ttu-id="a018e-163">/app1/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="a018e-164">2</span><span class="sxs-lookup"><span data-stu-id="a018e-164">2</span></span>     | <span data-ttu-id="a018e-165">/app1/ifd/exif/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="a018e-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="a018e-166">3</span><span class="sxs-lookup"><span data-stu-id="a018e-166">3</span></span>     | <span data-ttu-id="a018e-167">/app1/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="a018e-168">4</span><span class="sxs-lookup"><span data-stu-id="a018e-168">4</span></span>     | <span data-ttu-id="a018e-169">/app1/ifd/exif/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="a018e-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="a018e-170">5</span><span class="sxs-lookup"><span data-stu-id="a018e-170">5</span></span>     | <span data-ttu-id="a018e-171">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="a018e-172">6</span><span class="sxs-lookup"><span data-stu-id="a018e-172">6</span></span>     | <span data-ttu-id="a018e-173">/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="a018e-174">7</span><span class="sxs-lookup"><span data-stu-id="a018e-174">7</span></span>     | <span data-ttu-id="a018e-175">/app13/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="a018e-176">8</span><span class="sxs-lookup"><span data-stu-id="a018e-176">8</span></span>     | <span data-ttu-id="a018e-177">/app13/irb/8bimiptc/iptc/time 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="a018e-178">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="a018e-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a018e-179">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-179">Read Paths</span></span>



| <span data-ttu-id="a018e-180">單</span><span class="sxs-lookup"><span data-stu-id="a018e-180">Order</span></span> | <span data-ttu-id="a018e-181">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-181">Path</span></span>                                | <span data-ttu-id="a018e-182">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="a018e-183">1</span><span class="sxs-lookup"><span data-stu-id="a018e-183">1</span></span>     | <span data-ttu-id="a018e-184">/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="a018e-185">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-185">ascii</span></span>       |
| <span data-ttu-id="a018e-186">2</span><span class="sxs-lookup"><span data-stu-id="a018e-186">2</span></span>     | <span data-ttu-id="a018e-187">/ifd/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a018e-188">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-188">unicode</span></span>     |
| <span data-ttu-id="a018e-189">3</span><span class="sxs-lookup"><span data-stu-id="a018e-189">3</span></span>     | <span data-ttu-id="a018e-190">/ifd/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="a018e-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-191">unicode</span></span>     |
| <span data-ttu-id="a018e-192">4</span><span class="sxs-lookup"><span data-stu-id="a018e-192">4</span></span>     | <span data-ttu-id="a018e-193">/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="a018e-194">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-194">ascii</span></span>       |
| <span data-ttu-id="a018e-195">5</span><span class="sxs-lookup"><span data-stu-id="a018e-195">5</span></span>     | <span data-ttu-id="a018e-196">/ifd/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a018e-197">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-197">unicode</span></span>     |
| <span data-ttu-id="a018e-198">6</span><span class="sxs-lookup"><span data-stu-id="a018e-198">6</span></span>     | <span data-ttu-id="a018e-199">/ifd/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a018e-200">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-200">unicode</span></span>     |
| <span data-ttu-id="a018e-201">7</span><span class="sxs-lookup"><span data-stu-id="a018e-201">7</span></span>     | <span data-ttu-id="a018e-202">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="a018e-203">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a018e-204">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-204">Write Paths</span></span>



| <span data-ttu-id="a018e-205">單</span><span class="sxs-lookup"><span data-stu-id="a018e-205">Order</span></span> | <span data-ttu-id="a018e-206">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-206">Path</span></span>                                | <span data-ttu-id="a018e-207">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="a018e-208">1</span><span class="sxs-lookup"><span data-stu-id="a018e-208">1</span></span>     | <span data-ttu-id="a018e-209">/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="a018e-210">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-210">ascii</span></span>       |
| <span data-ttu-id="a018e-211">2</span><span class="sxs-lookup"><span data-stu-id="a018e-211">2</span></span>     | <span data-ttu-id="a018e-212">/ifd/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a018e-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-213">unicode</span></span>     |
| <span data-ttu-id="a018e-214">3</span><span class="sxs-lookup"><span data-stu-id="a018e-214">3</span></span>     | <span data-ttu-id="a018e-215">/ifd/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="a018e-216">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-216">unicode</span></span>     |
| <span data-ttu-id="a018e-217">4</span><span class="sxs-lookup"><span data-stu-id="a018e-217">4</span></span>     | <span data-ttu-id="a018e-218">/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="a018e-219">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-219">ascii</span></span>       |
| <span data-ttu-id="a018e-220">5</span><span class="sxs-lookup"><span data-stu-id="a018e-220">5</span></span>     | <span data-ttu-id="a018e-221">/ifd/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a018e-222">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-222">unicode</span></span>     |
| <span data-ttu-id="a018e-223">6</span><span class="sxs-lookup"><span data-stu-id="a018e-223">6</span></span>     | <span data-ttu-id="a018e-224">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="a018e-225">Unicode</span><span class="sxs-lookup"><span data-stu-id="a018e-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a018e-226">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-226">Remove Paths</span></span>



| <span data-ttu-id="a018e-227">單</span><span class="sxs-lookup"><span data-stu-id="a018e-227">Order</span></span> | <span data-ttu-id="a018e-228">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="a018e-229">1</span><span class="sxs-lookup"><span data-stu-id="a018e-229">1</span></span>     | <span data-ttu-id="a018e-230">/ifd/exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a018e-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="a018e-231">2</span><span class="sxs-lookup"><span data-stu-id="a018e-231">2</span></span>     | <span data-ttu-id="a018e-232">/ifd/exif/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="a018e-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="a018e-233">3</span><span class="sxs-lookup"><span data-stu-id="a018e-233">3</span></span>     | <span data-ttu-id="a018e-234">/ifd/exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a018e-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="a018e-235">4</span><span class="sxs-lookup"><span data-stu-id="a018e-235">4</span></span>     | <span data-ttu-id="a018e-236">/ifd/exif/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="a018e-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="a018e-237">5</span><span class="sxs-lookup"><span data-stu-id="a018e-237">5</span></span>     | <span data-ttu-id="a018e-238">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a018e-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="a018e-239">6</span><span class="sxs-lookup"><span data-stu-id="a018e-239">6</span></span>     | <span data-ttu-id="a018e-240">/ifd/xmp/xmp:CreateDate</span><span class="sxs-lookup"><span data-stu-id="a018e-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="a018e-241">7</span><span class="sxs-lookup"><span data-stu-id="a018e-241">7</span></span>     | <span data-ttu-id="a018e-242">/ifd/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="a018e-243">8</span><span class="sxs-lookup"><span data-stu-id="a018e-243">8</span></span>     | <span data-ttu-id="a018e-244">/ifd/iptc/time 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="a018e-245">9</span><span class="sxs-lookup"><span data-stu-id="a018e-245">9</span></span>     | <span data-ttu-id="a018e-246">/ifd/irb/8bimiptc/iptc/date 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="a018e-247">10</span><span class="sxs-lookup"><span data-stu-id="a018e-247">10</span></span>    | <span data-ttu-id="a018e-248">/ifd/irb/8bimiptc/iptc/time 已建立</span><span class="sxs-lookup"><span data-stu-id="a018e-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="a018e-249">PNG 原則</span><span class="sxs-lookup"><span data-stu-id="a018e-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a018e-250">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-250">Read Paths</span></span>



| <span data-ttu-id="a018e-251">單</span><span class="sxs-lookup"><span data-stu-id="a018e-251">Order</span></span> | <span data-ttu-id="a018e-252">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-252">Path</span></span>                      | <span data-ttu-id="a018e-253">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a018e-254">1</span><span class="sxs-lookup"><span data-stu-id="a018e-254">1</span></span>     | <span data-ttu-id="a018e-255">/\[\*\]文字/建立時間</span><span class="sxs-lookup"><span data-stu-id="a018e-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="a018e-256">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="a018e-257">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-257">Write Paths</span></span>



| <span data-ttu-id="a018e-258">單</span><span class="sxs-lookup"><span data-stu-id="a018e-258">Order</span></span> | <span data-ttu-id="a018e-259">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-259">Path</span></span>                      | <span data-ttu-id="a018e-260">磁片格式</span><span class="sxs-lookup"><span data-stu-id="a018e-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a018e-261">2</span><span class="sxs-lookup"><span data-stu-id="a018e-261">2</span></span>     | <span data-ttu-id="a018e-262">/\[\*\]文字/建立時間</span><span class="sxs-lookup"><span data-stu-id="a018e-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="a018e-263">ascii</span><span class="sxs-lookup"><span data-stu-id="a018e-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="a018e-264">移除路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-264">Remove Paths</span></span>



| <span data-ttu-id="a018e-265">單</span><span class="sxs-lookup"><span data-stu-id="a018e-265">Order</span></span> | <span data-ttu-id="a018e-266">路徑</span><span class="sxs-lookup"><span data-stu-id="a018e-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a018e-267">3</span><span class="sxs-lookup"><span data-stu-id="a018e-267">3</span></span>     | <span data-ttu-id="a018e-268">/\[\*\]文字/建立時間</span><span class="sxs-lookup"><span data-stu-id="a018e-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a018e-269">備註</span><span class="sxs-lookup"><span data-stu-id="a018e-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a018e-270">相關主題</span><span class="sxs-lookup"><span data-stu-id="a018e-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a018e-271">DateTaken</span><span class="sxs-lookup"><span data-stu-id="a018e-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
