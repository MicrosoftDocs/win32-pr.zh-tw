---
description: MapDatum 屬性的相片中繼資料原則。
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: MapDatum 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991921"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="d4ed0-103">MapDatum 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="d4ed0-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="d4ed0-104">[MapDatum](../properties/props-system-gps-mapdatum.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="d4ed0-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d4ed0-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d4ed0-105">PKEY</span></span>

<span data-ttu-id="d4ed0-106">PKEY \_ GPS \_ MapDatum</span><span class="sxs-lookup"><span data-stu-id="d4ed0-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="d4ed0-107">容器</span><span class="sxs-lookup"><span data-stu-id="d4ed0-107">Containers</span></span>

<span data-ttu-id="d4ed0-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="d4ed0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d4ed0-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="d4ed0-109">Read-Only</span></span>

<span data-ttu-id="d4ed0-110">No</span><span class="sxs-lookup"><span data-stu-id="d4ed0-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d4ed0-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="d4ed0-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d4ed0-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d4ed0-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d4ed0-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="d4ed0-113">Input Type</span></span>

<span data-ttu-id="d4ed0-114">偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR</span><span class="sxs-lookup"><span data-stu-id="d4ed0-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d4ed0-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="d4ed0-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d4ed0-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="d4ed0-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="d4ed0-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="d4ed0-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="d4ed0-118">如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="d4ed0-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="d4ed0-119">單</span><span class="sxs-lookup"><span data-stu-id="d4ed0-119">Order</span></span> | <span data-ttu-id="d4ed0-120">路徑</span><span class="sxs-lookup"><span data-stu-id="d4ed0-120">Path</span></span>                          | <span data-ttu-id="d4ed0-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d4ed0-121">Disk Format</span></span> | <span data-ttu-id="d4ed0-122">必要</span><span class="sxs-lookup"><span data-stu-id="d4ed0-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="d4ed0-123">1</span><span class="sxs-lookup"><span data-stu-id="d4ed0-123">1</span></span>     | <span data-ttu-id="d4ed0-124">/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="d4ed0-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="d4ed0-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4ed0-125">Unicode</span></span>     | <span data-ttu-id="d4ed0-126">Yes</span><span class="sxs-lookup"><span data-stu-id="d4ed0-126">Yes</span></span>      |
| <span data-ttu-id="d4ed0-127">2</span><span class="sxs-lookup"><span data-stu-id="d4ed0-127">2</span></span>     | <span data-ttu-id="d4ed0-128">/app1/ifd/gps/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="d4ed0-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="d4ed0-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="d4ed0-129">ASCII</span></span>       | <span data-ttu-id="d4ed0-130">No</span><span class="sxs-lookup"><span data-stu-id="d4ed0-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="d4ed0-131">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="d4ed0-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="d4ed0-132">如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：</span><span class="sxs-lookup"><span data-stu-id="d4ed0-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="d4ed0-133">單</span><span class="sxs-lookup"><span data-stu-id="d4ed0-133">Order</span></span> | <span data-ttu-id="d4ed0-134">路徑</span><span class="sxs-lookup"><span data-stu-id="d4ed0-134">Path</span></span>                      | <span data-ttu-id="d4ed0-135">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d4ed0-135">Disk Format</span></span> | <span data-ttu-id="d4ed0-136">必要</span><span class="sxs-lookup"><span data-stu-id="d4ed0-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="d4ed0-137">1</span><span class="sxs-lookup"><span data-stu-id="d4ed0-137">1</span></span>     | <span data-ttu-id="d4ed0-138">/ifd/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="d4ed0-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="d4ed0-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4ed0-139">Unicode</span></span>     | <span data-ttu-id="d4ed0-140">Yes</span><span class="sxs-lookup"><span data-stu-id="d4ed0-140">Yes</span></span>      |
| <span data-ttu-id="d4ed0-141">2</span><span class="sxs-lookup"><span data-stu-id="d4ed0-141">2</span></span>     | <span data-ttu-id="d4ed0-142">/ifd/gps/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="d4ed0-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="d4ed0-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="d4ed0-143">ASCII</span></span>       | <span data-ttu-id="d4ed0-144">否</span><span class="sxs-lookup"><span data-stu-id="d4ed0-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="d4ed0-145">備註</span><span class="sxs-lookup"><span data-stu-id="d4ed0-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4ed0-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4ed0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4ed0-147">MapDatum</span><span class="sxs-lookup"><span data-stu-id="d4ed0-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
