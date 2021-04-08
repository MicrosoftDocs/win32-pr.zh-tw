---
title: 使用 RPC 搭配 Winsock Proxy
description: 使用 RPC 搭配 Winsock Proxy
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024049"
---
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="40149-103">使用 RPC 搭配 Winsock Proxy</span><span class="sxs-lookup"><span data-stu-id="40149-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="40149-104">Microsoft Internet Access Server 的發行版本包含 Winsock Proxy，這是 Windows 通訊端 API 1.1 版的增強版。</span><span class="sxs-lookup"><span data-stu-id="40149-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="40149-105">Winsock Proxy 可讓在私人網路用戶端上執行的 Windows 通訊端應用程式，其行為就像是直接連接到遠端網際網路伺服器應用程式一樣。</span><span class="sxs-lookup"><span data-stu-id="40149-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="40149-106">Microsoft Proxy 伺服器作為此連線的主機。</span><span class="sxs-lookup"><span data-stu-id="40149-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="40149-107">這表示所有應用層級的通訊都是透過單一受保護的電腦（執行 Microsoft Proxy 伺服器的閘道電腦）來傳遞。</span><span class="sxs-lookup"><span data-stu-id="40149-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="40149-108">一般來說，對於資料包封包傳輸，RPC 傳輸 DLL 會略過 Wsock32.dll 中提供的 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 和 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 函式，並直接與基礎設備磁碟機通訊。</span><span class="sxs-lookup"><span data-stu-id="40149-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="40149-109">這可改善封包傳送的速度，但無法讓應用程式使用 Winsock Proxy 功能。</span><span class="sxs-lookup"><span data-stu-id="40149-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="40149-110">每個網路通訊協定提供者都有相關聯的 GUID。</span><span class="sxs-lookup"><span data-stu-id="40149-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="40149-111">RPC 執行時間程式庫會將 UDP 和 IPX Guid 與知名的 Microsoft 識別碼進行比較。</span><span class="sxs-lookup"><span data-stu-id="40149-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="40149-112">如果不相符，RPC 會自動使用 Winsock。</span><span class="sxs-lookup"><span data-stu-id="40149-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="40149-113">Winsock Proxy 的另一項功能是能夠在 SPX 用戶端電腦未安裝 TCP 時，透過 Novell SPX 傳輸模擬 TCP 傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="40149-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="40149-114">若要在 RPC 應用程式中使用這項功能，請在每部用戶端電腦上編輯系統登錄以新增此專案：</span><span class="sxs-lookup"><span data-stu-id="40149-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="40149-115">在每部伺服器電腦上編輯登錄，以新增此專案：</span><span class="sxs-lookup"><span data-stu-id="40149-115">Edit the registry on each server computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="40149-116">如需 RPC 傳輸通訊協定的詳細資訊，請參閱 [指定通訊協定順序](specifying-protocol-sequences.md)。</span><span class="sxs-lookup"><span data-stu-id="40149-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="40149-117">如需 Winsock Proxy 的詳細資訊，請參閱 Microsoft Internet Access Server 的產品檔集。</span><span class="sxs-lookup"><span data-stu-id="40149-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="40149-118">Windows 2000 不會執行 **ClientProtocols** 和 **ServerProtocols** 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="40149-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="40149-119">Microsoft 會在執行時間程式庫中提供所有知名的傳輸。</span><span class="sxs-lookup"><span data-stu-id="40149-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="40149-120">因此，這些專案並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="40149-120">Therefore, these entries are not necessary.</span></span>

 

 