---
description: CreateProtocol 函數會通知網路監視器有特定的通訊協定剖析器存在。
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: 'CreateProtocol 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115741"
---
# <a name="createprotocol-function"></a><span data-ttu-id="e5ac2-103">CreateProtocol 函式</span><span class="sxs-lookup"><span data-stu-id="e5ac2-103">CreateProtocol function</span></span>

<span data-ttu-id="e5ac2-104">**CreateProtocol** 函數會通知網路監視器有特定的通訊協定剖析器存在。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ac2-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5ac2-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="e5ac2-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5ac2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ac2-107">*ProtocolName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5ac2-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ac2-108">剖析器將偵測到的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="e5ac2-109">*lpEntryPoints* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5ac2-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ac2-110">[E](entrypoints.md)結構，其中包含其餘的剖析器 DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="e5ac2-111">如需每個進入點所參考的匯出函式清單，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="e5ac2-112">輸入點必須以 **e** 結構所指定的順序來提供。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="e5ac2-113">*cbEntryPoints* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5ac2-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ac2-114">**E** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="e5ac2-115">網路監視器提供 e \_ 大小宏，可讓您用來指定結構的大小。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ac2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5ac2-116">Return value</span></span>

<span data-ttu-id="e5ac2-117">如果函式成功，則傳回值為通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="e5ac2-118">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5ac2-119">備註</span><span class="sxs-lookup"><span data-stu-id="e5ac2-119">Remarks</span></span>

<span data-ttu-id="e5ac2-120">剖析器 DLL 會在其 [DllMain](dllmain-parser.md)的執行期間呼叫 **CreateProtocol** 。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="e5ac2-121">當作業系統第一次載入剖析器 DLL 時，會呼叫 **CreateProtocol** 函數。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="e5ac2-122">*LpEntryPoints* 參數中所參考的進入點包含下列匯出函式的指標，這些函式必須依照此處提供的順序提供。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="e5ac2-123">註冊</span><span class="sxs-lookup"><span data-stu-id="e5ac2-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="e5ac2-124">取消註冊</span><span class="sxs-lookup"><span data-stu-id="e5ac2-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="e5ac2-125">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="e5ac2-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="e5ac2-126">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="e5ac2-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="e5ac2-127">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="e5ac2-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="e5ac2-128">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="e5ac2-128">For information on</span></span>                                                                                 | <span data-ttu-id="e5ac2-129">請參閱</span><span class="sxs-lookup"><span data-stu-id="e5ac2-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e5ac2-130">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="e5ac2-131">解析 器</span><span class="sxs-lookup"><span data-stu-id="e5ac2-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="e5ac2-132">如何執行 **dllmain** 包含在 **Dllmain** 內呼叫 **CreateProtocol** 的範例。</span><span class="sxs-lookup"><span data-stu-id="e5ac2-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="e5ac2-133">執行 DllMain</span><span class="sxs-lookup"><span data-stu-id="e5ac2-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="e5ac2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5ac2-134">Requirements</span></span>



| <span data-ttu-id="e5ac2-135">需求</span><span class="sxs-lookup"><span data-stu-id="e5ac2-135">Requirement</span></span> | <span data-ttu-id="e5ac2-136">值</span><span class="sxs-lookup"><span data-stu-id="e5ac2-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ac2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5ac2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ac2-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5ac2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e5ac2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5ac2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ac2-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5ac2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5ac2-141">標頭</span><span class="sxs-lookup"><span data-stu-id="e5ac2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ac2-142"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e5ac2-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5ac2-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5ac2-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5ac2-144"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5ac2-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5ac2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ac2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ac2-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ac2-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ac2-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5ac2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ac2-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="e5ac2-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

