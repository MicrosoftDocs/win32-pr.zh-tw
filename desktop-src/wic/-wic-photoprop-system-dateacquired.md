---
description: DateAcquired 屬性的相片中繼資料原則。
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: DateAcquired 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194778"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="d4b08-103">DateAcquired 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="d4b08-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="d4b08-104">[DateAcquired](../properties/props-system-dateacquired.md)屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="d4b08-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d4b08-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d4b08-105">PKEY</span></span>

<span data-ttu-id="d4b08-106">PKEY \_ DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d4b08-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="d4b08-107">容器</span><span class="sxs-lookup"><span data-stu-id="d4b08-107">Containers</span></span>

<span data-ttu-id="d4b08-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="d4b08-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d4b08-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="d4b08-109">Read-Only</span></span>

<span data-ttu-id="d4b08-110">No</span><span class="sxs-lookup"><span data-stu-id="d4b08-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d4b08-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="d4b08-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d4b08-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="d4b08-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d4b08-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="d4b08-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d4b08-114">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="d4b08-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d4b08-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="d4b08-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d4b08-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="d4b08-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="d4b08-117"> (JPEG) 的路徑優先順序</span><span class="sxs-lookup"><span data-stu-id="d4b08-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="d4b08-118">如果檔案是 JPEG 格式，則處理常式會依下列順序搜尋資料：</span><span class="sxs-lookup"><span data-stu-id="d4b08-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="d4b08-119">單</span><span class="sxs-lookup"><span data-stu-id="d4b08-119">Order</span></span> | <span data-ttu-id="d4b08-120">路徑</span><span class="sxs-lookup"><span data-stu-id="d4b08-120">Path</span></span>                             | <span data-ttu-id="d4b08-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d4b08-121">Disk Format</span></span>                        | <span data-ttu-id="d4b08-122">必要</span><span class="sxs-lookup"><span data-stu-id="d4b08-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="d4b08-123">1</span><span class="sxs-lookup"><span data-stu-id="d4b08-123">1</span></span>     | <span data-ttu-id="d4b08-124">/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d4b08-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="d4b08-125">XMP 日期格式的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="d4b08-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="d4b08-126">Yes</span><span class="sxs-lookup"><span data-stu-id="d4b08-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="d4b08-127">路徑 (TIFF) 的優先順序</span><span class="sxs-lookup"><span data-stu-id="d4b08-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="d4b08-128">如果檔案採用 TIFF 格式，則處理常式會依下列順序搜尋資料：</span><span class="sxs-lookup"><span data-stu-id="d4b08-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="d4b08-129">單</span><span class="sxs-lookup"><span data-stu-id="d4b08-129">Order</span></span> | <span data-ttu-id="d4b08-130">路徑</span><span class="sxs-lookup"><span data-stu-id="d4b08-130">Path</span></span>                                 | <span data-ttu-id="d4b08-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="d4b08-131">Disk Format</span></span>                        | <span data-ttu-id="d4b08-132">必要</span><span class="sxs-lookup"><span data-stu-id="d4b08-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="d4b08-133">1</span><span class="sxs-lookup"><span data-stu-id="d4b08-133">1</span></span>     | <span data-ttu-id="d4b08-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d4b08-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="d4b08-135">XMP 日期格式的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="d4b08-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="d4b08-136">Yes</span><span class="sxs-lookup"><span data-stu-id="d4b08-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="d4b08-137">備註</span><span class="sxs-lookup"><span data-stu-id="d4b08-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4b08-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4b08-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b08-139">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d4b08-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
