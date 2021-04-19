---
description: 剖析器的 DllMain 匯出函式會識別剖析器是否存在，並釋放網路監視器用於剖析器的資源。 DllMain 必須在所有剖析器 Dll 中實作為。
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: 'DllMain 剖析器回呼函數 (進程 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980524"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="fa17c-104">DllMain 剖析器回呼函數</span><span class="sxs-lookup"><span data-stu-id="fa17c-104">DllMain Parser callback function</span></span>

<span data-ttu-id="fa17c-105">剖析器的 **DllMain** 匯出函式會識別剖析器是否存在，並釋放網路監視器用於剖析器的資源。</span><span class="sxs-lookup"><span data-stu-id="fa17c-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="fa17c-106">**DllMain** 必須在所有剖析器 dll 中實作為。</span><span class="sxs-lookup"><span data-stu-id="fa17c-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa17c-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa17c-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="fa17c-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa17c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa17c-109">*hInstance* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa17c-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa17c-110">剖析器實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa17c-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="fa17c-111">*命令* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa17c-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa17c-112">判斷如何呼叫函式的指標。</span><span class="sxs-lookup"><span data-stu-id="fa17c-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="fa17c-113">如需所有可能旗標的清單，請參閱 [DllMain](/windows/desktop/Dlls/dllmain)。</span><span class="sxs-lookup"><span data-stu-id="fa17c-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="fa17c-114">剖析器的執行必須處理下列值。</span><span class="sxs-lookup"><span data-stu-id="fa17c-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="fa17c-115">值</span><span class="sxs-lookup"><span data-stu-id="fa17c-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="fa17c-116">意義</span><span class="sxs-lookup"><span data-stu-id="fa17c-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="fa17c-117"><dt>**DLL \_ 進程 \_ 附加**</dt></span><span class="sxs-lookup"><span data-stu-id="fa17c-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="fa17c-118">當您第一次呼叫 **DllMain** 時，DLL 必須呼叫 [CreateProtocol](createprotocol.md) 來提供網路監視器的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa17c-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="fa17c-119"><dt>**DLL \_ 進程卸 \_ 離**</dt></span><span class="sxs-lookup"><span data-stu-id="fa17c-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="fa17c-120">當您最後一次呼叫 **DllMain** 時，dll 必須呼叫 [DESTROYPROTOCOL](destroyprotocol.md) 來釋放 DLL 使用的資源。</span><span class="sxs-lookup"><span data-stu-id="fa17c-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="fa17c-121">*已保留*</span><span class="sxs-lookup"><span data-stu-id="fa17c-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="fa17c-122">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="fa17c-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa17c-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa17c-123">Return value</span></span>

<span data-ttu-id="fa17c-124">剖析器 DLL 一律會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="fa17c-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa17c-125">備註</span><span class="sxs-lookup"><span data-stu-id="fa17c-125">Remarks</span></span>

<span data-ttu-id="fa17c-126">作業系統會呼叫 **DllMain** 來載入和卸載剖析器 DLL。</span><span class="sxs-lookup"><span data-stu-id="fa17c-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="fa17c-127">這個函式是以動態連結程式庫 [DllMain](/windows/desktop/Dlls/dllmain) 函數為基礎。</span><span class="sxs-lookup"><span data-stu-id="fa17c-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="fa17c-128">您也可以使用 **DllMain** 的執行來儲存剖析器的實例，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="fa17c-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="fa17c-129">例如，您可以儲存剖析器 DLL 實例，然後將它用於未來的系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="fa17c-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="fa17c-130">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="fa17c-130">For information on</span></span>                                        | <span data-ttu-id="fa17c-131">請參閱</span><span class="sxs-lookup"><span data-stu-id="fa17c-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fa17c-132">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="fa17c-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="fa17c-133">解析 器</span><span class="sxs-lookup"><span data-stu-id="fa17c-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="fa17c-134">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="fa17c-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="fa17c-135">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="fa17c-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="fa17c-136">如何執行 **DllMain**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="fa17c-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="fa17c-137">執行 DllMain</span><span class="sxs-lookup"><span data-stu-id="fa17c-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="fa17c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa17c-138">Requirements</span></span>



| <span data-ttu-id="fa17c-139">需求</span><span class="sxs-lookup"><span data-stu-id="fa17c-139">Requirement</span></span> | <span data-ttu-id="fa17c-140">值</span><span class="sxs-lookup"><span data-stu-id="fa17c-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa17c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa17c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fa17c-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa17c-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fa17c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa17c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fa17c-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa17c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fa17c-145">標頭</span><span class="sxs-lookup"><span data-stu-id="fa17c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa17c-146"><dt>處理。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa17c-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa17c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa17c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa17c-148">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="fa17c-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="fa17c-149">DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="fa17c-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="fa17c-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="fa17c-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

