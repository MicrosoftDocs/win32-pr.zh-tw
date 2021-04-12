---
title: Windows 篩選平台的新功能
description: Windows 8 和 Windows Server 2012 引進了新的 Windows 篩選平台程式設計項目。
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316927"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Windows 篩選平台的新功能

Windows 8 和 Windows Server 2012 引進了新的 Windows 篩選平台程式設計項目。 新功能包括下列各項：

-   *第2層篩選*：提供對 L2 (MAC) 層的存取權，以允許篩選該層的流量。
-   *vSwitch 篩選*：允許對 vSwitch 進行檢查及/或修改的封包。 您可以在 vSwitch 輸入和輸出中使用 WFP 篩選器或標注。
-   *應用程式容器管理*：允許存取應用程式容器和網路隔離連線問題的相關資訊。
-   *Ipsec 更新*：延伸的 ipsec 功能，包括線上狀態監視、憑證選取和金鑰管理。

Windows 驅動程式套件也包含 [Windows 8 之 WFP 變更的](/windows-hardware/drivers/network/wfp-changes-for-windows-8)相關資訊。

## <a name="windows-8-api-updates"></a>Windows 8 API 更新

已針對 Windows 8 和 Windows Server 2012 新增許多新的 Api。

## <a name="new-functions"></a>新的函式

