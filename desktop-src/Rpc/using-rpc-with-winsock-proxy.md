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
# <a name="using-rpc-with-winsock-proxy"></a>使用 RPC 搭配 Winsock Proxy

Microsoft Internet Access Server 的發行版本包含 Winsock Proxy，這是 Windows 通訊端 API 1.1 版的增強版。 Winsock Proxy 可讓在私人網路用戶端上執行的 Windows 通訊端應用程式，其行為就像是直接連接到遠端網際網路伺服器應用程式一樣。 Microsoft Proxy 伺服器作為此連線的主機。 這表示所有應用層級的通訊都是透過單一受保護的電腦（執行 Microsoft Proxy 伺服器的閘道電腦）來傳遞。

一般來說，對於資料包封包傳輸，RPC 傳輸 DLL 會略過 Wsock32.dll 中提供的 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 和 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 函式，並直接與基礎設備磁碟機通訊。 這可改善封包傳送的速度，但無法讓應用程式使用 Winsock Proxy 功能。

每個網路通訊協定提供者都有相關聯的 GUID。 RPC 執行時間程式庫會將 UDP 和 IPX Guid 與知名的 Microsoft 識別碼進行比較。 如果不相符，RPC 會自動使用 Winsock。

Winsock Proxy 的另一項功能是能夠在 SPX 用戶端電腦未安裝 TCP 時，透過 Novell SPX 傳輸模擬 TCP 傳輸通訊協定。 若要在 RPC 應用程式中使用這項功能，請在每部用戶端電腦上編輯系統登錄以新增此專案：

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

在每部伺服器電腦上編輯登錄，以新增此專案：

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

如需 RPC 傳輸通訊協定的詳細資訊，請參閱 [指定通訊協定順序](specifying-protocol-sequences.md)。 如需 Winsock Proxy 的詳細資訊，請參閱 Microsoft Internet Access Server 的產品檔集。

Windows 2000 不會執行 **ClientProtocols** 和 **ServerProtocols** 登錄專案。 Microsoft 會在執行時間程式庫中提供所有知名的傳輸。 因此，這些專案並不是必要的。

 

 