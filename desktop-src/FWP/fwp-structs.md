---
title: WFP 結構
description: Windows 篩選平台 (WFP) API 結構如下所示。
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows 篩選平台 API 列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10e4d47c307766758cc935787d975ffb636f8f9
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/26/2020
ms.locfileid: "103681569"
---
# <a name="wfp-structures"></a>WFP 結構

Windows 篩選平台 (WFP) API 結構如下所示。

管理結構

-   [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**FWPM \_ CALLOUT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**FWPM \_ 標注 \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**FWPM \_ 標注 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**FWPM \_ 標注 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**FWPM \_ 分類 \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**FWPM \_ 分類 \_ OPTIONS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ 連接 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ 連接 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ 顯示 \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**FWPM \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**FWPM \_ 篩選 \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**FWPM \_ 篩選 \_ CONDITION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**FWPM \_ 篩選 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**FWPM \_ 篩選 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**FWPM \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**FWPM \_ 圖層 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**FWPM \_ 圖層 \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   FWPM \_ NET \_ 活動：
    -   [**FWPM \_ (\_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) Windows Vista) 的 NET EVENT0
    -   [**FWPM \_NET \_ event1.png**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7) 
    -   [**FWPM \_NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8) 
-   [**FWPM \_ NET \_ 事件 \_ 功能 \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ 事件 \_ 功能 \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ 事件 \_ 分類 \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   FWPM \_ NET \_ 事件 \_ 分類 \_ 捨棄：
    -   [**FWPM \_ (Windows Vista) 的網路 \_ 活動 \_ 分類 \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0)
    -   [**FWPM \_\_ \_ \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 和更新版本的網路事件分類) 
    -   [**FWPM \_網路 \_ 事件 \_ 分類 \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8) 
-   [**FWPM \_ NET \_ 事件 \_ 分類 \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ 事件 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   FWPM \_ NET \_ 事件 \_ 標頭：
    -   [**FWPM \_NET \_ EVENT \_ HEADER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista) 
    -   [**FWPM \_NET \_ EVENT \_ Header1.xml**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7) 
    -   [**FWPM \_NET \_ EVENT \_ h 2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8) 
-   FWPM \_ NET \_ EVENT \_ IKEEXT \_ EM \_ 失敗：
    -   [**FWPM \_NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista) 
    -   [**FWPM \_NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 及更新版本) 
-   FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM \_ 失敗：
    -   [**FWPM \_NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista) 
    -   [**FWPM \_NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 及更新版本) 
-   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ DOSP \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ KERNEL \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**FWPM \_ NET \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**FWPM \_ 提供者 \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   FWPM \_ 提供者 \_ 內容：
    -   [**FWPM \_ (Windows Vista) 提供者 \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0)
    -   [**FWPM \_提供者 \_ CONTEXT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7) 
    -   FWPM \_ PROVIDER \_ CONTEXT2 (Windows 8) 
-   [**FWPM \_ 提供者 \_ 內容 \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**FWPM \_ 提供者 \_ 內容 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**FWPM \_ 提供者 \_ 內容 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**FWPM \_ 提供者 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**FWPM \_ 提供者 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**FWPM \_ SESSION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**FWPM \_ 會話 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**FWPM \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**FWPM \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**FWPM \_ 子層 \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**FWPM \_ 子層 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**FWPM \_ 子層 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**FWPM \_ 系統 \_ PORTS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**\_ \_ \_ 依 TYPE0 的 FWPM 系統埠 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ 事件 \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

共用結構

-   [**.FWP \_ 位元組 \_ ARRAY6**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**.FWP \_ 位元組 \_ ARRAY16**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**.FWP \_ 位元組 \_ BLOB**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**VALUE0 的 .FWP \_ 條件 \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**.FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**.FWP \_ 相符 \_ 型別**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**.FWP \_ V4 \_ 位址 \_ 和 \_ 遮罩**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**.FWP \_ V6 \_ 位址 \_ 和 \_ 遮罩**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**.FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

IKE/AuthIP 結構

-   IKEEXT \_ 驗證 \_ 方法：
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) Windows VISTA) 驗證 METHOD0
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) Windows 7) 驗證 METHOD1
    -   [**IKEEXT \_驗證 \_ METHOD2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8) 
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ .name0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ 憑證 \_ 根 \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   IKEEXT \_ 憑證 \_ 驗證：
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) Windows Vista) 的憑證 AUTHENTICATION0
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) Windows 7) 的憑證 AUTHENTICATION1
    -   [**IKEEXT \_憑證 \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8) 
-   IKEEXT \_ \_ 憑證認證：
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) Windows Vista) 的憑證 CREDENTIAL0
    -   [**IKEEXT \_憑證 \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ 憑證 \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ 加密 \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   IKEEXT \_ 一般 \_ 統計資料：
    -   [**IKEEXT \_Windows \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) Vista) 的一般 STATISTICS0 (
    -   [**IKEEXT \_COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 和更新版本) 
-   [**IKEEXT \_ COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   IKEEXT \_ 認證：
    -   [**IKEEXT \_CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista) 
    -   [**IKEEXT \_CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 及更新版本) 
-   IKEEXT \_ 認證 \_ 配對：
    -   [**IKEEXT \_認證 \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista) 
    -   [**IKEEXT \_認證 \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 及更新版本) 
-   IKEEXT \_ 認證：
    -   [**IKEEXT \_CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista) 
    -   [**IKEEXT \_CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   IKEEXT \_ EM \_ 原則：
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) Windows VISTA) EM POLICY0
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) Windows 7) EM POLICY1
    -   [**IKEEXT \_EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8) 
