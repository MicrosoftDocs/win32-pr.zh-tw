---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: GPS. DOP 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945156"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="157b6-103">GPS. DOP 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="157b6-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="157b6-104">適用于 [system.object](../properties/props-system-gps-dop.md) 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="157b6-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="157b6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="157b6-105">PKEY</span></span>

<span data-ttu-id="157b6-106">PKEY \_ GPS \_ DOP</span><span class="sxs-lookup"><span data-stu-id="157b6-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="157b6-107">容器</span><span class="sxs-lookup"><span data-stu-id="157b6-107">Containers</span></span>

<span data-ttu-id="157b6-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="157b6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="157b6-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="157b6-109">Read-Only</span></span>

<span data-ttu-id="157b6-110">Yes</span><span class="sxs-lookup"><span data-stu-id="157b6-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="157b6-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="157b6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="157b6-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="157b6-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="157b6-113">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="157b6-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="157b6-114">您可以藉由寫入 DOPNumerator 和 DOPDenominator 來寫入這個值。</span><span class="sxs-lookup"><span data-stu-id="157b6-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="157b6-115">無法直接寫入。</span><span class="sxs-lookup"><span data-stu-id="157b6-115">It cannot be written directly.</span></span> <span data-ttu-id="157b6-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="157b6-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="157b6-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="157b6-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="157b6-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="157b6-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="157b6-119">單</span><span class="sxs-lookup"><span data-stu-id="157b6-119">Order</span></span> | <span data-ttu-id="157b6-120">路徑</span><span class="sxs-lookup"><span data-stu-id="157b6-120">Path</span></span>                          | <span data-ttu-id="157b6-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="157b6-121">Disk Format</span></span>   | <span data-ttu-id="157b6-122">必要</span><span class="sxs-lookup"><span data-stu-id="157b6-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="157b6-123">1</span><span class="sxs-lookup"><span data-stu-id="157b6-123">1</span></span>     | <span data-ttu-id="157b6-124">/xmp/exif:GPSDOP</span><span class="sxs-lookup"><span data-stu-id="157b6-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="157b6-125">XMP 有理</span><span class="sxs-lookup"><span data-stu-id="157b6-125">XMP rational</span></span>  | <span data-ttu-id="157b6-126">Yes</span><span class="sxs-lookup"><span data-stu-id="157b6-126">Yes</span></span>      |
| <span data-ttu-id="157b6-127">2</span><span class="sxs-lookup"><span data-stu-id="157b6-127">2</span></span>     | <span data-ttu-id="157b6-128">/app1/ifd/gps/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="157b6-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="157b6-129">EXIF 有理</span><span class="sxs-lookup"><span data-stu-id="157b6-129">EXIF rational</span></span> | <span data-ttu-id="157b6-130">No</span><span class="sxs-lookup"><span data-stu-id="157b6-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="157b6-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="157b6-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="157b6-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="157b6-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="157b6-133">單</span><span class="sxs-lookup"><span data-stu-id="157b6-133">Order</span></span> | <span data-ttu-id="157b6-134">路徑</span><span class="sxs-lookup"><span data-stu-id="157b6-134">Path</span></span>                     | <span data-ttu-id="157b6-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="157b6-135">Disk Format</span></span>   | <span data-ttu-id="157b6-136">必要</span><span class="sxs-lookup"><span data-stu-id="157b6-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="157b6-137">1</span><span class="sxs-lookup"><span data-stu-id="157b6-137">1</span></span>     | <span data-ttu-id="157b6-138">/ifd/xmp/exif:GPSDop</span><span class="sxs-lookup"><span data-stu-id="157b6-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="157b6-139">XMP 有理</span><span class="sxs-lookup"><span data-stu-id="157b6-139">XMP rational</span></span>  | <span data-ttu-id="157b6-140">Yes</span><span class="sxs-lookup"><span data-stu-id="157b6-140">Yes</span></span>      |
| <span data-ttu-id="157b6-141">2</span><span class="sxs-lookup"><span data-stu-id="157b6-141">2</span></span>     | <span data-ttu-id="157b6-142">/ifd/gps/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="157b6-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="157b6-143">EXIF 有理</span><span class="sxs-lookup"><span data-stu-id="157b6-143">EXIF rational</span></span> | <span data-ttu-id="157b6-144">否</span><span class="sxs-lookup"><span data-stu-id="157b6-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="157b6-145">備註</span><span class="sxs-lookup"><span data-stu-id="157b6-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="157b6-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="157b6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157b6-147">GPS</span><span class="sxs-lookup"><span data-stu-id="157b6-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
