---
description: LensManufacturer 屬性的相片中繼資料原則。
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: LensManufacturer 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194126"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="2561b-103">LensManufacturer 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="2561b-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="2561b-104">[LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="2561b-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2561b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2561b-105">PKEY</span></span>

<span data-ttu-id="2561b-106">PKEY \_ 相片 \_ LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="2561b-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="2561b-107">容器</span><span class="sxs-lookup"><span data-stu-id="2561b-107">Containers</span></span>

<span data-ttu-id="2561b-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="2561b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2561b-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="2561b-109">Read-Only</span></span>

<span data-ttu-id="2561b-110">No</span><span class="sxs-lookup"><span data-stu-id="2561b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2561b-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="2561b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2561b-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="2561b-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="2561b-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="2561b-113">Input Type</span></span>

<span data-ttu-id="2561b-114">字串。</span><span class="sxs-lookup"><span data-stu-id="2561b-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2561b-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="2561b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2561b-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="2561b-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="2561b-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="2561b-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="2561b-118">如果檔案是 JPEG 格式，則處理常式會在讀取或寫入資料時使用下列路徑。</span><span class="sxs-lookup"><span data-stu-id="2561b-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="2561b-119">單</span><span class="sxs-lookup"><span data-stu-id="2561b-119">Order</span></span> | <span data-ttu-id="2561b-120">路徑</span><span class="sxs-lookup"><span data-stu-id="2561b-120">Path</span></span>                                 | <span data-ttu-id="2561b-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="2561b-121">Disk Format</span></span> | <span data-ttu-id="2561b-122">必要</span><span class="sxs-lookup"><span data-stu-id="2561b-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="2561b-123">1</span><span class="sxs-lookup"><span data-stu-id="2561b-123">1</span></span>     | <span data-ttu-id="2561b-124">/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="2561b-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="2561b-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="2561b-125">Unicode</span></span>     | <span data-ttu-id="2561b-126">Yes</span><span class="sxs-lookup"><span data-stu-id="2561b-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="2561b-127">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="2561b-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="2561b-128">如果檔案採用 TIFF 格式，則處理常式會在讀取或寫入資料時使用下列優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="2561b-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="2561b-129">單</span><span class="sxs-lookup"><span data-stu-id="2561b-129">Order</span></span> | <span data-ttu-id="2561b-130">路徑</span><span class="sxs-lookup"><span data-stu-id="2561b-130">Path</span></span>                                     | <span data-ttu-id="2561b-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="2561b-131">Disk Format</span></span> | <span data-ttu-id="2561b-132">必要</span><span class="sxs-lookup"><span data-stu-id="2561b-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="2561b-133">1</span><span class="sxs-lookup"><span data-stu-id="2561b-133">1</span></span>     | <span data-ttu-id="2561b-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="2561b-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="2561b-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="2561b-135">Unicode</span></span>     | <span data-ttu-id="2561b-136">Yes</span><span class="sxs-lookup"><span data-stu-id="2561b-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="2561b-137">備註</span><span class="sxs-lookup"><span data-stu-id="2561b-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2561b-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="2561b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2561b-139">LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="2561b-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
