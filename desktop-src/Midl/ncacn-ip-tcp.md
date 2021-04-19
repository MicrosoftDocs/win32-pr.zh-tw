---
title: ncacn_ip_tcp 屬性
description: Ncacn \_ ip \_ tcp 關鍵字會將 tcp/ip 識別為端點的通訊協定系列。
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967479"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="204a2-104">ncacn \_ ip \_ tcp 屬性</span><span class="sxs-lookup"><span data-stu-id="204a2-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="204a2-105">**Ncacn \_ ip \_ tcp** 關鍵字會將 tcp/ip 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="204a2-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="204a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="204a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="204a2-107">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="204a2-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="204a2-108">指定伺服器或主機電腦的名稱或網際網路位址。</span><span class="sxs-lookup"><span data-stu-id="204a2-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="204a2-109">名稱是字元字串。</span><span class="sxs-lookup"><span data-stu-id="204a2-109">The name is a character string.</span></span> <span data-ttu-id="204a2-110">網際網路位址是常見的網際網路位址標記法。</span><span class="sxs-lookup"><span data-stu-id="204a2-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="204a2-111">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="204a2-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="204a2-112">指定選用的16位數位。</span><span class="sxs-lookup"><span data-stu-id="204a2-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="204a2-113">通常會保留小於1024的值。</span><span class="sxs-lookup"><span data-stu-id="204a2-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="204a2-114">如果未指定任何值，則端點對應服務會選取有效的 *埠名稱* 值。</span><span class="sxs-lookup"><span data-stu-id="204a2-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="204a2-115">備註</span><span class="sxs-lookup"><span data-stu-id="204a2-115">Remarks</span></span>

<span data-ttu-id="204a2-116">TCP/IP 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="204a2-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="204a2-117">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="204a2-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="204a2-118">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="204a2-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="204a2-119">範例</span><span class="sxs-lookup"><span data-stu-id="204a2-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="204a2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="204a2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204a2-121">**端點**</span><span class="sxs-lookup"><span data-stu-id="204a2-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="204a2-122"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="204a2-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="204a2-123">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="204a2-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="204a2-124">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="204a2-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="204a2-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="204a2-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="204a2-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="204a2-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="204a2-127">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="204a2-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 