---
title: 'FreeNetworkSoH 函式 (NapUtil) '
description: 釋放 NetworkSoH 資料結構。
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- FreeNetworkSoH 函數 NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea2b72011332939aa0c814203d0004949c8341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466465"
---
# <a name="freenetworksoh-function"></a><span data-ttu-id="f0168-104">FreeNetworkSoH 函式</span><span class="sxs-lookup"><span data-stu-id="f0168-104">FreeNetworkSoH function</span></span>

> [!Note]  
> <span data-ttu-id="f0168-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f0168-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f0168-106">**FreeNetworkSoH** 函數會釋出 [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh)資料結構。</span><span class="sxs-lookup"><span data-stu-id="f0168-106">The **FreeNetworkSoH** function frees a [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0168-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0168-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a><span data-ttu-id="f0168-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0168-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0168-109">*networkSoh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0168-109">*networkSoh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0168-110">要釋放的 [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 資料結構指標。</span><span class="sxs-lookup"><span data-stu-id="f0168-110">A pointer to the [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0168-111">備註</span><span class="sxs-lookup"><span data-stu-id="f0168-111">Remarks</span></span>

<span data-ttu-id="f0168-112">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="f0168-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="f0168-113">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="f0168-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="f0168-114">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="f0168-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="f0168-115">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="f0168-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="f0168-116">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="f0168-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0168-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0168-117">Requirements</span></span>



| <span data-ttu-id="f0168-118">需求</span><span class="sxs-lookup"><span data-stu-id="f0168-118">Requirement</span></span> | <span data-ttu-id="f0168-119">值</span><span class="sxs-lookup"><span data-stu-id="f0168-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0168-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0168-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0168-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0168-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f0168-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0168-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0168-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0168-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f0168-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f0168-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0168-125"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0168-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f0168-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f0168-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0168-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0168-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





