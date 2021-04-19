---
description: VDS 常數
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: VDS 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981040"
---
# <a name="vds-constants"></a><span data-ttu-id="fbe65-103">VDS 常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-103">VDS Constants</span></span>

<span data-ttu-id="fbe65-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="fbe65-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fbe65-105">VDS 常數的分類方式如下：</span><span class="sxs-lookup"><span data-stu-id="fbe65-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="fbe65-106">物件狀態常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="fbe65-107">Automagic 提示常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="fbe65-108">其他常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="fbe65-109">物件狀態常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-109">Object Status Constants</span></span>



| <span data-ttu-id="fbe65-110">常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-110">Constant</span></span>           | <span data-ttu-id="fbe65-111">值</span><span class="sxs-lookup"><span data-stu-id="fbe65-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="fbe65-112">狀態 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="fbe65-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="fbe65-113">0</span><span class="sxs-lookup"><span data-stu-id="fbe65-113">0</span></span>     |
| <span data-ttu-id="fbe65-114">\_線上狀態</span><span class="sxs-lookup"><span data-stu-id="fbe65-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="fbe65-115">1</span><span class="sxs-lookup"><span data-stu-id="fbe65-115">1</span></span>     |
| <span data-ttu-id="fbe65-116">狀態 \_ 未 \_ 就緒</span><span class="sxs-lookup"><span data-stu-id="fbe65-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="fbe65-117">2</span><span class="sxs-lookup"><span data-stu-id="fbe65-117">2</span></span>     |
| <span data-ttu-id="fbe65-118">狀態 \_ 沒有 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="fbe65-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="fbe65-119">3</span><span class="sxs-lookup"><span data-stu-id="fbe65-119">3</span></span>     |
| <span data-ttu-id="fbe65-120">\_離線狀態</span><span class="sxs-lookup"><span data-stu-id="fbe65-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="fbe65-121">4</span><span class="sxs-lookup"><span data-stu-id="fbe65-121">4</span></span>     |
| <span data-ttu-id="fbe65-122">狀態 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="fbe65-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="fbe65-123">5</span><span class="sxs-lookup"><span data-stu-id="fbe65-123">5</span></span>     |
| <span data-ttu-id="fbe65-124">狀態 \_ 遺失</span><span class="sxs-lookup"><span data-stu-id="fbe65-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="fbe65-125">6</span><span class="sxs-lookup"><span data-stu-id="fbe65-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="fbe65-126">Automagic 提示常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="fbe65-127">常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-127">Constant</span></span>                               | <span data-ttu-id="fbe65-128">值</span><span class="sxs-lookup"><span data-stu-id="fbe65-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="fbe65-129">VDS \_ 提示 \_ MOSTLYREADS</span><span class="sxs-lookup"><span data-stu-id="fbe65-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="fbe65-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="fbe65-130">0x0002L</span></span> |
| <span data-ttu-id="fbe65-131">VDS \_ 提示 \_ OPTIMIZEFORSEQUENTIALREADS</span><span class="sxs-lookup"><span data-stu-id="fbe65-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="fbe65-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="fbe65-132">0x0004L</span></span> |
| <span data-ttu-id="fbe65-133">VDS \_ 提示 \_ OPTIMIZEFORSEQUENTIALWRITES</span><span class="sxs-lookup"><span data-stu-id="fbe65-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="fbe65-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="fbe65-134">0x0008L</span></span> |
| <span data-ttu-id="fbe65-135">VDS \_ 提示 \_ REMAPENABLED</span><span class="sxs-lookup"><span data-stu-id="fbe65-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="fbe65-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="fbe65-136">0x0020L</span></span> |
| <span data-ttu-id="fbe65-137">VDS \_ 提示 \_ WRITETHROUGHCACHINGENABLED</span><span class="sxs-lookup"><span data-stu-id="fbe65-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="fbe65-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="fbe65-138">0x0040L</span></span> |
| <span data-ttu-id="fbe65-139">VDS \_ 提示 \_ HARDWARECHECKSUMENABLED</span><span class="sxs-lookup"><span data-stu-id="fbe65-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="fbe65-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="fbe65-140">0x0080L</span></span> |
| <span data-ttu-id="fbe65-141">VDS \_ 提示 \_ ISYANKABLE</span><span class="sxs-lookup"><span data-stu-id="fbe65-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="fbe65-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="fbe65-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="fbe65-143">其他常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="fbe65-144">常數</span><span class="sxs-lookup"><span data-stu-id="fbe65-144">Constant</span></span>                     | <span data-ttu-id="fbe65-145">值</span><span class="sxs-lookup"><span data-stu-id="fbe65-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="fbe65-146">VDS \_ 重建 \_ 優先順序 \_ 下限</span><span class="sxs-lookup"><span data-stu-id="fbe65-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="fbe65-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="fbe65-147">0x0001L</span></span>    |
| <span data-ttu-id="fbe65-148">VER \_ VDS \_ LUN \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="fbe65-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="fbe65-149">1</span><span class="sxs-lookup"><span data-stu-id="fbe65-149">1</span></span>          |
| <span data-ttu-id="fbe65-150">最大 \_ COMPUTERNAME \_ 長度</span><span class="sxs-lookup"><span data-stu-id="fbe65-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="fbe65-151">15</span><span class="sxs-lookup"><span data-stu-id="fbe65-151">15</span></span>         |
| <span data-ttu-id="fbe65-152">最大 \_ PROVIDERNAME \_ 長度</span><span class="sxs-lookup"><span data-stu-id="fbe65-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="fbe65-153">200</span><span class="sxs-lookup"><span data-stu-id="fbe65-153">200</span></span>        |
| <span data-ttu-id="fbe65-154">最大 \_ VERSIONSTRING \_ 長度</span><span class="sxs-lookup"><span data-stu-id="fbe65-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="fbe65-155">16</span><span class="sxs-lookup"><span data-stu-id="fbe65-155">16</span></span>         |
| <span data-ttu-id="fbe65-156">磁碟機 \_ 號 \_ 的</span><span class="sxs-lookup"><span data-stu-id="fbe65-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="fbe65-157">N/A</span><span class="sxs-lookup"><span data-stu-id="fbe65-157">N/A</span></span>        |
| <span data-ttu-id="fbe65-158">最大 \_ FS \_ 名稱 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="fbe65-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="fbe65-159">8</span><span class="sxs-lookup"><span data-stu-id="fbe65-159">8</span></span>          |
| <span data-ttu-id="fbe65-160">不正確 \_ 成員 \_ IDX</span><span class="sxs-lookup"><span data-stu-id="fbe65-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="fbe65-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="fbe65-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="fbe65-162">GPT \_ 磁碟分割 \_ 名稱 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="fbe65-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="fbe65-163">36</span><span class="sxs-lookup"><span data-stu-id="fbe65-163">36</span></span>         |
| <span data-ttu-id="fbe65-164">最大 \_ 路徑</span><span class="sxs-lookup"><span data-stu-id="fbe65-164">MAX\_PATH</span></span>                    | <span data-ttu-id="fbe65-165">260</span><span class="sxs-lookup"><span data-stu-id="fbe65-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fbe65-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbe65-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbe65-167">VDS 參考</span><span class="sxs-lookup"><span data-stu-id="fbe65-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
