---
description: LatitudeRef 屬性的相片中繼資料原則。
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: LatitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194262"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="63061-103">LatitudeRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="63061-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="63061-104">[LatitudeRef](../properties/props-system-gps-latitude.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="63061-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="63061-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="63061-105">PKEY</span></span>

<span data-ttu-id="63061-106">PKEY \_ GPS \_ LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="63061-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="63061-107">容器</span><span class="sxs-lookup"><span data-stu-id="63061-107">Containers</span></span>

<span data-ttu-id="63061-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="63061-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="63061-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="63061-109">Read-Only</span></span>

<span data-ttu-id="63061-110">No</span><span class="sxs-lookup"><span data-stu-id="63061-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="63061-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="63061-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="63061-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="63061-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="63061-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="63061-113">Input Type</span></span>

<span data-ttu-id="63061-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="63061-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="63061-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="63061-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="63061-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="63061-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="63061-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="63061-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="63061-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="63061-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="63061-119">單</span><span class="sxs-lookup"><span data-stu-id="63061-119">Order</span></span> | <span data-ttu-id="63061-120">路徑</span><span class="sxs-lookup"><span data-stu-id="63061-120">Path</span></span>                         | <span data-ttu-id="63061-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="63061-121">Disk Format</span></span> | <span data-ttu-id="63061-122">必要</span><span class="sxs-lookup"><span data-stu-id="63061-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="63061-123">1</span><span class="sxs-lookup"><span data-stu-id="63061-123">1</span></span>     | <span data-ttu-id="63061-124">/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="63061-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="63061-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="63061-125">Unicode</span></span>     | <span data-ttu-id="63061-126">Yes</span><span class="sxs-lookup"><span data-stu-id="63061-126">Yes</span></span>      |
| <span data-ttu-id="63061-127">2</span><span class="sxs-lookup"><span data-stu-id="63061-127">2</span></span>     | <span data-ttu-id="63061-128">/app1/ifd/gps/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="63061-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="63061-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="63061-129">ASCII</span></span>       | <span data-ttu-id="63061-130">No</span><span class="sxs-lookup"><span data-stu-id="63061-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="63061-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="63061-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="63061-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="63061-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="63061-133">單</span><span class="sxs-lookup"><span data-stu-id="63061-133">Order</span></span> | <span data-ttu-id="63061-134">路徑</span><span class="sxs-lookup"><span data-stu-id="63061-134">Path</span></span>                         | <span data-ttu-id="63061-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="63061-135">Disk Format</span></span> | <span data-ttu-id="63061-136">必要</span><span class="sxs-lookup"><span data-stu-id="63061-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="63061-137">1</span><span class="sxs-lookup"><span data-stu-id="63061-137">1</span></span>     | <span data-ttu-id="63061-138">/ifd/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="63061-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="63061-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="63061-139">Unicode</span></span>     | <span data-ttu-id="63061-140">Yes</span><span class="sxs-lookup"><span data-stu-id="63061-140">Yes</span></span>      |
| <span data-ttu-id="63061-141">2</span><span class="sxs-lookup"><span data-stu-id="63061-141">2</span></span>     | <span data-ttu-id="63061-142">/ifd/gps/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="63061-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="63061-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="63061-143">ASCII</span></span>       | <span data-ttu-id="63061-144">否</span><span class="sxs-lookup"><span data-stu-id="63061-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="63061-145">備註</span><span class="sxs-lookup"><span data-stu-id="63061-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="63061-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="63061-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63061-147">LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="63061-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
