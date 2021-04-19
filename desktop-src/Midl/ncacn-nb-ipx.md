---
title: ncacn_nb_ipx 屬性
description: Ncacn \_ nb \_ ipx 關鍵字會將 NETBIOS 透過 ipx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106995565"
---
# <a name="ncacn_nb_ipx-attribute"></a><span data-ttu-id="37266-105">ncacn \_ nb \_ ipx 屬性</span><span class="sxs-lookup"><span data-stu-id="37266-105">ncacn\_nb\_ipx attribute</span></span>

<span data-ttu-id="37266-106">**Ncacn \_ nb \_ ipx** 關鍵字會將 NetBIOS 透過 ipx 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="37266-106">The **ncacn\_nb\_ipx** keyword identifies NetBIOS over IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="37266-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="37266-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="37266-108">參數</span><span class="sxs-lookup"><span data-stu-id="37266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37266-109">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="37266-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="37266-110">指定選擇性的8位值範圍從1到254。</span><span class="sxs-lookup"><span data-stu-id="37266-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="37266-111">小於0x20 的值會保留下來。</span><span class="sxs-lookup"><span data-stu-id="37266-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="37266-112">如果未指定 *埠名稱* 值，則端點對應服務會選取埠值。</span><span class="sxs-lookup"><span data-stu-id="37266-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37266-113">備註</span><span class="sxs-lookup"><span data-stu-id="37266-113">Remarks</span></span>

<span data-ttu-id="37266-114">NetBIOS 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="37266-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="37266-115">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="37266-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="37266-116">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="37266-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="37266-117">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="37266-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="37266-118">範例</span><span class="sxs-lookup"><span data-stu-id="37266-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="37266-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37266-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37266-120">**端點**</span><span class="sxs-lookup"><span data-stu-id="37266-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="37266-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="37266-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="37266-122">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="37266-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="37266-123">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="37266-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="37266-124">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="37266-124">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="37266-125">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="37266-125">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="37266-126">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="37266-126">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="37266-127">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="37266-127">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="37266-128">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="37266-128">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="37266-129">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="37266-129">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="37266-130">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="37266-130">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="37266-131">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="37266-131">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 