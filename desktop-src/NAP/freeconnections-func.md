---
title: 'FreeConnections 函式 (NapUtil) '
description: 釋放連接資料結構。
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- FreeConnections 函數 NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317135"
---
# <a name="freeconnections-function"></a><span data-ttu-id="91eda-104">FreeConnections 函式</span><span class="sxs-lookup"><span data-stu-id="91eda-104">FreeConnections function</span></span>

> [!Note]  
> <span data-ttu-id="91eda-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="91eda-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="91eda-106">**FreeConnections** 函數會釋出 [**連接**](connections-struct.md)資料結構。</span><span class="sxs-lookup"><span data-stu-id="91eda-106">The **FreeConnections** function frees a [**Connections**](connections-struct.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="91eda-107">語法</span><span class="sxs-lookup"><span data-stu-id="91eda-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a><span data-ttu-id="91eda-108">參數</span><span class="sxs-lookup"><span data-stu-id="91eda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91eda-109">*連接* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91eda-109">*connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91eda-110">要釋放的 [**連接**](connections-struct.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="91eda-110">A pointer to the [**Connections**](connections-struct.md) structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91eda-111">備註</span><span class="sxs-lookup"><span data-stu-id="91eda-111">Remarks</span></span>

<span data-ttu-id="91eda-112">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="91eda-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="91eda-113">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="91eda-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="91eda-114">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="91eda-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="91eda-115">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="91eda-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="91eda-116">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="91eda-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="91eda-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="91eda-117">Requirements</span></span>



| <span data-ttu-id="91eda-118">需求</span><span class="sxs-lookup"><span data-stu-id="91eda-118">Requirement</span></span> | <span data-ttu-id="91eda-119">值</span><span class="sxs-lookup"><span data-stu-id="91eda-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91eda-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91eda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91eda-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91eda-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="91eda-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91eda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91eda-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91eda-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="91eda-124">標頭</span><span class="sxs-lookup"><span data-stu-id="91eda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="91eda-125"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="91eda-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="91eda-126">DLL</span><span class="sxs-lookup"><span data-stu-id="91eda-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91eda-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91eda-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91eda-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91eda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91eda-129">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="91eda-129">**AllocConnections**</span></span>](allocconnections-func.md)
</dt> </dl>

 

 





