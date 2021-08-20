---
description: 裝置上的 Web 服務程式設計介面會定義並使用下列結構：
ms.assetid: daaa7d18-7af9-4f03-bbbd-378f4af79eec
title: 裝置上的 Web 服務結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4f963676dfdc8e7d931bb2c61fd1d661b30f544caf51d0d76e5bf79fc42612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920009"
---
# <a name="web-services-on-devices-structures"></a>裝置上的 Web 服務結構

裝置上的 Web 服務程式設計介面會定義並使用下列結構：

-   [**REQUESTBODY \_ GetStatus**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_getstatus)
-   [**REQUESTBODY \_ 續約**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_renew)
-   [**REQUESTBODY \_ 訂閱**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_subscribe)
-   [**REQUESTBODY \_ 取消訂閱**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_unsubscribe)
-   [**RESPONSEBODY \_ GetMetadata**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_getmetadata)
-   [**RESPONSEBODY \_ GetStatus**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_getstatus)
-   [**RESPONSEBODY \_ 續約**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_renew)
-   [**RESPONSEBODY \_ 訂閱**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_subscribe)
-   [**RESPONSEBODY \_ SubscriptionEnd**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_subscriptionend)
-   [**WSD \_ 應用程式 \_ 順序**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_app_sequence)
-   [**WSD \_ 再見**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_bye)
-   [**WSD \_ 設定 \_ 位址**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_addresses)
-   [**WSD \_ 設定 \_ 參數**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param)
-   [**WSD \_ DATETIME**](/windows/desktop/api/WsdXml/ns-wsdxml-wsd_datetime)
-   [**WSD \_ 持續時間**](/windows/desktop/api/WsdXml/ns-wsdxml-wsd_duration)
-   [**WSD \_ 端點 \_ 參考**](/windows/desktop/api/Wsdtypes/ns-wsdtypes-wsd_endpoint_reference)
-   [**WSD \_ 端點 \_ 參考 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_endpoint_reference_list)
-   [**WSD \_ 事件**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_event)
-   [**WSD \_ 事件 \_ 傳遞 \_ 模式**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_delivery_mode)
-   [**WSD \_ 事件 \_ 傳遞 \_ 模式 \_ 推入**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_delivery_mode_push)
-   [**WSD \_ 事件 \_ 到期**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_expires)
-   [**WSD \_ 事件 \_ 篩選器**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_filter)
-   [**WSD \_ 事件 \_ 篩選器 \_ 動作**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_filter_action)
-   [**WSD \_ 處理常式 \_ 內容**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_handler_context)
-   [**WSD \_ 標頭 \_ RELATESTO**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_header_relatesto)
-   [**WSD \_ HELLO**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_hello)
-   [**WSD \_ 主機 \_ 中繼資料**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_host_metadata)
-   [**WSD \_ 當地語系化 \_ 字串**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_localized_string)
-   [**WSD \_ 當地語系化 \_ 字串 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_localized_string_list)
-   [**WSD \_ 中繼資料 \_ 區段**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_metadata_section)
-   [**WSD \_ 中繼資料 \_ 區段 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_metadata_section_list)
-   [**WSD \_ 名稱 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_name_list)
-   [**WSD \_ 操作**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_operation)
-   [**WSD \_ 埠 \_ 類型**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_port_type)
-   [**WSD \_ 探查**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe)
-   [**WSD \_ 探查 \_ 相符**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_match)
-   [**WSD \_ 探查 \_ 符合 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_match_list)
-   [**WSD \_ 探查 \_ 相符專案**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_matches)
-   [**WSD \_ 參考 \_ 參數**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_reference_parameters)
-   [**WSD \_ 參考 \_ 屬性**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_reference_properties)
-   [**WSD \_ 關聯 \_ 中繼資料**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_relationship_metadata)
-   [**WSD \_ 解析**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve)
-   [**WSD \_ 解析 \_ 相符**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve_match)
-   [**WSD \_ 解析 \_ 相符**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve_matches)
-   [**WSD \_ 範圍**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_scopes)
-   [**WSD \_ 安全性 \_ 憑證 \_ 驗證**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_security_cert_validation)
-   [**WSD \_ 安全性簽章 \_ \_ 驗證**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_security_signature_validation)
-   [**WSD \_ 服務 \_ 中繼資料**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_service_metadata)
-   [**WSD \_ 服務 \_ 中繼資料 \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_service_metadata_list)
-   [**WSD \_ SOAP \_ 錯誤**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault)
-   [**WSD \_ SOAP \_ 錯誤 \_ 代碼**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_code)
-   [**WSD \_ SOAP \_ 錯誤 \_ 原因**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_reason)
-   [**WSD \_ SOAP \_ 錯誤子 \_ 代碼**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_subcode)
-   [**WSD \_ SOAP \_ 標頭**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_header)
-   [**WSD \_ SOAP \_ 訊息**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_message)
-   [**WSD \_ 同步 \_ 回應 \_ 內容**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_synchronous_response_context)
-   [**WSD \_ 此 \_ 裝置 \_ 中繼資料**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_this_device_metadata)
-   [**WSD \_ 此 \_ 模型 \_ 中繼資料**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_this_model_metadata)
-   [**WSD \_ 未知 \_ 查閱**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_unknown_lookup)
-   [**WSD \_ URI \_ 清單**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_uri_list)
-   [**WSDUdpRetransmitParams**](/windows/desktop/api/Wsdbase/ns-wsdbase-wsdudpretransmitparams)
-   [**WSDXML \_ 屬性**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_attribute)
-   [**WSDXML \_ 元素**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_element)
-   [**WSDXML \_ 元素 \_ 清單**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_element_list)
-   [**WSDXML \_ 名稱**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_name)
-   [**WSDXML \_ 命名空間**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_namespace)
-   [**WSDXML \_ 節點**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_node)
-   [**WSDXML \_ 前置詞 \_ 對應**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_prefix_mapping)
-   [**WSDXML \_ 文字**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_text)
-   [**WSDXML \_ 類型**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_type)

 

 



