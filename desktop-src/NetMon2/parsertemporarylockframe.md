---
description: ParserTemporaryLockFrame 函式會在進入剖析器時鎖定框架，並在函式結束剖析器時將框架解除鎖定。
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: 'ParserTemporaryLockFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001424"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="e15e2-103">ParserTemporaryLockFrame 函式</span><span class="sxs-lookup"><span data-stu-id="e15e2-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="e15e2-104">**ParserTemporaryLockFrame** 函式會在進入剖析器時鎖定框架，並在函式結束剖析器時將框架解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="e15e2-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="e15e2-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="e15e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="e15e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e15e2-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e15e2-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e15e2-108">剖析器所指向框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e15e2-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e15e2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e15e2-109">Return value</span></span>

<span data-ttu-id="e15e2-110">如果函式成功，則傳回值為框架中資料第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="e15e2-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="e15e2-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e15e2-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e15e2-112">備註</span><span class="sxs-lookup"><span data-stu-id="e15e2-112">Remarks</span></span>

<span data-ttu-id="e15e2-113">剖析器不應呼叫 **LockFrame** 函數。</span><span class="sxs-lookup"><span data-stu-id="e15e2-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="e15e2-114">如果剖析器接受鎖定，然後產生錯誤或傳回但未解除鎖定框架，則剖析器會讓系統處於無法變更通訊協定或剪下或複製畫面格的狀態。</span><span class="sxs-lookup"><span data-stu-id="e15e2-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="e15e2-115">剖析器應該使用 **ParserTemporaryLockFrame** 函式，此函式只會在函式專案的內容進入剖析器時授與鎖定。</span><span class="sxs-lookup"><span data-stu-id="e15e2-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="e15e2-116">從剖析器結束時，會釋放該框架的鎖定。</span><span class="sxs-lookup"><span data-stu-id="e15e2-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="e15e2-117">因此，只有在剖析器從呼叫 **AttachProperties** 或 **RecognizeFrame** 函式傳回之後，指標才會是有效的。</span><span class="sxs-lookup"><span data-stu-id="e15e2-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e15e2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e15e2-118">Requirements</span></span>



| <span data-ttu-id="e15e2-119">需求</span><span class="sxs-lookup"><span data-stu-id="e15e2-119">Requirement</span></span> | <span data-ttu-id="e15e2-120">值</span><span class="sxs-lookup"><span data-stu-id="e15e2-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e15e2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e15e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e15e2-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e15e2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e15e2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e15e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e15e2-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e15e2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e15e2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e15e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e15e2-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e15e2-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e15e2-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e15e2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e15e2-128"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e15e2-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e15e2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e15e2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e15e2-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e15e2-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




