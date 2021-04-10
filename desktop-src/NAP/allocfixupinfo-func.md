---
title: 'AllocFixupInfo 函式 (NapUtil) '
description: 為指定大小的 FixupInfo 結構配置記憶體。
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- AllocFixupInfo 函數 NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843184"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="2569a-104">AllocFixupInfo 函式</span><span class="sxs-lookup"><span data-stu-id="2569a-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="2569a-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="2569a-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2569a-106">**AllocFixupInfo** 函數會為指定大小的 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="2569a-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="2569a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2569a-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="2569a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2569a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2569a-109">*fixupInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2569a-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569a-110">新配置之 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) 結構的位址指標。</span><span class="sxs-lookup"><span data-stu-id="2569a-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2569a-111">*countResultCodes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2569a-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2569a-112">要配置給 *fixupInfo* 的結果碼數目。</span><span class="sxs-lookup"><span data-stu-id="2569a-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2569a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2569a-113">Return value</span></span>



| <span data-ttu-id="2569a-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2569a-114">Return code</span></span>                                                                                   | <span data-ttu-id="2569a-115">Description</span><span class="sxs-lookup"><span data-stu-id="2569a-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2569a-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2569a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2569a-117">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="2569a-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="2569a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2569a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2569a-119">傳遞了無效的引數。</span><span class="sxs-lookup"><span data-stu-id="2569a-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2569a-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2569a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2569a-121">系統的虛擬記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2569a-121">The system is out of virtual memory.</span></span> <span data-ttu-id="2569a-122">此操作失敗。</span><span class="sxs-lookup"><span data-stu-id="2569a-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2569a-123">備註</span><span class="sxs-lookup"><span data-stu-id="2569a-123">Remarks</span></span>

<span data-ttu-id="2569a-124">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="2569a-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="2569a-125">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="2569a-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="2569a-126">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="2569a-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="2569a-127">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="2569a-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="2569a-128">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="2569a-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2569a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2569a-129">Requirements</span></span>



| <span data-ttu-id="2569a-130">需求</span><span class="sxs-lookup"><span data-stu-id="2569a-130">Requirement</span></span> | <span data-ttu-id="2569a-131">值</span><span class="sxs-lookup"><span data-stu-id="2569a-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2569a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2569a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2569a-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2569a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2569a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2569a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2569a-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2569a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2569a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="2569a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2569a-137"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="2569a-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="2569a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2569a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2569a-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2569a-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2569a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2569a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2569a-141">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="2569a-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





