---
description: System. Title 屬性的相片中繼資料原則。
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: System. 職稱相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980586"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="12d06-103">System. 職稱相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="12d06-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="12d06-104">[System. Title](../properties/props-system-title.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="12d06-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="12d06-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="12d06-105">PKEY</span></span>

<span data-ttu-id="12d06-106">PKEY \_ 標題</span><span class="sxs-lookup"><span data-stu-id="12d06-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="12d06-107">容器</span><span class="sxs-lookup"><span data-stu-id="12d06-107">Containers</span></span>

<span data-ttu-id="12d06-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="12d06-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="12d06-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="12d06-109">Read-Only</span></span>

<span data-ttu-id="12d06-110">No</span><span class="sxs-lookup"><span data-stu-id="12d06-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="12d06-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="12d06-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="12d06-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="12d06-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="12d06-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="12d06-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="12d06-114">VT \_ LPWSTR 或 vt \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="12d06-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="12d06-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="12d06-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="12d06-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="12d06-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="12d06-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="12d06-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="12d06-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-118">Read Paths</span></span>



| <span data-ttu-id="12d06-119">單</span><span class="sxs-lookup"><span data-stu-id="12d06-119">Order</span></span> | <span data-ttu-id="12d06-120">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-120">Path</span></span>                                | <span data-ttu-id="12d06-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="12d06-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="12d06-122">1</span><span class="sxs-lookup"><span data-stu-id="12d06-122">1</span></span>     | <span data-ttu-id="12d06-123">/app1/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="12d06-124">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="12d06-124">unicode\_bytes</span></span> |
| <span data-ttu-id="12d06-125">2</span><span class="sxs-lookup"><span data-stu-id="12d06-125">2</span></span>     | <span data-ttu-id="12d06-126">/xmp/ <xmpalt> dc：標題</span><span class="sxs-lookup"><span data-stu-id="12d06-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="12d06-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-127">unicode</span></span>        |
| <span data-ttu-id="12d06-128">3</span><span class="sxs-lookup"><span data-stu-id="12d06-128">3</span></span>     | <span data-ttu-id="12d06-129">/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="12d06-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-130">unicode</span></span>        |
| <span data-ttu-id="12d06-131">4</span><span class="sxs-lookup"><span data-stu-id="12d06-131">4</span></span>     | <span data-ttu-id="12d06-132">/app1/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="12d06-133">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-133">unicode</span></span>        |
| <span data-ttu-id="12d06-134">5</span><span class="sxs-lookup"><span data-stu-id="12d06-134">5</span></span>     | <span data-ttu-id="12d06-135">/app1/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="12d06-136">ascii</span><span class="sxs-lookup"><span data-stu-id="12d06-136">ascii</span></span>          |
| <span data-ttu-id="12d06-137">6</span><span class="sxs-lookup"><span data-stu-id="12d06-137">6</span></span>     | <span data-ttu-id="12d06-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="12d06-139">7</span><span class="sxs-lookup"><span data-stu-id="12d06-139">7</span></span>     | <span data-ttu-id="12d06-140">/xmp/ <xmpalt> dc： description</span><span class="sxs-lookup"><span data-stu-id="12d06-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="12d06-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-141">unicode</span></span>        |
| <span data-ttu-id="12d06-142">8</span><span class="sxs-lookup"><span data-stu-id="12d06-142">8</span></span>     | <span data-ttu-id="12d06-143">/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="12d06-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-144">unicode</span></span>        |
| <span data-ttu-id="12d06-145">9</span><span class="sxs-lookup"><span data-stu-id="12d06-145">9</span></span>     | <span data-ttu-id="12d06-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="12d06-147">10</span><span class="sxs-lookup"><span data-stu-id="12d06-147">10</span></span>    | <span data-ttu-id="12d06-148">/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="12d06-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="12d06-150">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-150">Write Paths</span></span>



| <span data-ttu-id="12d06-151">單</span><span class="sxs-lookup"><span data-stu-id="12d06-151">Order</span></span> | <span data-ttu-id="12d06-152">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-152">Path</span></span>                                | <span data-ttu-id="12d06-153">磁片格式</span><span class="sxs-lookup"><span data-stu-id="12d06-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="12d06-154">1</span><span class="sxs-lookup"><span data-stu-id="12d06-154">1</span></span>     | <span data-ttu-id="12d06-155">/app1/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="12d06-156">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="12d06-156">unicode\_bytes</span></span> |
| <span data-ttu-id="12d06-157">2</span><span class="sxs-lookup"><span data-stu-id="12d06-157">2</span></span>     | <span data-ttu-id="12d06-158">/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="12d06-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-159">unicode</span></span>        |
| <span data-ttu-id="12d06-160">3</span><span class="sxs-lookup"><span data-stu-id="12d06-160">3</span></span>     | <span data-ttu-id="12d06-161">/xmp/ <xmpalt> dc：標題</span><span class="sxs-lookup"><span data-stu-id="12d06-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="12d06-162">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-162">unicode</span></span>        |
| <span data-ttu-id="12d06-163">4</span><span class="sxs-lookup"><span data-stu-id="12d06-163">4</span></span>     | <span data-ttu-id="12d06-164">/app1/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="12d06-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-165">unicode</span></span>        |
| <span data-ttu-id="12d06-166">5</span><span class="sxs-lookup"><span data-stu-id="12d06-166">5</span></span>     | <span data-ttu-id="12d06-167">/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="12d06-168">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-168">unicode</span></span>        |
| <span data-ttu-id="12d06-169">6</span><span class="sxs-lookup"><span data-stu-id="12d06-169">6</span></span>     | <span data-ttu-id="12d06-170">/app1/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="12d06-171">ascii</span><span class="sxs-lookup"><span data-stu-id="12d06-171">ascii</span></span>          |
| <span data-ttu-id="12d06-172">7</span><span class="sxs-lookup"><span data-stu-id="12d06-172">7</span></span>     | <span data-ttu-id="12d06-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="12d06-174">8</span><span class="sxs-lookup"><span data-stu-id="12d06-174">8</span></span>     | <span data-ttu-id="12d06-175">/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="12d06-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-176">unicode</span></span>        |
| <span data-ttu-id="12d06-177">9</span><span class="sxs-lookup"><span data-stu-id="12d06-177">9</span></span>     | <span data-ttu-id="12d06-178">/xmp/ <xmpalt> dc： description</span><span class="sxs-lookup"><span data-stu-id="12d06-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="12d06-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="12d06-180">移除路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-180">Remove Paths</span></span>



| <span data-ttu-id="12d06-181">單</span><span class="sxs-lookup"><span data-stu-id="12d06-181">Order</span></span> | <span data-ttu-id="12d06-182">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="12d06-183">1</span><span class="sxs-lookup"><span data-stu-id="12d06-183">1</span></span>     | <span data-ttu-id="12d06-184">/app1/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="12d06-185">2</span><span class="sxs-lookup"><span data-stu-id="12d06-185">2</span></span>     | <span data-ttu-id="12d06-186">/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="12d06-187">3</span><span class="sxs-lookup"><span data-stu-id="12d06-187">3</span></span>     | <span data-ttu-id="12d06-188">/app1/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="12d06-189">4</span><span class="sxs-lookup"><span data-stu-id="12d06-189">4</span></span>     | <span data-ttu-id="12d06-190">/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="12d06-191">5</span><span class="sxs-lookup"><span data-stu-id="12d06-191">5</span></span>     | <span data-ttu-id="12d06-192">/app1/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="12d06-193">6</span><span class="sxs-lookup"><span data-stu-id="12d06-193">6</span></span>     | <span data-ttu-id="12d06-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="12d06-195">7</span><span class="sxs-lookup"><span data-stu-id="12d06-195">7</span></span>     | <span data-ttu-id="12d06-196">/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="12d06-197">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="12d06-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="12d06-198">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-198">Read Paths</span></span>



| <span data-ttu-id="12d06-199">單</span><span class="sxs-lookup"><span data-stu-id="12d06-199">Order</span></span> | <span data-ttu-id="12d06-200">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-200">Path</span></span>                                    | <span data-ttu-id="12d06-201">磁片格式</span><span class="sxs-lookup"><span data-stu-id="12d06-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="12d06-202">1</span><span class="sxs-lookup"><span data-stu-id="12d06-202">1</span></span>     | <span data-ttu-id="12d06-203">/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="12d06-204">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="12d06-204">unicode\_bytes</span></span> |
| <span data-ttu-id="12d06-205">2</span><span class="sxs-lookup"><span data-stu-id="12d06-205">2</span></span>     | <span data-ttu-id="12d06-206">/ifd/xmp/ <xmpalt> dc：標題</span><span class="sxs-lookup"><span data-stu-id="12d06-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="12d06-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-207">unicode</span></span>        |
| <span data-ttu-id="12d06-208">3</span><span class="sxs-lookup"><span data-stu-id="12d06-208">3</span></span>     | <span data-ttu-id="12d06-209">/ifd/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="12d06-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-210">unicode</span></span>        |
| <span data-ttu-id="12d06-211">4</span><span class="sxs-lookup"><span data-stu-id="12d06-211">4</span></span>     | <span data-ttu-id="12d06-212">/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="12d06-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-213">unicode</span></span>        |
| <span data-ttu-id="12d06-214">5</span><span class="sxs-lookup"><span data-stu-id="12d06-214">5</span></span>     | <span data-ttu-id="12d06-215">/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="12d06-216">ascii</span><span class="sxs-lookup"><span data-stu-id="12d06-216">ascii</span></span>          |
| <span data-ttu-id="12d06-217">6</span><span class="sxs-lookup"><span data-stu-id="12d06-217">6</span></span>     | <span data-ttu-id="12d06-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="12d06-219">7</span><span class="sxs-lookup"><span data-stu-id="12d06-219">7</span></span>     | <span data-ttu-id="12d06-220">/ifd/xmp/ <xmpalt> dc： description</span><span class="sxs-lookup"><span data-stu-id="12d06-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="12d06-221">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-221">unicode</span></span>        |
| <span data-ttu-id="12d06-222">8</span><span class="sxs-lookup"><span data-stu-id="12d06-222">8</span></span>     | <span data-ttu-id="12d06-223">/ifd/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="12d06-224">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-224">unicode</span></span>        |
| <span data-ttu-id="12d06-225">9</span><span class="sxs-lookup"><span data-stu-id="12d06-225">9</span></span>     | <span data-ttu-id="12d06-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="12d06-227">10</span><span class="sxs-lookup"><span data-stu-id="12d06-227">10</span></span>    | <span data-ttu-id="12d06-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="12d06-229">11</span><span class="sxs-lookup"><span data-stu-id="12d06-229">11</span></span>    | <span data-ttu-id="12d06-230">/ifd/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="12d06-231">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="12d06-232">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-232">Write Paths</span></span>



| <span data-ttu-id="12d06-233">單</span><span class="sxs-lookup"><span data-stu-id="12d06-233">Order</span></span> | <span data-ttu-id="12d06-234">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-234">Path</span></span>                                    | <span data-ttu-id="12d06-235">磁片格式</span><span class="sxs-lookup"><span data-stu-id="12d06-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="12d06-236">1</span><span class="sxs-lookup"><span data-stu-id="12d06-236">1</span></span>     | <span data-ttu-id="12d06-237">/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="12d06-238">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="12d06-238">unicode\_bytes</span></span> |
| <span data-ttu-id="12d06-239">2</span><span class="sxs-lookup"><span data-stu-id="12d06-239">2</span></span>     | <span data-ttu-id="12d06-240">/ifd/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="12d06-241">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-241">unicode</span></span>        |
| <span data-ttu-id="12d06-242">3</span><span class="sxs-lookup"><span data-stu-id="12d06-242">3</span></span>     | <span data-ttu-id="12d06-243">/ifd/xmp/ <xmpalt> dc：標題</span><span class="sxs-lookup"><span data-stu-id="12d06-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="12d06-244">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-244">unicode</span></span>        |
| <span data-ttu-id="12d06-245">4</span><span class="sxs-lookup"><span data-stu-id="12d06-245">4</span></span>     | <span data-ttu-id="12d06-246">/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="12d06-247">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-247">unicode</span></span>        |
| <span data-ttu-id="12d06-248">5</span><span class="sxs-lookup"><span data-stu-id="12d06-248">5</span></span>     | <span data-ttu-id="12d06-249">/ifd/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="12d06-250">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-250">unicode</span></span>        |
| <span data-ttu-id="12d06-251">6</span><span class="sxs-lookup"><span data-stu-id="12d06-251">6</span></span>     | <span data-ttu-id="12d06-252">/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="12d06-253">ascii</span><span class="sxs-lookup"><span data-stu-id="12d06-253">ascii</span></span>          |
| <span data-ttu-id="12d06-254">7</span><span class="sxs-lookup"><span data-stu-id="12d06-254">7</span></span>     | <span data-ttu-id="12d06-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="12d06-256">8</span><span class="sxs-lookup"><span data-stu-id="12d06-256">8</span></span>     | <span data-ttu-id="12d06-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="12d06-258">9</span><span class="sxs-lookup"><span data-stu-id="12d06-258">9</span></span>     | <span data-ttu-id="12d06-259">/ifd/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="12d06-260">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-260">unicode</span></span>        |
| <span data-ttu-id="12d06-261">10</span><span class="sxs-lookup"><span data-stu-id="12d06-261">10</span></span>    | <span data-ttu-id="12d06-262">/ifd/xmp/ <xmpalt> dc： description</span><span class="sxs-lookup"><span data-stu-id="12d06-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="12d06-263">Unicode</span><span class="sxs-lookup"><span data-stu-id="12d06-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="12d06-264">移除路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-264">Remove Paths</span></span>



| <span data-ttu-id="12d06-265">單</span><span class="sxs-lookup"><span data-stu-id="12d06-265">Order</span></span> | <span data-ttu-id="12d06-266">路徑</span><span class="sxs-lookup"><span data-stu-id="12d06-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="12d06-267">1</span><span class="sxs-lookup"><span data-stu-id="12d06-267">1</span></span>     | <span data-ttu-id="12d06-268">/ifd/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="12d06-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="12d06-269">2</span><span class="sxs-lookup"><span data-stu-id="12d06-269">2</span></span>     | <span data-ttu-id="12d06-270">/ifd/xmp/dc： title</span><span class="sxs-lookup"><span data-stu-id="12d06-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="12d06-271">3</span><span class="sxs-lookup"><span data-stu-id="12d06-271">3</span></span>     | <span data-ttu-id="12d06-272">/ifd/exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="12d06-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="12d06-273">4</span><span class="sxs-lookup"><span data-stu-id="12d06-273">4</span></span>     | <span data-ttu-id="12d06-274">/ifd/xmp/ <xmpalt> exif： UserComment</span><span class="sxs-lookup"><span data-stu-id="12d06-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="12d06-275">5</span><span class="sxs-lookup"><span data-stu-id="12d06-275">5</span></span>     | <span data-ttu-id="12d06-276">/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="12d06-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="12d06-277">6</span><span class="sxs-lookup"><span data-stu-id="12d06-277">6</span></span>     | <span data-ttu-id="12d06-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="12d06-279">7</span><span class="sxs-lookup"><span data-stu-id="12d06-279">7</span></span>     | <span data-ttu-id="12d06-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="12d06-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="12d06-281">8</span><span class="sxs-lookup"><span data-stu-id="12d06-281">8</span></span>     | <span data-ttu-id="12d06-282">/ifd/xmp/dc：描述</span><span class="sxs-lookup"><span data-stu-id="12d06-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="12d06-283">備註</span><span class="sxs-lookup"><span data-stu-id="12d06-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="12d06-284">相關主題</span><span class="sxs-lookup"><span data-stu-id="12d06-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d06-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="12d06-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
