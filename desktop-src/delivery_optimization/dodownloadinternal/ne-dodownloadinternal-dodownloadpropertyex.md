---
title: DODownloadPropertyEx 列舉
description: 指定「進行下載」作業的擴充屬性識別碼。
keywords:
- DODownloadPropertyEx 列舉，DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843716"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="151ec-104">DODownloadPropertyEx 列舉</span><span class="sxs-lookup"><span data-stu-id="151ec-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="151ec-105">**DODownloadPropertyEx** 列舉已被取代。</span><span class="sxs-lookup"><span data-stu-id="151ec-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="151ec-106">相反地，請使用 [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) 列舉搭配 [IDODownload：： GetProperty](../do/nf-do-idodownload-getproperty.md) 和 [IDODownload：： SetProperty](../do/nf-do-idodownload-setproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="151ec-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="151ec-107">**DODownloadPropertyEx** 列舉會指定 DO 下載作業的擴充屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="151ec-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="151ec-108">這個列舉是由 **IDODownloadInternal** 介面使用，而 **變數** 值則是用來取得和設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="151ec-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="151ec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="151ec-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="151ec-110">常數</span><span class="sxs-lookup"><span data-stu-id="151ec-110">Constants</span></span>

| <span data-ttu-id="151ec-111">需求</span><span class="sxs-lookup"><span data-stu-id="151ec-111">Requirement</span></span> | <span data-ttu-id="151ec-112">值</span><span class="sxs-lookup"><span data-stu-id="151ec-112">Value</span></span> |
|-|-|
| <span data-ttu-id="151ec-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="151ec-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="151ec-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="151ec-114">Reserved.</span></span> <span data-ttu-id="151ec-115">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="151ec-115">Do not use.</span></span> |
| <span data-ttu-id="151ec-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="151ec-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="151ec-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="151ec-117">Optional.</span></span> <span data-ttu-id="151ec-118">針對遙測用途設定特定的相互關聯向量。</span><span class="sxs-lookup"><span data-stu-id="151ec-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="151ec-119">VARIANT 類型為 VT_BSTR。</span><span class="sxs-lookup"><span data-stu-id="151ec-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="151ec-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="151ec-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="151ec-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="151ec-121">Reserved.</span></span> <span data-ttu-id="151ec-122">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="151ec-122">Do not use.</span></span> |
| <span data-ttu-id="151ec-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="151ec-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="151ec-124">選擇性只寫入。</span><span class="sxs-lookup"><span data-stu-id="151ec-124">Optional write-only.</span></span> <span data-ttu-id="151ec-125">設定 (PHF) 位置的片段雜湊檔，這會用來執行所下載內容的執行時間完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="151ec-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="151ec-126">VARIANT 類型為 VT_BSTR。</span><span class="sxs-lookup"><span data-stu-id="151ec-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="151ec-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="151ec-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="151ec-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="151ec-128">Optional.</span></span> <span data-ttu-id="151ec-129">設定布林值旗標，指出部分雜湊檔 (PHF) 是否為強制性。</span><span class="sxs-lookup"><span data-stu-id="151ec-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="151ec-130">如果 VARIANT_TRUE，當完整性檢查失敗時，將會中止下載。</span><span class="sxs-lookup"><span data-stu-id="151ec-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="151ec-131">VARIANT 類型為 VT_BOOL。</span><span class="sxs-lookup"><span data-stu-id="151ec-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="151ec-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="151ec-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="151ec-133">保留的。</span><span class="sxs-lookup"><span data-stu-id="151ec-133">Reserved.</span></span> <span data-ttu-id="151ec-134">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="151ec-134">Do not use.</span></span> |
| <span data-ttu-id="151ec-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="151ec-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="151ec-136">保留的。</span><span class="sxs-lookup"><span data-stu-id="151ec-136">Reserved.</span></span> <span data-ttu-id="151ec-137">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="151ec-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="151ec-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="151ec-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="151ec-139">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="151ec-139">**Minimum supported client**</span></span> | <span data-ttu-id="151ec-140">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="151ec-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="151ec-141">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="151ec-141">**Minimum supported server**</span></span> | <span data-ttu-id="151ec-142">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="151ec-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="151ec-143">**標頭**</span><span class="sxs-lookup"><span data-stu-id="151ec-143">**Header**</span></span> | <span data-ttu-id="151ec-144">DODownloadInternal。h</span><span class="sxs-lookup"><span data-stu-id="151ec-144">DODownloadInternal.h</span></span> |
