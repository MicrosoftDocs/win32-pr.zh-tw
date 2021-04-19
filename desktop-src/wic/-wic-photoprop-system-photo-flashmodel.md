---
description: FlashModel 屬性的相片中繼資料原則。
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: FlashModel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994379"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="4f3a4-103">FlashModel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="4f3a4-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="4f3a4-104">[FlashModel](../properties/props-system-photo-flashmodel.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="4f3a4-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4f3a4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4f3a4-105">PKEY</span></span>

<span data-ttu-id="4f3a4-106">PKEY \_ 相片 \_ FlashModel</span><span class="sxs-lookup"><span data-stu-id="4f3a4-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="4f3a4-107">容器</span><span class="sxs-lookup"><span data-stu-id="4f3a4-107">Containers</span></span>

<span data-ttu-id="4f3a4-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="4f3a4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4f3a4-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="4f3a4-109">Read-Only</span></span>

<span data-ttu-id="4f3a4-110">No</span><span class="sxs-lookup"><span data-stu-id="4f3a4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4f3a4-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="4f3a4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4f3a4-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4f3a4-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4f3a4-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="4f3a4-113">Input Type</span></span>

<span data-ttu-id="4f3a4-114">字串。</span><span class="sxs-lookup"><span data-stu-id="4f3a4-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4f3a4-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="4f3a4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4f3a4-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="4f3a4-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="4f3a4-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="4f3a4-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="4f3a4-118">如果檔案是 JPEG 格式，則處理常式會在讀取或寫入資料時使用下列路徑。</span><span class="sxs-lookup"><span data-stu-id="4f3a4-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="4f3a4-119">單</span><span class="sxs-lookup"><span data-stu-id="4f3a4-119">Order</span></span> | <span data-ttu-id="4f3a4-120">路徑</span><span class="sxs-lookup"><span data-stu-id="4f3a4-120">Path</span></span>                           | <span data-ttu-id="4f3a4-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4f3a4-121">Disk Format</span></span> | <span data-ttu-id="4f3a4-122">資料格式</span><span class="sxs-lookup"><span data-stu-id="4f3a4-122">Data Format</span></span> | <span data-ttu-id="4f3a4-123">必要</span><span class="sxs-lookup"><span data-stu-id="4f3a4-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="4f3a4-124">1</span><span class="sxs-lookup"><span data-stu-id="4f3a4-124">1</span></span>     | <span data-ttu-id="4f3a4-125">/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="4f3a4-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="4f3a4-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="4f3a4-126">Unicode</span></span>     |             | <span data-ttu-id="4f3a4-127">Yes</span><span class="sxs-lookup"><span data-stu-id="4f3a4-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="4f3a4-128">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="4f3a4-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="4f3a4-129">如果檔案採用 TIFF 格式，則處理常式會在讀取或寫入資料時使用下列優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="4f3a4-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="4f3a4-130">單</span><span class="sxs-lookup"><span data-stu-id="4f3a4-130">Order</span></span> | <span data-ttu-id="4f3a4-131">路徑</span><span class="sxs-lookup"><span data-stu-id="4f3a4-131">Path</span></span>                               | <span data-ttu-id="4f3a4-132">磁片格式</span><span class="sxs-lookup"><span data-stu-id="4f3a4-132">Disk Format</span></span> | <span data-ttu-id="4f3a4-133">資料格式</span><span class="sxs-lookup"><span data-stu-id="4f3a4-133">Data Format</span></span> | <span data-ttu-id="4f3a4-134">必要</span><span class="sxs-lookup"><span data-stu-id="4f3a4-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="4f3a4-135">1</span><span class="sxs-lookup"><span data-stu-id="4f3a4-135">1</span></span>     | <span data-ttu-id="4f3a4-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="4f3a4-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="4f3a4-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="4f3a4-137">Unicode</span></span>     |             | <span data-ttu-id="4f3a4-138">Yes</span><span class="sxs-lookup"><span data-stu-id="4f3a4-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="4f3a4-139">備註</span><span class="sxs-lookup"><span data-stu-id="4f3a4-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f3a4-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f3a4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f3a4-141">FlashModel</span><span class="sxs-lookup"><span data-stu-id="4f3a4-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
