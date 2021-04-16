---
description: SetCCInstPtr 函式會捕捉內容實例指標。
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: 'SetCCInstPtr 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511829"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="de16f-103">SetCCInstPtr 函式</span><span class="sxs-lookup"><span data-stu-id="de16f-103">SetCCInstPtr function</span></span>

<span data-ttu-id="de16f-104">**SetCCInstPtr** 函式會捕捉內容實例指標。</span><span class="sxs-lookup"><span data-stu-id="de16f-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="de16f-105">語法</span><span class="sxs-lookup"><span data-stu-id="de16f-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="de16f-106">參數</span><span class="sxs-lookup"><span data-stu-id="de16f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de16f-107">*lpCurCaptureInst*</span><span class="sxs-lookup"><span data-stu-id="de16f-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="de16f-108">新增至 capture 的實例資料指標。</span><span class="sxs-lookup"><span data-stu-id="de16f-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de16f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="de16f-109">Return value</span></span>

<span data-ttu-id="de16f-110">無。</span><span class="sxs-lookup"><span data-stu-id="de16f-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="de16f-111">備註</span><span class="sxs-lookup"><span data-stu-id="de16f-111">Remarks</span></span>

<span data-ttu-id="de16f-112">使用此函式可將指標儲存至使用 **CCHeapAlloc** 函式所配置的區塊。</span><span class="sxs-lookup"><span data-stu-id="de16f-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="de16f-113">每個剖析器都可以在 capture 上設定單一的資料實例。</span><span class="sxs-lookup"><span data-stu-id="de16f-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="de16f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="de16f-114">Requirements</span></span>



| <span data-ttu-id="de16f-115">需求</span><span class="sxs-lookup"><span data-stu-id="de16f-115">Requirement</span></span> | <span data-ttu-id="de16f-116">值</span><span class="sxs-lookup"><span data-stu-id="de16f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de16f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de16f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de16f-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de16f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="de16f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de16f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de16f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de16f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de16f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="de16f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de16f-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="de16f-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="de16f-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="de16f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="de16f-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="de16f-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="de16f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de16f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de16f-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de16f-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de16f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de16f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de16f-128">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="de16f-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="de16f-129">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="de16f-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="de16f-130">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="de16f-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="de16f-131">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="de16f-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="de16f-132">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="de16f-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




