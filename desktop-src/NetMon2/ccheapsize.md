---
description: CCHeapSize 函式會傳回 CCHeapAlloc 函數所配置的記憶體大小。
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: 'CCHeapSize 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987651"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="03a47-103">CCHeapSize 函式</span><span class="sxs-lookup"><span data-stu-id="03a47-103">CCHeapSize function</span></span>

<span data-ttu-id="03a47-104">**CCHeapSize** 函式會傳回 **CCHeapAlloc** 函數所配置的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="03a47-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a47-105">語法</span><span class="sxs-lookup"><span data-stu-id="03a47-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="03a47-106">參數</span><span class="sxs-lookup"><span data-stu-id="03a47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a47-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="03a47-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="03a47-108">配置的記憶體之指標。</span><span class="sxs-lookup"><span data-stu-id="03a47-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a47-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="03a47-109">Return value</span></span>

<span data-ttu-id="03a47-110">如果函式成功，則傳回值為要求的記憶體區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="03a47-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="03a47-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03a47-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a47-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="03a47-112">Requirements</span></span>



| <span data-ttu-id="03a47-113">需求</span><span class="sxs-lookup"><span data-stu-id="03a47-113">Requirement</span></span> | <span data-ttu-id="03a47-114">值</span><span class="sxs-lookup"><span data-stu-id="03a47-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="03a47-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03a47-115">Minimum supported client</span></span><br/> | <span data-ttu-id="03a47-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a47-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="03a47-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03a47-117">Minimum supported server</span></span><br/> | <span data-ttu-id="03a47-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a47-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="03a47-119">標頭</span><span class="sxs-lookup"><span data-stu-id="03a47-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a47-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="03a47-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="03a47-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="03a47-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="03a47-122"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="03a47-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="03a47-123">DLL</span><span class="sxs-lookup"><span data-stu-id="03a47-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a47-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a47-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a47-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03a47-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a47-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="03a47-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="03a47-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="03a47-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="03a47-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="03a47-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="03a47-129">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="03a47-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="03a47-130">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="03a47-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




