---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: System. 關鍵字相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194574"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="f5e3d-103">System. 關鍵字相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f5e3d-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="f5e3d-104">[ [System.object](../properties/props-system-keywords.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f5e3d-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f5e3d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f5e3d-105">PKEY</span></span>

<span data-ttu-id="f5e3d-106">PKEY \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="f5e3d-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="f5e3d-107">容器</span><span class="sxs-lookup"><span data-stu-id="f5e3d-107">Containers</span></span>

<span data-ttu-id="f5e3d-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f5e3d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f5e3d-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f5e3d-109">Read-Only</span></span>

<span data-ttu-id="f5e3d-110">No</span><span class="sxs-lookup"><span data-stu-id="f5e3d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f5e3d-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f5e3d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f5e3d-112">VT \_ 向量 \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f5e3d-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="f5e3d-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f5e3d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="f5e3d-114">\_ \| 慣用的 vt 向量 vt \_ LPWSTR 是慣用的。</span><span class="sxs-lookup"><span data-stu-id="f5e3d-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="f5e3d-115">\_也接受包含分號分隔字串的 VT LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="f5e3d-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f5e3d-116">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f5e3d-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="f5e3d-117">會合並來自不同架構的值。</span><span class="sxs-lookup"><span data-stu-id="f5e3d-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f5e3d-118">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="f5e3d-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f5e3d-119">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-119">Read Paths</span></span>



| <span data-ttu-id="f5e3d-120">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-120">Order</span></span> | <span data-ttu-id="f5e3d-121">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-121">Path</span></span>                              | <span data-ttu-id="f5e3d-122">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f5e3d-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="f5e3d-123">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-123">1</span></span>     | <span data-ttu-id="f5e3d-124">/xmp/ <xmpbag> dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="f5e3d-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-125">unicode</span></span>        |
| <span data-ttu-id="f5e3d-126">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-126">2</span></span>     | <span data-ttu-id="f5e3d-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="f5e3d-128">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-128">3</span></span>     | <span data-ttu-id="f5e3d-129">/app1/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="f5e3d-130">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-130">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-131">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-131">4</span></span>     | <span data-ttu-id="f5e3d-132">/app1/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="f5e3d-133">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="f5e3d-134">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-134">Write Paths</span></span>



| <span data-ttu-id="f5e3d-135">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-135">Order</span></span> | <span data-ttu-id="f5e3d-136">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-136">Path</span></span>                                              | <span data-ttu-id="f5e3d-137">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f5e3d-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="f5e3d-138">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-138">1</span></span>     | <span data-ttu-id="f5e3d-139">/xmp/ <xmpbag> dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="f5e3d-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-140">unicode</span></span>        |
| <span data-ttu-id="f5e3d-141">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-141">2</span></span>     | <span data-ttu-id="f5e3d-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="f5e3d-143">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-143">3</span></span>     | <span data-ttu-id="f5e3d-144">/app1/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="f5e3d-145">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-145">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-146">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-146">4</span></span>     | <span data-ttu-id="f5e3d-147">/app1/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="f5e3d-148">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-148">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-149">5</span><span class="sxs-lookup"><span data-stu-id="f5e3d-149">5</span></span>     | <span data-ttu-id="f5e3d-150">/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="f5e3d-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="f5e3d-151">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-151">unicode</span></span>        |
| <span data-ttu-id="f5e3d-152">6</span><span class="sxs-lookup"><span data-stu-id="f5e3d-152">6</span></span>     | <span data-ttu-id="f5e3d-153">/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="f5e3d-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="f5e3d-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="f5e3d-155">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-155">Remove Paths</span></span>



| <span data-ttu-id="f5e3d-156">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-156">Order</span></span> | <span data-ttu-id="f5e3d-157">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="f5e3d-158">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-158">1</span></span>     | <span data-ttu-id="f5e3d-159">/xmp/dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="f5e3d-160">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-160">2</span></span>     | <span data-ttu-id="f5e3d-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="f5e3d-162">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-162">3</span></span>     | <span data-ttu-id="f5e3d-163">/app1/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="f5e3d-164">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-164">4</span></span>     | <span data-ttu-id="f5e3d-165">/app1/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="f5e3d-166">5</span><span class="sxs-lookup"><span data-stu-id="f5e3d-166">5</span></span>     | <span data-ttu-id="f5e3d-167">/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="f5e3d-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="f5e3d-168">6</span><span class="sxs-lookup"><span data-stu-id="f5e3d-168">6</span></span>     | <span data-ttu-id="f5e3d-169">/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="f5e3d-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="f5e3d-170">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="f5e3d-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f5e3d-171">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-171">Read Paths</span></span>



