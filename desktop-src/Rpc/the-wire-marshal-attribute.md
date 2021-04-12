---
title: Wire_marshal 屬性
description: '\\ 傳址 \_ 封送處理 \ 屬性是類似于 \ 傳輸形式的 IDL 型別屬性 \_ （attribute），但提供更有效率的方式，在網路上封送處理資料。'
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- 遠端程序呼叫 RPC、屬性、wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376105"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="21ae6-105">有線 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="21ae6-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="21ae6-106">[ \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理] \] 屬性是一種 IDL 型別屬性，類似于 \[ [傳輸 \_ ](/windows/desktop/Midl/transmit-as)的語法 \] ，但是提供更有效率的方式在網路上封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="21ae6-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="21ae6-107">您可以使用 [ \[ **有線 \_ 封送** 處理] \] 屬性來指定要傳送的資料類型，以取代應用程式特定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="21ae6-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="21ae6-108">每個應用程式特定類型都有對應的可類型，可定義網路) 上所用標記法 (的網路標記法。應用程式專屬的型別不需要可，但必須是 MIDL 可識別的型別。</span><span class="sxs-lookup"><span data-stu-id="21ae6-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="21ae6-109">若要將未知的類型封送處理為 MIDL，請使用 ACF 屬性 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理 \] 。</span><span class="sxs-lookup"><span data-stu-id="21ae6-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="21ae6-110">您的應用程式特定類型可以是簡單、複合或指標類型。</span><span class="sxs-lookup"><span data-stu-id="21ae6-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="21ae6-111">主要限制是型別實例必須有固定且妥善定義的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="21ae6-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="21ae6-112">如果您的型別實例大小需要變更，請使用指標欄位，而不是符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="21ae6-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="21ae6-113">或者，您也可以定義可變更型別的指標。</span><span class="sxs-lookup"><span data-stu-id="21ae6-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="21ae6-114">您必須提供用來調整大小、封送處理和封送處理資料的常式，以及釋放相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="21ae6-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="21ae6-115">下表描述四個使用者提供的常式名稱。</span><span class="sxs-lookup"><span data-stu-id="21ae6-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="21ae6-116"><type>是在 \[ **有線 \_ 封送** 處理類型定義中指定的 userm 類型 \] 。</span><span class="sxs-lookup"><span data-stu-id="21ae6-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="21ae6-117">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="21ae6-117">Routine</span></span>                                                            | <span data-ttu-id="21ae6-118">Description</span><span class="sxs-lookup"><span data-stu-id="21ae6-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="21ae6-119"><type>\_UserSize</span><span class="sxs-lookup"><span data-stu-id="21ae6-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="21ae6-120">在用戶端或伺服器端上進行封送處理之前，先調整 RPC 資料緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="21ae6-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="21ae6-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="21ae6-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="21ae6-122">將用戶端或伺服器端上的資料封送處理。</span><span class="sxs-lookup"><span data-stu-id="21ae6-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="21ae6-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="21ae6-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="21ae6-124">拆收用戶端或伺服器端上的資料。</span><span class="sxs-lookup"><span data-stu-id="21ae6-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="21ae6-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="21ae6-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="21ae6-126">釋放伺服器端的資料。</span><span class="sxs-lookup"><span data-stu-id="21ae6-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="21ae6-127">這些程式設計人員提供的常式是由用戶端或伺服器應用程式根據方向屬性提供。</span><span class="sxs-lookup"><span data-stu-id="21ae6-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="21ae6-128">如果參數為 \[ [](/windows/desktop/Midl/in) \] ，則用戶端會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="21ae6-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="21ae6-129">用戶端需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。</span><span class="sxs-lookup"><span data-stu-id="21ae6-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="21ae6-130">伺服器需要 **<type> \_ UserUnmarshal** 和 **<type> \_ UserFree** 函數。</span><span class="sxs-lookup"><span data-stu-id="21ae6-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="21ae6-131">針對 \[ [out](/windows/desktop/Midl/out-idl) \] 參數，伺服器會傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="21ae6-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="21ae6-132">當用戶端需要 **<type> \_ UserMarshal** 函式時，伺服器需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。</span><span class="sxs-lookup"><span data-stu-id="21ae6-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21ae6-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="21ae6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ae6-134">使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="21ae6-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="21ae6-135">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="21ae6-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="21ae6-136">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="21ae6-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="21ae6-137">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="21ae6-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="21ae6-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="21ae6-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 