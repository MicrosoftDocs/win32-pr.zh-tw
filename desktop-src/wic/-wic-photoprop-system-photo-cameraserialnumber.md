---
description: CameraSerialNumber 屬性的相片中繼資料原則。
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: CameraSerialNumber 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980005"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="05b83-103">CameraSerialNumber 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="05b83-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="05b83-104">[CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="05b83-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="05b83-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="05b83-105">PKEY</span></span>

<span data-ttu-id="05b83-106">PKEY \_ 相片 \_ CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="05b83-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="05b83-107">容器</span><span class="sxs-lookup"><span data-stu-id="05b83-107">Containers</span></span>

<span data-ttu-id="05b83-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="05b83-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="05b83-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="05b83-109">Read-Only</span></span>

<span data-ttu-id="05b83-110">No</span><span class="sxs-lookup"><span data-stu-id="05b83-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="05b83-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="05b83-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="05b83-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="05b83-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="05b83-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="05b83-113">Input Type</span></span>

<span data-ttu-id="05b83-114">字串。</span><span class="sxs-lookup"><span data-stu-id="05b83-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="05b83-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="05b83-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="05b83-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="05b83-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="05b83-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="05b83-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="05b83-118">如果檔案是 JPEG 格式，處理常式將會讀取、寫入和移除下列路徑中的資料：</span><span class="sxs-lookup"><span data-stu-id="05b83-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="05b83-119">單</span><span class="sxs-lookup"><span data-stu-id="05b83-119">Order</span></span> | <span data-ttu-id="05b83-120">路徑</span><span class="sxs-lookup"><span data-stu-id="05b83-120">Path</span></span>                                   | <span data-ttu-id="05b83-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="05b83-121">Disk Format</span></span> | <span data-ttu-id="05b83-122">必要</span><span class="sxs-lookup"><span data-stu-id="05b83-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="05b83-123">1</span><span class="sxs-lookup"><span data-stu-id="05b83-123">1</span></span>     | <span data-ttu-id="05b83-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="05b83-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="05b83-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="05b83-125">Unicode</span></span>     | <span data-ttu-id="05b83-126">Yes</span><span class="sxs-lookup"><span data-stu-id="05b83-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="05b83-127">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="05b83-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="05b83-128">如果檔案採用 TIFF 格式，處理常式將會讀取、寫入和移除下列路徑中的資料</span><span class="sxs-lookup"><span data-stu-id="05b83-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="05b83-129">單</span><span class="sxs-lookup"><span data-stu-id="05b83-129">Order</span></span> | <span data-ttu-id="05b83-130">路徑</span><span class="sxs-lookup"><span data-stu-id="05b83-130">Path</span></span>                                       | <span data-ttu-id="05b83-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="05b83-131">Disk Format</span></span> | <span data-ttu-id="05b83-132">必要</span><span class="sxs-lookup"><span data-stu-id="05b83-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="05b83-133">1</span><span class="sxs-lookup"><span data-stu-id="05b83-133">1</span></span>     | <span data-ttu-id="05b83-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="05b83-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="05b83-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="05b83-135">Unicode</span></span>     | <span data-ttu-id="05b83-136">Yes</span><span class="sxs-lookup"><span data-stu-id="05b83-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="05b83-137">備註</span><span class="sxs-lookup"><span data-stu-id="05b83-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="05b83-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="05b83-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05b83-139">CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="05b83-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
