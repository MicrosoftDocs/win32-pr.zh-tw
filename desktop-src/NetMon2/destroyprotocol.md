---
description: DestroyProtocol 函式會終結 CreateProtocol 函數所建立的通訊協定。
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: 'DestroyProtocol 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192632"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="4de9a-103">DestroyProtocol 函式</span><span class="sxs-lookup"><span data-stu-id="4de9a-103">DestroyProtocol function</span></span>

<span data-ttu-id="4de9a-104">**DestroyProtocol** 函式會終結 **CreateProtocol** 函數所建立的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4de9a-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4de9a-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="4de9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4de9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de9a-107">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4de9a-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de9a-108">要終結之通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4de9a-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4de9a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4de9a-109">Return value</span></span>

<span data-ttu-id="4de9a-110">無。</span><span class="sxs-lookup"><span data-stu-id="4de9a-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de9a-111">備註</span><span class="sxs-lookup"><span data-stu-id="4de9a-111">Remarks</span></span>

<span data-ttu-id="4de9a-112">剖析器 DLL 會在其 [DllMain](dllmain-parser.md)的執行期間呼叫 **DestroyProtocol** 函數。</span><span class="sxs-lookup"><span data-stu-id="4de9a-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="4de9a-113">當作業系統即將卸載 DLL 時，會呼叫 **DestroyProtocol** 。</span><span class="sxs-lookup"><span data-stu-id="4de9a-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="4de9a-114">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="4de9a-114">For information on</span></span>                                        | <span data-ttu-id="4de9a-115">請參閱</span><span class="sxs-lookup"><span data-stu-id="4de9a-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4de9a-116">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="4de9a-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="4de9a-117">解析 器</span><span class="sxs-lookup"><span data-stu-id="4de9a-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="4de9a-118">如何執行 **DllMain** 包含範例。</span><span class="sxs-lookup"><span data-stu-id="4de9a-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="4de9a-119">執行 DllMain</span><span class="sxs-lookup"><span data-stu-id="4de9a-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="4de9a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4de9a-120">Requirements</span></span>



| <span data-ttu-id="4de9a-121">需求</span><span class="sxs-lookup"><span data-stu-id="4de9a-121">Requirement</span></span> | <span data-ttu-id="4de9a-122">值</span><span class="sxs-lookup"><span data-stu-id="4de9a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4de9a-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4de9a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4de9a-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4de9a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4de9a-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4de9a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4de9a-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4de9a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4de9a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4de9a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de9a-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4de9a-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4de9a-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="4de9a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4de9a-130"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4de9a-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4de9a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4de9a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de9a-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de9a-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de9a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4de9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de9a-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="4de9a-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




