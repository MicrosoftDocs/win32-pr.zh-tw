---
title: call_as 屬性
description: '\ 呼叫 \_ as \ 屬性可讓您將無法遠端呼叫的函式對應至遠端函式。'
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as 屬性 MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968679"
---
# <a name="call_as-attribute"></a><span data-ttu-id="c7f1c-104">呼叫 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="c7f1c-104">call\_as attribute</span></span>

<span data-ttu-id="c7f1c-105">**\[ Call \_ as \]** 屬性可讓您將無法遠端呼叫的函式對應至遠端函式。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="c7f1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f1c-107">*本機進程*</span><span class="sxs-lookup"><span data-stu-id="c7f1c-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="c7f1c-108">指定作業定義的常式。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="c7f1c-109">*操作-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="c7f1c-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c7f1c-110">指定套用至作業的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="c7f1c-111">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c7f1c-112">*操作-名稱*</span><span class="sxs-lookup"><span data-stu-id="c7f1c-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c7f1c-113">指定要呈現給應用程式的已命名操作。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7f1c-114">備註</span><span class="sxs-lookup"><span data-stu-id="c7f1c-114">Remarks</span></span>

<span data-ttu-id="c7f1c-115">將無法從遠端呼叫的函式對應至遠端函式的能力，在具有許多參數類型且無法透過網路傳輸的介面上特別有用。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="c7f1c-116">**\[** [**\_**](represent-as.md) **\]** **\[** [**\_**](transmit-as.md) **\]** 您可以使用 **\[ 呼叫 \_ 做 \]** 為常式來合併所有轉換，而不是使用許多表示 as 和傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="c7f1c-117">您可以 (用戶端和伺服器端) 提供兩個 **\[ 呼叫 \_ \]** ，以系結應用程式呼叫與遠端呼叫之間的常式。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="c7f1c-118">**\[ 呼叫 \_ as \]** 屬性可用於物件介面。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="c7f1c-119">在此情況下，介面定義可用於本機呼叫和遠端呼叫，因為 **\[ 呼叫 \_ as \]** 允許無法從遠端存取介面，以明確地對應到遠端介面。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="c7f1c-120">**\[ 呼叫 \_ as \]** 屬性不能與 [**/osf**](-osf.md)模式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="c7f1c-121">例如，假設物件介面 **IFace** 中的常式 **f1** 需要在使用者呼叫和實際傳輸的之間進行許多轉換。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="c7f1c-122">下列範例說明介面 **IFace** 的 IDL 和 ACF 檔案：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="c7f1c-123">在介面 **IFace** 的 IDL 檔案中：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="c7f1c-124">在介面 **IFace** 的 ACF 中：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="c7f1c-125">這會導致產生的標頭檔使用 **f1** 的定義來定義介面，但它也提供 **Remf1** 的存根。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="c7f1c-126">MIDL 編譯器會在介面 **IFace** 的標頭檔中產生下列 Vtable：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="c7f1c-127">然後，用戶端 proxy 會有一般 MIDL 產生的 proxy 以進行 **Remf1**，而 **Remf1** 的伺服器端 STUB 會與一般 MIDL 產生的存根相同：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="c7f1c-128">然後，兩個 (用戶端和伺服器端) 的 **\[ 呼叫 \_ \]** ，都必須手動編碼：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="c7f1c-129">針對物件介面，這些是適用于證券紙的原型。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="c7f1c-130">針對用戶端：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="c7f1c-131">針對伺服器端：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="c7f1c-132">針對非物件介面，這些是適用于此類證券紙的原型。</span><span class="sxs-lookup"><span data-stu-id="c7f1c-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="c7f1c-133">針對用戶端：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="c7f1c-134">針對伺服器端：</span><span class="sxs-lookup"><span data-stu-id="c7f1c-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="c7f1c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7f1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f1c-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c7f1c-137">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="c7f1c-138">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




