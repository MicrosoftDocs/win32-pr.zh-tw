---
description: DestLatitudeRef 屬性的相片中繼資料原則。
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: DestLatitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985218"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="c0abc-103">DestLatitudeRef 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="c0abc-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="c0abc-104">[DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="c0abc-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c0abc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c0abc-105">PKEY</span></span>

<span data-ttu-id="c0abc-106">PKEY \_ GPS \_ DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0abc-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="c0abc-107">容器</span><span class="sxs-lookup"><span data-stu-id="c0abc-107">Containers</span></span>

<span data-ttu-id="c0abc-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="c0abc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c0abc-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="c0abc-109">Read-Only</span></span>

<span data-ttu-id="c0abc-110">No</span><span class="sxs-lookup"><span data-stu-id="c0abc-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c0abc-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="c0abc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c0abc-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c0abc-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c0abc-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="c0abc-113">Input Type</span></span>

<span data-ttu-id="c0abc-114">偏好以 VT \_ LPWSTR，但 \_ 會接受 vt LPSTR。</span><span class="sxs-lookup"><span data-stu-id="c0abc-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c0abc-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="c0abc-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c0abc-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="c0abc-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="c0abc-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="c0abc-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="c0abc-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="c0abc-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0abc-119">單</span><span class="sxs-lookup"><span data-stu-id="c0abc-119">Order</span></span> | <span data-ttu-id="c0abc-120">路徑</span><span class="sxs-lookup"><span data-stu-id="c0abc-120">Path</span></span>                          | <span data-ttu-id="c0abc-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c0abc-121">Disk Format</span></span> | <span data-ttu-id="c0abc-122">必要</span><span class="sxs-lookup"><span data-stu-id="c0abc-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="c0abc-123">1</span><span class="sxs-lookup"><span data-stu-id="c0abc-123">1</span></span>     | <span data-ttu-id="c0abc-124">/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0abc-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="c0abc-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0abc-125">Unicode</span></span>     | <span data-ttu-id="c0abc-126">Yes</span><span class="sxs-lookup"><span data-stu-id="c0abc-126">Yes</span></span>      |
| <span data-ttu-id="c0abc-127">2</span><span class="sxs-lookup"><span data-stu-id="c0abc-127">2</span></span>     | <span data-ttu-id="c0abc-128">/app1/ifd/gps/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0abc-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="c0abc-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0abc-129">ASCII</span></span>       | <span data-ttu-id="c0abc-130">No</span><span class="sxs-lookup"><span data-stu-id="c0abc-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="c0abc-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="c0abc-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="c0abc-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="c0abc-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0abc-133">單</span><span class="sxs-lookup"><span data-stu-id="c0abc-133">Order</span></span> | <span data-ttu-id="c0abc-134">路徑</span><span class="sxs-lookup"><span data-stu-id="c0abc-134">Path</span></span>                             | <span data-ttu-id="c0abc-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="c0abc-135">Disk Format</span></span> | <span data-ttu-id="c0abc-136">必要</span><span class="sxs-lookup"><span data-stu-id="c0abc-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="c0abc-137">1</span><span class="sxs-lookup"><span data-stu-id="c0abc-137">1</span></span>     | <span data-ttu-id="c0abc-138">/ifd/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0abc-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="c0abc-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0abc-139">Unicode</span></span>     | <span data-ttu-id="c0abc-140">Yes</span><span class="sxs-lookup"><span data-stu-id="c0abc-140">Yes</span></span>      |
| <span data-ttu-id="c0abc-141">2</span><span class="sxs-lookup"><span data-stu-id="c0abc-141">2</span></span>     | <span data-ttu-id="c0abc-142">/ifd/gps/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0abc-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="c0abc-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0abc-143">ASCII</span></span>       | <span data-ttu-id="c0abc-144">否</span><span class="sxs-lookup"><span data-stu-id="c0abc-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="c0abc-145">備註</span><span class="sxs-lookup"><span data-stu-id="c0abc-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0abc-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0abc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0abc-147">DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0abc-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
