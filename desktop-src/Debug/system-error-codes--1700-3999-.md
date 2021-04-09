---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1700-3999，適用于開發人員。
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: '系統錯誤碼 (1700-3999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847068"
---
# <a name="system-error-codes-1700-3999"></a>系統錯誤碼 (1700-3999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述錯誤1700到3999的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC \_ S \_ 不正確 \_ 字串 \_ 系結**
</dt> <dd> <dl> <dt>

1700 (0x6A4) 
</dt> <dt>



字串系結無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC \_ S \_ 錯誤的系結 \_ 類型 \_ \_**
</dt> <dd> <dl> <dt>

1701 (0x6A5) 
</dt> <dt>



系結控制碼不是正確的類型。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC \_ S \_ 不正確系結 \_**
</dt> <dd> <dl> <dt>

1702 (0x6A6) 
</dt> <dt>



系結控制碼無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_ \_ \_ 不支援 RPC S \_ PROTSEQ**
</dt> <dd> <dl> <dt>

1703 (0x6A7) 
</dt> <dt>



不支援 RPC 通訊協定順序。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ 不正確 \_ RPC \_ PROTSEQ**
</dt> <dd> <dl> <dt>

1704 (0x6A8) 
</dt> <dt>



RPC 通訊協定序列無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC \_ S \_ 不正確 \_ 字串 \_ UUID**
</dt> <dd> <dl> <dt>

1705 (0x6A9) 
</dt> <dt>



字串通用唯一識別碼 (UUID) 無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC \_ S \_ 不正確 \_ 端點 \_ 格式**
</dt> <dd> <dl> <dt>

1706 (0x6AA) 
</dt> <dt>



端點格式無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ 不正確 \_ NET \_ ADDR**
</dt> <dd> <dl> <dt>

1707 (0x6AB) 
</dt> <dt>



網路位址無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ \_ 找不 \_ 到端點**
</dt> <dd> <dl> <dt>

1708 (0x6AC) 
</dt> <dt>



找不到任何端點。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC \_ S \_ 不正確 \_ 超時時間**
</dt> <dd> <dl> <dt>

1709 (0x6AD) 
</dt> <dt>



Timeout 值無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 物件**
</dt> <dd> <dl> <dt>

1710 (0x6AE) 
</dt> <dt>



找不到 (UUID) 的物件通用唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**\_ \_ 已 \_ 註冊 RPC**
</dt> <dd> <dl> <dt>

1711 (0x6AF) 
</dt> <dt>



已註冊 (UUID) 的物件通用唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_ \_ \_ 已註冊 RPC S \_ 類型**
</dt> <dd> <dl> <dt>

1712 (0x6B0) 
</dt> <dt>



已註冊 (UUID) 類型的通用唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ 已在 \_ 接聽**
</dt> <dd> <dl> <dt>

1713 (0x6B1) 
</dt> <dt>



RPC 伺服器已經在接聽。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ 未 \_ \_ 註冊 PROTSEQS**
</dt> <dd> <dl> <dt>

1714 (0x6B2) 
</dt> <dt>



尚未註冊任何通訊協定序列。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ 未 \_ 接聽**
</dt> <dd> <dl> <dt>

1715 (0x6B3) 
</dt> <dt>



RPC 伺服器未接聽。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC \_ S \_ 未知的 \_ MGR \_ 類型**
</dt> <dd> <dl> <dt>

1716 (0x6B4) 
</dt> <dt>



管理員類型未知。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ \_ 未知（ \_ 如果**
</dt> <dd> <dl> <dt>

1717 (0x6B5) 
</dt> <dt>



介面未知。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ 沒有系結 \_**
</dt> <dd> <dl> <dt>

1718 (0x6B6) 
</dt> <dt>



沒有任何系結。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ 無 \_ PROTSEQS**
</dt> <dd> <dl> <dt>

1719 (0x6B7) 
</dt> <dt>



沒有通訊協定順序。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ 無法 \_ 建立 \_ 端點**
</dt> <dd> <dl> <dt>

1720 (0x6B8) 
</dt> <dt>



無法建立端點。


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ \_ 資源不足 \_**
</dt> <dd> <dl> <dt>

1721 (0x6B9) 
</dt> <dt>



可用的資源不足，無法完成此操作。


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC \_ S \_ 伺服器 \_ 無法使用**
</dt> <dd> <dl> <dt>

1722 (0x6BA) 
</dt> <dt>



RPC 伺服器無法使用。


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC \_ S \_ 伺服器 \_ 太 \_ 忙碌**
</dt> <dd> <dl> <dt>

1723 (0x6BB) 
</dt> <dt>



RPC 伺服器太忙碌，無法完成此操作。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC \_ S \_ 不正確 \_ 網路 \_ 選項**
</dt> <dd> <dl> <dt>

1724 (0x6BC) 
</dt> <dt>



網路選項無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S 沒有作用中的 \_ \_ 呼叫 \_**
</dt> <dd> <dl> <dt>

1725 (0x6BD) 
</dt> <dt>



此執行緒上沒有作用中的遠端程序呼叫。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC \_ S \_ 呼叫 \_ 失敗**
</dt> <dd> <dl> <dt>

1726 (0x6BE) 
</dt> <dt>



遠端程序呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC \_ S \_ 呼叫 \_ 失敗 \_ DNE**
</dt> <dd> <dl> <dt>

