---
title: ncacn_np 屬性
description: Ncacn \_ np 關鍵字會將具名管道識別為端點的通訊協定系列。
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682216"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="aaa37-104">ncacn \_ np 屬性</span><span class="sxs-lookup"><span data-stu-id="aaa37-104">ncacn\_np attribute</span></span>

<span data-ttu-id="aaa37-105">**Ncacn \_ np** 關鍵字會將具名管道識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="aaa37-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="aaa37-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaa37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa37-107">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="aaa37-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa37-108">選擇性。</span><span class="sxs-lookup"><span data-stu-id="aaa37-108">Optional.</span></span> <span data-ttu-id="aaa37-109">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaa37-109">Specifies the name of the server.</span></span> <span data-ttu-id="aaa37-110">反斜線字元是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aaa37-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="aaa37-111">*管道名稱*</span><span class="sxs-lookup"><span data-stu-id="aaa37-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa37-112">指定有效的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="aaa37-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="aaa37-113">有效的管道名稱是一個字串，其中包含以反斜線字元分隔的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaa37-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="aaa37-114">第一個識別碼必須是 [**管道**](pipe.md)。</span><span class="sxs-lookup"><span data-stu-id="aaa37-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="aaa37-115">每個識別碼都必須以兩個反斜線字元分隔。</span><span class="sxs-lookup"><span data-stu-id="aaa37-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaa37-116">備註</span><span class="sxs-lookup"><span data-stu-id="aaa37-116">Remarks</span></span>

<span data-ttu-id="aaa37-117">伺服器會建立具名管道的實例，然後可供任何用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="aaa37-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="aaa37-118">當用戶端嘗試連接時，現有的實例會與該用戶端相關聯。</span><span class="sxs-lookup"><span data-stu-id="aaa37-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="aaa37-119">在另一個用戶端可以連線之前，伺服器必須建立另一個具名管道的實例。</span><span class="sxs-lookup"><span data-stu-id="aaa37-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="aaa37-120">如果用戶端在建立新的實例之前嘗試系結至伺服器，系結呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)可能會失敗，並出現錯誤訊息： RPC \_ S \_ 伺服器 \_ 太 \_ 忙碌。</span><span class="sxs-lookup"><span data-stu-id="aaa37-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="aaa37-121">因此，您必須確定您的用戶端應用程式會處理伺服器太忙碌而無法接受連接的情況。</span><span class="sxs-lookup"><span data-stu-id="aaa37-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="aaa37-122">用戶端應該會自動重試、提示使用者進行動作，或正常地失敗。</span><span class="sxs-lookup"><span data-stu-id="aaa37-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="aaa37-123">具名管道埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="aaa37-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="aaa37-124">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="aaa37-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="aaa37-125">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="aaa37-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="aaa37-126">範例</span><span class="sxs-lookup"><span data-stu-id="aaa37-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="aaa37-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaa37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa37-128">**端點**</span><span class="sxs-lookup"><span data-stu-id="aaa37-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="aaa37-129"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="aaa37-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="aaa37-130">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="aaa37-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-131">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="aaa37-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-132">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="aaa37-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-133">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="aaa37-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="aaa37-134">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="aaa37-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="aaa37-135">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="aaa37-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="aaa37-136">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="aaa37-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-137">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="aaa37-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="aaa37-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="aaa37-139">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="aaa37-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="aaa37-140">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="aaa37-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="aaa37-141">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="aaa37-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 