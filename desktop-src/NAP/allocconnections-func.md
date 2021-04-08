---
title: 'AllocConnections 函式 (NapUtil) '
description: 為指定數目的連接結構配置記憶體。
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- AllocConnections 函數 NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686627"
---
# <a name="allocconnections-function"></a><span data-ttu-id="7fbc0-104">AllocConnections 函式</span><span class="sxs-lookup"><span data-stu-id="7fbc0-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="7fbc0-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="7fbc0-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7fbc0-106">**AllocConnections** 函式會為指定數目的 [**連接**](connections-struct.md)結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbc0-107">語法</span><span class="sxs-lookup"><span data-stu-id="7fbc0-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="7fbc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fbc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbc0-109">*連接* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7fbc0-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbc0-110">新配置之 [**連接**](connections-struct.md) 結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="7fbc0-111">*connectionsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7fbc0-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbc0-112">要配置給 *連接* 的結構數目。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbc0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fbc0-113">Return value</span></span>



| <span data-ttu-id="7fbc0-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7fbc0-114">Return code</span></span>                                                                                   | <span data-ttu-id="7fbc0-115">Description</span><span class="sxs-lookup"><span data-stu-id="7fbc0-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fbc0-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc0-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7fbc0-117">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="7fbc0-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7fbc0-119">傳遞了無效的引數。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7fbc0-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc0-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7fbc0-121">系統的虛擬記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-121">The system is out of virtual memory.</span></span> <span data-ttu-id="7fbc0-122">此操作失敗。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fbc0-123">備註</span><span class="sxs-lookup"><span data-stu-id="7fbc0-123">Remarks</span></span>

<span data-ttu-id="7fbc0-124">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="7fbc0-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7fbc0-125">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7fbc0-126">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7fbc0-127">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7fbc0-128">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="7fbc0-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbc0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fbc0-129">Requirements</span></span>



| <span data-ttu-id="7fbc0-130">需求</span><span class="sxs-lookup"><span data-stu-id="7fbc0-130">Requirement</span></span> | <span data-ttu-id="7fbc0-131">值</span><span class="sxs-lookup"><span data-stu-id="7fbc0-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc0-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fbc0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbc0-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fbc0-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7fbc0-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fbc0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbc0-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fbc0-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7fbc0-136">標頭</span><span class="sxs-lookup"><span data-stu-id="7fbc0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fbc0-137"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc0-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7fbc0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbc0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fbc0-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc0-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbc0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fbc0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbc0-141">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="7fbc0-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