| <span data-ttu-id="f5e3d-172">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-172">Order</span></span> | <span data-ttu-id="f5e3d-173">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-173">Path</span></span>                              | <span data-ttu-id="f5e3d-174">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f5e3d-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="f5e3d-175">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-175">1</span></span>     | <span data-ttu-id="f5e3d-176">/ifd/xmp/ <xmpbag> dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="f5e3d-177">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-177">unicode</span></span>        |
| <span data-ttu-id="f5e3d-178">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-178">2</span></span>     | <span data-ttu-id="f5e3d-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="f5e3d-180">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-180">3</span></span>     | <span data-ttu-id="f5e3d-181">/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="f5e3d-182">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-182">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-183">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-183">4</span></span>     | <span data-ttu-id="f5e3d-184">/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="f5e3d-185">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-185">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-186">5</span><span class="sxs-lookup"><span data-stu-id="f5e3d-186">5</span></span>     | <span data-ttu-id="f5e3d-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="f5e3d-188">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-188">Write Paths</span></span>



| <span data-ttu-id="f5e3d-189">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-189">Order</span></span> | <span data-ttu-id="f5e3d-190">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-190">Path</span></span>                                                             | <span data-ttu-id="f5e3d-191">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f5e3d-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="f5e3d-192">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-192">1</span></span>     | <span data-ttu-id="f5e3d-193">/ifd/xmp/ <xmpbag> dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="f5e3d-194">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-194">unicode</span></span>        |
| <span data-ttu-id="f5e3d-195">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-195">2</span></span>     | <span data-ttu-id="f5e3d-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="f5e3d-197">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-197">3</span></span>     | <span data-ttu-id="f5e3d-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="f5e3d-199">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-199">4</span></span>     | <span data-ttu-id="f5e3d-200">/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="f5e3d-201">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-201">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-202">5</span><span class="sxs-lookup"><span data-stu-id="f5e3d-202">5</span></span>     | <span data-ttu-id="f5e3d-203">/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="f5e3d-204">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f5e3d-204">unicode\_bytes</span></span> |
| <span data-ttu-id="f5e3d-205">6</span><span class="sxs-lookup"><span data-stu-id="f5e3d-205">6</span></span>     | <span data-ttu-id="f5e3d-206">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="f5e3d-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="f5e3d-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-207">unicode</span></span>        |
| <span data-ttu-id="f5e3d-208">7</span><span class="sxs-lookup"><span data-stu-id="f5e3d-208">7</span></span>     | <span data-ttu-id="f5e3d-209">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="f5e3d-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="f5e3d-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-210">unicode</span></span>        |
| <span data-ttu-id="f5e3d-211">8</span><span class="sxs-lookup"><span data-stu-id="f5e3d-211">8</span></span>     | <span data-ttu-id="f5e3d-212">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="f5e3d-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="f5e3d-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="f5e3d-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="f5e3d-214">移除路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-214">Remove Paths</span></span>



| <span data-ttu-id="f5e3d-215">單</span><span class="sxs-lookup"><span data-stu-id="f5e3d-215">Order</span></span> | <span data-ttu-id="f5e3d-216">路徑</span><span class="sxs-lookup"><span data-stu-id="f5e3d-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="f5e3d-217">1</span><span class="sxs-lookup"><span data-stu-id="f5e3d-217">1</span></span>     | <span data-ttu-id="f5e3d-218">/ifd/xmp/dc： subject</span><span class="sxs-lookup"><span data-stu-id="f5e3d-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="f5e3d-219">2</span><span class="sxs-lookup"><span data-stu-id="f5e3d-219">2</span></span>     | <span data-ttu-id="f5e3d-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="f5e3d-221">3</span><span class="sxs-lookup"><span data-stu-id="f5e3d-221">3</span></span>     | <span data-ttu-id="f5e3d-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="f5e3d-223">4</span><span class="sxs-lookup"><span data-stu-id="f5e3d-223">4</span></span>     | <span data-ttu-id="f5e3d-224">/ifd/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="f5e3d-225">5</span><span class="sxs-lookup"><span data-stu-id="f5e3d-225">5</span></span>     | <span data-ttu-id="f5e3d-226">/ifd/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="f5e3d-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="f5e3d-227">6</span><span class="sxs-lookup"><span data-stu-id="f5e3d-227">6</span></span>     | <span data-ttu-id="f5e3d-228">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="f5e3d-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="f5e3d-229">7</span><span class="sxs-lookup"><span data-stu-id="f5e3d-229">7</span></span>     | <span data-ttu-id="f5e3d-230">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="f5e3d-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="f5e3d-231">8</span><span class="sxs-lookup"><span data-stu-id="f5e3d-231">8</span></span>     | <span data-ttu-id="f5e3d-232">/ifd/xmp/ <xmpbag> MicrosoftPhoto： LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="f5e3d-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="f5e3d-233">備註</span><span class="sxs-lookup"><span data-stu-id="f5e3d-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5e3d-234">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5e3d-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5e3d-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="f5e3d-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
