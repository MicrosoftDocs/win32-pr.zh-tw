---
title: ncadg_mq 屬性
description: Ncadg \_ mq 關鍵字會識別 Microsoft Message Queuing 服務 (MSMQ) 作為端點的傳輸通訊協定。 此通訊協定已淘汰，不應在新的應用程式中使用。
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq 屬性 MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933155"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="4e73e-105">ncadg \_ mq 屬性</span><span class="sxs-lookup"><span data-stu-id="4e73e-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="4e73e-106">**Ncadg \_ mq** 關鍵字會識別 MICROSOFT MESSAGE QUEUING 服務 (MSMQ) 作為端點的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4e73e-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="4e73e-107">此通訊協定已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="4e73e-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="4e73e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e73e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e73e-109">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="4e73e-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4e73e-110">指定伺服器或主機的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4e73e-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="4e73e-111">名稱是字元字串，而且可能是完整的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4e73e-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e73e-112">備註</span><span class="sxs-lookup"><span data-stu-id="4e73e-112">Remarks</span></span>

<span data-ttu-id="4e73e-113">若要使用 **ncadg \_ mq** 傳輸通訊協定，必須完整安裝 MSMQ 元件，而且用戶端和伺服器系統必須可透過 mq 通訊協定連線。</span><span class="sxs-lookup"><span data-stu-id="4e73e-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="4e73e-114">**Ncadg \_ mq** 通訊協定不支援動態端點或 [**廣播**](broadcast.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e73e-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="4e73e-115">如同其他資料包通訊協定， **ncadg \_ mq** 不支援回呼; 使用 [**回呼**](callback.md) 屬性的任何函式都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4e73e-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="4e73e-116">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="4e73e-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4e73e-117">範例</span><span class="sxs-lookup"><span data-stu-id="4e73e-117">Examples</span></span>

<span data-ttu-id="4e73e-118">訊息佇列通訊協定的語法會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="4e73e-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="4e73e-119">MIDL 編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="4e73e-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="4e73e-120">某些錯誤可能會在執行時間（而不是在編譯期間）回報。</span><span class="sxs-lookup"><span data-stu-id="4e73e-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="4e73e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e73e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e73e-122">**廣播**</span><span class="sxs-lookup"><span data-stu-id="4e73e-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="4e73e-123">**回撥**</span><span class="sxs-lookup"><span data-stu-id="4e73e-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="4e73e-124">**端點**</span><span class="sxs-lookup"><span data-stu-id="4e73e-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="4e73e-125"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="4e73e-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4e73e-126">**消息**</span><span class="sxs-lookup"><span data-stu-id="4e73e-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="4e73e-127">RPC 訊息佇列</span><span class="sxs-lookup"><span data-stu-id="4e73e-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="4e73e-128">字串系結</span><span class="sxs-lookup"><span data-stu-id="4e73e-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 