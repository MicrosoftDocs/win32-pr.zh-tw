---
title: ncacn_vns_spp 屬性
description: Ncacn \_ vns \_ spp 關鍵字會將 BANYAN Vines spp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682052"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="643bb-105">ncacn \_ vns \_ spp 屬性</span><span class="sxs-lookup"><span data-stu-id="643bb-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="643bb-106">**Ncacn \_ vns \_ spp** 關鍵字會將 Banyan Vines spp 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="643bb-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="643bb-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="643bb-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="643bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="643bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643bb-109">*伺服器名稱*</span><span class="sxs-lookup"><span data-stu-id="643bb-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="643bb-110">指定伺服器的 StreetTalk 名稱。</span><span class="sxs-lookup"><span data-stu-id="643bb-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="643bb-111">名稱的格式為 item@group @organization 。</span><span class="sxs-lookup"><span data-stu-id="643bb-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="643bb-112">專案的長度最多可以有31個字元，且群組和組織最多可以有15個字元。</span><span class="sxs-lookup"><span data-stu-id="643bb-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="643bb-113">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="643bb-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="643bb-114">指定 Banyan Vines SPP 埠。</span><span class="sxs-lookup"><span data-stu-id="643bb-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="643bb-115">靜態端點的有效範圍是250–511。</span><span class="sxs-lookup"><span data-stu-id="643bb-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="643bb-116">備註</span><span class="sxs-lookup"><span data-stu-id="643bb-116">Remarks</span></span>

<span data-ttu-id="643bb-117">為了在 Windows 2000 上執行的分散式應用程式中使用 **ncacn \_ vns \_ spp** 傳輸通訊協定，必須安裝適當的 Banyan 企業用戶端軟體。</span><span class="sxs-lookup"><span data-stu-id="643bb-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="643bb-118">安裝之後，開啟 **主控台**，選擇 [設定] **和 [新增**]，然後選取 [ **\| Banyan 的服務 Banyan \| RPC 服務**]。</span><span class="sxs-lookup"><span data-stu-id="643bb-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="643bb-119">支援16位用戶端需要適當的 Vines 軟體。</span><span class="sxs-lookup"><span data-stu-id="643bb-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="643bb-120">如需 Banyan 企業用戶端產品和16位 Vines 軟體的詳細資訊，請洽詢 Banyan。</span><span class="sxs-lookup"><span data-stu-id="643bb-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="643bb-121">Banyan Vines SPP 傳輸埠字串的語法（如同所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="643bb-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="643bb-122">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="643bb-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="643bb-123">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="643bb-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="643bb-124">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="643bb-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="643bb-125">範例</span><span class="sxs-lookup"><span data-stu-id="643bb-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="643bb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="643bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643bb-127">**端點**</span><span class="sxs-lookup"><span data-stu-id="643bb-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="643bb-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="643bb-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="643bb-129">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="643bb-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="643bb-130">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="643bb-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="643bb-131">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="643bb-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="643bb-132">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="643bb-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="643bb-133">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="643bb-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="643bb-134">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="643bb-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="643bb-135">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="643bb-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="643bb-136">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="643bb-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="643bb-137">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="643bb-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="643bb-138">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="643bb-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="643bb-139">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="643bb-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="643bb-140">字串系結</span><span class="sxs-lookup"><span data-stu-id="643bb-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 