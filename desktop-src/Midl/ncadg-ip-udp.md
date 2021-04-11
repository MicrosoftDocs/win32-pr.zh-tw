---
title: ncadg_ip_udp 屬性
description: Ncadg \_ ip \_ udp 關鍵字會識別 tcp/ip 的資料包版本，作為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092676"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="eda1d-105">ncadg \_ ip \_ udp 屬性</span><span class="sxs-lookup"><span data-stu-id="eda1d-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="eda1d-106">**Ncadg \_ ip \_ udp** 關鍵字會識別 tcp/ip 的資料包版本，作為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="eda1d-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="eda1d-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="eda1d-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="eda1d-108">參數</span><span class="sxs-lookup"><span data-stu-id="eda1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda1d-109">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="eda1d-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="eda1d-110">指定伺服器或主機電腦的名稱或網際網路位址。</span><span class="sxs-lookup"><span data-stu-id="eda1d-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="eda1d-111">名稱是字元字串，而且可能是完整的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="eda1d-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="eda1d-112">網際網路位址是常見的網際網路位址標記法。</span><span class="sxs-lookup"><span data-stu-id="eda1d-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="eda1d-113">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="eda1d-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="eda1d-114">指定選用的16位數位。</span><span class="sxs-lookup"><span data-stu-id="eda1d-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="eda1d-115">通常會保留小於1024的值。</span><span class="sxs-lookup"><span data-stu-id="eda1d-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="eda1d-116">如果未指定任何值，則端點對應服務會選取有效的 *埠名稱* 值。</span><span class="sxs-lookup"><span data-stu-id="eda1d-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eda1d-117">備註</span><span class="sxs-lookup"><span data-stu-id="eda1d-117">Remarks</span></span>

<span data-ttu-id="eda1d-118">下列限制適用于資料包協定、 [**ncadg \_ ipx**](ncadg-ipx.md) 和 **ncadg \_ ip \_ udp**：</span><span class="sxs-lookup"><span data-stu-id="eda1d-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="eda1d-119">它們不支援回呼。</span><span class="sxs-lookup"><span data-stu-id="eda1d-119">They do not support callbacks.</span></span> <span data-ttu-id="eda1d-120">使用回呼屬性的任何函數 **\[** [](callback.md) **\]** 都會失敗。</span><span class="sxs-lookup"><span data-stu-id="eda1d-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="eda1d-121">它們不支援使用 [**管道**](pipe.md) 類型的函式。</span><span class="sxs-lookup"><span data-stu-id="eda1d-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="eda1d-122">TCP/IP 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="eda1d-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="eda1d-123">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="eda1d-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="eda1d-124">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="eda1d-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="eda1d-125">範例</span><span class="sxs-lookup"><span data-stu-id="eda1d-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="eda1d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eda1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda1d-127">**端點**</span><span class="sxs-lookup"><span data-stu-id="eda1d-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="eda1d-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="eda1d-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="eda1d-129">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="eda1d-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="eda1d-130">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="eda1d-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="eda1d-131">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="eda1d-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="eda1d-132">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="eda1d-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="eda1d-133">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="eda1d-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="eda1d-134">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="eda1d-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="eda1d-135">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="eda1d-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="eda1d-136">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="eda1d-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="eda1d-137">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="eda1d-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="eda1d-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="eda1d-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="eda1d-139">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="eda1d-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="eda1d-140">字串系結</span><span class="sxs-lookup"><span data-stu-id="eda1d-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 