---
description: CCHeapAlloc 函式會依捕獲來配置記憶體。
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: 'CCHeapAlloc 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849131"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="4337d-103">CCHeapAlloc 函式</span><span class="sxs-lookup"><span data-stu-id="4337d-103">CCHeapAlloc function</span></span>

<span data-ttu-id="4337d-104">**CCHeapAlloc** 函式會依捕獲來配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4337d-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4337d-105">語法</span><span class="sxs-lookup"><span data-stu-id="4337d-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="4337d-106">參數</span><span class="sxs-lookup"><span data-stu-id="4337d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4337d-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="4337d-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="4337d-108">所配置的記憶體長度。</span><span class="sxs-lookup"><span data-stu-id="4337d-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="4337d-109">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="4337d-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="4337d-110">配置的記憶體是否已初始化的指標。</span><span class="sxs-lookup"><span data-stu-id="4337d-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="4337d-111">如果參數值為 **TRUE**，則配置的記憶體會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="4337d-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4337d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4337d-112">Return value</span></span>

<span data-ttu-id="4337d-113">如果函式成功，則傳回值會是所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="4337d-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="4337d-114">當您完成使用已配置的記憶體時，請呼叫 [**CCHeapFree**](ccheapfree.md) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4337d-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="4337d-115">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4337d-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4337d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4337d-116">Requirements</span></span>



| <span data-ttu-id="4337d-117">需求</span><span class="sxs-lookup"><span data-stu-id="4337d-117">Requirement</span></span> | <span data-ttu-id="4337d-118">值</span><span class="sxs-lookup"><span data-stu-id="4337d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4337d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4337d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4337d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4337d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4337d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4337d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4337d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4337d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4337d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4337d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4337d-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4337d-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4337d-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4337d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4337d-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4337d-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4337d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4337d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4337d-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4337d-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4337d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4337d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4337d-130">**SetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="4337d-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4337d-131">**GetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="4337d-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4337d-132">**CCHeapFree**</span><span class="sxs-lookup"><span data-stu-id="4337d-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="4337d-133">**CCHeapReAlloc**</span><span class="sxs-lookup"><span data-stu-id="4337d-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="4337d-134">**CCHeapSize**</span><span class="sxs-lookup"><span data-stu-id="4337d-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




