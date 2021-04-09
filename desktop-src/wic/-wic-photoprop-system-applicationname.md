---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: System.servicemodel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694979"
---
# <a name="systemapplicationname-photo-metadata-policy"></a><span data-ttu-id="189f6-103">System.servicemodel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="189f6-103">System.ApplicationName Photo Metadata Policy</span></span>

<span data-ttu-id="189f6-104">System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-applicationname.md)</span><span class="sxs-lookup"><span data-stu-id="189f6-104">The photo metadata policy for the [System.ApplicationName](../properties/props-system-applicationname.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="189f6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="189f6-105">PKEY</span></span>

<span data-ttu-id="189f6-106">PKEY \_ ApplicationName</span><span class="sxs-lookup"><span data-stu-id="189f6-106">PKEY\_ApplicationName</span></span>

### <a name="containers"></a><span data-ttu-id="189f6-107">容器</span><span class="sxs-lookup"><span data-stu-id="189f6-107">Containers</span></span>

<span data-ttu-id="189f6-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="189f6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="189f6-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="189f6-109">Read-Only</span></span>

<span data-ttu-id="189f6-110">No</span><span class="sxs-lookup"><span data-stu-id="189f6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="189f6-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="189f6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="189f6-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="189f6-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="189f6-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="189f6-113">Input Type</span></span>

<span data-ttu-id="189f6-114">String</span><span class="sxs-lookup"><span data-stu-id="189f6-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="189f6-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="189f6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="189f6-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="189f6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="189f6-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="189f6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="189f6-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-118">Read Paths</span></span>



| <span data-ttu-id="189f6-119">單</span><span class="sxs-lookup"><span data-stu-id="189f6-119">Order</span></span> | <span data-ttu-id="189f6-120">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-120">Path</span></span>                                         | <span data-ttu-id="189f6-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="189f6-121">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="189f6-122">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-122">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="189f6-123">ascii</span><span class="sxs-lookup"><span data-stu-id="189f6-123">ascii</span></span>       |
|       | <span data-ttu-id="189f6-124">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-124">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |
|       | <span data-ttu-id="189f6-125">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-125">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="189f6-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-126">unicode</span></span>     |
|       | <span data-ttu-id="189f6-127">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-127">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="189f6-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-128">unicode</span></span>     |
|       | <span data-ttu-id="189f6-129">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-129">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="189f6-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-130">unicode</span></span>     |
|       | <span data-ttu-id="189f6-131">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-131">/xmp/tiff:software</span></span>                           | <span data-ttu-id="189f6-132">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-132">unicode</span></span>     |
|       | <span data-ttu-id="189f6-133">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-133">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="189f6-134">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-134">Write Paths</span></span>



| <span data-ttu-id="189f6-135">單</span><span class="sxs-lookup"><span data-stu-id="189f6-135">Order</span></span> | <span data-ttu-id="189f6-136">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-136">Path</span></span>                                         | <span data-ttu-id="189f6-137">磁片格式</span><span class="sxs-lookup"><span data-stu-id="189f6-137">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="189f6-138">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-138">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="189f6-139">ascii</span><span class="sxs-lookup"><span data-stu-id="189f6-139">ascii</span></span>       |
|       | <span data-ttu-id="189f6-140">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-140">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="189f6-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-141">unicode</span></span>     |
|       | <span data-ttu-id="189f6-142">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-142">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="189f6-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-143">unicode</span></span>     |
|       | <span data-ttu-id="189f6-144">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-144">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="189f6-145">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-145">unicode</span></span>     |
|       | <span data-ttu-id="189f6-146">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-146">/xmp/tiff:software</span></span>                           | <span data-ttu-id="189f6-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-147">unicode</span></span>     |
|       | <span data-ttu-id="189f6-148">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-148">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="189f6-149">移除路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-149">Remove Paths</span></span>



| <span data-ttu-id="189f6-150">單</span><span class="sxs-lookup"><span data-stu-id="189f6-150">Order</span></span> | <span data-ttu-id="189f6-151">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-151">Path</span></span>                                         |
|-------|----------------------------------------------|
|       | <span data-ttu-id="189f6-152">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-152">/app1/ifd/{ushort=305}</span></span>                       |
|       | <span data-ttu-id="189f6-153">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-153">/xmp/xmp:CreatorTool</span></span>                         |
|       | <span data-ttu-id="189f6-154">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-154">/xmp/xmp:creatortool</span></span>                         |
|       | <span data-ttu-id="189f6-155">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-155">/xmp/tiff:Software</span></span>                           |
|       | <span data-ttu-id="189f6-156">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-156">/xmp/tiff:software</span></span>                           |
|       | <span data-ttu-id="189f6-157">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-157">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="189f6-158">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="189f6-158">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="189f6-159">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-159">Read Paths</span></span>



| <span data-ttu-id="189f6-160">單</span><span class="sxs-lookup"><span data-stu-id="189f6-160">Order</span></span> | <span data-ttu-id="189f6-161">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-161">Path</span></span>                                       | <span data-ttu-id="189f6-162">磁片格式</span><span class="sxs-lookup"><span data-stu-id="189f6-162">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="189f6-163">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-163">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="189f6-164">ascii</span><span class="sxs-lookup"><span data-stu-id="189f6-164">ascii</span></span>       |
|       | <span data-ttu-id="189f6-165">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-165">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="189f6-166">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-166">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="189f6-167">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-167">unicode</span></span>     |
|       | <span data-ttu-id="189f6-168">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-168">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="189f6-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-169">unicode</span></span>     |
|       | <span data-ttu-id="189f6-170">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-170">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="189f6-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-171">unicode</span></span>     |
|       | <span data-ttu-id="189f6-172">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-172">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="189f6-173">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-173">unicode</span></span>     |
|       | <span data-ttu-id="189f6-174">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-174">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="189f6-175">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-175">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="189f6-176">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-176">Write Paths</span></span>



| <span data-ttu-id="189f6-177">單</span><span class="sxs-lookup"><span data-stu-id="189f6-177">Order</span></span> | <span data-ttu-id="189f6-178">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-178">Path</span></span>                                       | <span data-ttu-id="189f6-179">磁片格式</span><span class="sxs-lookup"><span data-stu-id="189f6-179">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="189f6-180">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-180">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="189f6-181">ascii</span><span class="sxs-lookup"><span data-stu-id="189f6-181">ascii</span></span>       |
|       | <span data-ttu-id="189f6-182">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-182">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="189f6-183">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-183">unicode</span></span>     |
|       | <span data-ttu-id="189f6-184">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-184">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="189f6-185">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-185">unicode</span></span>     |
|       | <span data-ttu-id="189f6-186">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-186">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="189f6-187">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-187">unicode</span></span>     |
|       | <span data-ttu-id="189f6-188">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-188">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="189f6-189">Unicode</span><span class="sxs-lookup"><span data-stu-id="189f6-189">unicode</span></span>     |
|       | <span data-ttu-id="189f6-190">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-190">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="189f6-191">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-191">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="189f6-192">移除路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-192">Remove Paths</span></span>



| <span data-ttu-id="189f6-193">單</span><span class="sxs-lookup"><span data-stu-id="189f6-193">Order</span></span> | <span data-ttu-id="189f6-194">路徑</span><span class="sxs-lookup"><span data-stu-id="189f6-194">Path</span></span>                                       |
|-------|--------------------------------------------|
|       | <span data-ttu-id="189f6-195">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="189f6-195">/ifd/{ushort=305}</span></span>                          |
|       | <span data-ttu-id="189f6-196">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="189f6-196">/ifd/xmp/xmp:CreatorTool</span></span>                   |
|       | <span data-ttu-id="189f6-197">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="189f6-197">/ifd/xmp/xmp:creatortool</span></span>                   |
|       | <span data-ttu-id="189f6-198">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-198">/ifd/xmp/tiff:Software</span></span>                     |
|       | <span data-ttu-id="189f6-199">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="189f6-199">/ifd/xmp/tiff:software</span></span>                     |
|       | <span data-ttu-id="189f6-200">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-200">/ifd/iptc/Originating Program</span></span>              |
|       | <span data-ttu-id="189f6-201">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="189f6-201">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="189f6-202">備註</span><span class="sxs-lookup"><span data-stu-id="189f6-202">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="189f6-203">相關主題</span><span class="sxs-lookup"><span data-stu-id="189f6-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="189f6-204">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="189f6-204">System.ApplicationName</span></span>](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
