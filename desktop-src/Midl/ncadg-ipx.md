---
title: ncadg_ipx 屬性
description: Ncadg \_ ipx 關鍵字會識別 ipx 作為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx 屬性 MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681877"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="86f14-105">ncadg \_ ipx 屬性</span><span class="sxs-lookup"><span data-stu-id="86f14-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="86f14-106">**Ncadg \_ ipx** 關鍵字會識別 ipx 作為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="86f14-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="86f14-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="86f14-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="86f14-108">參數</span><span class="sxs-lookup"><span data-stu-id="86f14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f14-109">*連結位址*</span><span class="sxs-lookup"><span data-stu-id="86f14-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="86f14-110">指定主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="86f14-110">Specifies the host server.</span></span> <span data-ttu-id="86f14-111">這可以是 (伺服器名稱) 的字元字串，或是包含主機伺服器的網路位址之20位數的十六進位數位 (8 位數) 與節點位址 (12 位數) 串連。</span><span class="sxs-lookup"><span data-stu-id="86f14-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="86f14-112">如需如何取得網路位址和節點位址的指示，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="86f14-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="86f14-113">**Null** 字串會指定本機電腦。</span><span class="sxs-lookup"><span data-stu-id="86f14-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="86f14-114">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="86f14-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86f14-115">指定代表通訊端位址的選用16位數位。</span><span class="sxs-lookup"><span data-stu-id="86f14-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="86f14-116">值的範圍可以從1到65535。</span><span class="sxs-lookup"><span data-stu-id="86f14-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="86f14-117">未指定任何值時，端點對應服務會選取有效的 *埠名稱* 值。</span><span class="sxs-lookup"><span data-stu-id="86f14-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86f14-118">備註</span><span class="sxs-lookup"><span data-stu-id="86f14-118">Remarks</span></span>

<span data-ttu-id="86f14-119">下列限制適用于資料包協定、 **ncadg \_ ipx** 和 [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)：</span><span class="sxs-lookup"><span data-stu-id="86f14-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="86f14-120">它們不支援回呼。</span><span class="sxs-lookup"><span data-stu-id="86f14-120">They do not support callbacks.</span></span> <span data-ttu-id="86f14-121">使用回呼屬性的任何函數 **\[** [](callback.md) **\]** 都會失敗。</span><span class="sxs-lookup"><span data-stu-id="86f14-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="86f14-122">它們不支援使用 [**管道**](pipe.md) 類型的函式。</span><span class="sxs-lookup"><span data-stu-id="86f14-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="86f14-123">使用 **ncadg \_ ipx** 傳輸時，伺服器名稱與32位 Windows server 名稱完全相同。</span><span class="sxs-lookup"><span data-stu-id="86f14-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="86f14-124">不過，因為名稱是使用 Novell 通訊協定來散發，所以它們必須符合 Novell 命名慣例。</span><span class="sxs-lookup"><span data-stu-id="86f14-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="86f14-125">如果伺服器名稱不是有效的 Novell 名稱，伺服器將無法使用 **ncadg 的 \_ ipx** 傳輸來建立端點。</span><span class="sxs-lookup"><span data-stu-id="86f14-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="86f14-126">以下是 Novell 伺服器名稱禁止的部分字元清單：</span><span class="sxs-lookup"><span data-stu-id="86f14-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="86f14-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="86f14-127">" \* + .</span></span> <span data-ttu-id="86f14-128">/ : ;< = >？</span><span class="sxs-lookup"><span data-stu-id="86f14-128">/ : ; < = > ?</span></span> <span data-ttu-id="86f14-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="86f14-129">\[ \] \\ \|</span></span>

<span data-ttu-id="86f14-130">MS 用戶端3.0 提供的 NWLink 版本支援 **ncadg \_ ipx** 傳輸。</span><span class="sxs-lookup"><span data-stu-id="86f14-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="86f14-131">使用 **ncadg \_ ipx** 傳輸的16位 Windows 用戶端應用程式需要安裝 Nwipxspx.dll 的檔案，才能在 WOW 子系統下執行。</span><span class="sxs-lookup"><span data-stu-id="86f14-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="86f14-132">請聯絡 Novell 以取得此檔案。</span><span class="sxs-lookup"><span data-stu-id="86f14-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="86f14-133">若要取得網路和節點位址，請使用 Novell 的 **comcheck** 公用程式或 novell 定義的 API **IPXGetInternetAddress**。</span><span class="sxs-lookup"><span data-stu-id="86f14-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="86f14-134">在 Windows 上，您也可以使用 **ipxroute config** 命令取得這些位址。</span><span class="sxs-lookup"><span data-stu-id="86f14-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="86f14-135">TCP/IP 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。</span><span class="sxs-lookup"><span data-stu-id="86f14-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="86f14-136">編譯器會執行一些語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="86f14-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="86f14-137">某些錯誤可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="86f14-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="86f14-138">Windows XP 不支援此通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="86f14-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="86f14-139">範例</span><span class="sxs-lookup"><span data-stu-id="86f14-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="86f14-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86f14-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f14-141">**端點**</span><span class="sxs-lookup"><span data-stu-id="86f14-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="86f14-142"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="86f14-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="86f14-143">**\_在 \_ dsp ncacn**</span><span class="sxs-lookup"><span data-stu-id="86f14-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="86f14-144">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="86f14-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="86f14-145">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="86f14-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="86f14-146">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="86f14-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="86f14-147">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="86f14-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="86f14-148">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="86f14-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="86f14-149">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="86f14-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="86f14-150">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="86f14-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="86f14-151">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="86f14-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="86f14-152">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="86f14-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="86f14-153">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="86f14-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="86f14-154">字串系結</span><span class="sxs-lookup"><span data-stu-id="86f14-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 