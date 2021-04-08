---
title: '篩選準則旗標 (Fwptypes .h) '
description: Windows 篩選平台 (WFP) 篩選準則旗標都是以位位表示。
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686320"
---
# <a name="filtering-condition-flags"></a>篩選準則旗標

Windows 篩選平台 (WFP) 篩選準則旗標都是以位位表示。

您可以使用這些旗標和篩選層來定義它們，如下所示。

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 回送**
</dt> <dd> <dl> <dt>



測試網路流量是否為回送流量。

篩選圖層：

-   FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ 輸出 \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ 資料流程 \_ {V4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖層 \_ 輸入 \_ ICMP \_ 錯誤 \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖層 \_ 輸出 \_ ICMP \_ 錯誤 \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖層 \_ ALE \_ 流程已 \_ 建立 \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ IPSEC \_ 安全**
</dt> <dd> <dl> <dt>



測試網路流量是否由 IPsec 保護。

篩選圖層：

-   FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**\_ \_ \_ 已重新授權的 .FWP 條件旗標 \_**
</dt> <dd> <dl> <dt>



原則變更的測試，而不是新的連接。

篩選圖層：

-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 萬用字元 \_ 系結**
</dt> <dd> <dl> <dt>



測試應用程式是否在系結至區域網路位址時指定萬用字元位址。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 原始 \_ 端點**
</dt> <dd> <dl> <dt>



測試傳送和接收流量的本機端點是否為原始端點。

篩選圖層：

-   FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ 圖 \_ 層 \_ 資料包資料 \_ {V4 \| 6}
    > [!Note]  
    > 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

     

-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 片段**
</dt> <dd> <dl> <dt>



測試 \_ \_ 傳遞給 callout 驅動程式的淨緩衝區清單結構是否為 IP 封包片段。

篩選圖層：

-   FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6} \_ 捨棄


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 片段 \_ 群組**
</dt> <dd> <dl> <dt>



測試 \_ \_ 傳遞給 callout 驅動程式的淨緩衝區清單結構是否描述封包片段的連結清單。

篩選層：

-   FWPM \_ LAYER \_ IPFORWARD \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ IPSEC NATT 重新 \_ \_ 分類**
</dt> <dd> <dl> <dt>



指出當 IPsec NAT 填充碼轉譯遠端埠值時，會將相同的封包重新分類至傳輸層。


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**.FWP \_ 條件 \_ 旗標 \_ 需要 \_ ALE \_ 分類**
</dt> <dd> <dl> <dt>



指出將在 ALE 接收/接受層重新分類封包。


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 隱含 \_ 系結**
</dt> <dd> <dl> <dt>



測試 Windows 通訊端是否正在執行隱含系結。

僅適用于 Windows Vista 和 Windows Server 2008。


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**\_已重新 \_ \_ 組合的 \_ .FWP 條件旗標**
</dt> <dd> <dl> <dt>



測試封包是否已重組。

> [!Note]  
> 僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。

 

篩選層：

-   FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**\_ \_ \_ 已 \_ \_ 指定名稱應用程式的 \_ .FWP 條件旗標**
</dt> <dd> <dl> <dt>



測試是否已透過 API （例如 [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) ）接收應用程式所要連接之對等電腦的名稱，而不是透過快取啟發學習法取得。

> [!Note]  
> 僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。

 

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 混合的**
</dt> <dd> <dl> <dt>



保留的。


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 驗證 \_ FW**
</dt> <dd> <dl> <dt>



測試連接是否經過端對端驗證，即使個別的封包尚未經過驗證也是一樣。

> [!Note]  
> 僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。

 

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**\_已重新 \_ \_ 分類的 \_ .FWP 條件旗標**
</dt> <dd> <dl> <dt>



測試篩選引擎是否將先前的系結或接聽要求。

> [!Note]  
> 僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。

 

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ PROXY \_ 連接**
</dt> <dd> <dl> <dt>



測試連接是否使用 proxy。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ APPCONTAINER \_ 回送**
</dt> <dd> <dl> <dt>



測試網路流量是否為應用程式容器回送流量。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 非 \_ APPCONTAINER \_ 回送**
</dt> <dd> <dl> <dt>



測試網路流量是否為非應用程式容器回送流量。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**\_ \_ \_ 已保留 .FWP 條件旗標 \_**
</dt> <dd> <dl> <dt>



保留的。


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**.FWP \_ 條件 \_ 旗標 \_ 正在接受 \_ \_ 原則 \_ 授權**
</dt> <dd> <dl> <dt>



