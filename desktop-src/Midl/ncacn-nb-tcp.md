---
title: ncacn_nb_tcp 屬性
description: Ncacn \_ nb \_ tcp 關鍵字是用來將 Tcp over NetBIOS 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314998"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="72ed6-105">ncacn \_ nb \_ tcp 屬性</span><span class="sxs-lookup"><span data-stu-id="72ed6-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="72ed6-106">**Ncacn \_ nb \_ tcp** 關鍵字是用來將 tcp over NetBIOS 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="72ed6-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="72ed6-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="72ed6-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="72ed6-108">參數</span><span class="sxs-lookup"><span data-stu-id="72ed6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ed6-109">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="72ed6-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="72ed6-110">指定選擇性的8位值範圍從1到254。</span><span class="sxs-lookup"><span data-stu-id="72ed6-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="72ed6-111">小於0x20 的值會保留下來。</span><span class="sxs-lookup"><span data-stu-id="72ed6-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="72ed6-112">如果未指定 *埠名稱* 值，則端點對應服務會選取埠值。</span><span class="sxs-lookup"><span data-stu-id="72ed6-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72ed6-113">備註</span><span class="sxs-lookup"><span data-stu-id="72ed6-113">Remarks</span></span>

<span data-ttu-id="72ed6-114">NetBIOS 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="72ed6-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="72ed6-115">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="72ed6-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="72ed6-116">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="72ed6-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="72ed6-117">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="72ed6-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="72ed6-118">範例</span><span class="sxs-lookup"><span data-stu-id="72ed6-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="72ed6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72ed6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ed6-120">**端點**</span><span class="sxs-lookup"><span data-stu-id="72ed6-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="72ed6-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="72ed6-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="72ed6-122">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="72ed6-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="72ed6-123">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="72ed6-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="72ed6-124">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="72ed6-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="72ed6-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="72ed6-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="72ed6-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="72ed6-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="72ed6-127">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="72ed6-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 