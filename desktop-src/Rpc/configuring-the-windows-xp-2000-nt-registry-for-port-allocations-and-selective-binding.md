---
title: 設定用於埠配置和選擇性系結的登錄
description: 從 Windows 2000 開始，Windows 資源套件中稱為 Rpccfg.exe 的公用程式應該用來設定系結。 如需詳細資訊，請參閱 Windows 資源套件以取得適當的作業系統版本。
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- 遠端程序呼叫 RPC、工作、設定埠配置和選擇性系結的登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b220e0e3415b7906c847c0f1196fbc815521dee0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465475"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>設定用於埠配置和選擇性系結的登錄

從 Windows 2000 開始，Windows 資源套件中稱為 Rpccfg.exe 的公用程式應該用來設定系結。 如需詳細資訊，請參閱 Windows 資源套件以取得適當的作業系統版本。

在 Windows 2000 之前的 windows 版本中，下表中的登錄機碼會指定動態埠配置的系統預設值，以及在多重主目錄電腦上系結至 nic 的系統預設值。 您必須先建立這些金鑰，然後指定適當的設定。

使用 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) 函數會影響這些設定。 開發人員應該熟悉本節中說明的登錄設定，以及管理埠配置時的 **RpcServerUseProtseqEx** 函式。 如下表所示，其中包含三個假設性應用程式的範例，並說明這些設定和 **RpcServerUseProtseqEx** 函式如何相交互操作。

如果遺失索引鍵或其包含不正確值，整個設定會標示為無效，而且所有 **RpcServerUseProtseq \** _ 呼叫超過 [_ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp)或 [**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)將會失敗。

> [!Note]  
> 配置給處理常式的埠會保持配置，直到該進程無法使用為止。 如果所有可用的埠都在使用中，此函式會傳回 RPC \_ \_ \_ 的 \_ 資源不足。

 




| 埠金鑰 | 資料類型 | 描述 | 
|----------|-----------|-------------|
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               Ports</code></pre> | <strong>REG_MULTI_SZ</strong> | 指定一組 IP 埠範圍，其中包括可從網際網路取得的所有埠，或網際網路上所有無法使用的埠。 每個字串都代表一個埠或一組內含的埠 (例如 1000-1050、1984) 。 如果有任何專案超出範圍0至65535，或如果任何字串無法解讀，則 RPC 執行時間會將整個設定視為無效。 | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               PortsInternetAvailable</code></pre> | <strong>REG_SZ</strong> | Y 或 N (不區分大小寫) 。 如果是 Y，埠機碼中列出的埠就是該電腦上的所有網際網路可用埠。 如果是 N，埠機碼中列出的埠就是所有無法使用網際網路的通訊埠。 | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               UseInternetPorts</code></pre> | <strong>REG_SZ</strong> | Y 或 N (不區分大小寫) 。 指定系統預設原則。 如果是 Y，則使用預設值的處理常式會從一組網際網路可用埠指派埠，如上面所定義。 如果是 N，則會從內部網路專用埠集合中指派埠給使用預設的處理常式。 | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   System      CurrentControlSet         Services            Rpc               Linkage                  Bind</code></pre> | <strong>REG_MULTI_SZ</strong> | 列出預設要系結之所有 Nic 的裝置名稱 (例如 \Device\AMDPCN1) 。 如果機碼不存在，則伺服器會系結至所有 Nic。 如果機碼存在，除非 NICFlags 欄位設定為 RPC_C_BIND_TO_ALL_NICS，否則伺服器會系結至機碼中指定的 Nic。 如果索引鍵的值為 null ( "" ) 值，則設定會標示為無效，而且所有對 <strong>RpcServerUseProtseq *</strong> 的呼叫會透過 <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> 或 <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> 進行失敗。 | 




 

下表說明三個範例應用程式如何受到上表中定義的設定影響，以及如何使用 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) 函數套用的設定也會受到影響。

在此範例中，會考慮三個假設的應用程式：

-   InternetApp：此應用程式是為了公開到網際網路，並且 \_ \_ \_ \_ 在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中，指定了 rpc C 使用網際網路埠。
-   LocalApp：此應用程式不是為了公開到網際網路，並且 \_ \_ \_ \_ 在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中，指定了 rpc C USE 內部網路埠。
-   Builder.defaultapp：此應用程式會在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**RPC \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中指定零。

下表根據上表所說明的登錄專案中指定的值，說明這些設定的影響。 針對格式考慮，會指派下列程式碼：

PIA = PortsInternetAvailable 金鑰值

UIP = UseInternetPorts 索引鍵值

針對此範例，埠索引鍵的值為每個專案5000-5100。



| 應用程式 | PIA | UIP | 結果                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | Y   | Y   | 使用5000和5100之間的埠        |
| LocalApp    | Y   | Y   | 使用5000-5100 範圍之外的埠 |
| Builder.defaultapp  | Y   | Y   | 使用5000和5100之間的埠        |
| InternetApp | Y   | N   | 使用5000和5100之間的埠        |
| LocalApp    | Y   | N   | 使用5000-5100 範圍之外的埠 |
| Builder.defaultapp  | Y   | N   | 使用5000-5100 範圍之外的埠 |
| InternetApp | N   | Y   | 使用5000-5100 範圍之外的埠 |
| LocalApp    | N   | Y   | 使用5000和5100之間的埠        |
| Builder.defaultapp  | N   | Y   | 使用5000-5100 範圍之外的埠 |
| InternetApp | N   | N   | 使用5000-5100 範圍之外的埠 |
| LocalApp    | N   | N   | 使用5000和5100之間的埠        |
| Builder.defaultapp  | N   | N   | 使用5000和5100之間的埠        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**RPC \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 