指出正在執行目前的分類，以接受重新導向的 Windows Store 應用程式連接至指定主機的意圖。 這類分類將包含的資料欄值與應用程式永遠不會重新導向的相同。 此旗標也會指出將會叫用未來的分類，以符合有效的重新導向目的地。 如果將應用程式重新導向至 proxy 服務進行檢查，也表示將在 proxy 連線上叫用未來的分類。 注標驅動程式通常應該允許此分類。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

下列旗標指定之先前授權連接的原因。 您可以使用這些旗標和篩選層來定義它們，如下所示。

> [!Note]  
> 這些篩選準則僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 原則 \_ 變更**
</dt> <dd> <dl> <dt>



指出因為加入或移除篩選而重新授權連接。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 新 \_ 抵達 \_ 介面**
</dt> <dd> <dl> <dt>



指出封包已從未知的介面抵達。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 新的 \_ NEXTHOP \_ 介面**
</dt> <dd> <dl> <dt>



指出封包將從未知的介面中脫離。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**已 \_ \_ \_ 交叉分析的重新授權原因 \_ 設定檔 \_**
</dt> <dd> <dl> <dt>



指出封包已通過一個以上網路類別的介面。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**已 \_ \_ \_ \_ \_ 完成分類完成的 .FWP 條件重新授權原因**
</dt> <dd> <dl> <dt>



表示現在已允許先前保留的連接完成。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_ \_ \_ \_ \_ 已變更 IPSEC 屬性的重新授權 \_ 原因**
</dt> <dd> <dl> <dt>



指出 IPsec 屬性已變更，或連接已從純文字變更為安全連線。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**\_重新授權進行 \_ \_ \_ \_ 資料流程 \_ 檢查的 .FWP 條件**
</dt> <dd> <dl> <dt>



指出先前建立的 TCP 連接現在正在檢查。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_已變更的 .FWP 條件 \_ 重新授權 \_ 原因 \_ 通訊端 \_ 屬性 \_**
</dt> <dd> <dl> <dt>



指出在授權並建立連接之後，已設定通訊端屬性。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_ \_ 重新授權新的 \_ \_ \_ 輸入 \_ MCAST BCAST 封 \_ \_ 包的 .FWP 條件**
</dt> <dd> <dl> <dt>



指出新的輸入多播或廣播封包正在重新授權于 ALE \_ 接收 \_ 接受標注。

篩選層：

-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

下列旗標會指定與應用程式是否要接收 Edge 遍歷流量相關的通訊端屬性。 您可以使用這些旗標和篩選層來定義它們，如下所示。

> [!Note]  
> 這些篩選準則僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 是 \_ 系統 \_ 埠 \_ RPC**
</dt> <dd> <dl> <dt>



指出應用程式正在與動態 RPC 埠通訊。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 允許 \_ 邊緣 \_ 流量**
</dt> <dd> <dl> <dt>



表示應用程式想要接收 edge 遍歷特定的流量。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 拒絕 \_ 邊緣 \_ 流量**
</dt> <dd> <dl> <dt>



表示應用程式不想接收或處理 edge 遍歷特定的流量。

篩選層：

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

下列旗標指定與 L2 篩選相關的連接詳細資料。

> [!Note]  
> 這些篩選準則僅適用于 Windows 8 和 Windows Server 2012。

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ 原生 \_ 乙太網路**
</dt> <dd> <dl> <dt>



指出連接是原生乙太網路。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI**
</dt> <dd> <dl> <dt>



指出連接是 Wi-fi。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ MOBILE \_ 寬頻**
</dt> <dd> <dl> <dt>



指出連接是 mobile 寬頻。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI \_ DIRECT \_ 資料**
</dt> <dd> <dl> <dt>



表示連接 Wi-Fi 直接。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_ \_ \_ 已 VM2VM 的 .fwp 條件 L2 \_**
</dt> <dd> <dl> <dt>



指出連接是在虛擬機器之間。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ 格式不正確的封 \_ 包**
</dt> <dd> <dl> <dt>



指出封包看似格式不正確。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ IP \_ 片段 \_ 群組**
</dt> <dd> <dl> <dt>



表示 IP 封包片段群組。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_ \_ \_ 當 \_ 連接器 \_ 存在時的 .fwp 條件 L2**
</dt> <dd> <dl> <dt>



表示連接器存在。

篩選層：

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Fwptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

