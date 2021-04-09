---
title: ncalrpc 屬性
description: Ncalrpc 關鍵字會將本機處理序間通訊識別為端點的通訊協定系列。 這個關鍵字是必須搭配 \ endpoint \ 屬性使用的其中一個有效通訊協定系列名稱。
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc 屬性 MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933205"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="b6cc5-105">ncalrpc 屬性</span><span class="sxs-lookup"><span data-stu-id="b6cc5-105">ncalrpc attribute</span></span>

<span data-ttu-id="b6cc5-106">**Ncalrpc** 關鍵字會將本機處理序間通訊識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="b6cc5-107">此關鍵字是必須搭配端點屬性使用的其中一個有效的通訊協定系列名稱 **\[** [](endpoint.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="b6cc5-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6cc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6cc5-109">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="b6cc5-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b6cc5-110">指定通訊埠的字元字串， (應用程式、服務或) 服務的實例，以供用戶端用來對伺服器進行進程間呼叫。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="b6cc5-111">字串最多可以包含53個字元，而且不能包含任何反斜線 (\) 字元。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-111">The string can contain up to 53 characters and should not contain any backslash (\) characters.</span></span> <span data-ttu-id="b6cc5-112">電腦名稱稱不得與 **ncalrpc** 關鍵字一起使用。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6cc5-113">備註</span><span class="sxs-lookup"><span data-stu-id="b6cc5-113">Remarks</span></span>

<span data-ttu-id="b6cc5-114">本機處理序間通訊埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="b6cc5-115">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="b6cc5-116">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="b6cc5-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="b6cc5-117">範例</span><span class="sxs-lookup"><span data-stu-id="b6cc5-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="b6cc5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6cc5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6cc5-119">**端點**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-120"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="b6cc5-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-121">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-122">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-123">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-124">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-126">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-127">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-128">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-129">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-130">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-131">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="b6cc5-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="b6cc5-132">字串系結</span><span class="sxs-lookup"><span data-stu-id="b6cc5-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 