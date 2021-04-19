---
description: ExpertFreeMemory 函式會釋出呼叫 ExpertAllocMemory 和 ExpertReallocMemory 函數所取得的記憶體。
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: 'ExpertFreeMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970373"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="62a72-103">ExpertFreeMemory 函式</span><span class="sxs-lookup"><span data-stu-id="62a72-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="62a72-104">**ExpertFreeMemory** 函式會釋出呼叫 [**ExpertAllocMemory**](expertallocmemory.md)和 [**ExpertReallocMemory**](expertreallocmemory.md)函數所取得的記憶體。</span><span class="sxs-lookup"><span data-stu-id="62a72-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a72-105">語法</span><span class="sxs-lookup"><span data-stu-id="62a72-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="62a72-106">參數</span><span class="sxs-lookup"><span data-stu-id="62a72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a72-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="62a72-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="62a72-108">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="62a72-108">Unique expert identifier.</span></span> <span data-ttu-id="62a72-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="62a72-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="62a72-110">*pMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a72-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a72-111">網路監視器配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="62a72-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="62a72-112">*PMemory* 指標可由前一個對 [**ExpertAllocMemory**](expertallocmemory.md)或 [**ExpertReallocMemory**](expertreallocmemory.md)的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="62a72-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a72-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="62a72-113">Return value</span></span>

<span data-ttu-id="62a72-114">如果函式成功，則為。</span><span class="sxs-lookup"><span data-stu-id="62a72-114">If the function is successful.</span></span> <span data-ttu-id="62a72-115">傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="62a72-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="62a72-116">如果函式不成功，則傳回值會指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="62a72-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="62a72-117">如果傳回值是 NMERR \_ 專家 \_ 終止，則專家會立即清除並返回。</span><span class="sxs-lookup"><span data-stu-id="62a72-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a72-118">備註</span><span class="sxs-lookup"><span data-stu-id="62a72-118">Remarks</span></span>

<span data-ttu-id="62a72-119">請務必注意，專家應該使用網路監視器記憶體配置函式來進行記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="62a72-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="62a72-120">如果您的專家在執行時間失敗，使用這些函式會允許網路監視器釋出它所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="62a72-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a72-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="62a72-121">Requirements</span></span>



| <span data-ttu-id="62a72-122">需求</span><span class="sxs-lookup"><span data-stu-id="62a72-122">Requirement</span></span> | <span data-ttu-id="62a72-123">值</span><span class="sxs-lookup"><span data-stu-id="62a72-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62a72-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62a72-124">Minimum supported client</span></span><br/> | <span data-ttu-id="62a72-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62a72-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="62a72-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62a72-126">Minimum supported server</span></span><br/> | <span data-ttu-id="62a72-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62a72-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="62a72-128">標頭</span><span class="sxs-lookup"><span data-stu-id="62a72-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="62a72-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="62a72-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="62a72-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="62a72-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="62a72-131"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a72-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="62a72-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62a72-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a72-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a72-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




