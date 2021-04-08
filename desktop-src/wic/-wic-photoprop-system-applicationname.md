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
# <a name="systemapplicationname-photo-metadata-policy"></a><span data-ttu-id="ce745-103">System.servicemodel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="ce745-103">System.ApplicationName Photo Metadata Policy</span></span>

<span data-ttu-id="ce745-104">System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-applicationname.md)</span><span class="sxs-lookup"><span data-stu-id="ce745-104">The photo metadata policy for the [System.ApplicationName](../properties/props-system-applicationname.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ce745-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ce745-105">PKEY</span></span>

<span data-ttu-id="ce745-106">PKEY \_ ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce745-106">PKEY\_ApplicationName</span></span>

### <a name="containers"></a><span data-ttu-id="ce745-107">容器</span><span class="sxs-lookup"><span data-stu-id="ce745-107">Containers</span></span>

<span data-ttu-id="ce745-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="ce745-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ce745-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="ce745-109">Read-Only</span></span>

<span data-ttu-id="ce745-110">No</span><span class="sxs-lookup"><span data-stu-id="ce745-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ce745-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="ce745-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ce745-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ce745-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="ce745-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="ce745-113">Input Type</span></span>

<span data-ttu-id="ce745-114">String</span><span class="sxs-lookup"><span data-stu-id="ce745-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ce745-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="ce745-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ce745-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="ce745-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ce745-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="ce745-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce745-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-118">Read Paths</span></span>



| <span data-ttu-id="ce745-119">單</span><span class="sxs-lookup"><span data-stu-id="ce745-119">Order</span></span> | <span data-ttu-id="ce745-120">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-120">Path</span></span>                                         | <span data-ttu-id="ce745-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce745-121">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="ce745-122">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-122">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="ce745-123">ascii</span><span class="sxs-lookup"><span data-stu-id="ce745-123">ascii</span></span>       |
|       | <span data-ttu-id="ce745-124">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-124">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |
|       | <span data-ttu-id="ce745-125">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-125">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="ce745-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-126">unicode</span></span>     |
|       | <span data-ttu-id="ce745-127">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-127">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="ce745-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-128">unicode</span></span>     |
|       | <span data-ttu-id="ce745-129">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-129">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="ce745-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-130">unicode</span></span>     |
|       | <span data-ttu-id="ce745-131">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-131">/xmp/tiff:software</span></span>                           | <span data-ttu-id="ce745-132">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-132">unicode</span></span>     |
|       | <span data-ttu-id="ce745-133">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-133">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ce745-134">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-134">Write Paths</span></span>



| <span data-ttu-id="ce745-135">單</span><span class="sxs-lookup"><span data-stu-id="ce745-135">Order</span></span> | <span data-ttu-id="ce745-136">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-136">Path</span></span>                                         | <span data-ttu-id="ce745-137">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce745-137">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="ce745-138">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-138">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="ce745-139">ascii</span><span class="sxs-lookup"><span data-stu-id="ce745-139">ascii</span></span>       |
|       | <span data-ttu-id="ce745-140">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-140">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="ce745-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-141">unicode</span></span>     |
|       | <span data-ttu-id="ce745-142">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-142">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="ce745-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-143">unicode</span></span>     |
|       | <span data-ttu-id="ce745-144">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-144">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="ce745-145">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-145">unicode</span></span>     |
|       | <span data-ttu-id="ce745-146">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-146">/xmp/tiff:software</span></span>                           | <span data-ttu-id="ce745-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-147">unicode</span></span>     |
|       | <span data-ttu-id="ce745-148">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-148">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ce745-149">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-149">Remove Paths</span></span>



| <span data-ttu-id="ce745-150">單</span><span class="sxs-lookup"><span data-stu-id="ce745-150">Order</span></span> | <span data-ttu-id="ce745-151">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-151">Path</span></span>                                         |
|-------|----------------------------------------------|
|       | <span data-ttu-id="ce745-152">/app1/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-152">/app1/ifd/{ushort=305}</span></span>                       |
|       | <span data-ttu-id="ce745-153">/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-153">/xmp/xmp:CreatorTool</span></span>                         |
|       | <span data-ttu-id="ce745-154">/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-154">/xmp/xmp:creatortool</span></span>                         |
|       | <span data-ttu-id="ce745-155">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-155">/xmp/tiff:Software</span></span>                           |
|       | <span data-ttu-id="ce745-156">/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-156">/xmp/tiff:software</span></span>                           |
|       | <span data-ttu-id="ce745-157">/app13/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-157">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="ce745-158">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="ce745-158">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce745-159">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-159">Read Paths</span></span>



| <span data-ttu-id="ce745-160">單</span><span class="sxs-lookup"><span data-stu-id="ce745-160">Order</span></span> | <span data-ttu-id="ce745-161">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-161">Path</span></span>                                       | <span data-ttu-id="ce745-162">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce745-162">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="ce745-163">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-163">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="ce745-164">ascii</span><span class="sxs-lookup"><span data-stu-id="ce745-164">ascii</span></span>       |
|       | <span data-ttu-id="ce745-165">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-165">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="ce745-166">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-166">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="ce745-167">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-167">unicode</span></span>     |
|       | <span data-ttu-id="ce745-168">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-168">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="ce745-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-169">unicode</span></span>     |
|       | <span data-ttu-id="ce745-170">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-170">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="ce745-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-171">unicode</span></span>     |
|       | <span data-ttu-id="ce745-172">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-172">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="ce745-173">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-173">unicode</span></span>     |
|       | <span data-ttu-id="ce745-174">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-174">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="ce745-175">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-175">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ce745-176">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-176">Write Paths</span></span>



| <span data-ttu-id="ce745-177">單</span><span class="sxs-lookup"><span data-stu-id="ce745-177">Order</span></span> | <span data-ttu-id="ce745-178">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-178">Path</span></span>                                       | <span data-ttu-id="ce745-179">磁片格式</span><span class="sxs-lookup"><span data-stu-id="ce745-179">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="ce745-180">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-180">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="ce745-181">ascii</span><span class="sxs-lookup"><span data-stu-id="ce745-181">ascii</span></span>       |
|       | <span data-ttu-id="ce745-182">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-182">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="ce745-183">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-183">unicode</span></span>     |
|       | <span data-ttu-id="ce745-184">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-184">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="ce745-185">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-185">unicode</span></span>     |
|       | <span data-ttu-id="ce745-186">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-186">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="ce745-187">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-187">unicode</span></span>     |
|       | <span data-ttu-id="ce745-188">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-188">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="ce745-189">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce745-189">unicode</span></span>     |
|       | <span data-ttu-id="ce745-190">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-190">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="ce745-191">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-191">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ce745-192">移除路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-192">Remove Paths</span></span>



| <span data-ttu-id="ce745-193">單</span><span class="sxs-lookup"><span data-stu-id="ce745-193">Order</span></span> | <span data-ttu-id="ce745-194">路徑</span><span class="sxs-lookup"><span data-stu-id="ce745-194">Path</span></span>                                       |
|-------|--------------------------------------------|
|       | <span data-ttu-id="ce745-195">/ifd/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="ce745-195">/ifd/{ushort=305}</span></span>                          |
|       | <span data-ttu-id="ce745-196">/ifd/xmp/xmp:CreatorTool</span><span class="sxs-lookup"><span data-stu-id="ce745-196">/ifd/xmp/xmp:CreatorTool</span></span>                   |
|       | <span data-ttu-id="ce745-197">/ifd/xmp/xmp:creatortool</span><span class="sxs-lookup"><span data-stu-id="ce745-197">/ifd/xmp/xmp:creatortool</span></span>                   |
|       | <span data-ttu-id="ce745-198">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-198">/ifd/xmp/tiff:Software</span></span>                     |
|       | <span data-ttu-id="ce745-199">/ifd/xmp/tiff：軟體</span><span class="sxs-lookup"><span data-stu-id="ce745-199">/ifd/xmp/tiff:software</span></span>                     |
|       | <span data-ttu-id="ce745-200">/ifd/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-200">/ifd/iptc/Originating Program</span></span>              |
|       | <span data-ttu-id="ce745-201">/ifd/irb/8bimiptc/iptc/Originating 計畫</span><span class="sxs-lookup"><span data-stu-id="ce745-201">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ce745-202">備註</span><span class="sxs-lookup"><span data-stu-id="ce745-202">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce745-203">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce745-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce745-204">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="ce745-204">System.ApplicationName</span></span>](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
