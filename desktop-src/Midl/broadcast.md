---
title: 廣播屬性
description: 關鍵字 \ 廣播 \ 指定將遠端程序呼叫傳送至區域網路上的所有伺服器。
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- 廣播屬性 MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312854"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="a52c2-104">廣播屬性</span><span class="sxs-lookup"><span data-stu-id="a52c2-104">broadcast attribute</span></span>

<span data-ttu-id="a52c2-105">關鍵字 **\[ 廣播 \]** 指定將遠端程序呼叫傳送至區域網路上的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a52c2-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="a52c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="a52c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52c2-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a52c2-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-108">指定套用至整個介面的零或多個 IDL 屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a52c2-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a52c2-109">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="a52c2-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a52c2-110">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="a52c2-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-111">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="a52c2-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a52c2-112">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a52c2-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-113">指定要套用至函數的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="a52c2-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="a52c2-114">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a52c2-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a52c2-115">*returntype*</span><span class="sxs-lookup"><span data-stu-id="a52c2-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-116">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="a52c2-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="a52c2-117">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a52c2-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-118">指定將套用 **\[ 廣播 \]** 屬性的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="a52c2-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="a52c2-119">*params*</span><span class="sxs-lookup"><span data-stu-id="a52c2-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a52c2-120">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="a52c2-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a52c2-121">備註</span><span class="sxs-lookup"><span data-stu-id="a52c2-121">Remarks</span></span>

<span data-ttu-id="a52c2-122">**\[ 廣播 \]** 關鍵字指定常式一律會廣播到網路上的所有伺服器，而不是傳遞至一部特定的伺服器。用戶端會接收第一個回復的輸出以成功傳回，而後續回復則會捨棄。</span><span class="sxs-lookup"><span data-stu-id="a52c2-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="a52c2-123">具有 **\[ 廣播 \]** 屬性的作業會隱含為 [**\[ 等冪 \]**](idempotent.md)運算。</span><span class="sxs-lookup"><span data-stu-id="a52c2-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="a52c2-124">但是， **\[ 廣播 \]** 屬性會指定具有 **\[ 等冪 \]** 屬性之函式沒有的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="a52c2-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="a52c2-125">具體而言，使用 [ **\[ 廣播 \]** ] 屬性的函式會指定在一個遠端程序呼叫的結果中，可以多次呼叫常式。</span><span class="sxs-lookup"><span data-stu-id="a52c2-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="a52c2-126">同時，可以將它們傳送至多部伺服器。</span><span class="sxs-lookup"><span data-stu-id="a52c2-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="a52c2-127">這與 **\[ 等冪 \]** 屬性不同，它只會指定當呼叫未完成時，可以重試呼叫。</span><span class="sxs-lookup"><span data-stu-id="a52c2-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="a52c2-128">如果遠端程式將它的呼叫廣播到區域網路上的所有主機，則必須使用 [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md) 或 [**ncadg \_ ipx**](ncadg-ipx.md) 通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="a52c2-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="a52c2-129">請注意， **\[ 廣播 \]** 封包的大小取決於使用中的資料包服務。</span><span class="sxs-lookup"><span data-stu-id="a52c2-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="a52c2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a52c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52c2-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="a52c2-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="a52c2-132"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="a52c2-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a52c2-133">**也許**</span><span class="sxs-lookup"><span data-stu-id="a52c2-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="a52c2-134">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="a52c2-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="a52c2-135">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="a52c2-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




