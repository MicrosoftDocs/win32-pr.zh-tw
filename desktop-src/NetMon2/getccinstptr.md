---
description: GetCCInstPtr 函式會將指標傳回至已加入至抓取內容的實例資料。
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: 'GetCCInstPtr 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689723"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="f3a4f-103">GetCCInstPtr 函式</span><span class="sxs-lookup"><span data-stu-id="f3a4f-103">GetCCInstPtr function</span></span>

<span data-ttu-id="f3a4f-104">**GetCCInstPtr** 函式會將指標傳回至已加入至抓取內容的實例資料。</span><span class="sxs-lookup"><span data-stu-id="f3a4f-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a4f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3a4f-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="f3a4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3a4f-106">Parameters</span></span>

<span data-ttu-id="f3a4f-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f3a4f-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3a4f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3a4f-108">Return value</span></span>

<span data-ttu-id="f3a4f-109">如果函式成功，則傳回值是特定捕獲之實例資料的指標。</span><span class="sxs-lookup"><span data-stu-id="f3a4f-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="f3a4f-110">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3a4f-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a4f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3a4f-111">Requirements</span></span>



| <span data-ttu-id="f3a4f-112">需求</span><span class="sxs-lookup"><span data-stu-id="f3a4f-112">Requirement</span></span> | <span data-ttu-id="f3a4f-113">值</span><span class="sxs-lookup"><span data-stu-id="f3a4f-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a4f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3a4f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a4f-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a4f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3a4f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3a4f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a4f-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a4f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3a4f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f3a4f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a4f-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f3a4f-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f3a4f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3a4f-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3a4f-121"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3a4f-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3a4f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a4f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a4f-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a4f-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a4f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3a4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a4f-125">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="f3a4f-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="f3a4f-126">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="f3a4f-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="f3a4f-127">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="f3a4f-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="f3a4f-128">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="f3a4f-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="f3a4f-129">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="f3a4f-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