-   [**FWPM \_ NET \_ EVENT \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderCoNtextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderCoNtextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderCoNtextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderCoNtextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ 按鍵 \_ 聽寫 \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**IPSEC \_ 金鑰 \_ 管理員會 \_ 聽寫 \_ KEY0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ 通知 \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**IPSEC \_ SA \_ 內容 \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaCoNtextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaCoNtextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaCoNtextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**PAC \_ 變更 \_ 回呼 \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>新結構

-   [**IKEEXT \_ 驗證 \_ METHOD2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ .name0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ 憑證 \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IKEEXT \_ 憑證 \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IPSEC \_ 金鑰 \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**IPSEC \_ 金鑰 \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**IPSEC \_ SA \_ 內容 \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ 內容 \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**IPSEC \_ 傳輸 \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**IPSEC \_ 通道 \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**IPSEC \_ 通道 \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**IPSEC \_ 通道 \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ 連接 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ 連接 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FWPM \_ NET \_ 事件 \_ 功能 \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ 事件 \_ 功能 \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ 事件 \_ 分類 \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ NET \_ 事件 \_ 分類 \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ NET \_ 事件 \_ 分類 \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ h 2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**FWPM \_ 提供者 \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ 事件 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>新的列舉類型

-   [**.FWP \_ VSWITCH \_ 網路 \_ 類型**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**FWPM \_ APPC \_ 網路 \_ 功能 \_ 類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**FWPM \_ 連接 \_ 事件 \_ 類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**FWPM \_ VSWITCH \_ 事件 \_ 類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**IKEEXT \_ 憑證 \_ 準則 \_ 名稱 \_ 類型**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**IPSEC \_ SA \_ 內容 \_ 事件 \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>新的篩選層識別碼

[**篩選圖層識別碼：**](management-filtering-layer-identifiers-.md)

-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路
-   FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生
-   FWPM \_ 圖層輸入 \_ \_ VSWITCH \_ 乙太網路
-   FWPM \_ 圖層輸出 \_ \_ VSWITCH \_ 乙太網路
-   FWPM \_ 圖層輸入 \_ \_ vswitch \_ 傳輸 \_ V4/FWPM \_ 層輸入 \_ \_ vswitch \_ 傳輸 \_ V6
-   FWPM \_ 層 \_ \_ 輸出 vswitch \_ 傳輸 \_ V4/FWPM \_ 層 \_ \_ 輸出 vswitch \_ 傳輸 \_ V6

## <a name="new-filtering-condition-identifiers"></a>新的篩選準則識別碼

[**篩選準則識別碼：**](filtering-condition-identifiers-.md)

-   FWPM \_ 條件 \_ 介面 \_ MAC \_ 位址
-   FWPM \_ 條件 \_ MAC \_ 本機 \_ 位址
-   FWPM \_ 條件 \_ MAC \_ 遠端 \_ 位址
-   FWPM \_ CONDITION \_ 乙太幣 \_ TYPE
-   FWPM \_ 條件 \_ VLAN \_ 識別碼
-   FWPM \_ 條件 \_ NDIS \_ 埠
-   FWPM \_ 條件 \_ NDIS \_ 媒體 \_ 類型
-   FWPM \_ 條件 \_ NDIS \_ 實體 \_ 媒體 \_ 類型
-   FWPM \_ 條件 \_ L2 \_ 旗標
-   FWPM \_ 條件 \_ MAC \_ 本機 \_ 位址 \_ 類型
-   FWPM \_ 條件 \_ MAC \_ 遠端 \_ 位址 \_ 類型
-   FWPM \_ 條件 \_ ALE \_ 套件 \_ 識別碼
-   FWPM \_ 條件 \_ MAC \_ 來源 \_ 位址
-   FWPM \_ 條件 \_ MAC \_ 目的地 \_ 位址
-   FWPM \_ 條件 \_ MAC \_ 來源 \_ 位址 \_ 類型
-   FWPM \_ 條件 \_ MAC \_ 目的地 \_ 位址 \_ 類型
-   FWPM \_ 條件 \_ IP \_ 來源 \_ 埠
-   FWPM \_ 條件 \_ IP \_ 目的地 \_ 埠
-   FWPM \_ 條件 \_ VSWITCH \_ 識別碼
-   FWPM \_ 條件 \_ VSWITCH \_ 網路 \_ 類型
-   FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ 介面 \_ 識別碼
-   FWPM \_ 條件 \_ VSWITCH \_ 目的地 \_ 介面 \_ 識別碼
-   FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ VM \_ 識別碼
-   FWPM \_ 條件 \_ VSWITCH \_ 目的地 \_ VM \_ 識別碼
-   FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ 介面 \_ 類型
-   FWPM \_ 條件 \_ VSWITCH \_ 租使用者 \_ 網路 \_ 識別碼

## <a name="new-filtering-condition-flags"></a>新的篩選準則旗標

[**篩選準則旗標：**](filtering-condition-flags-.md)

-   .FWP \_ 條件 \_ 旗標 \_ 是 \_ PROXY \_ 連接
-   .FWP \_ 條件 \_ 旗標 \_ 是 \_ APPCONTAINER \_ 回送
-   .FWP \_ 條件 \_ 旗標 \_ 為 \_ 非 \_ APPCONTAINER \_ 回送
-   .FWP \_ 條件 \_ 旗標 \_ 正在接受 \_ \_ 原則 \_ 授權
-   .FWP \_ 條件 \_ L2 \_ 是 \_ 原生 \_ 乙太網路
-   .FWP \_ 條件 \_ L2 \_ 為 \_ WIFI
-   .FWP \_ 條件 \_ L2 \_ 為 \_ MOBILE \_ 寬頻
-   .FWP \_ 條件 \_ L2 \_ 為 \_ WIFI \_ DIRECT \_ 資料
-   \_ \_ \_ 已 VM2VM 的 .fwp 條件 L2 \_
-   .FWP \_ 條件 \_ L2 \_ 是 \_ 格式不正確的封 \_ 包
-   .FWP \_ 條件 \_ L2 \_ 是 \_ IP \_ 片段 \_ 群組
-   \_ \_ \_ 當 \_ 連接器 \_ 存在時的 .fwp 條件 L2

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Windows 7 更新至 Windows 篩選平台

[Windows 篩選平台的新功能]()詳述了許多 windows 7 的更新。 您也可以在 Windows 7 上的 [WFP 變更](/windows-hardware/drivers/network/wfp-changes-for-windows-7)Windows 驅動程式套件中取得資訊。

 

 