-   [**IKEEXT \_ 完整性 \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   IKEEXT \_ IP \_ 版本的 \_ 特定 \_ 一般 \_ 統計資料：
    -   [**IKEEXT \_IP \_ 版本 \_ 特定的 \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista) 
    -   [**IKEEXT \_IP \_ 版本 \_ 特定的 \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 及更新版本) 
-   IKEEXT \_ IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ 統計資料：
    -   [**IKEEXT \_IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista) 
    -   [**IKEEXT \_IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 和更新版本) 
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   IKEEXT \_ KEYMODULE \_ 統計資料：
    -   [**IKEEXT \_ (\_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) windows Vista 和 windows 7) 的 KERBEROS AUTHENTICATION0
    -   [**IKEEXT \_KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8) 
-   -   IKEEXT \_ KEYMODULE \_ 統計資料：
    -   [**IKEEXT \_Windows \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) Vista)  (KEYMODULE STATISTICS0
    -   [**IKEEXT \_KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ 名稱 \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   IKEEXT \_ 原則：
    -   [**IKEEXT \_POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista) 
    -   [**IKEEXT \_POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7) 
    -   [**IKEEXT \_POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8) 
-   IKEEXT \_ 預先共用 \_ 金鑰 \_ 驗證：
    -   [**IKEEXT \_ (Windows Vista) 的預先共用 \_ 金鑰 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
    -   [**IKEEXT \_預先共用的 \_ 金鑰 \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**IKEEXT \_ 保留的 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   IKEEXT \_ SA \_ 詳細資料：
    -   [**IKEEXT \_ (\_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) Windows Vista) 的 SA DETAILS0
    -   [**IKEEXT \_SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ SA \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   IKEEXT \_ 統計資料：
    -   [**IKEEXT \_STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista) 
    -   [**IKEEXT \_STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 及更新版本) 
-   [**IKEEXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

IPsec 結構

-   [**IPSEC \_ 位址 \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   IPSEC \_ 匯總 \_ 捨棄封 \_ 包 \_ 統計資料：
    -   [**IPSEC \_ (Windows Vista) 的匯總 \_ 捨棄封 \_ 包 \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
    -   [**IPSEC \_ (Windows 7 和更新版本的匯總 \_ 捨棄封 \_ 包 \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)) 
-   [**IPSEC \_ 匯總 \_ SA \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ AH \_ 捨棄封 \_ 包 \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**IPSEC \_ 驗證 \_ 和 \_ 加密 \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**IPSEC \_ 驗證 \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**IPSEC \_ 驗證 \_ 轉換 \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**IPSEC \_ 加密 \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**IPSEC \_ 密碼 \_ 轉換 \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**IPSEC \_ DOSP \_ OPTIONS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ DOSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**IPSEC \_ DOSP \_ 狀態 \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ DOSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSEC \_ ESP \_ 捨棄封 \_ 包 \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   IPSEC \_ GETSPI：
    -   [**IPSEC \_GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista) 
    -   [**IPSEC \_GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 及更新版本) 
-   [**IPSEC \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**IPSEC \_ 金鑰 \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   IPSEC \_ 加密 \_ 原則：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) windows Vista 和 windows 7) 的金鑰加密 POLICY0
    -   [**IPSEC \_金鑰 \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8) 
-   [**IPSEC \_ KEYMODULE \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**IPSEC \_ PROPOSAL0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**IPSEC \_ SA0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**IPSEC \_ SA \_ 驗證 \_ 和 \_ 加密 \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**IPSEC \_ SA \_ 驗證 \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   IPSEC \_ SA 配套 \_ ：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) Windows Vista) 的 SA BUNDLE0
    -   [**IPSEC \_SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 及更新版本) 
-   [**IPSEC \_ SA \_ 加密 \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   IPSEC \_ SA 內容 \_ ：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) Windows Vista) 的 SA CONTEXT0
    -   [**IPSEC \_SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 及更新版本) 
-   [**IPSEC \_ SA \_ 內容 \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ 內容列舉 \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**IPSEC \_ SA \_ 內容 \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   IPSEC \_ SA \_ 詳細資料：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) Windows Vista) 的 SA DETAILS0
    -   [**IPSEC \_SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 及更新版本) 
-   [**IPSEC \_ SA \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**IPSEC \_ SA \_ 閒置 \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   IPSEC \_ 統計資料：
    -   [**IPSEC \_STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista) 
    -   [**IPSEC \_STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 及更新版本) 
-   [**IPSEC \_ TOKEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   IPSEC \_ 流量：
    -   [**IPSEC \_TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista) 
    -   [**IPSEC \_流量 1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 及更新版本) 
-   IPSEC \_ 流量 \_ 統計資料：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) Windows Vista) 的流量 STATISTICS0
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) Windows 7 和更新版本的流量 STATISTICS1) 
-   IPSEC \_ 傳輸 \_ 原則：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) Windows Vista) 的傳輸 POLICY0
    -   [**IPSEC \_傳輸 \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7) 
    -   [**IPSEC \_傳輸 \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8) 
-   [**IPSEC \_ 通道 \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   IPSEC \_ 通道 \_ 端點：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) Windows Vista) 的通道 ENDPOINTS0
    -   [**IPSEC \_通道 \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7) 
    -   [**IPSEC \_通道 \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8) 
-   IPSEC \_ 通道 \_ 原則：
    -   [**IPSEC \_ (\_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) Windows Vista) 的通道 POLICY0
    -   [**IPSEC \_通道 \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7) 
    -   [**IPSEC \_通道 \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8) 
-   [**IPSEC \_ V4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ 虛擬（ \_ 如果通道 \_ \_ INFO0）**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




