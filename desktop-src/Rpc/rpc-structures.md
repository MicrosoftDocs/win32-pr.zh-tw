---
title: RPC 結構
description: 本節說明 Microsoft RPC 定義和使用的結構。
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- 遠端程序呼叫 RPC、參考、結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c59552f775b56519620e46c610bef234fba488d4d6e0a7dfe7d4266e7ae2c50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018209"
---
# <a name="rpc-structures"></a>RPC 結構

本節說明 Microsoft RPC 定義和使用的結構。

-   [**NDR \_ SCONTEXT**](/previous-versions/aa374336(v=vs.80))
-   [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [**NDR \_ 使用者 \_ 封送處理 \_ 資訊**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [**NDR \_ 使用者 \_ 封送處理 \_ 資訊 \_ 1-1**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [**RPC \_ 非同步 \_ 通知 \_ 資訊**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [**RPC \_ 非同步 \_ 狀態**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [**RPC 系結 \_ \_ 控制碼 \_ 選項 \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [**RPC 系結 \_ \_ 處理 \_ 安全性 \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [**RPC 系結 \_ \_ 控制碼 \_ 範本 \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [**RPC 系結 \_ \_ 向量**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [**RPC \_ C \_ OPT \_ COOKIE \_ 驗證 \_ 描述元**](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [**RPC \_ 呼叫 \_ 屬性 \_ V1**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [**RPC \_ 呼叫 \_ 屬性 \_ V2**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [**RPC \_ 呼叫 \_ 本機 \_ 位址 \_ V1**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [**RPC \_ 用戶端 \_ 介面**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [**RPC \_ 分派 \_ 資料表**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [**RPC \_ EE \_ INFO \_ 參數**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [**RPC \_ 端點 \_ 範本**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [**RPC \_ 錯誤 \_ 列舉 \_ 控制碼**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [**RPC \_ 延伸 \_ 錯誤 \_ 資訊**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [**RPC \_ HTTP \_ 傳輸 \_ 認證**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [**RPC \_ HTTP \_ 傳輸 \_ 認證 \_ V2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [**RPC \_ HTTP \_ 傳輸 \_ 認證 \_ V3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [**RPC （ \_ 如果 \_ 識別碼）**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [**RPC （ \_ 如果 \_ 識別碼 \_ 向量）**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [**RPC \_ 介面 \_ 範本**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [**RPC \_ 原則**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [**RPC \_ PROTSEQ \_ 向量**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [**RPC \_ 安全性 \_ QOS**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [**RPC \_ 安全性 \_ QOS \_ V2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [**RPC \_ 安全性 \_ QOS \_ V3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [**RPC \_ 安全性 \_ QOS \_ V4**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [**RPC \_ 安全性 \_ QOS \_ V5**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [**RPC \_ 統計資料 \_ 向量**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [**秒的 \_ WINNT \_ 驗證身分 \_ 識別**](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [**UUID**](./rpcdce/ns-rpcdce-uuid.md)
-   [**UUID \_ 向量**](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 