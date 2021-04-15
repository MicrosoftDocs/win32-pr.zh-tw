---
title: message 屬性
description: '\ Message \ 屬性工作表示遠端程序呼叫會被視為從用戶端到伺服器的訊息。'
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- message 屬性 MIDL
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463056"
---
# <a name="message-attribute"></a><span data-ttu-id="16781-104">message 屬性</span><span class="sxs-lookup"><span data-stu-id="16781-104">message attribute</span></span>

<span data-ttu-id="16781-105">Message 屬性（ **\[ message \]** attribute）指出遠端程序呼叫會被視為從用戶端到伺服器的訊息。</span><span class="sxs-lookup"><span data-stu-id="16781-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="16781-106">參數</span><span class="sxs-lookup"><span data-stu-id="16781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16781-107">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="16781-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="16781-108">適用于函數的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="16781-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="16781-109">只有 **\[** [**local**](local.md) **\]** 、 **\[** [**了 nocode**](nocode.md) **\]** 、 **\[** [**code**](code.md) **\]** 和 **\[** [**optimize**](optimize.md) **\]** 屬性可搭配 **\[ message \]** 屬性使用。</span><span class="sxs-lookup"><span data-stu-id="16781-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="16781-110">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="16781-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="16781-111">IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="16781-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="16781-112">*選擇性-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="16781-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="16781-113">將套用至參數的零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="16781-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="16781-114">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="16781-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="16781-115">在 IDL 檔案中定義之參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="16781-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16781-116">備註</span><span class="sxs-lookup"><span data-stu-id="16781-116">Remarks</span></span>

<span data-ttu-id="16781-117">當用戶端收到來自用戶端的訊息時，會透過 [**ncadg \_ mq**](ncadg-mq.md)訊息佇列傳輸，以非同步方式將 **\[ \] 訊息** 屬性的遠端程序呼叫傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="16781-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="16781-118">您可以指定 **ncadg \_ mq** 傳輸通訊協定，而不使用 **\[ \] message** 屬性，來指出同步模式的訊息。</span><span class="sxs-lookup"><span data-stu-id="16781-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="16781-119">藉由指定非同步模式訊息， **\[ message \]** 屬性可讓用戶端進行遠端程序呼叫，並立即傳回，即使伺服器應用程式沒有回應。</span><span class="sxs-lookup"><span data-stu-id="16781-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="16781-120">如果目標伺服器無法使用，則會儲存呼叫，直到伺服器變成可用為止。</span><span class="sxs-lookup"><span data-stu-id="16781-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="16781-121">此外，非同步模式的訊息可讓您控制伺服器接收佇列的訊息佇列屬性。</span><span class="sxs-lookup"><span data-stu-id="16781-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="16781-122">如需有關選取服務品質、呼叫優先順序，以及伺服器進程的呼叫存留期的詳細資訊，請參閱 [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="16781-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="16781-123">下列限制也適用于 **\[ message \]** 屬性：</span><span class="sxs-lookup"><span data-stu-id="16781-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="16781-124">Microsoft Message Queuing 必須在用戶端和伺服器系統中執行，而且這些系統必須由訊息佇列安裝範圍所判斷，彼此都可以看見。</span><span class="sxs-lookup"><span data-stu-id="16781-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="16781-125">系結必須使用已知的端點和 [**ncadg \_ mq**](ncadg-mq.md) 傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="16781-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="16781-126">函數不能包含 output 參數或 [**void**](void.md)以外的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="16781-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="16781-127">請注意，後者的限制會讓 **\[ 訊息 \]** 屬性不適合 COM (物件) 介面方法。</span><span class="sxs-lookup"><span data-stu-id="16781-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="16781-128">下一版的 MIDL 將允許 **\[ 訊息 \]** 函數傳回錯誤 \_ 狀態 \_ t 或 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="16781-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="16781-129">至少包含一個 **\[ 訊息 \]** 呼叫的任何介面，都必須先呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)或 [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex)來註冊，然後再呼叫 [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex)。</span><span class="sxs-lookup"><span data-stu-id="16781-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="16781-130">否則，在註冊介面之前，在佇列中等候伺服器的呼叫會被讀取，且呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="16781-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="16781-131">範例</span><span class="sxs-lookup"><span data-stu-id="16781-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="16781-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16781-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16781-133">**代碼**</span><span class="sxs-lookup"><span data-stu-id="16781-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="16781-134">**當地**</span><span class="sxs-lookup"><span data-stu-id="16781-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="16781-135">**ncadg \_ mq**</span><span class="sxs-lookup"><span data-stu-id="16781-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="16781-136">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="16781-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="16781-137">**優化**</span><span class="sxs-lookup"><span data-stu-id="16781-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="16781-138">RPC 訊息佇列</span><span class="sxs-lookup"><span data-stu-id="16781-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="16781-139">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="16781-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="16781-140">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="16781-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="16781-141">**void**</span><span class="sxs-lookup"><span data-stu-id="16781-141">**void**</span></span>](void.md)
</dt> </dl>

 

 