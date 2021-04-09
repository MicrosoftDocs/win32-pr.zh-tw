---
title: 'FreeCountedString 函式 (NapUtil) '
description: 釋放 CountedString 資料結構。
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- FreeCountedString 函數 NAP
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f732a069d19d6b8948854bd1fe2e23be070aa23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933937"
---
# <a name="freecountedstring-function"></a><span data-ttu-id="14b7c-104">FreeCountedString 函式</span><span class="sxs-lookup"><span data-stu-id="14b7c-104">FreeCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="14b7c-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="14b7c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="14b7c-106">**FreeCountedString** 函數會釋出 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)資料結構。</span><span class="sxs-lookup"><span data-stu-id="14b7c-106">The **FreeCountedString** function frees a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b7c-107">語法</span><span class="sxs-lookup"><span data-stu-id="14b7c-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a><span data-ttu-id="14b7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="14b7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b7c-109">*countedString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-109">*countedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b7c-110">要釋放的 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 資料結構指標。</span><span class="sxs-lookup"><span data-stu-id="14b7c-110">A pointer to the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14b7c-111">備註</span><span class="sxs-lookup"><span data-stu-id="14b7c-111">Remarks</span></span>

<span data-ttu-id="14b7c-112">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="14b7c-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="14b7c-113">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="14b7c-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="14b7c-114">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="14b7c-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="14b7c-115">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="14b7c-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="14b7c-116">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="14b7c-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b7c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="14b7c-117">Requirements</span></span>



| <span data-ttu-id="14b7c-118">需求</span><span class="sxs-lookup"><span data-stu-id="14b7c-118">Requirement</span></span> | <span data-ttu-id="14b7c-119">值</span><span class="sxs-lookup"><span data-stu-id="14b7c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14b7c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14b7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14b7c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="14b7c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14b7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14b7c-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14b7c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="14b7c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b7c-125"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="14b7c-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="14b7c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="14b7c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b7c-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b7c-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b7c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14b7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b7c-129">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="14b7c-129">**AllocCountedString**</span></span>](alloccountedstring-func.md)
</dt> </dl>

 

 





