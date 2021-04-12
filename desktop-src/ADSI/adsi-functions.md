---
title: ADSI 函數
description: Active Directory 服務介面會將下列 helper 函式公開給未使用 Automation 的用戶端。
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、reference、函數
- 函數 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300100"
---
# <a name="adsi-functions"></a><span data-ttu-id="59704-105">ADSI 函數</span><span class="sxs-lookup"><span data-stu-id="59704-105">ADSI Functions</span></span>

<span data-ttu-id="59704-106">Active Directory 服務介面會將下列 helper 函式公開給未使用 Automation 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="59704-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="59704-107">函式</span><span class="sxs-lookup"><span data-stu-id="59704-107">Function</span></span>                                           | <span data-ttu-id="59704-108">描述</span><span class="sxs-lookup"><span data-stu-id="59704-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59704-109">**ADsBuildEnumerator**</span><span class="sxs-lookup"><span data-stu-id="59704-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="59704-110">建立指定 ADSI 容器物件的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="59704-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="59704-111">**ADsBuildVarArrayInt**</span><span class="sxs-lookup"><span data-stu-id="59704-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="59704-112">從 **DWORD** s 陣列建立 variant 陣列。</span><span class="sxs-lookup"><span data-stu-id="59704-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="59704-113">**ADsBuildVarArrayStr**</span><span class="sxs-lookup"><span data-stu-id="59704-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="59704-114">從 Unicode 字串的陣列建立變體陣列。</span><span class="sxs-lookup"><span data-stu-id="59704-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="59704-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="59704-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="59704-116">將二進位資料的 blob 轉換成適合搜尋篩選的格式。</span><span class="sxs-lookup"><span data-stu-id="59704-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="59704-117">**ADsEnumerateNext**</span><span class="sxs-lookup"><span data-stu-id="59704-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="59704-118">使用從指定的列舉值物件取出的元素，填入 variant 陣列。</span><span class="sxs-lookup"><span data-stu-id="59704-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="59704-119">**ADsFreeEnumerator**</span><span class="sxs-lookup"><span data-stu-id="59704-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="59704-120">釋放 [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)先前建立的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="59704-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="59704-121">**ADsGetLastError**</span><span class="sxs-lookup"><span data-stu-id="59704-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="59704-122">抓取呼叫執行緒的最後一個錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="59704-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="59704-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="59704-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="59704-124">使用目前的認證系結至 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="59704-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="59704-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="59704-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="59704-126">使用指定的認證系結至 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="59704-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="59704-127">**ADsSetLastError**</span><span class="sxs-lookup"><span data-stu-id="59704-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="59704-128">設定呼叫執行緒的錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="59704-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="59704-129">**AllocADsMem**</span><span class="sxs-lookup"><span data-stu-id="59704-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="59704-130">配置記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="59704-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="59704-131">**AllocADsStr**</span><span class="sxs-lookup"><span data-stu-id="59704-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="59704-132">配置指定字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59704-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="59704-133">**FreeADsMem**</span><span class="sxs-lookup"><span data-stu-id="59704-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="59704-134">釋放 [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59704-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="59704-135">**FreeADsStr**</span><span class="sxs-lookup"><span data-stu-id="59704-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="59704-136">釋放為指定字串配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59704-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="59704-137">**ReallocADsMem**</span><span class="sxs-lookup"><span data-stu-id="59704-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="59704-138">將現有的記憶體內容指派給新建立的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="59704-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="59704-139">**ReallocADsStr**</span><span class="sxs-lookup"><span data-stu-id="59704-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="59704-140">以新的字串取代現有的字串。</span><span class="sxs-lookup"><span data-stu-id="59704-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="59704-141">下列 ADSI 函數已淘汰。</span><span class="sxs-lookup"><span data-stu-id="59704-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="59704-142">函式</span><span class="sxs-lookup"><span data-stu-id="59704-142">Function</span></span>                                                  | <span data-ttu-id="59704-143">描述</span><span class="sxs-lookup"><span data-stu-id="59704-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="59704-144">**AdsFreeAllErrorRecords**</span><span class="sxs-lookup"><span data-stu-id="59704-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="59704-145">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-145">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-146">**AdsDecodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="59704-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="59704-147">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-147">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-148">**PropVariantToAdsType**</span><span class="sxs-lookup"><span data-stu-id="59704-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="59704-149">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-149">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-150">**AdsTypeToPropVariant**</span><span class="sxs-lookup"><span data-stu-id="59704-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="59704-151">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-151">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-152">**AdsFreeAdsValues**</span><span class="sxs-lookup"><span data-stu-id="59704-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="59704-153">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-153">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-154">**InitAdsMem**</span><span class="sxs-lookup"><span data-stu-id="59704-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="59704-155">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-155">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-156">**AssertAdsmemLeaks**</span><span class="sxs-lookup"><span data-stu-id="59704-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="59704-157">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-157">Obsolete.</span></span>   |
| [<span data-ttu-id="59704-158">**DumpMemorytracker**</span><span class="sxs-lookup"><span data-stu-id="59704-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="59704-159">已過時。</span><span class="sxs-lookup"><span data-stu-id="59704-159">Obsolete.</span></span>   |



 

 

 




