---
description: CCHeapReAlloc 函式會重新配置 CCHeapAlloc 函數所配置的記憶體。
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: 'CCHeapReAlloc 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692943"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="34a64-103">CCHeapReAlloc 函式</span><span class="sxs-lookup"><span data-stu-id="34a64-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="34a64-104">**CCHeapReAlloc** 函式會重新配置 **CCHeapAlloc** 函數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="34a64-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a64-105">語法</span><span class="sxs-lookup"><span data-stu-id="34a64-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="34a64-106">參數</span><span class="sxs-lookup"><span data-stu-id="34a64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a64-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="34a64-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="34a64-108">原始配置記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="34a64-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="34a64-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="34a64-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="34a64-110">重新配置的記憶體大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="34a64-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="34a64-111">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="34a64-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="34a64-112">是否已初始化重新配置記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="34a64-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="34a64-113">如果參數值為 **TRUE**，則新重新配置的記憶體會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="34a64-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a64-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="34a64-114">Return value</span></span>

<span data-ttu-id="34a64-115">如果函式成功，則傳回值是重新配置記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="34a64-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="34a64-116">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="34a64-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a64-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="34a64-117">Requirements</span></span>



| <span data-ttu-id="34a64-118">需求</span><span class="sxs-lookup"><span data-stu-id="34a64-118">Requirement</span></span> | <span data-ttu-id="34a64-119">值</span><span class="sxs-lookup"><span data-stu-id="34a64-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34a64-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34a64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34a64-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34a64-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="34a64-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34a64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34a64-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34a64-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="34a64-124">標頭</span><span class="sxs-lookup"><span data-stu-id="34a64-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a64-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="34a64-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="34a64-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="34a64-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="34a64-127"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a64-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="34a64-128">DLL</span><span class="sxs-lookup"><span data-stu-id="34a64-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a64-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a64-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34a64-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34a64-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a64-131">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="34a64-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="34a64-132">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="34a64-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="34a64-133">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="34a64-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="34a64-134">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="34a64-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="34a64-135">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="34a64-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