1727 (0x6BF) 
</dt> <dt>



遠端程序呼叫失敗且未執行。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC \_ S \_ 通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

1728 (0x6C0) 
</dt> <dt>



發生 RPC) 通訊協定錯誤 (的遠端程序呼叫。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**已 \_ 拒絕 RPC S \_ PROXY \_ 存取 \_**
</dt> <dd> <dl> <dt>

1729 (0x6C1) 
</dt> <dt>



拒絕存取 HTTP proxy。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ S \_ 不支援的 \_ 交易 \_ SYN**
</dt> <dd> <dl> <dt>

1730 (0x6C2) 
</dt> <dt>



RPC 伺服器不支援傳輸語法。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC \_ S \_ 不支援的 \_ 類型**
</dt> <dd> <dl> <dt>

1732 (0x6C4) 
</dt> <dt>



不支援 (UUID) 類型的通用唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC \_ S \_ 無效 \_ 標記**
</dt> <dd> <dl> <dt>

1733 (0x6C5) 
</dt> <dt>



標記無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC \_ S 系結 \_ 無效 \_**
</dt> <dd> <dl> <dt>

1734 (0x6C6) 
</dt> <dt>



陣列界限無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ 沒有 \_ 專案 \_ 名稱**
</dt> <dd> <dl> <dt>

1735 (0x6C7) 
</dt> <dt>



系結不包含專案名稱。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC \_ S \_ 不正確 \_ 名稱 \_ 語法**
</dt> <dd> <dl> <dt>

1736 (0x6C8) 
</dt> <dt>



名稱語法無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC \_ S \_ 不支援的 \_ 名稱 \_ 語法**
</dt> <dd> <dl> <dt>

1737 (0x6C9) 
</dt> <dt>



不支援名稱語法。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ 沒有 \_ 位址**
</dt> <dd> <dl> <dt>

1739 (0x6CB) 
</dt> <dt>



沒有任何可用的網路位址，無法用來建立 (UUID) 的通用唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC \_ S \_ 重複 \_ 端點**
</dt> <dd> <dl> <dt>

1740 (0x6CC) 
</dt> <dt>



端點重複。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 類型**
</dt> <dd> <dl> <dt>

1741 (0x6CD) 
</dt> <dt>



驗證類型未知。


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC \_ S \_ 最大 \_ 呼叫數 \_ 太 \_ 小**
</dt> <dd> <dl> <dt>

1742 (0x6CE) 
</dt> <dt>



呼叫次數上限太小。


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC \_ S \_ 字串 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

1743 (0x6CF) 
</dt> <dt>



字串太長。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S PROTSEQ**
</dt> <dd> <dl> <dt>

1744 (0x6D0) 
</dt> <dt>



找不到 RPC 通訊協定順序。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

1745 (0x6D1) 
</dt> <dt>



程式編號超出範圍。


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC \_ S 系結 \_ \_ \_ 沒有 \_ 驗證**
</dt> <dd> <dl> <dt>

1746 (0x6D2) 
</dt> <dt>



系結不包含任何驗證資訊。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 服務**
</dt> <dd> <dl> <dt>

1747 (0x6D3) 
</dt> <dt>



驗證服務未知。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 層級**
</dt> <dd> <dl> <dt>

1748 (0x6D4) 
</dt> <dt>



驗證層級未知。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC \_ S \_ 不正確 \_ 驗證身分 \_ 識別**
</dt> <dd> <dl> <dt>

1749 (0x6D5) 
</dt> <dt>



安全性內容無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ 未知的 \_ AUTHZ \_ 服務**
</dt> <dd> <dl> <dt>

1750 (0x6D6) 
</dt> <dt>



授權服務未知。


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ 不正確 \_ 專案**
</dt> <dd> <dl> <dt>

1751 (0x6D7) 
</dt> <dt>



專案無效。


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ 無法 \_ 執行 \_ OP**
</dt> <dd> <dl> <dt>

1752 (0x6D8) 
</dt> <dt>



伺服器端點無法執行此作業。


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

1753 (0x6D9) 
</dt> <dt>



端點對應程式中沒有其他可用的端點。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ 沒有 \_ 要匯出的 \_ RPC**
</dt> <dd> <dl> <dt>

1754 (0x6DA) 
</dt> <dt>



未匯出任何介面。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC \_ S \_ 不完整 \_ 名稱**
</dt> <dd> <dl> <dt>

1755 (0x6DB) 
</dt> <dt>



專案名稱不完整。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ 無效 \_ 的 \_ 。**
</dt> <dd> <dl> <dt>

1756 (0x6DC) 
</dt> <dt>



Version 選項無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ 沒有 \_ 更多 \_ 成員**
</dt> <dd> <dl> <dt>

1757 (0x6DD) 
</dt> <dt>



沒有其他成員。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ 並非 \_ 所有 \_ OBJ \_ UNEXPORTED**
</dt> <dd> <dl> <dt>

1758 (0x6DE) 
</dt> <dt>



沒有任何要 unexport 的專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 介面**
</dt> <dd> <dl> <dt>

1759 (0x6DF) 
</dt> <dt>



找不到介面。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC \_ S \_ 專案 \_ 已經 \_ 存在**
</dt> <dd> <dl> <dt>

1760 (0x6E0) 
</dt> <dt>



專案已經存在。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 專案**
</dt> <dd> <dl> <dt>

1761 (0x6E1) 
</dt> <dt>



找不到專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC \_ S \_ 名稱 \_ 服務 \_ 無法使用**
</dt> <dd> <dl> <dt>

1762 (0x6E2) 
</dt> <dt>



名稱服務無法使用。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC \_ S \_ 不正確 \_ NAF \_ 識別碼**
</dt> <dd> <dl> <dt>

1763 (0x6E3) 
</dt> <dt>



網路位址系列無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ 無法 \_ 支援**
</dt> <dd> <dl> <dt>

1764 (0x6E4) 
</dt> <dt>



不支援要求的作業。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S \_ 沒有 \_ 內容 \_ 可用**
</dt> <dd> <dl> <dt>

1765 (0x6E5) 
</dt> <dt>



沒有任何安全性內容可允許模擬。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC \_ S \_ 內部 \_ 錯誤**
</dt> <dd> <dl> <dt>

1766 (0x6E6) 
</dt> <dt>



 (RPC) 的遠端程序呼叫中發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ 零 \_ 除**
</dt> <dd> <dl> <dt>

1767 (0x6E7) 
</dt> <dt>



RPC 伺服器嘗試以零除的整數。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC \_ S \_ 位址 \_ 錯誤**
</dt> <dd> <dl> <dt>

1768 (0x6E8) 
</dt> <dt>



RPC 伺服器發生定址錯誤。


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ DIV \_ 零**
</dt> <dd> <dl> <dt>

1769 (0x6E9) 
</dt> <dt>



RPC 伺服器上的浮點運算導致零除。


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC \_ S \_ FP \_ 下溢**
</dt> <dd> <dl> <dt>

1770 (0x6EA) 
</dt> <dt>



RPC 伺服器發生浮點下溢。


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC \_ S \_ FP \_ 溢位**
</dt> <dd> <dl> <dt>

1771 (0x6EB) 
</dt> <dt>



RPC 伺服器發生浮點溢位。


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ 沒有 \_ 其他 \_ 專案**
</dt> <dd> <dl> <dt>

1772 (0x6EC) 
</dt> <dt>



可用來系結 auto 控制碼的 RPC 伺服器清單已用盡。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ CHAR \_ 交易 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

1773 (0x6ED) 
</dt> <dt>



無法開啟字元轉譯表檔。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ CHAR \_ 交易 \_ 短 \_ 檔案**
</dt> <dd> <dl> <dt>

1774 (0x6EE) 
</dt> <dt>



包含字元轉譯表的檔案具有少於512個位元組。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**\_ \_ \_ \_ Null 內容中的 RPC X SS \_**
</dt> <dd> <dl> <dt>

1775 (0x6EF) 
</dt> <dt>



在遠端程序呼叫期間，從用戶端傳遞至主機的是 null 內容控制碼。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC \_ X \_ SS \_ 內容 \_ 損毀**
</dt> <dd> <dl> <dt>

1777 (0x6F1) 
</dt> <dt>



在遠端程序呼叫期間，內容控制碼已變更。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS \_ 控制碼 \_ 不符**
</dt> <dd> <dl> <dt>

1778 (0x6F2) 
</dt> <dt>



傳遞給遠端程序呼叫的系結控制碼不相符。


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ 無法 \_ 取得 \_ 呼叫 \_ 控制碼**
</dt> <dd> <dl> <dt>

1779 (0x6F3) 
</dt> <dt>



Stub 無法取得遠端程序呼叫控制碼。


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC \_ X \_ Null \_ REF \_ 指標**
</dt> <dd> <dl> <dt>

1780 (0x6F4) 
</dt> <dt>



傳遞給存根的 null 參考指標。


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC \_ X \_ 列舉 \_ 值 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

1781 (0x6F5) 
</dt> <dt>



列舉值超出範圍。


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC \_ X \_ 位元組 \_ 計數 \_ 太 \_ 小**
</dt> <dd> <dl> <dt>

1782 (0x6F6) 
</dt> <dt>



位元組計數太小。


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X \_ 錯誤的 \_ 存根 \_ 資料**
</dt> <dd> <dl> <dt>

1783 (0x6F7) 
</dt> <dt>



存根收到了不正確的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**錯誤 \_ 不正確 \_ 使用者 \_ 緩衝區**
</dt> <dd> <dl> <dt>

1784 (0x6F8) 
</dt> <dt>



提供的使用者緩衝區對要求的作業無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**\_無法辨識的 \_ 媒體錯誤**
</dt> <dd> <dl> <dt>

1785 (0x6F9) 
</dt> <dt>



無法辨認磁片媒體。 它可能未格式化。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**錯誤 \_ 沒有 \_ 信任 \_ LSA \_ 秘密**
</dt> <dd> <dl> <dt>

1786 (0x6FA) 
</dt> <dt>



工作站沒有信任秘密。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**錯誤 \_ 沒有 \_ 信任 \_ SAM \_ 帳戶**
</dt> <dd> <dl> <dt>

1787 (0x6FB) 
</dt> <dt>



伺服器上的安全性資料庫沒有此工作站信任關係的電腦帳戶。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**\_受信任的 \_ 網域 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

1788 (0x6FC) 
</dt> <dt>



主域與受信任網域之間的信任關係失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**錯誤 \_ 信任 \_ 關聯性 \_ 失敗**
</dt> <dd> <dl> <dt>

1789 (0x6FD) 
</dt> <dt>



此工作站和主要網域間的信任關係失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**錯誤 \_ 信任 \_ 失敗**
</dt> <dd> <dl> <dt>

1790 (0x6FE) 
</dt> <dt>



網路登入失敗。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC \_ S \_ 呼叫 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

1791 (0x6FF) 
</dt> <dt>



此執行緒的遠端程序呼叫已經在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**錯誤 \_ NETLOGON \_ 未 \_ 啟動**
</dt> <dd> <dl> <dt>

1792 (0x700) 
</dt> <dt>



嘗試登入，但未啟動網路登入服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**錯誤 \_ 帳戶已 \_ 過期**
</dt> <dd> <dl> <dt>

1793 (0x701) 
</dt> <dt>



使用者的帳戶已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**錯誤 \_ 重新導向程式 \_ 具有 \_ 開啟 \_ 控制碼**
</dt> <dd> <dl> <dt>

1794 (0x702) 
</dt> <dt>



重新導向器正在使用中，無法卸載。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_已安裝錯誤的印表機 \_ 驅動程式 \_ \_**
</dt> <dd> <dl> <dt>

1795 (0x703) 
</dt> <dt>



已安裝指定的印表機驅動程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**錯誤 \_ 不明 \_ 埠**
</dt> <dd> <dl> <dt>

1796 (0x704) 
</dt> <dt>



指定的埠未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**錯誤 \_ 未知的 \_ 印表機 \_ 驅動程式**
</dt> <dd> <dl> <dt>

1797 (0x705) 
</dt> <dt>



印表機驅動程式未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**錯誤 \_ 不明 \_ PRINTPROCESSOR**
</dt> <dd> <dl> <dt>

1798 (0x706) 
</dt> <dt>



列印處理器未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**錯誤 \_ 不正確 \_ 分隔檔 \_**
</dt> <dd> <dl> <dt>

1799 (0x707) 
</dt> <dt>



指定的分隔檔無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**錯誤 \_ 不正確 \_ 優先順序**
</dt> <dd> <dl> <dt>

1800 (0x708) 
</dt> <dt>



指定的優先順序無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 名稱**
</dt> <dd> <dl> <dt>

1801 (0x709) 
</dt> <dt>



印表機名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**錯誤 \_ 印表機 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

1802 (0x70A) 
</dt> <dt>



印表機已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 命令**
</dt> <dd> <dl> <dt>

1803 (0x70B) 
</dt> <dt>



印表機命令無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**錯誤 \_ 的 \_ 資料類型無效**
</dt> <dd> <dl> <dt>

1804 (0x70C) 
</dt> <dt>



指定的資料類型無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**錯誤 \_ 不正確 \_ 環境**
</dt> <dd> <dl> <dt>

1805 (0x70D) 
</dt> <dt>



指定的環境無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ 沒有 \_ 其他 \_ 系結**
</dt> <dd> <dl> <dt>

1806 (0x70E) 
</dt> <dt>



沒有其他系結。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**\_NOLOGON \_ 域間 \_ 信任 \_ 帳戶時發生錯誤**
</dt> <dd> <dl> <dt>

1807 (0x70F) 
</dt> <dt>



使用的帳戶是限域的信任帳戶。 使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**\_NOLOGON \_ 工作站 \_ 信任 \_ 帳戶時發生錯誤**
</dt> <dd> <dl> <dt>

1808 (0x710) 
</dt> <dt>



使用的帳戶是電腦帳戶。 使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**\_NOLOGON \_ 伺服器 \_ 信任 \_ 帳戶時發生錯誤**
</dt> <dd> <dl> <dt>

1809 (0x711) 
</dt> <dt>



使用的帳戶是伺服器信任帳戶。 使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**錯誤 \_ 網域 \_ 信任 \_ 不一致**
</dt> <dd> <dl> <dt>

1810 (0x712) 
</dt> <dt>



指定網域 (SID) 的名稱或安全性識別碼，與該網域的信任資訊不一致。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**錯誤 \_ 伺服器 \_ 有 \_ 開啟的 \_ 控制碼**
</dt> <dd> <dl> <dt>

1811 (0x713) 
</dt> <dt>



伺服器正在使用中，無法卸載。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源資料**
</dt> <dd> <dl> <dt>

1812 (0x714) 
</dt> <dt>



指定的影像檔案未包含資源區段。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源類型**
</dt> <dd> <dl> <dt>

1813 (0x715) 
</dt> <dt>



在影像檔中找不到指定的資源類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源名稱**
</dt> <dd> <dl> <dt>

1814 (0x716) 
</dt> <dt>



在影像檔中找不到指定的資源名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資來源語言**
</dt> <dd> <dl> <dt>

1815 (0x717) 
</dt> <dt>



在影像檔中找不到指定的資源語言識別項。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**錯誤 \_ 的 \_ \_ 配額不足**
</dt> <dd> <dl> <dt>

1816 (0x718) 
</dt> <dt>



配額不足，無法處理此命令。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ 沒有 \_ 介面**
</dt> <dd> <dl> <dt>

1817 (0x719) 
</dt> <dt>



未註冊任何介面。


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC \_ S \_ 呼叫已 \_ 取消**
</dt> <dd> <dl> <dt>

1818 (0x71A) 
</dt> <dt>



遠端程序呼叫已取消。


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC \_ S 系結 \_ \_ 未完成**
</dt> <dd> <dl> <dt>

1819 (0x71B) 
</dt> <dt>



系結控制碼不包含所有必要的資訊。


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC \_ S \_ 通訊 \_ 失敗**
</dt> <dd> <dl> <dt>

1820 (0x71C) 
</dt> <dt>



遠端程序呼叫期間發生通訊失敗。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC \_ S \_ 不支援的 \_ 驗證 \_ 層級**
</dt> <dd> <dl> <dt>

1821 (0x71D) 
</dt> <dt>



不支援要求的驗證層級。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ 沒有 \_ PRINC \_ 名稱**
</dt> <dd> <dl> <dt>

1822 (0x71E) 
</dt> <dt>



未註冊任何主體名稱。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ 不 \_ RPC \_ 錯誤**
</dt> <dd> <dl> <dt>

1823 (0x71F) 
</dt> <dt>



指定的錯誤不是有效的 Windows RPC 錯誤碼。


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_僅限 RPC S 的 \_ \_ 本機 UUID \_**
</dt> <dd> <dl> <dt>

1824 (0x720) 
</dt> <dt>



只有在這部電腦上才有有效的 UUID。


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC \_ S \_ SEC \_ PKG \_ 錯誤**
</dt> <dd> <dl> <dt>

1825 (0x721) 
</dt> <dt>



發生安全性封裝特定的錯誤。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ 未 \_ 取消**
</dt> <dd> <dl> <dt>

1826 (0x722) 
</dt> <dt>



執行緒尚未取消。


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC \_ X \_ 不正確 \_ ES \_ 動作**
</dt> <dd> <dl> <dt>

1827 (0x723) 
</dt> <dt>



編碼/解碼控制碼的操作無效。


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ 錯誤的 \_ ES \_ 版本**
</dt> <dd> <dl> <dt>

1828 (0x724) 
</dt> <dt>



序列化封裝的版本不相容。


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC \_ X \_ 錯誤的 \_ 存根 \_ 版本**
</dt> <dd> <dl> <dt>

1829 (0x725) 
</dt> <dt>



RPC 存根的版本不相容。


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ 不正確 \_ 管道 \_ 物件**
</dt> <dd> <dl> <dt>

1830 (0x726) 
</dt> <dt>



RPC 管道物件無效或已損毀。


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X \_ 錯誤的 \_ 管道 \_ 順序**
</dt> <dd> <dl> <dt>

1831 (0x727) 
</dt> <dt>



在 RPC 管道物件上嘗試了不正確作業。


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X \_ 錯誤的 \_ 管道 \_ 版本**
</dt> <dd> <dl> <dt>

1832 (0x728) 
</dt> <dt>



不支援的 RPC 管道版本。


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC \_ S \_ COOKIE \_ 驗證 \_ 失敗**
</dt> <dd> <dl> <dt>

1833 (0x729) 
</dt> <dt>



HTTP proxy 伺服器因為 cookie 驗證失敗，所以拒絕連線。


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ \_ \_ \_ 找不到 RPC S 群組成員**
</dt> <dd> <dl> <dt>

1898 (0x76A) 
</dt> <dt>



找不到群組成員。


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ 無法 \_ 建立**
</dt> <dd> <dl> <dt>

1899 (0x76B) 
</dt> <dt>



無法建立端點對應程式資料庫專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC \_ S \_ 無效 \_ 物件**
</dt> <dd> <dl> <dt>

1900 (0x76C) 
</dt> <dt>



物件通用唯一識別碼 (UUID) 是 nil UUID。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**錯誤 \_ 不正確 \_ 時間**
</dt> <dd> <dl> <dt>

1901 (0x76D) 
</dt> <dt>



指定的時間無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**錯誤 \_ 不正確 \_ 表單 \_ 名稱**
</dt> <dd> <dl> <dt>

1902 (0x76E) 
</dt> <dt>



指定的表單名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**錯誤 \_ 的 \_ 表單 \_ 大小無效**
</dt> <dd> <dl> <dt>

1903 (0x76F) 
</dt> <dt>



指定的表單大小無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**錯誤 \_ 已在 \_ 等候**
</dt> <dd> <dl> <dt>

1904 (0x770) 
</dt> <dt>



指定的印表機控制碼已在等候。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**\_印表機 \_ 已刪除錯誤**
</dt> <dd> <dl> <dt>

1905 (0x771) 
</dt> <dt>



指定的印表機已刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 狀態**
</dt> <dd> <dl> <dt>

1906 (0x772) 
</dt> <dt>



印表機的狀態無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**錯誤 \_ 密碼 \_ 必須 \_ 變更**
</dt> <dd> <dl> <dt>

1907 (0x773) 
</dt> <dt>



使用者的密碼必須在登入之前變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**\_ \_ \_ 找不到域 \_ 控制器的錯誤**
</dt> <dd> <dl> <dt>

1908 (0x774) 
</dt> <dt>



找不到此網域的網域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**錯誤 \_ 帳戶 \_ 被鎖定 \_**
</dt> <dd> <dl> <dt>

1909 (0x775) 
</dt> <dt>



參考的帳戶目前已被鎖定，而且可能無法登入。


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**或 \_ 不正確 \_ OXID**
</dt> <dd> <dl> <dt>

1910 (0x776) 
</dt> <dt>



找不到指定的物件匯出工具。


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**或 \_ 不正確 \_ OID**
</dt> <dd> <dl> <dt>

1911 (0x777) 
</dt> <dt>



找不到指定的物件。


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**或 \_ 不正確 \_ 集合**
</dt> <dd> <dl> <dt>

1912 (0x778) 
</dt> <dt>



找不到指定的物件解析程式集合。


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ 傳送 \_ 未完成**
</dt> <dd> <dl> <dt>

1913 (0x779) 
</dt> <dt>



某些資料仍會在要求緩衝區中傳送。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ 不正確 \_ 非同步 \_ 控制碼**
</dt> <dd> <dl> <dt>

1914 (0x77A) 
</dt> <dt>



非同步遠端程序呼叫控制碼無效。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ 不正確 \_ 非同步 \_ 呼叫**
</dt> <dd> <dl> <dt>

1915 (0x77B) 
</dt> <dt>



此操作的非同步 RPC 呼叫控制碼無效。


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC \_ X \_ 管線 \_ 已關閉**
</dt> <dd> <dl> <dt>

1916 (0x77C) 
</dt> <dt>



RPC 管道物件已經關閉。


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC \_ X \_ 管道 \_ 專業 \_ 錯誤**
</dt> <dd> <dl> <dt>

1917 (0x77D) 
</dt> <dt>



RPC 呼叫會在處理所有管道之前完成。


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC \_ X \_ 管道 \_ 空白**
</dt> <dd> <dl> <dt>

1918 (0x77E) 
</dt> <dt>



RPC 管道中沒有其他可用的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**錯誤 \_ 的 \_ SITENAME**
</dt> <dd> <dl> <dt>

1919 (0x77F) 
</dt> <dt>



這部電腦沒有可用的網站名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**無法存取檔案時發生錯誤 \_ \_ \_**
</dt> <dd> <dl> <dt>

1920 (0x780) 
</dt> <dt>



系統無法存取檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**錯誤 \_ 無法 \_ 解析 \_ 檔案名**
</dt> <dd> <dl> <dt>

1921 (0x781) 
</dt> <dt>



系統無法解析檔案的名稱。


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC \_ S \_ 專案 \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

1922 (0x782) 
</dt> <dt>



專案不是預期的類型。


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ 未 \_ \_ 匯出所有 OBJ \_**
</dt> <dd> <dl> <dt>

1923 (0x783) 
</dt> <dt>



並非所有物件 Uuid 都可以匯出至指定的專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_ \_ \_ 未匯出 RPC S \_ 介面**
</dt> <dd> <dl> <dt>

1924 (0x784) 
</dt> <dt>



無法將介面匯出至指定的專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_ \_ \_ 未新增 RPC S 設定檔 \_**
</dt> <dd> <dl> <dt>

1925 (0x785) 
</dt> <dt>



無法加入指定的設定檔專案。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT \_ 未 \_ 加入**
</dt> <dd> <dl> <dt>

1926 (0x786) 
</dt> <dt>



無法加入指定的設定檔元素。


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT \_ 未 \_ 移除**
</dt> <dd> <dl> <dt>

1927 (0x787) 
</dt> <dt>



無法移除指定的設定檔元素。


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**\_ \_ \_ \_ 未加入 RPC S GRP \_ ELT**
</dt> <dd> <dl> <dt>

1928 (0x788) 
</dt> <dt>



無法加入群組元素。


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**\_ \_ \_ \_ 未移除 RPC S GRP \_ ELT**
</dt> <dd> <dl> <dt>

1929 (0x789) 
</dt> <dt>



無法移除群組元素。


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**已 \_ 封鎖錯誤公里 \_ 驅動程式 \_**
</dt> <dd> <dl> <dt>

1930 (0x78A) 
</dt> <dt>



印表機驅動程式與封鎖 NT 4.0 驅動程式的電腦上啟用的原則不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**錯誤 \_ 內容已 \_ 過期**
</dt> <dd> <dl> <dt>

1931 (0x78B) 
</dt> <dt>



內容已過期，無法再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**\_超過每個 \_ 使用者 \_ 信任 \_ 配額 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1932 (0x78C) 
</dt> <dt>



已超過目前使用者的委派信任建立配額。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**\_超出所有 \_ 使用者 \_ 信任 \_ 配額 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1933 (0x78D) 
</dt> <dt>



已超過委派的信任建立配額總數。


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**\_超過使用者 \_ 刪除 \_ 信任 \_ 配額 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1934 (0x78E) 
</dt> <dt>



已超過目前使用者的委派信任刪除配額。


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**錯誤 \_ 驗證 \_ 防火牆 \_ 失敗**
</dt> <dd> <dl> <dt>

1935 (0x78F) 
</dt> <dt>



您登入的電腦會受到驗證防火牆的保護。 指定的帳號不允許對電腦進行驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**\_封鎖遠端 \_ 列印 \_ 連接 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

1936 (0x790) 
</dt> <dt>



在您的電腦上設定的原則會封鎖與列印多工緩衝處理器的遠端連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**\_封鎖 NTLM \_ 錯誤**
</dt> <dd> <dl> <dt>

1937 (0x791) 
</dt> <dt>



驗證失敗，因為 NTLM 驗證已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_ \_ 需要變更錯誤 \_ 密碼**
</dt> <dd> <dl> <dt>

1938 (0x792) 
</dt> <dt>



登入失敗： EAS 原則會要求使用者變更其密碼，才能執行這種操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**錯誤 \_ 不正確 \_ 圖元 \_ 格式**
</dt> <dd> <dl> <dt>

2000 (0x7D0) 
</dt> <dt>



像素格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**錯誤 \_ 的 \_ 驅動程式錯誤**
</dt> <dd> <dl> <dt>

2001 (0x7D1) 
</dt> <dt>



指定的驅動程式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**錯誤 \_ 不正確 \_ 視窗 \_ 樣式**
</dt> <dd> <dl> <dt>

2002 (0x7D2) 
</dt> <dt>



此操作的視窗樣式或類別屬性無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_ \_ 不支援的錯誤中繼檔 \_**
</dt> <dd> <dl> <dt>

2003 (0x7D3) 
</dt> <dt>



不支援要求的中繼檔作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_ \_ 不支援錯誤 \_ 轉換**
</dt> <dd> <dl> <dt>

2004 (0x7D4) 
</dt> <dt>



不支援要求的轉換作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_ \_ 不支援錯誤 \_ 裁剪**
</dt> <dd> <dl> <dt>

2005 (0x7D5) 
</dt> <dt>



不支援要求的剪切作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**錯誤 \_ 不正確 \_ CMM**
</dt> <dd> <dl> <dt>

2010 (0x7DA) 
</dt> <dt>



指定的色彩管理模組無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**錯誤 \_ 不正確 \_ 設定檔**
</dt> <dd> <dl> <dt>

2011 (0x7DB) 
</dt> <dt>



指定的色彩設定檔無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_ \_ 找不到錯誤標記 \_**
</dt> <dd> <dl> <dt>

2012 (0x7DC) 
</dt> <dt>



找不到指定的標記。


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**錯誤 \_ 標記 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

2013 (0x7DD) 
</dt> <dt>



必要的標記不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**錯誤 \_ 重複 \_ 標記**
</dt> <dd> <dl> <dt>

2014 (0x7DE) 
</dt> <dt>



指定的標記已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**錯誤 \_ 配置 \_ 檔 \_ 未 \_ 與 \_ 裝置相關聯**
</dt> <dd> <dl> <dt>

2015 (0x7DF) 
</dt> <dt>



指定的色彩設定檔未與指定的裝置建立關聯。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_ \_ 找不到錯誤設定檔 \_**
</dt> <dd> <dl> <dt>

2016 (0x7E0) 
</dt> <dt>



找不到指定的色彩設定檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**錯誤 \_ 無效 \_ COLORSPACE**
</dt> <dd> <dl> <dt>

2017 (0x7E1) 
</dt> <dt>



指定的色彩空間無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**錯誤 \_ ICM \_ 未 \_ 啟用**
</dt> <dd> <dl> <dt>

2018 (0x7E2) 
</dt> <dt>



未啟用影像色彩管理。


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**\_刪除 \_ ICM \_ XFORM 時發生錯誤**
</dt> <dd> <dl> <dt>

2019 (0x7E3) 
</dt> <dt>



刪除色彩轉換時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**錯誤 \_ 不正確 \_ 轉換**
</dt> <dd> <dl> <dt>

2020 (0x7E4) 
</dt> <dt>



指定的色彩轉換無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**錯誤 \_ COLORSPACE \_ 不相符**
</dt> <dd> <dl> <dt>

2021 (0x7E5) 
</dt> <dt>



指定的轉換與點陣圖的色彩空間不符。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**錯誤 \_ 無效 \_ COLORINDEX**
</dt> <dd> <dl> <dt>

2022 (0x7E6) 
</dt> <dt>



設定檔中不存在指定的命名色彩索引。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**錯誤 \_ 設定檔不 \_ \_ \_ 符合 \_ 裝置**
</dt> <dd> <dl> <dt>

2023 (0x7E7) 
</dt> <dt>



指定的設定檔適用于類型與指定裝置不同的裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**\_連接 \_ 其他 \_ 密碼時發生錯誤**
</dt> <dd> <dl> <dt>

2108 (0x83C) 
</dt> <dt>



已成功建立網路連線，但使用者必須收到原本指定之密碼以外的提示。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**\_連接 \_ 其他 \_ 密碼 \_ 預設值時發生錯誤**
</dt> <dd> <dl> <dt>

2109 (0x83D) 
</dt> <dt>



已使用預設認證成功建立網路連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**錯誤的使用者 \_ \_ 名稱錯誤**
</dt> <dd> <dl> <dt>

2202 (0x89A) 
</dt> <dt>



指定的使用者名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**\_未 \_ 連線錯誤**
</dt> <dd> <dl> <dt>

2250 (0x8CA) 
</dt> <dt>



此網路連接不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**開啟檔案時發生錯誤 \_ \_**
</dt> <dd> <dl> <dt>

2401 (0x961) 
</dt> <dt>



此網路連線已開啟檔案或要求暫止。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**使用中的連接時發生錯誤 \_ \_**
</dt> <dd> <dl> <dt>

2402 (0x962) 
</dt> <dt>



作用中的連接仍然存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_ \_ 使用中的錯誤裝置 \_**
</dt> <dd> <dl> <dt>

2404 (0x964) 
</dt> <dt>



使用中的進程正在使用此裝置，因此無法中斷連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**錯誤 \_ 不明的 \_ 列印 \_ 監視器**
</dt> <dd> <dl> <dt>

3000 (0xBB8) 
</dt> <dt>



指定的列印監視器未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_ \_ \_ 使用中的印表機驅動程式時發生錯誤 \_**
</dt> <dd> <dl> <dt>

3001 (0xBB9) 
</dt> <dt>



指定的印表機驅動程式目前正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ \_ 找不到錯誤的多工緩衝處理檔案**
</dt> <dd> <dl> <dt>

3002 (0xBBA) 
</dt> <dt>



找不到多工緩衝處理檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**\_SPL \_ 無 \_ STARTDOC 時發生錯誤**
</dt> <dd> <dl> <dt>

3003 (0xBBB) 
</dt> <dt>



未發出 StartDocPrinter 呼叫。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**\_SPL \_ 無 \_ SYSTEM.PRINTING.PRINTQUEUE.ADDJOB 時發生錯誤**
</dt> <dd> <dl> <dt>

3004 (0xBBC) 
</dt> <dt>



未發出 System.printing.printqueue.addjob 呼叫。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**\_ \_ \_ 已安裝錯誤列印 \_ 處理器**
</dt> <dd> <dl> <dt>

3005 (0xBBD) 
</dt> <dt>



已安裝指定的列印處理器。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**\_ \_ \_ 已安裝錯誤列印 \_ 監視器**
</dt> <dd> <dl> <dt>

3006 (0xBBE) 
</dt> <dt>



已安裝指定的列印監視器。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**錯誤 \_ 不正確 \_ 列印 \_ 監視器**
</dt> <dd> <dl> <dt>

3007 (0xBBF) 
</dt> <dt>



指定的列印監視器沒有必要的功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**\_ \_ \_ 使用中的列印監視錯誤 \_**
</dt> <dd> <dl> <dt>

3008 (0xBC0) 
</dt> <dt>



指定的列印監視器目前正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**錯誤 \_ 印表機 \_ 已將 \_ 作業 \_ 排入佇列**
</dt> <dd> <dl> <dt>

3009 (0xBC1) 
</dt> <dt>



當有作業排入印表機佇列時，不允許要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**\_ \_ 需要重新開機 \_ 錯誤**
</dt> <dd> <dl> <dt>

3010 (0xBC2) 
</dt> <dt>



要求的作業已成功。 在系統重新開機之前，變更將不會生效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**\_ \_ 需要重新開機錯誤成功 \_**
</dt> <dd> <dl> <dt>

3011 (0xBC3) 
</dt> <dt>



要求的作業已成功。 在服務重新開機之前，變更將不會生效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_ \_ 找不到錯誤印表機 \_**
</dt> <dd> <dl> <dt>

3012 (0xBC4) 
</dt> <dt>



找不到任何印表機。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**錯誤 \_ 印表機 \_ 驅動程式 \_ 警告**
</dt> <dd> <dl> <dt>

3013 (0xBC5) 
</dt> <dt>



印表機驅動程式已知不可靠。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_印表機 \_ 驅動程式 \_ 封鎖錯誤**
</dt> <dd> <dl> <dt>

3014 (0xBC6) 
</dt> <dt>



已知印表機驅動程式會危害系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**\_ \_ \_ \_ 使用中的印表機驅動程式套件錯誤 \_**
</dt> <dd> <dl> <dt>

3015 (0xBC7) 
</dt> <dt>



指定的印表機驅動程式套件目前正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤核心驅動程式套件**
</dt> <dd> <dl> <dt>

3016 (0xBC8) 
</dt> <dt>



找不到印表機驅動程式套件所需的核心驅動程式套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**\_無法 \_ 重新開機 \_ 所需的錯誤**
</dt> <dd> <dl> <dt>

3017 (0xBC9) 
</dt> <dt>



要求的作業失敗。 需要重新開機系統，才能復原所做的變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**啟動 \_ \_ 重新開機錯誤失敗 \_**
</dt> <dd> <dl> <dt>

3018 (0xBCA) 
</dt> <dt>



要求的作業失敗。 已起始系統重新開機以回復所做的變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**\_需要下載錯誤的印表機 \_ 驅動程式 \_ \_**
</dt> <dd> <dl> <dt>

3019 (0xBCB) 
</dt> <dt>



在系統上找不到指定的印表機驅動程式，因此需要下載。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**錯誤 \_ 列印 \_ 作業 \_ 需要重新開機 \_**
</dt> <dd> <dl> <dt>

3020 (0xBCC) 
</dt> <dt>



要求的列印工作無法列印。 列印系統更新需要重新提交作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 驅動程式 \_ 資訊清單**
</dt> <dd> <dl> <dt>

3021 (0xBCD) 
</dt> <dt>



印表機驅動程式不包含有效的資訊清單，或包含太多資訊清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**\_ \_ 無法共用錯誤 \_ 印表機**
</dt> <dd> <dl> <dt>

3022 (0xBCE) 
</dt> <dt>



指定的印表機無法共用。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**錯誤 \_ 要求已 \_ 暫停**
</dt> <dd> <dl> <dt>

3050 (0xBEA) 
</dt> <dt>



作業已暫停。


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**錯誤 \_ IO 重新 \_ 發出 \_ 為 \_ 快取**
</dt> <dd> <dl> <dt>

3950 (0xF6E) 
</dt> <dt>



將指定的作業重新發出為快取的 IO 作業。


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




