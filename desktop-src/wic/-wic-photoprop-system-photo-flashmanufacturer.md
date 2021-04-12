---
description: FlashManufacturer 屬性的相片中繼資料原則。
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: FlashManufacturer 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027405"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="f0bbd-103">FlashManufacturer 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="f0bbd-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="f0bbd-104">[FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="f0bbd-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f0bbd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f0bbd-105">PKEY</span></span>

<span data-ttu-id="f0bbd-106">PKEY \_ 相片 \_ FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f0bbd-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="f0bbd-107">容器</span><span class="sxs-lookup"><span data-stu-id="f0bbd-107">Containers</span></span>

<span data-ttu-id="f0bbd-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="f0bbd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f0bbd-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="f0bbd-109">Read-Only</span></span>

<span data-ttu-id="f0bbd-110">No</span><span class="sxs-lookup"><span data-stu-id="f0bbd-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f0bbd-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="f0bbd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f0bbd-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f0bbd-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f0bbd-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="f0bbd-113">Input Type</span></span>

<span data-ttu-id="f0bbd-114">字串。</span><span class="sxs-lookup"><span data-stu-id="f0bbd-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f0bbd-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="f0bbd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f0bbd-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="f0bbd-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f0bbd-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="f0bbd-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f0bbd-118">如果檔案是 JPEG 格式，則處理常式會在讀取或寫入資料時使用下列路徑。</span><span class="sxs-lookup"><span data-stu-id="f0bbd-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="f0bbd-119">單</span><span class="sxs-lookup"><span data-stu-id="f0bbd-119">Order</span></span> | <span data-ttu-id="f0bbd-120">路徑</span><span class="sxs-lookup"><span data-stu-id="f0bbd-120">Path</span></span>                                  | <span data-ttu-id="f0bbd-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f0bbd-121">Disk Format</span></span> | <span data-ttu-id="f0bbd-122">資料格式</span><span class="sxs-lookup"><span data-stu-id="f0bbd-122">Data Format</span></span> | <span data-ttu-id="f0bbd-123">必要</span><span class="sxs-lookup"><span data-stu-id="f0bbd-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="f0bbd-124">1</span><span class="sxs-lookup"><span data-stu-id="f0bbd-124">1</span></span>     | <span data-ttu-id="f0bbd-125">/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f0bbd-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="f0bbd-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="f0bbd-126">Unicode</span></span>     |             | <span data-ttu-id="f0bbd-127">Yes</span><span class="sxs-lookup"><span data-stu-id="f0bbd-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f0bbd-128">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="f0bbd-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f0bbd-129">如果檔案採用 TIFF 格式，則處理常式會在讀取或寫入資料時使用下列優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="f0bbd-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="f0bbd-130">單</span><span class="sxs-lookup"><span data-stu-id="f0bbd-130">Order</span></span> | <span data-ttu-id="f0bbd-131">路徑</span><span class="sxs-lookup"><span data-stu-id="f0bbd-131">Path</span></span>                                      | <span data-ttu-id="f0bbd-132">磁片格式</span><span class="sxs-lookup"><span data-stu-id="f0bbd-132">Disk Format</span></span> | <span data-ttu-id="f0bbd-133">資料格式</span><span class="sxs-lookup"><span data-stu-id="f0bbd-133">Data Format</span></span> | <span data-ttu-id="f0bbd-134">必要</span><span class="sxs-lookup"><span data-stu-id="f0bbd-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="f0bbd-135">1</span><span class="sxs-lookup"><span data-stu-id="f0bbd-135">1</span></span>     | <span data-ttu-id="f0bbd-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f0bbd-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="f0bbd-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f0bbd-137">Unicode</span></span>     |             | <span data-ttu-id="f0bbd-138">Yes</span><span class="sxs-lookup"><span data-stu-id="f0bbd-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="f0bbd-139">備註</span><span class="sxs-lookup"><span data-stu-id="f0bbd-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0bbd-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0bbd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0bbd-141">FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f0bbd-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
