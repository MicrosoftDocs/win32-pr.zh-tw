---
description: CCHeapFree 函式會釋放 CCHeapAlloc 函數所配置的記憶體。
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: 'CCHeapFree 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115744"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="49175-103">CCHeapFree 函式</span><span class="sxs-lookup"><span data-stu-id="49175-103">CCHeapFree function</span></span>

<span data-ttu-id="49175-104">**CCHeapFree** 函式會釋放 **CCHeapAlloc** 函數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="49175-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="49175-105">語法</span><span class="sxs-lookup"><span data-stu-id="49175-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="49175-106">參數</span><span class="sxs-lookup"><span data-stu-id="49175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49175-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="49175-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="49175-108">此函式所釋放之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="49175-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49175-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="49175-109">Return value</span></span>

<span data-ttu-id="49175-110">如果 **CCHeapFree** 函數成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="49175-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="49175-111">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="49175-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="49175-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="49175-112">Requirements</span></span>



| <span data-ttu-id="49175-113">需求</span><span class="sxs-lookup"><span data-stu-id="49175-113">Requirement</span></span> | <span data-ttu-id="49175-114">值</span><span class="sxs-lookup"><span data-stu-id="49175-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49175-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49175-115">Minimum supported client</span></span><br/> | <span data-ttu-id="49175-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49175-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="49175-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49175-117">Minimum supported server</span></span><br/> | <span data-ttu-id="49175-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49175-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49175-119">標頭</span><span class="sxs-lookup"><span data-stu-id="49175-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="49175-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="49175-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="49175-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="49175-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="49175-122"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49175-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="49175-123">DLL</span><span class="sxs-lookup"><span data-stu-id="49175-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49175-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49175-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49175-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49175-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49175-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="49175-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="49175-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="49175-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="49175-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="49175-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="49175-129">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="49175-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="49175-130">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="49175-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




