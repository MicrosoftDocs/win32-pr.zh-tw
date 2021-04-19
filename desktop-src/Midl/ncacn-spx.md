---
title: ncacn_spx 屬性
description: Ncacn \_ spx 關鍵字會將 spx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967891"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="c1ed9-105">ncacn \_ spx 屬性</span><span class="sxs-lookup"><span data-stu-id="c1ed9-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="c1ed9-106">**Ncacn \_ spx** 關鍵字會將 spx 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="c1ed9-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="c1ed9-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1ed9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ed9-109">*連結位址*</span><span class="sxs-lookup"><span data-stu-id="c1ed9-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ed9-110">指定主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-110">Specifies the host server.</span></span> <span data-ttu-id="c1ed9-111">這可以是 (伺服器名稱) 的字元字串，或是包含主機伺服器的網路位址之20位數的十六進位數位 (8 位數) 與節點位址 (12 位數) 串連。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="c1ed9-112">如需如何取得網路位址和節點位址的指示，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="c1ed9-113">**Null** 字串會指定本機電腦。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="c1ed9-114">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="c1ed9-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ed9-115">指定代表通訊端位址的選用16位數位。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="c1ed9-116">值的範圍可以從1到65535。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="c1ed9-117">未指定任何值時，端點對應服務會選取有效的 *埠名稱* 值。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1ed9-118">備註</span><span class="sxs-lookup"><span data-stu-id="c1ed9-118">Remarks</span></span>

<span data-ttu-id="c1ed9-119">當您使用 **ncacn 的 \_ spx** 傳輸時，伺服器名稱與32位 Windows 名稱完全相同。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="c1ed9-120">不過，因為名稱是使用 Novell 通訊協定來散發，所以它們必須符合 Novell 命名慣例。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="c1ed9-121">如果伺服器名稱不是有效的 Novell 名稱，伺服器將無法使用 **ncacn 的 \_ spx** 傳輸來建立端點。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="c1ed9-122">以下是 Novell 伺服器名稱禁止的部分字元清單：</span><span class="sxs-lookup"><span data-stu-id="c1ed9-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="c1ed9-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="c1ed9-123">" \* + .</span></span> <span data-ttu-id="c1ed9-124">/ : ;< = >？</span><span class="sxs-lookup"><span data-stu-id="c1ed9-124">/ : ; < = > ?</span></span> <span data-ttu-id="c1ed9-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="c1ed9-125">\[ \] \\ \|</span></span>

<span data-ttu-id="c1ed9-126">MS 用戶端3.0 提供的 NWLink 版本不支援 **ncacn 的 \_ spx** 傳輸。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="c1ed9-127">使用 **ncacn \_ spx** 傳輸的16位 Windows 用戶端應用程式需要安裝 Nwipxspx.dll 的檔案，才能在 WOW 子系統下執行。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="c1ed9-128">請聯絡 Novell 以取得此檔案。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="c1ed9-129">若要取得網路和節點位址，請使用 Novell 的 **comcheck** 公用程式或 novell 定義的 API **IPXGetInternetAddress**。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="c1ed9-130">在 Windows 上，您也可以使用 **ipxroute config** 命令取得這些位址。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="c1ed9-131">SPX 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="c1ed9-132">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c1ed9-133">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="c1ed9-134">範例</span><span class="sxs-lookup"><span data-stu-id="c1ed9-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c1ed9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1ed9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ed9-136">**端點**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-137"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="c1ed9-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-138">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-139">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-140">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-141">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-142">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-143">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-144">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-145">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-146">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-147">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-148">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="c1ed9-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="c1ed9-149">字串系結</span><span class="sxs-lookup"><span data-stu-id="c1ed9-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 