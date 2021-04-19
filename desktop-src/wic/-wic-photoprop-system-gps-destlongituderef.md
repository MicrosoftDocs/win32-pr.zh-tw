---
description: DestLongitudeRef 屬性的相片中繼資料原則。
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: DestLongitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983852"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="46a72-103">DestLongitudeRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="46a72-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="46a72-104">[DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="46a72-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="46a72-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="46a72-105">PKEY</span></span>

<span data-ttu-id="46a72-106">PKEY \_ GPS。DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="46a72-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="46a72-107">容器</span><span class="sxs-lookup"><span data-stu-id="46a72-107">Containers</span></span>

<span data-ttu-id="46a72-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="46a72-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="46a72-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="46a72-109">Read-Only</span></span>

<span data-ttu-id="46a72-110">No</span><span class="sxs-lookup"><span data-stu-id="46a72-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="46a72-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="46a72-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="46a72-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="46a72-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="46a72-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="46a72-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="46a72-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="46a72-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="46a72-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="46a72-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="46a72-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="46a72-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="46a72-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="46a72-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="46a72-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="46a72-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="46a72-119">單</span><span class="sxs-lookup"><span data-stu-id="46a72-119">Order</span></span> | <span data-ttu-id="46a72-120">路徑</span><span class="sxs-lookup"><span data-stu-id="46a72-120">Path</span></span>                          | <span data-ttu-id="46a72-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46a72-121">Disk Format</span></span> | <span data-ttu-id="46a72-122">必要</span><span class="sxs-lookup"><span data-stu-id="46a72-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="46a72-123">1</span><span class="sxs-lookup"><span data-stu-id="46a72-123">1</span></span>     | <span data-ttu-id="46a72-124">/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="46a72-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="46a72-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="46a72-125">Unicode</span></span>     | <span data-ttu-id="46a72-126">Yes</span><span class="sxs-lookup"><span data-stu-id="46a72-126">Yes</span></span>      |
| <span data-ttu-id="46a72-127">2</span><span class="sxs-lookup"><span data-stu-id="46a72-127">2</span></span>     | <span data-ttu-id="46a72-128">/app1/ifd/gps/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="46a72-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="46a72-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="46a72-129">ASCII</span></span>       | <span data-ttu-id="46a72-130">No</span><span class="sxs-lookup"><span data-stu-id="46a72-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="46a72-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="46a72-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="46a72-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="46a72-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="46a72-133">單</span><span class="sxs-lookup"><span data-stu-id="46a72-133">Order</span></span> | <span data-ttu-id="46a72-134">路徑</span><span class="sxs-lookup"><span data-stu-id="46a72-134">Path</span></span>                              | <span data-ttu-id="46a72-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="46a72-135">Disk Format</span></span> | <span data-ttu-id="46a72-136">必要</span><span class="sxs-lookup"><span data-stu-id="46a72-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="46a72-137">1</span><span class="sxs-lookup"><span data-stu-id="46a72-137">1</span></span>     | <span data-ttu-id="46a72-138">/ifd/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="46a72-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="46a72-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="46a72-139">Unicode</span></span>     | <span data-ttu-id="46a72-140">Yes</span><span class="sxs-lookup"><span data-stu-id="46a72-140">Yes</span></span>      |
| <span data-ttu-id="46a72-141">2</span><span class="sxs-lookup"><span data-stu-id="46a72-141">2</span></span>     | <span data-ttu-id="46a72-142">/ifd/gps/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="46a72-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="46a72-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="46a72-143">ASCII</span></span>       | <span data-ttu-id="46a72-144">否</span><span class="sxs-lookup"><span data-stu-id="46a72-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="46a72-145">備註</span><span class="sxs-lookup"><span data-stu-id="46a72-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a72-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="46a72-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a72-147">DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="46a72-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
