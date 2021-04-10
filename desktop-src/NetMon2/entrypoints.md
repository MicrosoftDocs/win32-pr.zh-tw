---
description: E 結構定義了匯出函式的進入點，這些函數網路監視器用來操作剖析器。
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: 'E 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936640"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="65eef-103">E 結構</span><span class="sxs-lookup"><span data-stu-id="65eef-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="65eef-104">**E** 結構定義了匯出函式的進入點，這些函數網路監視器用來操作剖析器。</span><span class="sxs-lookup"><span data-stu-id="65eef-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="65eef-105">語法</span><span class="sxs-lookup"><span data-stu-id="65eef-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="65eef-106">成員</span><span class="sxs-lookup"><span data-stu-id="65eef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65eef-107">**註冊**</span><span class="sxs-lookup"><span data-stu-id="65eef-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="65eef-108">[*註冊專家*](register-expert.md)函式的實作為指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="65eef-109">**取消註冊**</span><span class="sxs-lookup"><span data-stu-id="65eef-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="65eef-110">取消 [**註冊**](deregister.md) 函式之執行的指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="65eef-111">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="65eef-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="65eef-112">[**RecognizeFrame**](recognizeframe.md)匯出函式之執行的指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="65eef-113">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="65eef-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="65eef-114">[**AttachProperties**](attachproperties.md)匯出函式之執行的指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="65eef-115">**FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="65eef-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="65eef-116">[**FormatProperties**](formatproperties.md)匯出函式之執行的指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65eef-117">備註</span><span class="sxs-lookup"><span data-stu-id="65eef-117">Remarks</span></span>

<span data-ttu-id="65eef-118">**CreateProtocol** 函式會使用 **e** 結構來提供網路監視器的指標。</span><span class="sxs-lookup"><span data-stu-id="65eef-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="65eef-119">指標必須依照 [先前成員] 區段中所識別的順序來指定。</span><span class="sxs-lookup"><span data-stu-id="65eef-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="65eef-120">如果網路監視器絕不會顯示通訊協定資料，則不需要執行 [**FormatProperties**](formatproperties.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="65eef-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="65eef-121">例如，如果匯出應用程式使用剖析器的輸出，則不需要執行 **FormatProperties** ，而且網路監視器不會顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="65eef-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="65eef-122">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="65eef-122">For information on</span></span>                                        | <span data-ttu-id="65eef-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="65eef-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="65eef-124">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="65eef-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="65eef-125">解析 器</span><span class="sxs-lookup"><span data-stu-id="65eef-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="65eef-126">如何執行 **DllMain**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="65eef-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="65eef-127">執行 DllMain</span><span class="sxs-lookup"><span data-stu-id="65eef-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="65eef-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="65eef-128">Requirements</span></span>



| <span data-ttu-id="65eef-129">需求</span><span class="sxs-lookup"><span data-stu-id="65eef-129">Requirement</span></span> | <span data-ttu-id="65eef-130">值</span><span class="sxs-lookup"><span data-stu-id="65eef-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65eef-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65eef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="65eef-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65eef-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="65eef-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65eef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="65eef-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65eef-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65eef-135">標頭</span><span class="sxs-lookup"><span data-stu-id="65eef-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="65eef-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="65eef-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65eef-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65eef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65eef-138">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="65eef-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="65eef-139">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="65eef-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="65eef-140">取消註冊</span><span class="sxs-lookup"><span data-stu-id="65eef-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="65eef-141">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="65eef-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="65eef-142">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="65eef-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="65eef-143">註冊</span><span class="sxs-lookup"><span data-stu-id="65eef-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




