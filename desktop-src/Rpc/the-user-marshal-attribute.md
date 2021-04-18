---
title: User_marshal 屬性
description: '\ 使用者 \_ 封送處理 \ 屬性是 ACF 類型的屬性，類似于以 \ 表示的語法 \_ 。'
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- 遠端程序呼叫 RPC、屬性、user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463489"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="2532d-105">使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="2532d-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="2532d-106">\[[使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理 \] 屬性是 ACF 類型的屬性，類似于用來 \[ [表示 \_ ](/windows/desktop/Midl/represent-as)的語法 \] 。</span><span class="sxs-lookup"><span data-stu-id="2532d-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="2532d-107">如同 IDL 屬性（ \[ network [ \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] ），它可提供更有效率的方式，在網路上封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="2532d-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="2532d-108">**\[ 使用者 \_ 封送 \]** 處理是 ACF 屬性，可讓您將未知的自訂資料類型封送處理。</span><span class="sxs-lookup"><span data-stu-id="2532d-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="2532d-109">每個應用程式特定類型都有對應的可類型，可定義網路標記法。</span><span class="sxs-lookup"><span data-stu-id="2532d-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="2532d-110">您的應用程式特定類型可以是簡單、複合或指標類型。</span><span class="sxs-lookup"><span data-stu-id="2532d-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="2532d-111">主要限制是型別實例必須有固定且妥善定義的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="2532d-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="2532d-112">如果您的型別實例大小需要變更，請使用指標欄位，而不是符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="2532d-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="2532d-113">或者，您也可以定義可變更型別的指標。</span><span class="sxs-lookup"><span data-stu-id="2532d-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="2532d-114">如同 [ **\[ 有線 \_ 封送 \]** 處理] 屬性，您可以提供用於調整大小、封送處理、封送處理和釋放行程的常式。</span><span class="sxs-lookup"><span data-stu-id="2532d-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="2532d-115">下表描述四個使用者提供的常式名稱。</span><span class="sxs-lookup"><span data-stu-id="2532d-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="2532d-116"><type>是在 **\[ 使用者 \_ 封送 \]** 處理類型定義中指定的 userm *類型*。</span><span class="sxs-lookup"><span data-stu-id="2532d-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="2532d-117">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="2532d-117">Routine</span></span>                                                            | <span data-ttu-id="2532d-118">Description</span><span class="sxs-lookup"><span data-stu-id="2532d-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2532d-119"><type>\_UserSize</span><span class="sxs-lookup"><span data-stu-id="2532d-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="2532d-120">在用戶端或伺服器端上進行封送處理之前，先調整 RPC 資料緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="2532d-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="2532d-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="2532d-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="2532d-122">將用戶端或伺服器端上的資料封送處理。</span><span class="sxs-lookup"><span data-stu-id="2532d-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="2532d-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="2532d-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="2532d-124">拆收用戶端或伺服器端上的資料。</span><span class="sxs-lookup"><span data-stu-id="2532d-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="2532d-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="2532d-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="2532d-126">釋放伺服器端的資料。</span><span class="sxs-lookup"><span data-stu-id="2532d-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="2532d-127">這些使用者提供的常式是由用戶端或伺服器應用程式，以方向屬性為基礎來提供。</span><span class="sxs-lookup"><span data-stu-id="2532d-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="2532d-128">如果參數為 \[ [](/windows/desktop/Midl/in) \] ，則用戶端會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="2532d-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="2532d-129">用戶端需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。</span><span class="sxs-lookup"><span data-stu-id="2532d-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="2532d-130">伺服器需要 **<type> \_ UserUnmarshal** 和 **<type> \_ UserFree** 函數。</span><span class="sxs-lookup"><span data-stu-id="2532d-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="2532d-131">針對 \[ [out](/windows/desktop/Midl/out-idl) \] 參數，伺服器會傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="2532d-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="2532d-132">當用戶端需要 **<type> \_ UserMarshal** 函式時，伺服器需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。</span><span class="sxs-lookup"><span data-stu-id="2532d-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2532d-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="2532d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2532d-134">有線 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="2532d-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="2532d-135">封送處理使用者封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="2532d-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="2532d-136">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="2532d-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="2532d-137">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="2532d-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="2532d-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="2532d-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 