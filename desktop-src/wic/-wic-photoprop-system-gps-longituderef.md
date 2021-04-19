---
description: LongitudeRef 屬性的相片中繼資料原則。
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: LongitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980501"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="3f162-103">LongitudeRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="3f162-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="3f162-104">[LongitudeRef](../properties/props-system-gps-longituderef.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="3f162-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3f162-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3f162-105">PKEY</span></span>

<span data-ttu-id="3f162-106">PKEY \_ GPS \_ LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="3f162-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="3f162-107">容器</span><span class="sxs-lookup"><span data-stu-id="3f162-107">Containers</span></span>

<span data-ttu-id="3f162-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="3f162-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3f162-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="3f162-109">Read-Only</span></span>

<span data-ttu-id="3f162-110">No</span><span class="sxs-lookup"><span data-stu-id="3f162-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3f162-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="3f162-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3f162-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3f162-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="3f162-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="3f162-113">Input Type</span></span>

<span data-ttu-id="3f162-114">字串。</span><span class="sxs-lookup"><span data-stu-id="3f162-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3f162-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="3f162-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3f162-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="3f162-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="3f162-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="3f162-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="3f162-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="3f162-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="3f162-119">單</span><span class="sxs-lookup"><span data-stu-id="3f162-119">Order</span></span> | <span data-ttu-id="3f162-120">路徑</span><span class="sxs-lookup"><span data-stu-id="3f162-120">Path</span></span>                         | <span data-ttu-id="3f162-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3f162-121">Disk Format</span></span> | <span data-ttu-id="3f162-122">必要</span><span class="sxs-lookup"><span data-stu-id="3f162-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="3f162-123">1</span><span class="sxs-lookup"><span data-stu-id="3f162-123">1</span></span>     | <span data-ttu-id="3f162-124">/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="3f162-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="3f162-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f162-125">Unicode</span></span>     | <span data-ttu-id="3f162-126">Yes</span><span class="sxs-lookup"><span data-stu-id="3f162-126">Yes</span></span>      |
| <span data-ttu-id="3f162-127">2</span><span class="sxs-lookup"><span data-stu-id="3f162-127">2</span></span>     | <span data-ttu-id="3f162-128">/app1/ifd/gps/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="3f162-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="3f162-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="3f162-129">ASCII</span></span>       | <span data-ttu-id="3f162-130">No</span><span class="sxs-lookup"><span data-stu-id="3f162-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="3f162-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="3f162-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="3f162-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="3f162-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="3f162-133">單</span><span class="sxs-lookup"><span data-stu-id="3f162-133">Order</span></span> | <span data-ttu-id="3f162-134">路徑</span><span class="sxs-lookup"><span data-stu-id="3f162-134">Path</span></span>                          | <span data-ttu-id="3f162-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="3f162-135">Disk Format</span></span> | <span data-ttu-id="3f162-136">必要</span><span class="sxs-lookup"><span data-stu-id="3f162-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="3f162-137">1</span><span class="sxs-lookup"><span data-stu-id="3f162-137">1</span></span>     | <span data-ttu-id="3f162-138">/ifd/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="3f162-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="3f162-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f162-139">Unicode</span></span>     | <span data-ttu-id="3f162-140">Yes</span><span class="sxs-lookup"><span data-stu-id="3f162-140">Yes</span></span>      |
| <span data-ttu-id="3f162-141">2</span><span class="sxs-lookup"><span data-stu-id="3f162-141">2</span></span>     | <span data-ttu-id="3f162-142">/ifd/gps/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="3f162-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="3f162-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="3f162-143">ASCII</span></span>       | <span data-ttu-id="3f162-144">否</span><span class="sxs-lookup"><span data-stu-id="3f162-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="3f162-145">備註</span><span class="sxs-lookup"><span data-stu-id="3f162-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f162-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f162-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f162-147">LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="3f162-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
