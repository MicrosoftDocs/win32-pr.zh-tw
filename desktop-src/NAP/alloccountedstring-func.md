---
title: 'AllocCountedString 函式 (NapUtil) '
description: 為以 null 結束的字串配置記憶體，並將其傳回 CountedString 結構中。
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString 函數 NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968534"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="2dc27-104">AllocCountedString 函式</span><span class="sxs-lookup"><span data-stu-id="2dc27-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="2dc27-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="2dc27-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2dc27-106">**AllocCountedString** 函式會為以 null 結束的字串配置記憶體，並在 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構中傳回。</span><span class="sxs-lookup"><span data-stu-id="2dc27-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc27-107">語法</span><span class="sxs-lookup"><span data-stu-id="2dc27-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="2dc27-108">參數</span><span class="sxs-lookup"><span data-stu-id="2dc27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc27-109">*countedString* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2dc27-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc27-110">新配置之 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 結構的位址指標。</span><span class="sxs-lookup"><span data-stu-id="2dc27-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2dc27-111">*字串* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2dc27-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc27-112">要在 *countedString* 中傳回之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="2dc27-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc27-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dc27-113">Return value</span></span>



| <span data-ttu-id="2dc27-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2dc27-114">Return code</span></span>                                                                                   | <span data-ttu-id="2dc27-115">Description</span><span class="sxs-lookup"><span data-stu-id="2dc27-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dc27-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc27-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2dc27-117">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="2dc27-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="2dc27-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc27-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2dc27-119">傳遞了無效的引數。</span><span class="sxs-lookup"><span data-stu-id="2dc27-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2dc27-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc27-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2dc27-121">系統的虛擬記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2dc27-121">The system is out of virtual memory.</span></span> <span data-ttu-id="2dc27-122">此操作失敗。</span><span class="sxs-lookup"><span data-stu-id="2dc27-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2dc27-123">備註</span><span class="sxs-lookup"><span data-stu-id="2dc27-123">Remarks</span></span>

<span data-ttu-id="2dc27-124">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="2dc27-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="2dc27-125">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="2dc27-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="2dc27-126">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="2dc27-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="2dc27-127">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="2dc27-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="2dc27-128">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="2dc27-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc27-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dc27-129">Requirements</span></span>



| <span data-ttu-id="2dc27-130">需求</span><span class="sxs-lookup"><span data-stu-id="2dc27-130">Requirement</span></span> | <span data-ttu-id="2dc27-131">值</span><span class="sxs-lookup"><span data-stu-id="2dc27-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc27-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2dc27-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc27-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dc27-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2dc27-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2dc27-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc27-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dc27-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2dc27-136">標頭</span><span class="sxs-lookup"><span data-stu-id="2dc27-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc27-137"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc27-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="2dc27-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2dc27-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc27-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc27-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc27-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dc27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc27-141">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="2dc27-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





