---
title: ncacn_dnet_nsp 屬性
description: Ncacn \_ dnet \_ nsp 關鍵字會將 DECnet 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092713"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="060d0-105">ncacn \_ dnet \_ nsp 屬性</span><span class="sxs-lookup"><span data-stu-id="060d0-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="060d0-106">**Ncacn \_ dnet \_ nsp** 關鍵字會將 DECnet 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="060d0-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="060d0-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="060d0-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="060d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="060d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060d0-109">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="060d0-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="060d0-110">指定伺服器或主機電腦的名稱或網際網路位址。</span><span class="sxs-lookup"><span data-stu-id="060d0-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="060d0-111">名稱是字元字串。</span><span class="sxs-lookup"><span data-stu-id="060d0-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="060d0-112">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="060d0-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="060d0-113">指定 DECnet 物件名稱或物件編號。</span><span class="sxs-lookup"><span data-stu-id="060d0-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="060d0-114">物件名稱最多可包含16個字元。</span><span class="sxs-lookup"><span data-stu-id="060d0-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="060d0-115">物件編號可以加上井字型大小 (\#) 。</span><span class="sxs-lookup"><span data-stu-id="060d0-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="060d0-116">備註</span><span class="sxs-lookup"><span data-stu-id="060d0-116">Remarks</span></span>

<span data-ttu-id="060d0-117">DECnet 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="060d0-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="060d0-118">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="060d0-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="060d0-119">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="060d0-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="060d0-120">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="060d0-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="060d0-121">範例</span><span class="sxs-lookup"><span data-stu-id="060d0-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="060d0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="060d0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060d0-123">**端點**</span><span class="sxs-lookup"><span data-stu-id="060d0-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="060d0-124">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="060d0-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 