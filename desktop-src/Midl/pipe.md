---
title: pipe 屬性
description: 管道類型的函式可讓您在遠端程序呼叫中，傳輸具型別資料的開放式資料流程。
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- pipe 屬性 MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314761"
---
# <a name="pipe-attribute"></a><span data-ttu-id="763d5-104">pipe 屬性</span><span class="sxs-lookup"><span data-stu-id="763d5-104">pipe attribute</span></span>

<span data-ttu-id="763d5-105">**管道** 類型的函式可讓您在遠端程序呼叫中，傳輸具型別資料的開放式資料流程。</span><span class="sxs-lookup"><span data-stu-id="763d5-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="763d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="763d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763d5-107">*元素類型*</span><span class="sxs-lookup"><span data-stu-id="763d5-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="763d5-108">定義傳輸緩衝區中單一元素的大小。</span><span class="sxs-lookup"><span data-stu-id="763d5-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="763d5-109">*元素類型* 可以是 [基底類型](midl-base-types.md)、預先定義的 \_ 類型、[**結構**](struct.md)、 [**32b 列舉**](v1-enum.md)或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="763d5-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="763d5-110">有幾項限制適用于 *元素 \_ 類型*，如下列備註所述。</span><span class="sxs-lookup"><span data-stu-id="763d5-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="763d5-111">*管道-宣告子*</span><span class="sxs-lookup"><span data-stu-id="763d5-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="763d5-112">指定一或多個識別符或識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="763d5-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="763d5-113">以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="763d5-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="763d5-114">備註</span><span class="sxs-lookup"><span data-stu-id="763d5-114">Remarks</span></span>

<span data-ttu-id="763d5-115">您可以使用 **管道** 類型的函式，以雙向傳送資料。</span><span class="sxs-lookup"><span data-stu-id="763d5-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="763d5-116">**\[** [**In**](in.md) **\]** pipe 參數可讓伺服器在遠端程序呼叫期間，從用戶端提取資料流程。</span><span class="sxs-lookup"><span data-stu-id="763d5-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="763d5-117">**\[**[**輸出**](out-idl.md) **\]** 管道參數可讓伺服器將資料流程推送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="763d5-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="763d5-118">您可以提供用戶端常式來推送和提取資料流程，以及配置資料的全域緩衝區。</span><span class="sxs-lookup"><span data-stu-id="763d5-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="763d5-119">用戶端和伺服器 stub 常式會封送處理和 unmarshal 資料，並將緩衝區的參考傳回到應用程式。</span><span class="sxs-lookup"><span data-stu-id="763d5-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="763d5-120">下列限制適用于管道：</span><span class="sxs-lookup"><span data-stu-id="763d5-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="763d5-121">管道元素不可以是或包含指標、符合標準的陣列、控制碼或內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="763d5-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="763d5-122">此外，在 Microsoft 管道的管道中，管道元素不能是或包含聯 [**集**](union.md)、 [**16b 列舉**](enum.md)或 [**\_ \_ int3264**](--int3264.md)。</span><span class="sxs-lookup"><span data-stu-id="763d5-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="763d5-123">您無法將 **\[** [**傳輸 \_ 視為**](transmit-as.md) **\]** 、 **\[** [**表示 \_ as**](represent-as.md) **\]** 、電傳 **\[** [**\_ 封送**](wire-marshal.md)處理 **\]** 或 **\[** [**使用者 \_ 封送**](user-marshal.md)處理 **\]** 屬性套用至管道類型或 *元素類型*。</span><span class="sxs-lookup"><span data-stu-id="763d5-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="763d5-124">管道類型不可以是結構或等位的成員、指標的目標或陣列的基底類型。</span><span class="sxs-lookup"><span data-stu-id="763d5-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="763d5-125">宣告為管道類型的資料類型只能用來做為遠端呼叫的參數。</span><span class="sxs-lookup"><span data-stu-id="763d5-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="763d5-126">您可以用傳值方式或參考 (**\[** [**ref**](ref.md)指標) 來傳遞管道參數 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="763d5-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="763d5-127">但是，您無法將 **\[** [**ptr**](ptr.md) **\]** 屬性套用至以傳址方式傳遞的管道。</span><span class="sxs-lookup"><span data-stu-id="763d5-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="763d5-128">不論方向為何，您都不能指定具有 **\[** [**唯一**](unique.md) **\]** 或完整指標的管道參數。</span><span class="sxs-lookup"><span data-stu-id="763d5-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="763d5-129">您無法在 **\[** [**物件**](object.md)介面中使用管道 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="763d5-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="763d5-130">您無法將 **\[** [**等冪**](idempotent.md) **\]** 屬性套用至具有管道參數的常式。</span><span class="sxs-lookup"><span data-stu-id="763d5-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="763d5-131">您無法使用序列化屬性，使用 **\[** 管線 [**進行編碼**](encode.md) **\]** 和解碼 **\[** [](decode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="763d5-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="763d5-132">您無法使用自動控制碼（預設值）或搭配使用 **\[** [**auto \_ 控制碼**](auto-handle.md) **\]** 屬性和管道。</span><span class="sxs-lookup"><span data-stu-id="763d5-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="763d5-133">MIDL 編譯器只支援 [**/Oif**](-oi.md) 模式中的管道。</span><span class="sxs-lookup"><span data-stu-id="763d5-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="763d5-134">如需使用管道參數來執行常式的詳細資訊，請參閱《 RPC 程式設計人員指南》中的 [管道](/windows/desktop/Rpc/pipes) 和參考。</span><span class="sxs-lookup"><span data-stu-id="763d5-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="763d5-135">範例</span><span class="sxs-lookup"><span data-stu-id="763d5-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="763d5-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="763d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="763d5-137">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="763d5-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="763d5-138">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="763d5-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="763d5-139">**解碼**</span><span class="sxs-lookup"><span data-stu-id="763d5-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="763d5-140">**編碼**</span><span class="sxs-lookup"><span data-stu-id="763d5-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="763d5-141">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="763d5-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="763d5-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="763d5-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="763d5-143">**在**</span><span class="sxs-lookup"><span data-stu-id="763d5-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="763d5-144">**物件**</span><span class="sxs-lookup"><span data-stu-id="763d5-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="763d5-145">**擴展**</span><span class="sxs-lookup"><span data-stu-id="763d5-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="763d5-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="763d5-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="763d5-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="763d5-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="763d5-148">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="763d5-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="763d5-149">**結構**</span><span class="sxs-lookup"><span data-stu-id="763d5-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="763d5-150">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="763d5-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="763d5-151">**獨特**</span><span class="sxs-lookup"><span data-stu-id="763d5-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="763d5-152">**使用者 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="763d5-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="763d5-153">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="763d5-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 