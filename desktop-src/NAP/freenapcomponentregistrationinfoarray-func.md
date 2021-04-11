---
title: 'FreeNapComponentRegistrationInfoArray 函式 (NapUtil) '
description: 從陣列釋出指定數目的 NapComponentRegistrationInfo 資料結構。
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- FreeNapComponentRegistrationInfoArray 函數 NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105419"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="1c75f-104">FreeNapComponentRegistrationInfoArray 函式</span><span class="sxs-lookup"><span data-stu-id="1c75f-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="1c75f-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="1c75f-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1c75f-106">**FreeNapComponentRegistrationInfoArray** 函式會從陣列釋出指定數目的 [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)資料結構。</span><span class="sxs-lookup"><span data-stu-id="1c75f-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c75f-107">語法</span><span class="sxs-lookup"><span data-stu-id="1c75f-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="1c75f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1c75f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c75f-109">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c75f-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c75f-110">要釋放的 *資訊* 中的 [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構數目。</span><span class="sxs-lookup"><span data-stu-id="1c75f-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="1c75f-111">*資訊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c75f-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c75f-112">要釋放之 [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) 資料結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1c75f-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c75f-113">備註</span><span class="sxs-lookup"><span data-stu-id="1c75f-113">Remarks</span></span>

<span data-ttu-id="1c75f-114">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="1c75f-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="1c75f-115">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="1c75f-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="1c75f-116">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="1c75f-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="1c75f-117">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="1c75f-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="1c75f-118">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="1c75f-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c75f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c75f-119">Requirements</span></span>



| <span data-ttu-id="1c75f-120">需求</span><span class="sxs-lookup"><span data-stu-id="1c75f-120">Requirement</span></span> | <span data-ttu-id="1c75f-121">值</span><span class="sxs-lookup"><span data-stu-id="1c75f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c75f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c75f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1c75f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c75f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1c75f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c75f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1c75f-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c75f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1c75f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1c75f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c75f-127"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c75f-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="1c75f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1c75f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c75f-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c75f-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





