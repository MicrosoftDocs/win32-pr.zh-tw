---
description: LensModel 屬性的相片中繼資料原則。
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: LensModel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027266"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="5d9cd-103">LensModel 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="5d9cd-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="5d9cd-104">[LensModel](../properties/props-system-photo-lensmodel.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="5d9cd-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5d9cd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5d9cd-105">PKEY</span></span>

<span data-ttu-id="5d9cd-106">PKEY \_ 相片 \_ LensModel</span><span class="sxs-lookup"><span data-stu-id="5d9cd-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="5d9cd-107">容器</span><span class="sxs-lookup"><span data-stu-id="5d9cd-107">Containers</span></span>

<span data-ttu-id="5d9cd-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="5d9cd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5d9cd-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="5d9cd-109">Read-Only</span></span>

<span data-ttu-id="5d9cd-110">No</span><span class="sxs-lookup"><span data-stu-id="5d9cd-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5d9cd-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="5d9cd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5d9cd-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5d9cd-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5d9cd-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="5d9cd-113">Input Type</span></span>

<span data-ttu-id="5d9cd-114">字串。</span><span class="sxs-lookup"><span data-stu-id="5d9cd-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5d9cd-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="5d9cd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5d9cd-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="5d9cd-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="5d9cd-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="5d9cd-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="5d9cd-118">如果檔案是 JPEG 格式，則處理常式會在讀取或寫入資料時使用下列路徑。</span><span class="sxs-lookup"><span data-stu-id="5d9cd-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="5d9cd-119">單</span><span class="sxs-lookup"><span data-stu-id="5d9cd-119">Order</span></span> | <span data-ttu-id="5d9cd-120">路徑</span><span class="sxs-lookup"><span data-stu-id="5d9cd-120">Path</span></span>                          | <span data-ttu-id="5d9cd-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5d9cd-121">Disk Format</span></span> | <span data-ttu-id="5d9cd-122">必要</span><span class="sxs-lookup"><span data-stu-id="5d9cd-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="5d9cd-123">1</span><span class="sxs-lookup"><span data-stu-id="5d9cd-123">1</span></span>     | <span data-ttu-id="5d9cd-124">/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="5d9cd-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="5d9cd-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="5d9cd-125">Unicode</span></span>     | <span data-ttu-id="5d9cd-126">Yes</span><span class="sxs-lookup"><span data-stu-id="5d9cd-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="5d9cd-127">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="5d9cd-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="5d9cd-128">如果檔案採用 TIFF 格式，則處理常式會在讀取或寫入資料時使用下列優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="5d9cd-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="5d9cd-129">單</span><span class="sxs-lookup"><span data-stu-id="5d9cd-129">Order</span></span> | <span data-ttu-id="5d9cd-130">路徑</span><span class="sxs-lookup"><span data-stu-id="5d9cd-130">Path</span></span>                              | <span data-ttu-id="5d9cd-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="5d9cd-131">Disk Format</span></span> | <span data-ttu-id="5d9cd-132">必要</span><span class="sxs-lookup"><span data-stu-id="5d9cd-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="5d9cd-133">1</span><span class="sxs-lookup"><span data-stu-id="5d9cd-133">1</span></span>     | <span data-ttu-id="5d9cd-134">/ifd/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="5d9cd-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="5d9cd-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="5d9cd-135">Unicode</span></span>     | <span data-ttu-id="5d9cd-136">Yes</span><span class="sxs-lookup"><span data-stu-id="5d9cd-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="5d9cd-137">備註</span><span class="sxs-lookup"><span data-stu-id="5d9cd-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d9cd-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d9cd-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d9cd-139">LensModel</span><span class="sxs-lookup"><span data-stu-id="5d9cd-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
