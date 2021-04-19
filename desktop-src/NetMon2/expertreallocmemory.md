---
description: ExpertReallocMemory 函式會增加或減少網路監視器所配置的記憶體數量。
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: 'ExpertReallocMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973420"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="96e47-103">ExpertReallocMemory 函式</span><span class="sxs-lookup"><span data-stu-id="96e47-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="96e47-104">**ExpertReallocMemory** 函式會增加或減少網路監視器所配置的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="96e47-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e47-105">語法</span><span class="sxs-lookup"><span data-stu-id="96e47-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="96e47-106">參數</span><span class="sxs-lookup"><span data-stu-id="96e47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e47-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96e47-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e47-108">[**執行**](run.md)或 [**設定**](configure.md)時傳遞給專家的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="96e47-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="96e47-109">*pOriginalMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96e47-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e47-110">網路監視器所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="96e47-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="96e47-111">*POriginalMemory* 指標可由前一個對 [**ExpertAllocMemory**](expertallocmemory.md)或 **ExpertReallocMemory** 的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="96e47-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="96e47-112">*n* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96e47-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e47-113">重新配置記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="96e47-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="96e47-114">*pError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96e47-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96e47-115">傳回時，如果函式失敗，則為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96e47-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="96e47-116">如果錯誤碼是 NMERR \_ 專家 \_ 終止，則專家必須清除並立即返回。</span><span class="sxs-lookup"><span data-stu-id="96e47-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e47-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="96e47-117">Return value</span></span>

<span data-ttu-id="96e47-118">如果函式成功，則傳回值會是所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="96e47-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="96e47-119">如果函式不成功，則傳回值為 **null**，而且如果是非 **Null** 值，則 *pError* () 指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="96e47-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e47-120">備註</span><span class="sxs-lookup"><span data-stu-id="96e47-120">Remarks</span></span>

<span data-ttu-id="96e47-121">請務必注意，專家應該使用網路監視器記憶體配置函式來進行記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="96e47-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="96e47-122">如果您的專家在執行時間失敗，使用這些函式會允許網路監視器釋出它所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="96e47-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e47-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="96e47-123">Requirements</span></span>



| <span data-ttu-id="96e47-124">需求</span><span class="sxs-lookup"><span data-stu-id="96e47-124">Requirement</span></span> | <span data-ttu-id="96e47-125">值</span><span class="sxs-lookup"><span data-stu-id="96e47-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96e47-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96e47-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96e47-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96e47-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="96e47-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96e47-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96e47-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96e47-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="96e47-130">標頭</span><span class="sxs-lookup"><span data-stu-id="96e47-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e47-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="96e47-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="96e47-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="96e47-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="96e47-133"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="96e47-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="96e47-134">DLL</span><span class="sxs-lookup"><span data-stu-id="96e47-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96e47-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e47-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




