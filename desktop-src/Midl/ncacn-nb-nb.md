---
title: ncacn_nb_nb 屬性
description: Ncacn \_ nb \_ nb 關鍵字會識別透過 NetBIOS 的 NetBEUI 作為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969902"
---
# <a name="ncacn_nb_nb-attribute"></a><span data-ttu-id="7242e-105">ncacn \_ nb \_ nb 屬性</span><span class="sxs-lookup"><span data-stu-id="7242e-105">ncacn\_nb\_nb attribute</span></span>

<span data-ttu-id="7242e-106">**Ncacn \_ nb \_ nb** 關鍵字會識別透過 NetBIOS 的 NetBEUI 作為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="7242e-106">The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="7242e-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="7242e-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="7242e-108">參數</span><span class="sxs-lookup"><span data-stu-id="7242e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7242e-109">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="7242e-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7242e-110">指定選擇性的8位值範圍從1到255。</span><span class="sxs-lookup"><span data-stu-id="7242e-110">Specifies an optional 8-bit value ranging from 1 to 255.</span></span> <span data-ttu-id="7242e-111">小於0x20 的值會保留下來。</span><span class="sxs-lookup"><span data-stu-id="7242e-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="7242e-112">如果未指定 *埠名稱* 值，則端點對應服務會選取埠值。</span><span class="sxs-lookup"><span data-stu-id="7242e-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7242e-113">備註</span><span class="sxs-lookup"><span data-stu-id="7242e-113">Remarks</span></span>

<span data-ttu-id="7242e-114">NetBIOS 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="7242e-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="7242e-115">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="7242e-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="7242e-116">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="7242e-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="7242e-117">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="7242e-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7242e-118">範例</span><span class="sxs-lookup"><span data-stu-id="7242e-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="7242e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7242e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7242e-120">**端點**</span><span class="sxs-lookup"><span data-stu-id="7242e-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="7242e-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="7242e-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7242e-122">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="7242e-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="7242e-123">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="7242e-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="7242e-124">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="7242e-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="7242e-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="7242e-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="7242e-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="7242e-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="7242e-127">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="7242e-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 