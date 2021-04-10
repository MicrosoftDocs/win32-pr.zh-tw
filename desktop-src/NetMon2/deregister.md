---
description: 取消註冊匯出函數會釋出用來建立通訊協定屬性資料庫的資源。 剖析器 DLL 必須執行取消註冊。
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: '取消註冊回呼函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192633"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="fce01-104">取消註冊回呼函數</span><span class="sxs-lookup"><span data-stu-id="fce01-104">Deregister callback function</span></span>

<span data-ttu-id="fce01-105">取消 **註冊** 匯出函數會釋出用來建立通訊協定 [*屬性資料庫*](p.md)的資源。</span><span class="sxs-lookup"><span data-stu-id="fce01-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="fce01-106">剖析器 DLL 必須執行取消 **註冊**。</span><span class="sxs-lookup"><span data-stu-id="fce01-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce01-107">語法</span><span class="sxs-lookup"><span data-stu-id="fce01-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="fce01-108">參數</span><span class="sxs-lookup"><span data-stu-id="fce01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce01-109">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fce01-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce01-110">特定資料庫之通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fce01-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce01-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fce01-111">Return value</span></span>

<span data-ttu-id="fce01-112">無。</span><span class="sxs-lookup"><span data-stu-id="fce01-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce01-113">備註</span><span class="sxs-lookup"><span data-stu-id="fce01-113">Remarks</span></span>

<span data-ttu-id="fce01-114">網路監視器在將所有 capture 資訊傳遞給剖析器 DLL 之後，會呼叫取消 **註冊** 。</span><span class="sxs-lookup"><span data-stu-id="fce01-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="fce01-115">剖析器 DLL 必須針對剖析器所支援的每個通訊協定，執行取消 **註冊** 函式。</span><span class="sxs-lookup"><span data-stu-id="fce01-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="fce01-116">執行取消 **註冊** 時，剖析器 DLL 必須呼叫 [DestroyPropertyDatabase](destroypropertydatabase.md) 函式來釋放 [*屬性資料庫*](p.md) 資源。</span><span class="sxs-lookup"><span data-stu-id="fce01-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="fce01-117">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="fce01-117">For information on</span></span>                                        | <span data-ttu-id="fce01-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="fce01-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="fce01-119">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="fce01-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="fce01-120">解析 器</span><span class="sxs-lookup"><span data-stu-id="fce01-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="fce01-121">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="fce01-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="fce01-122">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="fce01-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="fce01-123">如何執行取消 **註冊**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="fce01-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="fce01-124">執行取消註冊</span><span class="sxs-lookup"><span data-stu-id="fce01-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="fce01-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fce01-125">Requirements</span></span>



| <span data-ttu-id="fce01-126">需求</span><span class="sxs-lookup"><span data-stu-id="fce01-126">Requirement</span></span> | <span data-ttu-id="fce01-127">值</span><span class="sxs-lookup"><span data-stu-id="fce01-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fce01-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fce01-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fce01-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fce01-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fce01-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fce01-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fce01-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fce01-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fce01-132">標頭</span><span class="sxs-lookup"><span data-stu-id="fce01-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce01-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fce01-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce01-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fce01-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce01-135">DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="fce01-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




