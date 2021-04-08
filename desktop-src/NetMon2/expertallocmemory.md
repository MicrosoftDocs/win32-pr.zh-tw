---
description: ExpertAllocMemory 函式會為專家配置記憶體。
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: 'ExpertAllocMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689731"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="d4e17-103">ExpertAllocMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d4e17-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="d4e17-104">**ExpertAllocMemory** 函式會為專家配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="d4e17-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e17-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4e17-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="d4e17-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4e17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e17-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="d4e17-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e17-108">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4e17-108">Unique expert identifier.</span></span> <span data-ttu-id="d4e17-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="d4e17-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d4e17-110">*n* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4e17-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e17-111">配置的記憶體（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d4e17-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4e17-112">*pError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d4e17-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e17-113">錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="d4e17-113">Error indicator.</span></span> <span data-ttu-id="d4e17-114">如果函式失敗， *n* 參數會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4e17-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="d4e17-115">如果錯誤碼是 NMERR \_ 專家 \_ 終止，則專家必須清除並立即返回。</span><span class="sxs-lookup"><span data-stu-id="d4e17-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e17-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4e17-116">Return value</span></span>

<span data-ttu-id="d4e17-117">如果函式成功，則傳回值會是所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="d4e17-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="d4e17-118">如果函式不成功，則傳回值為 **Null**，而 *pError* 會提供錯誤碼來指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="d4e17-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4e17-119">備註</span><span class="sxs-lookup"><span data-stu-id="d4e17-119">Remarks</span></span>

<span data-ttu-id="d4e17-120">請務必注意，專家應該使用網路監視器記憶體配置函式 (包括記憶體管理的 [ExpertReallocMemory](expertreallocmemory.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d4e17-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="d4e17-121">如果您的專家在執行時間失敗，使用這些函式會允許網路監視器釋出它所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d4e17-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e17-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4e17-122">Requirements</span></span>



| <span data-ttu-id="d4e17-123">需求</span><span class="sxs-lookup"><span data-stu-id="d4e17-123">Requirement</span></span> | <span data-ttu-id="d4e17-124">值</span><span class="sxs-lookup"><span data-stu-id="d4e17-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e17-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4e17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d4e17-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4e17-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d4e17-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4e17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d4e17-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4e17-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4e17-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d4e17-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4e17-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d4e17-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d4e17-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4e17-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4e17-132"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4e17-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4e17-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d4e17-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4e17-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4e17-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




