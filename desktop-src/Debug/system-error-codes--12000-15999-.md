---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼12000-1599，適用于開發人員。
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: '系統錯誤碼 (12000-15999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468248"
---
# <a name="system-error-codes-12000-15999"></a>系統錯誤碼 (12000-15999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述 (錯誤12000到 15999) 的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**錯誤 \_\_網際網路 \** _
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0) 
</dt> <dt>



請參閱 [網際網路錯誤碼](../wininet/wininet-errors.md) 和 WinInet。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *錯誤 \_ IPSEC \_ QM \_ 原則 \_ 存在**
</dt> <dd> <dl> <dt>

13000 (0x32C8) 
</dt> <dt>



指定的快速模式原則已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC QM 原則錯誤**
</dt> <dd> <dl> <dt>

13001 (0x32C9) 
</dt> <dt>



找不到指定的快速模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**\_ \_ \_ \_ 使用中 IPSEC QM 原則時發生錯誤 \_**
</dt> <dd> <dl> <dt>

13002 (0x32CA) 
</dt> <dt>



正在使用指定的快速模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**\_IPSEC \_ MM \_ 原則 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

13003 (0x32CB) 
</dt> <dt>



指定的主要模式原則已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 原則錯誤**
</dt> <dd> <dl> <dt>

13004 (0x32CC) 
</dt> <dt>



找不到指定的主要模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**\_ \_ \_ \_ 使用中 IPSEC MM 原則時發生錯誤 \_**
</dt> <dd> <dl> <dt>

13005 (0x32CD) 
</dt> <dt>



正在使用指定的主要模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**\_IPSEC \_ MM \_ 篩選準則 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

13006 (0x32CE) 
</dt> <dt>



指定的主要模式篩選已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 篩選器錯誤**
</dt> <dd> <dl> <dt>

13007 (0x32CF) 
</dt> <dt>



找不到指定的主要模式篩選。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**\_IPSEC \_ 傳輸 \_ 篩選準則 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

13008 (0x32D0) 
</dt> <dt>



指定的傳輸模式篩選已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC 傳輸篩選錯誤**
</dt> <dd> <dl> <dt>

13009 (0x32D1) 
</dt> <dt>



指定的傳輸模式篩選不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**\_IPSEC \_ MM \_ 驗證 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

13010 (0x32D2) 
</dt> <dt>



指定的主要模式驗證清單存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 驗證錯誤**
</dt> <dd> <dl> <dt>

13011 (0x32D3) 
</dt> <dt>



找不到指定的主要模式驗證清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**\_ \_ \_ \_ 使用中的 IPSEC MM 驗證錯誤 \_**
</dt> <dd> <dl> <dt>

13012 (0x32D4) 
</dt> <dt>



正在使用指定的主要模式驗證清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設 MM 原則的錯誤**
</dt> <dd> <dl> <dt>

13013 (0x32D5) 
</dt> <dt>



找不到指定的預設主要模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設值 MM 驗證的錯誤**
</dt> <dd> <dl> <dt>

13014 (0x32D6) 
</dt> <dt>



找不到指定的預設主要模式驗證清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設 QM 原則的錯誤**
</dt> <dd> <dl> <dt>

13015 (0x32D7) 
</dt> <dt>



找不到指定的預設快速模式原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**\_IPSEC 通道 \_ \_ 篩選準則 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

13016 (0x32D8) 
</dt> <dt>



指定的通道模式篩選器存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC 通道篩選器錯誤**
</dt> <dd> <dl> <dt>

13017 (0x32D9) 
</dt> <dt>



找不到指定的通道模式篩選。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**\_IPSEC \_ MM \_ 篩選暫止 \_ \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13018 (0x32DA) 
</dt> <dt>



主要模式篩選正在暫止刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**\_IPSEC \_ 傳輸 \_ 篩選器 \_ 暫止 \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13019 (0x32DB) 
</dt> <dt>



傳輸篩選正在暫止刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**\_IPSEC 通道 \_ \_ 篩選暫 \_ 止 \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13020 (0x32DC) 
</dt> <dt>



通道篩選器正在等待刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**\_IPSEC \_ MM \_ 原則暫止 \_ \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13021 (0x32DD) 
</dt> <dt>



主要模式原則正在等待刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**\_IPSEC \_ MM \_ 驗證暫止 \_ \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13022 (0x32DE) 
</dt> <dt>



主要模式驗證配套正在等待刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**\_IPSEC \_ QM \_ 原則暫止 \_ \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13023 (0x32DF) 
</dt> <dt>



快速模式原則正在等待刪除。


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**已 \_ \_ 剪除 IPSEC MM \_ 原則 \_ 的警告**
</dt> <dd> <dl> <dt>

13024 (0x32E0) 
</dt> <dt>



已成功新增主要模式原則，但不支援某些要求的供應專案。


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**已 \_ \_ 剪除 IPSEC QM \_ 原則 \_ 的警告**
</dt> <dd> <dl> <dt>

13025 (0x32E1) 
</dt> <dt>



已成功新增快速模式原則，但不支援某些要求的供應專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 開始時發生錯誤**
</dt> <dd> <dl> <dt>

13800 (0x35E8) 
</dt> <dt>



\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 開始時發生錯誤


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**\_IPSEC \_ IKE \_ 驗證 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13801 (0x35E9) 
</dt> <dt>



IKE 驗證認證無法接受。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**錯誤 \_ IPSEC \_ IKE \_ ATTRIB \_ 失敗**
</dt> <dd> <dl> <dt>

13802 (0x35EA) 
</dt> <dt>



IKE 安全性屬性是無法接受的。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**\_IPSEC \_ IKE \_ 協商 \_ 暫止時發生錯誤**
</dt> <dd> <dl> <dt>

13803 (0x35EB) 
</dt> <dt>



正在進行 IKE 協商。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**\_IPSEC \_ IKE \_ 一般 \_ 處理 \_ 錯誤錯誤**
</dt> <dd> <dl> <dt>

13804 (0x35EC) 
</dt> <dt>



一般處理錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**\_IPSEC \_ IKE \_ 超時 \_ 錯誤**
</dt> <dd> <dl> <dt>

13805 (0x35ED) 
</dt> <dt>



協商超時。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**\_IPSEC \_ IKE \_ NO \_ CERT 錯誤**
</dt> <dd> <dl> <dt>

13806 (0x35EE) 
</dt> <dt>



IKE 無法找到有效的電腦憑證。 請洽詢您的網路安全性系統管理員，瞭解如何在適當的憑證存放區中安裝有效的憑證。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**\_IPSEC \_ IKE \_ SA \_ 已刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13807 (0x35EF) 
</dt> <dt>



建立完成之前，對等刪除 IKE SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**\_IPSEC \_ IKE \_ SA \_ REAPED 錯誤**
</dt> <dd> <dl> <dt>

13808 (0x35F0) 
</dt> <dt>



已在建立完成之前刪除 IKE SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**錯誤 \_ IPSEC \_ IKE \_ MM \_ 取得 \_ 捨棄**
</dt> <dd> <dl> <dt>

13809 (0x35F1) 
</dt> <dt>



協調要求在佇列中的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**\_IPSEC \_ IKE \_ QM \_ 取得 \_ 捨棄錯誤**
</dt> <dd> <dl> <dt>

13810 (0x35F2) 
</dt> <dt>



協調要求在佇列中的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**\_IPSEC \_ IKE \_ 佇列 \_ 捨棄 \_ 分鐘錯誤**
</dt> <dd> <dl> <dt>

13811 (0x35F3) 
</dt> <dt>



協調要求在佇列中的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**\_IPSEC \_ IKE \_ 佇列 \_ 捨棄 \_ \_ 錯誤**
</dt> <dd> <dl> <dt>

13812 (0x35F4) 
</dt> <dt>



協調要求在佇列中的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**錯誤 \_ IPSEC \_ IKE \_ 捨棄 \_ 沒有 \_ 回應**
</dt> <dd> <dl> <dt>

13813 (0x35F5) 
</dt> <dt>



沒有對等的回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**錯誤 \_ IPSEC \_ IKE \_ MM \_ 延遲 \_ 下降**
</dt> <dd> <dl> <dt>

13814 (0x35F6) 
</dt> <dt>



協商花費的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**\_IPSEC \_ IKE \_ QM \_ 延遲 \_ 下降錯誤**
</dt> <dd> <dl> <dt>

13815 (0x35F7) 
</dt> <dt>



協商花費的時間太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**\_IPSEC \_ IKE \_ 錯誤錯誤**
</dt> <dd> <dl> <dt>

13816 (0x35F8) 
</dt> <dt>



發生未知錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**\_IPSEC \_ IKE CRL \_ 錯誤 \_ 失敗**
</dt> <dd> <dl> <dt>

13817 (0x35F9) 
</dt> <dt>



憑證撤銷檢查失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 金鑰 \_ 使用方式錯誤**
</dt> <dd> <dl> <dt>

13818 (0x35FA) 
</dt> <dt>



憑證金鑰使用方式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**\_IPSEC \_ IKE 無效 \_ 憑證 \_ \_ 類型錯誤**
</dt> <dd> <dl> <dt>

13819 (0x35FB) 
</dt> <dt>



不正確憑證類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**\_IPSEC \_ IKE \_ 沒有私用 \_ \_ 金鑰錯誤**
</dt> <dd> <dl> <dt>

13820 (0x35FC) 
</dt> <dt>



IKE 協商失敗，因為使用的電腦憑證沒有私密金鑰。 IPsec 憑證需要私密金鑰。 請洽詢您的網路安全性系統管理員，將取代為具有私密金鑰的憑證。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**\_IPSEC IKE 同時重設 \_ \_ \_ 金鑰錯誤**
</dt> <dd> <dl> <dt>

13821 (0x35FD) 
</dt> <dt>



偵測到同時重新建立金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**\_IPSEC \_ IKE \_ DH \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13822 (0x35FE) 
</dt> <dt>



Diffie-Hellman 計算失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**錯誤 \_ IPSEC \_ IKE \_ 重要 \_ 承載 \_ 無法 \_ 辨識**
</dt> <dd> <dl> <dt>

13823 (0x35FF) 
</dt> <dt>



不知道如何處理重要承載。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**\_IPSEC \_ IKE \_ 無效 \_ 標頭錯誤**
</dt> <dd> <dl> <dt>

13824 (0x3600) 
</dt> <dt>



不正確標頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 原則錯誤**
</dt> <dd> <dl> <dt>

13825 (0x3601) 
</dt> <dt>



未設定任何原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**\_IPSEC \_ IKE \_ 無效 \_ 簽章錯誤**
</dt> <dd> <dl> <dt>

13826 (0x3602) 
</dt> <dt>



無法驗證簽章。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**\_IPSEC \_ IKE \_ KERBEROS \_ 錯誤錯誤**
</dt> <dd> <dl> <dt>

13827 (0x3603) 
</dt> <dt>



無法使用 Kerberos 進行驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 公開金鑰 \_ 的錯誤**
</dt> <dd> <dl> <dt>

13828 (0x3604) 
</dt> <dt>



對等的憑證沒有公開金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR 錯誤**
</dt> <dd> <dl> <dt>

13829 (0x3605) 
</dt> <dt>



處理錯誤承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ SA 時發生錯誤**
</dt> <dd> <dl> <dt>

13830 (0x3606) 
</dt> <dt>



處理 SA 承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**\_IPSEC \_ IKE \_ 進程 \_ \_ 錯誤的錯誤**
</dt> <dd> <dl> <dt>

13831 (0x3607) 
</dt> <dt>



處理提案承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 交易錯誤**
</dt> <dd> <dl> <dt>

13832 (0x3608) 
</dt> <dt>



處理轉換承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ KE 時發生錯誤**
</dt> <dd> <dl> <dt>

13833 (0x3609) 
</dt> <dt>



處理 KE 承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 識別碼錯誤**
</dt> <dd> <dl> <dt>

13834 (0x360A) 
</dt> <dt>



處理識別碼承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**\_IPSEC \_ IKE \_ 進程 \_ \_ 錯誤憑證錯誤**
</dt> <dd> <dl> <dt>

13835 (0x360B) 
</dt> <dt>



處理憑證承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ CERT \_ 要求時發生錯誤**
</dt> <dd> <dl> <dt>

13836 (0x360C) 
</dt> <dt>



處理憑證要求承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ 雜湊錯誤**
</dt> <dd> <dl> <dt>

13837 (0x360D) 
</dt> <dt>



處理雜湊承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ SIG 錯誤**
</dt> <dd> <dl> <dt>

13838 (0x360E) 
</dt> <dt>



處理簽章承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ NONCE 錯誤**
</dt> <dd> <dl> <dt>

13839 (0x360F) 
</dt> <dt>



處理 Nonce 承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 通知時發生錯誤**
</dt> <dd> <dl> <dt>

13840 (0x3610) 
</dt> <dt>



處理通知承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13841 (0x3611) 
</dt> <dt>



處理刪除承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 廠商錯誤**
</dt> <dd> <dl> <dt>

13842 (0x3612) 
</dt> <dt>



處理 VendorId 承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**\_IPSEC \_ IKE \_ 無效 \_ 承載錯誤**
</dt> <dd> <dl> <dt>

13843 (0x3613) 
</dt> <dt>



收到不正確承載。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**\_IPSEC \_ IKE \_ 載入 \_ 軟 \_ SA 錯誤**
</dt> <dd> <dl> <dt>

13844 (0x3614) 
</dt> <dt>



已載入的軟 SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**\_IPSEC \_ IKE \_ 軟 \_ SA \_ \_ 錯誤的錯誤**
</dt> <dd> <dl> <dt>

13845 (0x3615) 
</dt> <dt>



軟 SA 已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**\_IPSEC \_ IKE \_ 無效 \_ COOKIE 錯誤**
</dt> <dd> <dl> <dt>

13846 (0x3616) 
</dt> <dt>



收到不正確 cookie。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 對等 \_ 憑證錯誤**
</dt> <dd> <dl> <dt>

13847 (0x3617) 
</dt> <dt>



對等無法傳送有效的電腦憑證。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**\_IPSEC \_ IKE \_ 對等 \_ CRL 錯誤 \_ 失敗**
</dt> <dd> <dl> <dt>

13848 (0x3618) 
</dt> <dt>



對等憑證的認證撤銷檢查失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**\_IPSEC \_ IKE \_ 原則 \_ 變更時發生錯誤**
</dt> <dd> <dl> <dt>

13849 (0x3619) 
</dt> <dt>



新原則是以舊原則形成的無效 SAs。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**錯誤 \_ IPSEC \_ IKE \_ NO \_ MM \_ 原則**
</dt> <dd> <dl> <dt>

13850 (0x361A) 
</dt> <dt>



沒有可用的主要模式 IKE 原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**\_IPSEC \_ IKE \_ NOTCBPRIV 錯誤**
</dt> <dd> <dl> <dt>

13851 (0x361B) 
</dt> <dt>



無法啟用 TCB 許可權。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**\_IPSEC \_ IKE \_ SECLOADFAIL 錯誤**
</dt> <dd> <dl> <dt>

13852 (0x361C) 
</dt> <dt>



無法載入 SECURITY.DLL。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**\_IPSEC \_ IKE \_ FAILSSPINIT 錯誤**
</dt> <dd> <dl> <dt>

13853 (0x361D) 
</dt> <dt>



無法從 SSPI 取得安全性函數資料表分派位址。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**\_IPSEC \_ IKE \_ FAILQUERYSSP 錯誤**
</dt> <dd> <dl> <dt>

13854 (0x361E) 
</dt> <dt>



無法查詢 Kerberos 套件以取得權杖大小上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**\_IPSEC \_ IKE \_ SRVACQFAIL 錯誤**
</dt> <dd> <dl> <dt>

13855 (0x361F) 
</dt> <dt>



無法取得 ISAKMP/錯誤 \_ IPSEC IKE 服務的 Kerberos 伺服器認證 \_ 。 Kerberos 驗證將無法運作。 最可能的原因是缺少網域成員資格。 如果您的電腦是工作組的成員，這是正常的。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**\_IPSEC \_ IKE \_ SRVQUERYCRED 錯誤**
</dt> <dd> <dl> <dt>

13856 (0x3620) 
</dt> <dt>



無法判斷 ISAKMP/錯誤 \_ IPSEC \_ IKE 服務 ([**QUERYCREDENTIALSATTRIBUTES**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)) 的 SSPI 主體名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**\_IPSEC \_ IKE \_ GETSPIFAIL 錯誤**
</dt> <dd> <dl> <dt>

13857 (0x3621) 
</dt> <dt>



無法從 IPsec 驅動程式取得輸入 SA 的新 SPI。 最常見的原因是驅動程式沒有正確的篩選。 檢查您的原則，以驗證篩選準則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**\_IPSEC \_ IKE \_ 無效 \_ 篩選錯誤**
</dt> <dd> <dl> <dt>

13858 (0x3622) 
</dt> <dt>



指定的篩選準則無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**\_IPSEC \_ IKE \_ 記憶體不足 \_ 的 \_ 錯誤**
</dt> <dd> <dl> <dt>

13859 (0x3623) 
</dt> <dt>



記憶體配置失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**\_IPSEC \_ IKE \_ 新增 \_ 更新 \_ 金鑰 \_ 失敗的錯誤**
</dt> <dd> <dl> <dt>

13860 (0x3624) 
</dt> <dt>



無法將安全性關聯新增至 IPsec 驅動程式。 最常見的原因是 IKE 協商花費的時間太長而無法完成。 如果問題持續發生，請降低失敗電腦的負載。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**\_IPSEC \_ IKE \_ 無效 \_ 原則錯誤**
</dt> <dd> <dl> <dt>

13861 (0x3625) 
</dt> <dt>



原則無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**\_IPSEC \_ IKE \_ 未知 \_ DOI 錯誤**
</dt> <dd> <dl> <dt>

13862 (0x3626) 
</dt> <dt>



不正確 DOI。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**\_IPSEC \_ IKE \_ 無效 \_ 狀況錯誤的錯誤**
</dt> <dd> <dl> <dt>

13863 (0x3627) 
</dt> <dt>



不正確情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**\_IPSEC \_ IKE \_ DH \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

13864 (0x3628) 
</dt> <dt>



Diffie-Hellman 失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**\_IPSEC \_ IKE \_ 無效 \_ 群組錯誤**
</dt> <dd> <dl> <dt>

13865 (0x3629) 
</dt> <dt>



不正確 Diffie-Hellman 群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**\_IPSEC \_ IKE \_ 加密錯誤**
</dt> <dd> <dl> <dt>

13866 (0x362A) 
</dt> <dt>



加密承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**\_IPSEC \_ IKE \_ 解密時發生錯誤**
</dt> <dd> <dl> <dt>

13867 (0x362B) 
</dt> <dt>



解密承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**\_IPSEC \_ IKE \_ 原則 \_ 相符錯誤**
</dt> <dd> <dl> <dt>

13868 (0x362C) 
</dt> <dt>



原則相符錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**\_IPSEC \_ IKE \_ 不支援的 \_ 識別碼錯誤**
</dt> <dd> <dl> <dt>

13869 (0x362D) 
</dt> <dt>



不支援的識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**\_IPSEC \_ IKE \_ 無效 \_ 雜湊錯誤**
</dt> <dd> <dl> <dt>

13870 (0x362E) 
</dt> <dt>



雜湊驗證失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**\_IPSEC \_ IKE \_ 無效 \_ 雜湊 \_ ALG 錯誤**
</dt> <dd> <dl> <dt>

13871 (0x362F) 
</dt> <dt>



不正確雜湊演算法。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 雜湊 \_ 大小錯誤**
</dt> <dd> <dl> <dt>

13872 (0x3630) 
</dt> <dt>



不正確雜湊大小。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**\_IPSEC \_ IKE \_ 無效 \_ 加密 \_ ALG 錯誤**
</dt> <dd> <dl> <dt>

13873 (0x3631) 
</dt> <dt>



不正確加密演算法。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 驗證 \_ 演算法錯誤**
</dt> <dd> <dl> <dt>

13874 (0x3632) 
</dt> <dt>



不正確驗證演算法。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ SIG 錯誤**
</dt> <dd> <dl> <dt>

13875 (0x3633) 
</dt> <dt>



不正確憑證簽章。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**\_IPSEC \_ IKE \_ 載入 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13876 (0x3634) 
</dt> <dt>



載入失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**\_IPSEC \_ IKE \_ RPC \_ 刪除時發生錯誤**
</dt> <dd> <dl> <dt>

13877 (0x3635) 
</dt> <dt>



已透過 RPC 呼叫刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**\_IPSEC \_ IKE \_ 良性 \_ 重新初始化錯誤**
</dt> <dd> <dl> <dt>

13878 (0x3636) 
</dt> <dt>



為了執行重新初始化而建立的暫時狀態。 這不是真正的失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**\_IPSEC \_ IKE \_ 無效回應程式 \_ \_ 存留期 \_ 通知錯誤**
</dt> <dd> <dl> <dt>

13879 (0x3637) 
</dt> <dt>



在回應程式存留期通知中收到的存留期值低於 Windows 2000 設定的最小值。 請修正對等電腦上的原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 主要 \_ 版本錯誤**
</dt> <dd> <dl> <dt>

13880 (0x3638) 
</dt> <dt>



收件者無法處理標頭中指定的 IKE 版本。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**\_IPSEC \_ IKE \_ 無效 \_ CERT \_ KEYLEN 錯誤**
</dt> <dd> <dl> <dt>

13881 (0x3639) 
</dt> <dt>



憑證中的金鑰長度太小，無法設定安全性需求。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**\_IPSEC \_ IKE \_ MM \_ 限制錯誤**
</dt> <dd> <dl> <dt>

13882 (0x363A) 
</dt> <dt>



已超過對等的已建立 MM SAs 數目上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**\_ \_ \_ 停用 IPSEC IKE 協商 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

13883 (0x363B) 
</dt> <dt>



IKE 收到停用協商的原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**\_IPSEC \_ IKE \_ QM \_ 限制錯誤**
</dt> <dd> <dl> <dt>

13884 (0x363C) 
</dt> <dt>



已達到主要模式的最大快速模式限制。 將會啟動新的主要模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**\_IPSEC \_ IKE \_ MM \_ 過期時發生錯誤**
</dt> <dd> <dl> <dt>

13885 (0x363D) 
</dt> <dt>



主要模式 SA 存留期已過期或對等傳送了主要模式刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**\_IPSEC \_ IKE \_ 對等 \_ MM \_ 視為 \_ 不正確錯誤**
</dt> <dd> <dl> <dt>

13886 (0x363E) 
</dt> <dt>



主要模式 SA 假設為無效，因為對等已停止回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**\_IPSEC \_ IKE 憑證 \_ \_ 鏈 \_ 原則 \_ 不符的錯誤**
</dt> <dd> <dl> <dt>

13887 (0x363F) 
</dt> <dt>



憑證不會與 IPsec 原則中的根信任連結。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**\_IPSEC \_ IKE 未 \_ 預期的 \_ 訊息 \_ 識別碼錯誤**
</dt> <dd> <dl> <dt>

13888 (0x3640) 
</dt> <dt>



收到未預期的訊息識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 驗證 \_ 承載錯誤**
</dt> <dd> <dl> <dt>

13889 (0x3641) 
</dt> <dt>



收到不正確驗證優惠。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**\_傳送 IPSEC \_ IKE \_ DOS \_ COOKIE \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

13890 (0x3642) 
</dt> <dt>



傳送的 DoS cookie 通知給啟動器。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**\_IPSEC \_ IKE \_ 關閉 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

13891 (0x3643) 
</dt> <dt>



IKE 服務正在關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**\_IPSEC \_ IKE \_ CGA \_ 驗證 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13892 (0x3644) 
</dt> <dt>



無法驗證 CGA 位址和憑證之間的系結。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ NATOA 錯誤**
</dt> <dd> <dl> <dt>

13893 (0x3645) 
</dt> <dt>



處理 NatOA 承載時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**\_IPSEC \_ IKE \_ 無效 \_ \_ 的 QM 錯誤 \_ MM**
</dt> <dd> <dl> <dt>

13894 (0x3646) 
</dt> <dt>



主要模式的參數對此快速模式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**\_IPSEC \_ IKE \_ QM \_ 過期時發生錯誤**
</dt> <dd> <dl> <dt>

13895 (0x3647) 
</dt> <dt>



IPsec 驅動程式已過期的快速模式 SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**\_IPSEC \_ IKE \_ 太 \_ 多 \_ 篩選錯誤**
</dt> <dd> <dl> <dt>

13896 (0x3648) 
</dt> <dt>



偵測到太多動態新增的 IKEEXT 篩選。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 結束時發生錯誤**
</dt> <dd> <dl> <dt>

13897 (0x3649) 
</dt> <dt>



\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 結束時發生錯誤


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**\_IPSEC \_ IKE \_ 終止 \_ 虛擬 \_ NAP \_ 通道時發生錯誤**
</dt> <dd> <dl> <dt>

13898 (0x364A) 
</dt> <dt>



NAP reauth 成功，必須刪除虛擬 NAP IKEv2 通道。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**\_IPSEC \_ IKE \_ 內部 \_ IP \_ 指派 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

13899 (0x364B) 
</dt> <dt>



在通道模式中將內部 IP 位址指派給啟動器時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**\_IPSEC \_ IKE \_ 要求 \_ \_ \_ 缺少 CP 承載時發生錯誤**
</dt> <dd> <dl> <dt>

13900 (0x364C) 
</dt> <dt>



要求缺少設定承載。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**錯誤 \_ IPSEC \_ KEY \_ MODULE \_ 模擬 \_ 協商 \_ 暫止**
</dt> <dd> <dl> <dt>

13901 (0x364D) 
</dt> <dt>



以發出連接的安全性準則進行的協商正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**\_IPSEC \_ IKE \_ 並存 \_ 隱藏錯誤**
</dt> <dd> <dl> <dt>

13902 (0x364E) 
</dt> <dt>



因為 IKEv1/AuthIP 並存隱藏了檢查，所以已刪除 SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**\_IPSEC \_ IKE \_ RATELIMIT \_ 捨棄錯誤**
</dt> <dd> <dl> <dt>

13903 (0x364F) 
</dt> <dt>



傳入的 SA 要求因為對等 IP 位址速率限制而被捨棄。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**\_IPSEC \_ IKE 對等錯誤不 \_ \_ \_ 支援 \_ MOBIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650) 
</dt> <dt>



對等不支援 MOBIKE。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**\_IPSEC \_ IKE \_ 授權 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

13905 (0x3651) 
</dt> <dt>



SA 建立未獲授權。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**\_IPSEC \_ IKE 強 \_ 式 \_ \_ 認證授權 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

13906 (0x3652) 
</dt> <dt>



因為沒有足夠強式的 PKINIT 認證，所以未授權建立 SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**\_IPSEC \_ IKE \_ 授權 \_ 失敗 \_ 並 \_ 選擇性 \_ 重試錯誤**
</dt> <dd> <dl> <dt>

13907 (0x3653) 
</dt> <dt>



SA 建立未獲授權。 您可能需要輸入更新或不同的認證，例如智慧卡。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**\_IPSEC \_ IKE 強 \_ 式 \_ \_ 認證授權 \_ 和 \_ CERTMAP \_ 失敗的錯誤**
</dt> <dd> <dl> <dt>

13908 (0x3654) 
</dt> <dt>



因為沒有足夠強式的 PKINIT 認證，所以未授權建立 SA。 這可能與 SA 的憑證對帳戶對應失敗相關。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 延伸 \_ 結束時發生錯誤**
</dt> <dd> <dl> <dt>

13909 (0x3655) 
</dt> <dt>



\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 延伸 \_ 結束時發生錯誤


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**\_IPSEC 錯誤 \_ \_ SPI 錯誤**
</dt> <dd> <dl> <dt>

13910 (0x3656) 
</dt> <dt>



封包中的 SPI 不符合有效的 IPsec SA。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**\_IPSEC \_ SA \_ 存留期已 \_ 過期時發生錯誤**
</dt> <dd> <dl> <dt>

13911 (0x3657) 
</dt> <dt>



已在存留期過期的 IPsec SA 上收到封包。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**\_IPSEC 錯誤 \_ 的 \_ SA 錯誤**
</dt> <dd> <dl> <dt>

13912 (0x3658) 
</dt> <dt>



IPsec SA 接收到的封包不符合封包特性。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**\_IPSEC 重新 \_ 執行 \_ 檢查 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13913 (0x3659) 
</dt> <dt>



封包序號重新執行檢查失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**\_IPSEC 不正確封 \_ \_ 包錯誤**
</dt> <dd> <dl> <dt>

13914 (0x365A) 
</dt> <dt>



封包中的 IPsec 標頭和/或結尾無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**\_IPSEC \_ 完整性 \_ 檢查 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

13915 (0x365B) 
</dt> <dt>



IPsec 完整性檢查失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**錯誤 \_ IPSEC \_ 純 \_ 文本 \_ 捨棄**
</dt> <dd> <dl> <dt>

13916 (0x365C) 
</dt> <dt>



IPsec 卸載了純文字封包。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**\_IPSEC \_ 驗證 \_ 防火牆 \_ 捨棄錯誤**
</dt> <dd> <dl> <dt>

13917 (0x365D) 
</dt> <dt>



IPsec 會以已驗證的防火牆模式卸載傳入的 ESP 封包。 這項捨棄是良性的。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**\_IPSEC \_ 節流 \_ 下降錯誤**
</dt> <dd> <dl> <dt>

13918 (0x365E) 
</dt> <dt>



IPsec 因 DoS 節流而捨棄封包。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**\_IPSEC \_ DOSP \_ 封鎖錯誤**
</dt> <dd> <dl> <dt>

13925 (0x3665) 
</dt> <dt>



IPsec DoS 保護符合明確封鎖規則。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**\_IPSEC \_ DOSP \_ 收到 \_ 多播錯誤**
</dt> <dd> <dl> <dt>

13926 (0x3666) 
</dt> <dt>



IPsec DoS 保護收到 IPsec 專屬的多播封包，但這是不允許的。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**\_IPSEC DOSP 不正確封 \_ \_ 包時發生錯誤 \_**
</dt> <dd> <dl> <dt>

13927 (0x3667) 
</dt> <dt>



IPsec DoS 保護收到格式不正確的封包。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**錯誤 \_ IPSEC \_ DOSP \_ 狀態 \_ 查閱 \_ 失敗**
</dt> <dd> <dl> <dt>

13928 (0x3668) 
</dt> <dt>



IPsec DoS 保護無法查閱狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**\_IPSEC \_ DOSP 的 \_ 專案數上限 \_ 錯誤**
</dt> <dd> <dl> <dt>

13929 (0x3669) 
</dt> <dt>



IPsec DoS 保護無法建立狀態，因為已達到原則允許的最大專案數。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**錯誤 \_ IPSEC \_ DOSP \_ KEYMOD \_ 不 \_ 允許**
</dt> <dd> <dl> <dt>

13930 (0x366A) 
</dt> <dt>



IPsec DoS 保護收到「金鑰」模組的 IPsec 協商封包，但原則不允許此封包。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**\_ \_ \_ 未安裝 IPSEC DOSP \_ 錯誤**
</dt> <dd> <dl> <dt>

13931 (0x366B) 
</dt> <dt>



尚未啟用 IPsec DoS 保護。


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**\_IPSEC \_ DOSP \_ \_ 每個 \_ IP \_ RATELIMIT \_ 佇列的最大錯誤數**
</dt> <dd> <dl> <dt>

13932 (0x366C) 
</dt> <dt>



IPsec DoS 保護無法建立每個內部 IP 速率限制佇列，因為已達到原則允許的最大佇列數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 區段**
</dt> <dd> <dl> <dt>

14000 (0x36B0) 
</dt> <dt>



要求的區段不存在於啟用內容中。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**錯誤 \_ SXS 無法進行 \_ \_ GEN \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1) 
</dt> <dt>



應用程式無法啟動，因為其並存設定不正確。 如需詳細資訊，請參閱應用程式事件記錄檔或使用命令列 sxstrace.exe 工具。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**錯誤 \_ SXS \_ 不正確 \_ ACTCTXDATA \_ 格式**
</dt> <dd> <dl> <dt>

14002 (0x36B2) 
</dt> <dt>



應用程式系結資料格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 元件**
</dt> <dd> <dl> <dt>

14003 (0x36B3) 
</dt> <dt>



未在您的系統上安裝參考的元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 格式 \_ 錯誤**
</dt> <dd> <dl> <dt>

14004 (0x36B4) 
</dt> <dt>



資訊清單檔案的開頭不是必要的標記和格式資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 剖析 \_ 錯誤**
</dt> <dd> <dl> <dt>

14005 (0x36B5) 
</dt> <dt>



資訊清單檔案包含一或多個語法錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**錯誤 \_ SXS \_ 啟用 \_ 內容 \_ 已停用**
</dt> <dd> <dl> <dt>

14006 (0x36B6) 
</dt> <dt>



應用程式嘗試啟用已停用的啟用內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 索引鍵**
</dt> <dd> <dl> <dt>

14007 (0x36B7) 
</dt> <dt>



在任何使用中的啟用內容中找不到要求的查閱索引鍵。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**錯誤 \_ SXS \_ 版本 \_ 衝突**
</dt> <dd> <dl> <dt>

14008 (0x36B8) 
</dt> <dt>



應用程式所需的元件版本與另一個已在使用中的元件版本發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**錯誤 \_ SXS 錯誤的 \_ \_ 區段 \_ 類型**
</dt> <dd> <dl> <dt>

14009 (0x36B9) 
</dt> <dt>



要求的啟用內容區段類型與使用的查詢 API 不符。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**\_停用錯誤 SXS \_ 執行緒 \_ 查詢 \_**
</dt> <dd> <dl> <dt>

14010 (0x36BA) 
</dt> <dt>



缺少系統資源必須針對目前執行中的執行緒停用隔離啟用。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**\_ \_ 已設定錯誤 SXS 進程 \_ 預設值 \_ \_**
</dt> <dd> <dl> <dt>

14011 (0x36BB) 
</dt> <dt>



嘗試設定進程預設啟用內容失敗，因為已設定進程預設啟用內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**錯誤 \_ SXS \_ 未知的 \_ 編碼 \_ 群組**
</dt> <dd> <dl> <dt>

14012 (0x36BC) 
</dt> <dt>



無法辨識指定的編碼群組識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**錯誤 \_ SXS \_ 未知的 \_ 編碼**
</dt> <dd> <dl> <dt>

14013 (0x36BD) 
</dt> <dt>



無法辨識要求的編碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**錯誤 \_ SXS \_ 不正確 \_ XML \_ 命名空間 \_ URI**
</dt> <dd> <dl> <dt>

14014 (0x36BE) 
</dt> <dt>



資訊清單包含無效 URI 的參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**\_ \_ \_ \_ \_ 未 \_ 安裝錯誤 SXS 根資訊清單相依性**
</dt> <dd> <dl> <dt>

14015 (0x36BF) 
</dt> <dt>



應用程式資訊清單包含未安裝之相依元件的參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**\_未安裝錯誤 SXS 分 \_ 葉 \_ 資訊清單 \_ \_ \_ 相依性**
</dt> <dd> <dl> <dt>

14016 (0x36C0) 
</dt> <dt>



應用程式所使用之元件的資訊清單具有未安裝之相依元件的參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**錯誤 \_ SXS \_ 不正確 \_ 元件 \_ 標識 \_ 屬性**
</dt> <dd> <dl> <dt>

14017 (0x36C1) 
</dt> <dt>



資訊清單包含不正確元件身分識別的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 遺失 \_ 必要的 \_ 預設 \_ 命名空間**
</dt> <dd> <dl> <dt>

14018 (0x36C2) 
</dt> <dt>



資訊清單遺漏 assembly 元素上所需的預設命名空間規格。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 不正確 \_ 必要 \_ 預設 \_ 命名空間**
</dt> <dd> <dl> <dt>

14019 (0x36C3) 
</dt> <dt>



資訊清單具有元件元素上指定的預設命名空間，但其值不是 "urn：架構-microsoft-com： asm. v1"。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**錯誤 \_ SXS \_ 私 \_ 用資訊清單 \_ \_ 與重新 \_ \_ 剖析點之間的交互路徑 \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4) 
</dt> <dt>



私用資訊清單探查已跨越具有不支援之重新分析點的路徑。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**錯誤 \_ SXS \_ 重複 \_ DLL \_ 名稱**
</dt> <dd> <dl> <dt>

14021 (0x36C5) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同名稱的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**錯誤 \_ SXS \_ 重複 \_ WINDOWCLASS \_ 名稱**
</dt> <dd> <dl> <dt>

14022 (0x36C6) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同名稱的視窗類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**錯誤 \_ SXS \_ 重複 \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM 伺服器 Clsid。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**錯誤 \_ SXS \_ 重複 \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同 COM 介面 Iid 的 proxy。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**錯誤 \_ SXS \_ 重複 \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM 類型程式庫 TLBIDs。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**錯誤 \_ SXS \_ 重複 \_ PROGID**
</dt> <dd> <dl> <dt>

14026 (0x36CA) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM Progid。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**錯誤 \_ SXS \_ 重複的 \_ 元件 \_ 名稱**
</dt> <dd> <dl> <dt>

14027 (0x36CB) 
</dt> <dt>



應用程式資訊清單直接或間接參考的兩個或多個元件，是相同元件的不同版本，這是不允許的。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**錯誤 \_ SXS \_ 檔案 \_ 雜湊 \_ 不符**
</dt> <dd> <dl> <dt>

14028 (0x36CC) 
</dt> <dt>



元件的檔案不符合元件資訊清單中出現的驗證資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**錯誤 \_ SXS \_ 原則 \_ 剖析 \_ 錯誤**
</dt> <dd> <dl> <dt>

14029 (0x36CD) 
</dt> <dt>



原則資訊清單包含一或多個語法錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE) 
</dt> <dt>



資訊清單剖析錯誤：必須是字串常值，但找不到任何左引號字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**錯誤 \_ SXS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF) 
</dt> <dt>



資訊清單剖析錯誤：批註中使用的語法不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0) 
</dt> <dt>



資訊清單剖析錯誤：名稱是以不正確字元開頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1) 
</dt> <dt>



資訊清單剖析錯誤：名稱包含不正確字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2) 
</dt> <dt>



資訊清單剖析錯誤：字串常值包含不正確字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**錯誤 \_ SXS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3) 
</dt> <dt>



資訊清單剖析錯誤： xml 宣告的語法無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4) 
</dt> <dt>



資訊清單剖析錯誤：在文字內容中找到不正確字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5) 
</dt> <dt>



資訊清單剖析錯誤：缺少必要的空白字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**錯誤 \_ SXS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6) 
</dt> <dt>



資訊清單剖析錯誤：必須是 ' > ' 字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7) 
</dt> <dt>



資訊清單剖析錯誤：必須是分號字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8) 
</dt> <dt>



資訊清單剖析錯誤：不對稱的括弧。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**錯誤 \_ SXS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9) 
</dt> <dt>



資訊清單剖析錯誤：內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**錯誤 \_ SXS \_ XML \_ E 非 \_ 預期的 \_ 空格**
</dt> <dd> <dl> <dt>

14042 (0x36DA) 
</dt> <dt>



資訊清單剖析錯誤：此位置不允許空白字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**錯誤 \_ SXS \_ XML \_ 電子 \_ 未完成 \_ 編碼**
</dt> <dd> <dl> <dt>

14043 (0x36DB) 
</dt> <dt>



資訊清單剖析錯誤：以不正確狀態結束目前編碼的檔案結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**錯誤 \_ SXS \_ XML \_ E \_ 遺失 \_ 括弧**
</dt> <dd> <dl> <dt>

14044 (0x36DC) 
</dt> <dt>



資訊清單剖析錯誤：遺漏括弧。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**錯誤 \_ SXS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD) 
</dt> <dt>



資訊清單剖析錯誤：遺漏單引號或雙右引號字元 (\\ ' 或 \\ ") 。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**錯誤 \_ SXS \_ XML \_ E \_ 多個 \_ 冒號**
</dt> <dd> <dl> <dt>

14046 (0x36DE) 
</dt> <dt>



資訊清單剖析錯誤：名稱中不允許多個冒號。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ DECIMAL**
</dt> <dd> <dl> <dt>

14047 (0x36DF) 
</dt> <dt>



資訊清單剖析錯誤：十進位數的字元無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ 十六進位**
</dt> <dd> <dl> <dt>

14048 (0x36E0) 
</dt> <dt>



資訊清單剖析錯誤：十六進位數位的字元無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ UNICODE**
</dt> <dd> <dl> <dt>

14049 (0x36E1) 
</dt> <dt>



資訊清單剖析錯誤：此平臺的 unicode 字元值無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**錯誤 \_ SXS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2) 
</dt> <dt>



資訊清單剖析錯誤：應為空白或 '？ '。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3) 
</dt> <dt>



資訊清單剖析錯誤：這個位置不應該有結束標記。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4) 
</dt> <dt>



資訊清單剖析錯誤：下列標記未關閉： %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**錯誤 \_ SXS \_ XML \_ E \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5) 
</dt> <dt>



資訊清單剖析錯誤：重複的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**錯誤 \_ SXS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6) 
</dt> <dt>



資訊清單剖析錯誤： XML 檔中只允許一個最上層元素。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7) 
</dt> <dt>



資訊清單剖析錯誤：在檔的最上層無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8) 
</dt> <dt>



資訊清單剖析錯誤：不正確 xml 宣告。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9) 
</dt> <dt>



資訊清單剖析錯誤： XML 檔必須有最上層元素。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA) 
</dt> <dt>



資訊清單剖析錯誤：非預期的檔案結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB) 
</dt> <dt>



資訊清單剖析錯誤：參數實體不能用在內部子集的標記宣告內。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC) 
</dt> <dt>



資訊清單剖析錯誤：元素未關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED) 
</dt> <dt>



資訊清單剖析錯誤： End 元素遺漏 ' > ' 字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE) 
</dt> <dt>



資訊清單剖析錯誤：字串常值未關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF) 
</dt> <dt>



資訊清單剖析錯誤：批註尚未關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0) 
</dt> <dt>



資訊清單剖析錯誤：宣告未關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1) 
</dt> <dt>



資訊清單剖析錯誤： CDATA 區段未關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**錯誤 \_ SXS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2) 
</dt> <dt>



資訊清單剖析錯誤：命名空間前置詞不能以保留字元串 "xml" 開頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3) 
</dt> <dt>



資訊清單剖析錯誤：系統不支援指定的編碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4) 
</dt> <dt>



資訊清單剖析錯誤：不支援從目前的編碼切換為指定的編碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5) 
</dt> <dt>



資訊清單剖析錯誤：名稱 ' xml ' 是保留的，而且必須是小寫。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**錯誤 \_ SXS \_ XML \_ E \_ \_ 獨立無效**
</dt> <dd> <dl> <dt>

14070 (0x36F6) 
</dt> <dt>



資訊清單剖析錯誤：獨立屬性的值必須為 ' yes ' 或 ' no '。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**錯誤 \_ SXS \_ XML \_ 電子非 \_ 預期的 \_ 獨立**
</dt> <dd> <dl> <dt>

14071 (0x36F7) 
</dt> <dt>



資訊清單剖析錯誤：獨立屬性不能用在外部實體中。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ 版本**
</dt> <dd> <dl> <dt>

14072 (0x36F8) 
</dt> <dt>



資訊清單剖析錯誤：版本號碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9) 
</dt> <dt>



資訊清單剖析錯誤：遺漏屬性與屬性值之間的等號。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**錯誤 \_ SXS \_ 保護 \_ 復原 \_ 失敗**
</dt> <dd> <dl> <dt>

14074 (0x36FA) 
</dt> <dt>



元件保護錯誤：無法復原指定的元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**錯誤 \_ SXS \_ 保護 \_ 的 \_ 公開金鑰 \_ 太 \_ 短**
</dt> <dd> <dl> <dt>

14075 (0x36FB) 
</dt> <dt>



元件保護錯誤：元件的公開金鑰太短而無法允許。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**錯誤 \_ SXS \_ 保護 \_ 類別 \_ 目錄 \_ 無效**
</dt> <dd> <dl> <dt>

14076 (0x36FC) 
</dt> <dt>



元件保護錯誤：元件的目錄無效，或不符合元件的資訊清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**錯誤 \_ SXS \_ 產生無法翻譯 \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36FD) 
</dt> <dt>



HRESULT 無法轉譯為對應的 Win32 錯誤碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**\_遺漏錯誤 SXS \_ 保護 \_ 類別目錄 \_ \_ 檔案**
</dt> <dd> <dl> <dt>

14078 (0x36FE) 
</dt> <dt>



元件保護錯誤：遺漏元件的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**錯誤 \_ SXS \_ 遺漏 \_ 元件 \_ 標識 \_ 屬性**
</dt> <dd> <dl> <dt>

14079 (0x36FF) 
</dt> <dt>



提供的元件識別缺少一或多個必須存在於此內容中的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**錯誤 \_ SXS \_ 不正確 \_ 元件 \_ 標識 \_ 屬性 \_ 名稱**
</dt> <dd> <dl> <dt>

14080 (0x3700) 
</dt> <dt>



提供的元件識別有一或多個屬性名稱包含 XML 名稱中不允許的字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**\_遺漏錯誤 SXS \_ 元件 \_**
</dt> <dd> <dl> <dt>

14081 (0x3701) 
</dt> <dt>



找不到參考的元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**錯誤 \_ SXS \_ 已損毀 \_ 啟用 \_ 堆疊**
</dt> <dd> <dl> <dt>

14082 (0x3702) 
</dt> <dt>



執行中線程的啟用內容啟用堆疊已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**錯誤 \_ SXS \_ 損毀**
</dt> <dd> <dl> <dt>

14083 (0x3703) 
</dt> <dt>



此進程或執行緒的應用程式隔離中繼資料已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**錯誤 \_ SXS \_ 早期 \_ 停用**
</dt> <dd> <dl> <dt>

14084 (0x3704) 
</dt> <dt>



正在停用的啟用內容不是最近啟用的內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**錯誤 \_ SXS \_ 不正確 \_ 停用**
</dt> <dd> <dl> <dt>

14085 (0x3705) 
</dt> <dt>



目前執行中的執行緒不會使用已停用的啟用內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**錯誤 \_ SXS \_ 多次 \_ 停用**
</dt> <dd> <dl> <dt>

14086 (0x3706) 
</dt> <dt>



正在停用的啟用內容已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**要求的錯誤 \_ SXS \_ 進程 \_ 終止 \_**
</dt> <dd> <dl> <dt>

14087 (0x3707) 
</dt> <dt>



隔離設備所使用的元件已要求終止進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**錯誤 \_ SXS \_ 發行 \_ 啟用 \_ 內容**
</dt> <dd> <dl> <dt>

14088 (0x3708) 
</dt> <dt>



核心模式元件正在釋放啟用內容的參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**錯誤 \_ SXS \_ 系統 \_ 預設 \_ 啟用 \_ 內容 \_ 空白**
</dt> <dd> <dl> <dt>

14089 (0x3709) 
</dt> <dt>



無法產生系統預設元件的啟用內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**錯誤 \_ SXS \_ 不正確 \_ 識別 \_ 屬性 \_ 值**
</dt> <dd> <dl> <dt>

14090 (0x370A) 
</dt> <dt>



身分識別中的屬性值不在合法範圍內。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**錯誤 \_ SXS \_ 不正確 \_ 識別 \_ 屬性 \_ 名稱**
</dt> <dd> <dl> <dt>

14091 (0x370B) 
</dt> <dt>



身分識別中的屬性名稱不在合法範圍內。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**錯誤 \_ SXS \_ 識別 \_ 重複 \_ 屬性**
</dt> <dd> <dl> <dt>

14092 (0x370C) 
</dt> <dt>



身分識別包含相同屬性的兩個定義。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**錯誤 \_ SXS 身分 \_ 識別 \_ 剖析 \_ 錯誤**
</dt> <dd> <dl> <dt>

14093 (0x370D) 
</dt> <dt>



識別字串的格式不正確。 這可能是因為尾端逗號、兩個未命名屬性、遺漏屬性名稱或遺漏屬性值所致。


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**錯誤 \_ 的 \_ 替代 \_ 字串格式錯誤**
</dt> <dd> <dl> <dt>

14094 (0x370E) 
</dt> <dt>



包含當地語系化的替換內容的字串格式不正確。 貨幣符號 ($) 後面接著左括弧以外的某個字元，或找不到其他貨幣符號或替換的右括弧。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**錯誤 \_ SXS \_ 不正確的 \_ 公開金鑰 \_ \_ TOKEN**
</dt> <dd> <dl> <dt>

14095 (0x370F) 
</dt> <dt>



公開金鑰標記未對應到指定的公開金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**未對應的 \_ \_ 替代 \_ 字串時發生錯誤**
</dt> <dd> <dl> <dt>

14096 (0x3710) 
</dt> <dt>



替代字串沒有對應。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**錯誤 \_ SXS \_ 元件 \_ 未 \_ 鎖定**
</dt> <dd> <dl> <dt>

14097 (0x3711) 
</dt> <dt>



在提出要求之前，必須先鎖定元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**錯誤 \_ SXS \_ 元件 \_ 存放區 \_ 已損毀**
</dt> <dd> <dl> <dt>

14098 (0x3712) 
</dt> <dt>



元件存放區已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**錯誤 \_ ADVANCED \_ INSTALLER \_ 失敗**
</dt> <dd> <dl> <dt>

14099 (0x3713) 
</dt> <dt>



在安裝或服務期間，advanced installer 失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**錯誤 \_ XML \_ 編碼 \_ 不相符**
</dt> <dd> <dl> <dt>

14100 (0x3714) 
</dt> <dt>



XML 宣告中的字元編碼與檔中使用的編碼不相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 識別 \_ 相同 \_ 但 \_ 內容 \_ 不同**
</dt> <dd> <dl> <dt>

14101 (0x3715) 
</dt> <dt>



資訊清單的身分識別完全相同，但其內容不同。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**錯誤 \_ SXS 身分識別 \_ \_ 不同**
</dt> <dd> <dl> <dt>

14102 (0x3716) 
</dt> <dt>



元件身分識別不同。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**錯誤 \_ SXS \_ 元件 \_ \_ 不是 \_ \_ 部署**
</dt> <dd> <dl> <dt>

14103 (0x3717) 
</dt> <dt>



元件不是部署。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**錯誤 \_ SXS \_ 檔案 \_ 不 \_ \_ 是元件的一部分 \_**
</dt> <dd> <dl> <dt>

14104 (0x3718) 
</dt> <dt>



檔案不是元件的一部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

14105 (0x3719) 
</dt> <dt>



資訊清單的大小超過允許的最大值。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**\_ \_ \_ 未註冊錯誤 SXS \_ 設定**
</dt> <dd> <dl> <dt>

14106 (0x371A) 
</dt> <dt>



設定未註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**錯誤 \_ SXS \_ 交易 \_ 關閉 \_ 未完成**
</dt> <dd> <dl> <dt>

14107 (0x371B) 
</dt> <dt>



一或多個必要的交易成員不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**錯誤的 \_ SMI-S \_ 基本 \_ 安裝程式 \_ 失敗**
</dt> <dd> <dl> <dt>

14108 (0x371C) 
</dt> <dt>



在安裝或服務期間，SMI-S 基本安裝程式失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**錯誤 \_ 一般 \_ 命令 \_ 失敗**
</dt> <dd> <dl> <dt>

14109 (0x371D) 
</dt> <dt>



泛型命令可執行檔傳回指出失敗的結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**錯誤 \_ SXS \_ 檔案 \_ 雜湊 \_ 遺失**
</dt> <dd> <dl> <dt>

14110 (0x371E) 
</dt> <dt>



元件的資訊清單中遺漏檔案驗證資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 路徑**
</dt> <dd> <dl> <dt>

15000 (0x3A98) 
</dt> <dt>



指定的通道路徑無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**錯誤 \_ .EVT \_ 不正確 \_ 查詢**
</dt> <dd> <dl> <dt>

15001 (0x3A99) 
</dt> <dt>



指定的查詢無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**\_ \_ \_ \_ 找不到簽發者中繼資料 \_ 的錯誤**
</dt> <dd> <dl> <dt>

15002 (0x3A9A) 
</dt> <dt>



在資源中找不到發行者中繼資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件範本**
</dt> <dd> <dl> <dt>

15003 (0x3A9B) 
</dt> <dt>



資源 (錯誤 = %1) 中找不到事件定義的範本。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 名稱**
</dt> <dd> <dl> <dt>

15004 (0x3A9C) 
</dt> <dt>



指定的發行者名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**錯誤 \_ .EVT \_ 不正確 \_ 事件 \_ 資料**
</dt> <dd> <dl> <dt>

15005 (0x3A9D) 
</dt> <dt>



發行者所引發的事件資料與發行者資訊清單中的事件範本定義不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 頻道**
</dt> <dd> <dl> <dt>

15007 (0x3A9F) 
</dt> <dt>



找不到指定的通道。 檢查通道設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**錯誤 \_ .EVT \_ 格式不正確的 \_ XML \_ 文字**
</dt> <dd> <dl> <dt>

15008 (0x3AA0) 
</dt> <dt>



指定的 xml 文字格式不正確。 如需詳細資訊，請參閱擴充錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ \_ 對 \_ 直接 \_ 通道的錯誤 .EVT 訂用帳戶**
</dt> <dd> <dl> <dt>

15009 (0x3AA1) 
</dt> <dt>



呼叫端嘗試訂閱不允許的直接通道。 直接通道的事件會直接移至記錄檔，而且無法訂閱。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**錯誤 \_ .EVT \_ 設定 \_ 錯誤**
</dt> <dd> <dl> <dt>

15010 (0x3AA2) 
</dt> <dt>



組態錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 過時**
</dt> <dd> <dl> <dt>

15011 (0x3AA3) 
</dt> <dt>



查詢結果過時/無效。 這可能是因為在建立查詢結果之後清除或變換記錄所致。 使用者應藉由釋出查詢結果物件並重新發出查詢，來處理此程式碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 不正確 \_ 位置**
</dt> <dd> <dl> <dt>

15012 (0x3AA4) 
</dt> <dt>



查詢結果目前的位置無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**錯誤 \_ .EVT \_ 非 \_ 驗證 \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5) 
</dt> <dt>



註冊的 MSXML 不支援驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**錯誤 \_ .EVT \_ 篩選 \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6) 
</dt> <dt>



如果運算式本身評估為節點集，且不屬於範圍作業的一些其他變更，則運算式只能在範圍作業的變更之後接著變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**錯誤 \_ .EVT \_ 篩選 \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7) 
</dt> <dt>



無法從不代表元素集的詞彙執行步驟作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8) 
</dt> <dt>



二元運算子的左邊引數必須是屬性、節點或變數，且右邊引數必須是常數。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9) 
</dt> <dt>



步驟作業必須牽涉到節點測試，或者，如果是述詞，則會評估第一個節點集合所識別之節點集內每個節點的代數運算式。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTYPE .。。**
</dt> <dd> <dl> <dt>

15018 (0x3AAA) 
</dt> <dt>



目前不支援此資料類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**錯誤 \_ .EVT \_ 篩選 \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB) 
</dt> <dt>



位置 %1！ d！發生語法錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC) 
</dt> <dt>



此篩選準則的執行不支援這個運算子。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD) 
</dt> <dt>



發現未預期的權杖。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**錯誤 \_ .EVT \_ \_ 啟用的 \_ \_ \_ 直接 \_ 通道上有不正確操作**
</dt> <dd> <dl> <dt>

15022 (0x3AAE) 
</dt> <dt>



要求的作業無法在啟用的直接通道上執行。 必須先停用通道，才能執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 屬性 \_ 值**
</dt> <dd> <dl> <dt>

15023 (0x3AAF) 
</dt> <dt>



通道屬性 %1！ s！ 包含不正確值。 值的類型無效、不在有效範圍內、無法更新，或不支援此類型的通道。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 屬性 \_ 值**
</dt> <dd> <dl> <dt>

15024 (0x3AB0) 
</dt> <dt>



發行者屬性 %1！ s！ 包含不正確值。 值的類型無效、不在有效範圍內、無法更新，或是此類型的發行者不支援此值。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**錯誤 \_ .EVT \_ 通道 \_ 無法 \_ 啟動**
</dt> <dd> <dl> <dt>

15025 (0x3AB1) 
</dt> <dt>



通道無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**錯誤 \_ .EVT \_ 篩選 \_ 太 \_ 複雜**
</dt> <dd> <dl> <dt>

15026 (0x3AB2) 
</dt> <dt>



Xpath 運算式超過支援的複雜度。 請 symplify 它，或將它分割成兩個或更簡單的運算式。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 訊息**
</dt> <dd> <dl> <dt>

15027 (0x3AB3) 
</dt> <dt>



訊息資源存在，但在字串/訊息資料表中找不到訊息。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息識別碼**
</dt> <dd> <dl> <dt>

15028 (0x3AB4) 
</dt> <dt>



找不到所需訊息的訊息識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 值 \_ 插入**
</dt> <dd> <dl> <dt>

15029 (0x3AB5) 
</dt> <dt>



找不到插入索引 (% 1) 的替代字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 參數 \_ 插入**
</dt> <dd> <dl> <dt>

15030 (0x3AB6) 
</dt> <dt>



找不到參數參考 (% 1) 的描述字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**已 \_ 達到錯誤的 .EVT \_ 最大 \_ 插入 \_ 數**
</dt> <dd> <dl> <dt>

15031 (0x3AB7) 
</dt> <dt>



已達到最大取代數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件定義**
</dt> <dd> <dl> <dt>

15032 (0x3AB8) 
</dt> <dt>



找不到事件識別碼 (% 1) 的事件定義。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息地區設定**
</dt> <dd> <dl> <dt>

15033 (0x3AB9) 
</dt> <dt>



所需訊息的地區設定特定資源不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**錯誤的 \_ .EVT \_ 版本 \_ 太 \_ 舊**
</dt> <dd> <dl> <dt>

15034 (0x3ABA) 
</dt> <dt>



資源太舊而無法相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**錯誤 \_ .EVT \_ 版本 \_ 太 \_ 新**
</dt> <dd> <dl> <dt>

15035 (0x3ABB) 
</dt> <dt>



資源太新，無法相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**錯誤 \_ .EVT \_ 無法 \_ 開啟 \_ \_ 查詢通道 \_**
</dt> <dd> <dl> <dt>

15036 (0x3ABC) 
</dt> <dt>



位於索引 %1！ d！的通道 無法開啟查詢。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**錯誤的 \_ .EVT \_ 發行者 \_ 已停用**
</dt> <dd> <dl> <dt>

15037 (0x3ABD) 
</dt> <dt>



發行者已停用，且其資源無法使用。 當發行者正在卸載或升級時，通常就會發生這種情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**錯誤 \_ .EVT \_ 篩選 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

15038 (0x3ABE) 
</dt> <dt>



嘗試建立的數數值型別超出其有效範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**\_ \_ \_ 無法啟動錯誤 EC 訂用帳戶 \_**
</dt> <dd> <dl> <dt>

15080 (0x3AE8) 
</dt> <dt>



訂用帳戶無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**錯誤 \_ EC \_ 記錄檔 \_ 已停用**
</dt> <dd> <dl> <dt>

15081 (0x3AE9) 
</dt> <dt>



訂用帳戶的記錄處於停用狀態，無法用來將事件轉寄至。 必須先啟用記錄檔，才能啟用訂閱。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**錯誤 \_ EC \_ 迴圈 \_ 轉送**
</dt> <dd> <dl> <dt>

15082 (0x3AEA) 
</dt> <dt>



從本機電腦轉送事件到本身時，訂閱的查詢不能包含訂用帳戶的目標記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**錯誤 \_ EC \_ CREDSTORE \_ FULL**
</dt> <dd> <dl> <dt>

15083 (0x3AEB) 
</dt> <dt>



用來儲存認證的認證存放區已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 EC 認證**
</dt> <dd> <dl> <dt>

15084 (0x3AEC) 
</dt> <dt>



在認證存放區中找不到此訂用帳戶所使用的認證。


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**錯誤 \_ EC 沒有作用中的 \_ \_ \_ 通道**
</dt> <dd> <dl> <dt>

15085 (0x3AED) 
</dt> <dt>



找不到查詢的作用中通道。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 MUI 檔案**
</dt> <dd> <dl> <dt>

15100 (0x3AFC) 
</dt> <dt>



資源載入器找不到 MUI 檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**錯誤 \_ MUI \_ 不正確檔案 \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD) 
</dt> <dt>



資源載入器無法載入 MUI 檔案，因為檔案無法通過驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**錯誤 \_ MUI \_ 不正確 \_ RC \_ 設定**
</dt> <dd> <dl> <dt>

15102 (0x3AFE) 
</dt> <dt>



RC 資訊清單損毀，發生垃圾資料或不受支援的版本，或遺漏必要專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**錯誤 \_ MUI \_ 不正確 \_ 地區設定 \_ 名稱**
</dt> <dd> <dl> <dt>

15103 (0x3AFF) 
</dt> <dt>



RC 資訊清單具有不正確文化特性名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**錯誤 \_ MUI \_ 不正確 \_ ULTIMATEFALLBACK \_ 名稱**
</dt> <dd> <dl> <dt>

15104 (0x3B00) 
</dt> <dt>



RC 資訊清單有不正確 ultimatefallback 名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**\_ \_ \_ 未載入錯誤 MUI \_ 檔案**
</dt> <dd> <dl> <dt>

15105 (0x3B01) 
</dt> <dt>



資源載入器快取沒有載入的 MUI 專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**錯誤 \_ 資源 \_ 列舉 \_ 使用者 \_ 停止**
</dt> <dd> <dl> <dt>

15106 (0x3B02) 
</dt> <dt>



使用者已停止資源列舉。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**錯誤 \_ MUI \_ INTLSETTINGS \_ UILANG \_ 未 \_ 安裝**
</dt> <dd> <dl> <dt>

15107 (0x3B03) 
</dt> <dt>



UI 語言安裝失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**錯誤 \_ MUI \_ INTLSETTINGS \_ 不正確 \_ 地區設定 \_ 名稱**
</dt> <dd> <dl> <dt>

15108 (0x3B04) 
</dt> <dt>



地區設定安裝失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**\_MRM \_ 執行時間 \_ 沒有 \_ 預設 \_ 或 \_ 中立的 \_ 資源時發生錯誤**
</dt> <dd> <dl> <dt>

15110 (0x3B06) 
</dt> <dt>



資源沒有預設值或中性值。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**\_MRM \_ 不正確 \_ PRICONFIG.DEFAULT.XML 時發生錯誤**
</dt> <dd> <dl> <dt>

15111 (0x3B07) 
</dt> <dt>



不正確 PRI 設定檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**\_MRM \_ 不正確 \_ 檔 \_ 類型時發生錯誤**
</dt> <dd> <dl> <dt>

15112 (0x3B08) 
</dt> <dt>



不正確檔案類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**\_MRM \_ 未知 \_ 限定詞時發生錯誤**
</dt> <dd> <dl> <dt>

15113 (0x3B09) 
</dt> <dt>



未知的辨識符號。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**\_MRM 不正確辨識 \_ \_ 符號 \_ 值時發生錯誤**
</dt> <dd> <dl> <dt>

15114 (0x3B0A) 
</dt> <dt>



不正確辨識符號值。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**\_MRM \_ 沒有 \_ 候選的錯誤**
</dt> <dd> <dl> <dt>

15115 (0x3B0B) 
</dt> <dt>



找不到候選。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**\_MRM \_ 沒有 \_ 相符 \_ 或 \_ 預設 \_ 候選項時發生錯誤**
</dt> <dd> <dl> <dt>

15116 (0x3B0C) 
</dt> <dt>



Windows.applicationmodel.resources.core.resourcemap 或 NamedResource 的專案沒有預設或中立的資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**\_MRM \_ 資源 \_ 類型 \_ 不符時發生錯誤**
</dt> <dd> <dl> <dt>

15117 (0x3B0D) 
</dt> <dt>



不正確 ResourceCandidate 類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**\_MRM \_ 重複的 \_ 對應 \_ 名稱時發生錯誤**
</dt> <dd> <dl> <dt>

15118 (0x3B0E) 
</dt> <dt>



重複的資源對應。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**\_MRM \_ 重複 \_ 專案時發生錯誤**
</dt> <dd> <dl> <dt>

15119 (0x3B0F) 
</dt> <dt>



重複的專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**\_MRM \_ 不正確 \_ 資源 \_ 識別碼時發生錯誤**
</dt> <dd> <dl> <dt>

15120 (0x3B10) 
</dt> <dt>



資源識別碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**\_MRM \_ FILEPATH \_ 太 \_ 長時發生錯誤**
</dt> <dd> <dl> <dt>

15121 (0x3B11) 
</dt> <dt>



檔案路徑太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**\_MRM \_ 不支援的 \_ 目錄 \_ 類型時發生錯誤**
</dt> <dd> <dl> <dt>

15122 (0x3B12) 
</dt> <dt>



不支援的目錄類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**\_MRM \_ 不正確 \_ PRI \_ 檔案時發生錯誤**
</dt> <dd> <dl> <dt>

15126 (0x3B16) 
</dt> <dt>



不正確 PRI 檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**\_ \_ \_ \_ \_ 找不到名為資源的錯誤 MRM**
</dt> <dd> <dl> <dt>

15127 (0x3B17) 
</dt> <dt>



找不到 NamedResource。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ 找不到對應 \_ 的錯誤 MRM**
</dt> <dd> <dl> <dt>

15135 (0x3B1F) 
</dt> <dt>



找不到 Windows.applicationmodel.resources.core.resourcemap。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**\_MRM \_ 不支援的 \_ 設定檔 \_ 類型時發生錯誤**
</dt> <dd> <dl> <dt>

15136 (0x3B20) 
</dt> <dt>



不支援的 MRT.LOG 配置檔案類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**\_MRM 不正確辨識 \_ \_ 符號 \_ 運算子時發生錯誤**
</dt> <dd> <dl> <dt>

15137 (0x3B21) 
</dt> <dt>



不正確辨識符號運算子。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**\_MRM \_ 不定辨識 \_ 符號 \_ 值時發生錯誤**
</dt> <dd> <dl> <dt>

15138 (0x3B22) 
</dt> <dt>



無法判斷辨識符號值或辨識符號值尚未設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**\_MRM 自動 \_ 合併 \_ 已啟用時發生錯誤**
</dt> <dd> <dl> <dt>

15139 (0x3B23) 
</dt> <dt>



PRI 檔案中已啟用自動合併。


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**\_MRM \_ 太 \_ 多 \_ 資源時發生錯誤**
</dt> <dd> <dl> <dt>

15140 (0x3B24) 
</dt> <dt>



為封裝定義了太多資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**錯誤 \_ MCA \_ 不正確 \_ 功能 \_ 字串**
</dt> <dd> <dl> <dt>

15200 (0x3B60) 
</dt> <dt>



此監視器傳回的 DDC/CI 功能字串不符合存取權。匯流排3.0、DDC/CI 1.1 或 MCCS 2 修訂1規格。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**錯誤 \_ MCA \_ 不正確 \_ VCP \_ 版本**
</dt> <dd> <dl> <dt>

15201 (0x3B61) 
</dt> <dt>



監視器的 VCP 版本 (0xDF) VCP 程式碼傳回不正確版本值。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**錯誤 \_ MCA \_ 監視 \_ 違反 \_ MCCS \_ 規格**
</dt> <dd> <dl> <dt>

15202 (0x3B62) 
</dt> <dt>



此監視器不符合其宣稱支援的 MCCS 規格。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**錯誤 \_ MCA \_ MCCS \_ 版本 \_ 不符**
</dt> <dd> <dl> <dt>

15203 (0x3B63) 
</dt> <dt>



監視器的 mccs ver 功能中的 MCCS 版本，與 \_ 使用 VCP 版本 (0xDF) VCP 程式碼時，監視器所報告的 mccs 版本不符。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**\_MCA 錯誤 MCA \_ 不支援的 \_ MCCS \_ 版本**
</dt> <dd> <dl> <dt>

15204 (0x3B64) 
</dt> <dt>



監視器設定 API 僅適用于支援 MCCS 1.0 規格、MCCS 2.0 規格或 MCCS 2.0 修訂1規格的監視器。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**錯誤 \_ MCA \_ 內部 \_ 錯誤**
</dt> <dd> <dl> <dt>

15205 (0x3B65) 
</dt> <dt>



發生內部監視設定 API 錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**傳回的錯誤 \_ MCA \_ 無效 \_ 技術 \_ 類型 \_**
</dt> <dd> <dl> <dt>

15206 (0x3B66) 
</dt> <dt>



監視器傳回的監視器技術類型無效。 CRT、等離子和 LCD (TFT) 是監視器技術類型的範例。 此錯誤表示監視器違反了 MCCS 2.0 或 MCCS 2.0 修訂1規格。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**錯誤 \_ MCA \_ 不支援 \_ 色 \_ 溫度**
</dt> <dd> <dl> <dt>

15207 (0x3B67) 
</dt> <dt>



[**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)的呼叫者指定了目前監視器不支援的色溫。 此錯誤表示監視器違反了 MCCS 2.0 或 MCCS 2.0 修訂1規格。


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**錯誤不 \_ 明確的 \_ 系統 \_ 裝置**
</dt> <dd> <dl> <dt>

15250 (0x3B92) 
</dt> <dt>



無法識別要求的系統裝置，因為有多個不區分的裝置可能符合識別準則。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_ \_ \_ \_ 找不到錯誤系統裝置**
</dt> <dd> <dl> <dt>

15299 (0x3BC3) 
</dt> <dt>



找不到要求的系統裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_ \_ 不支援錯誤雜湊 \_**
</dt> <dd> <dl> <dt>

15300 (0x3BC4) 
</dt> <dt>



未在伺服器上啟用指定的雜湊版本與雜湊類型的雜湊產生。


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**錯誤 \_ 雜湊 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

15301 (0x3BC5) 
</dt> <dt>



從伺服器要求的雜湊無法使用或不再有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**錯誤 \_ 次要 \_ IC \_ 提供者 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

15321 (0x3BD9) 
</dt> <dt>



管理指定之中斷的次要中斷控制器實例並未註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**錯誤 \_ GPIO \_ 用戶端 \_ 資訊 \_ 無效**
</dt> <dd> <dl> <dt>

15322 (0x3BDA) 
</dt> <dt>



GPIO 用戶端驅動程式所提供的資訊無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**\_ \_ \_ 不支援錯誤 GPIO \_ 版本**
</dt> <dd> <dl> <dt>

15323 (0x3BDB) 
</dt> <dt>



不支援 GPIO 用戶端驅動程式所指定的版本。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**錯誤 \_ GPIO \_ 不正確 \_ 註冊封 \_ 包**
</dt> <dd> <dl> <dt>

15324 (0x3BDC) 
</dt> <dt>



GPIO 用戶端驅動程式所提供的註冊封包無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**錯誤 \_ GPIO \_ 操作已 \_ 拒絕**
</dt> <dd> <dl> <dt>

15325 (0x3BDD) 
</dt> <dt>



指定的控制碼不支援要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**錯誤 \_ GPIO \_ 不相容的 \_ 連接 \_ 模式**
</dt> <dd> <dl> <dt>

15326 (0x3BDE) 
</dt> <dt>



要求的連接模式與一或多個指定之 pin 的現有模式相衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**錯誤 \_ GPIO \_ 中斷 \_ 已取消 \_ 遮罩**
</dt> <dd> <dl> <dt>

15327 (0x3BDF) 
</dt> <dt>



要求取消遮罩的插斷不會被遮罩。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**錯誤 \_ 無法 \_ 切換 \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15400 (0x3C28) 
</dt> <dt>



要求的執行層級切換無法順利完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**錯誤 \_ 不正確 \_ RUNLEVEL \_ 設定**
</dt> <dd> <dl> <dt>

15401 (0x3C29) 
</dt> <dt>



服務具有不正確執行層級設定。 服務的執行層級不得高於其相依服務的執行層級。


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**錯誤 \_ RUNLEVEL \_ 切換 \_ 超時**
</dt> <dd> <dl> <dt>

15402 (0x3C2A) 
</dt> <dt>



要求的執行層級切換無法順利完成，因為一或多個服務將不會在指定的超時時間內停止或重新開機。


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_RUNLEVEL \_ 切換 \_ 代理程式 \_ 超時時發生錯誤**
</dt> <dd> <dl> <dt>

15403 (0x3C2B) 
</dt> <dt>



執行層級切換代理程式未在指定的超時時間內回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**錯誤 \_ RUNLEVEL \_ 切換 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

15404 (0x3C2C) 
</dt> <dt>



執行層級切換正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**錯誤 \_ 服務 \_ 失敗 \_ 自動啟動**
</dt> <dd> <dl> <dt>

15405 (0x3C2D) 
</dt> <dt>



在執行層級切換的服務啟動階段期間，有一或多項服務無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**\_COM \_ TASK \_ 停止 \_ 暫止時發生錯誤**
</dt> <dd> <dl> <dt>

15501 (0x3C8D) 
</dt> <dt>



因為工作需要更多時間才能關閉，所以無法立即完成工作停止要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**\_安裝 \_ 開啟 \_ 套件 \_ 失敗**
</dt> <dd> <dl> <dt>

15600 (0x3CF0) 
</dt> <dt>



無法開啟封裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**\_ \_ \_ 找不到安裝 \_ 套件的錯誤**
</dt> <dd> <dl> <dt>

15601 (0x3CF1) 
</dt> <dt>



找不到封裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**\_安裝 \_ 不正確 \_ 套件時發生錯誤**
</dt> <dd> <dl> <dt>

15602 (0x3CF2) 
</dt> <dt>



封裝資料無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**錯誤 \_ 安裝 \_ 解析相依性 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

15603 (0x3CF3) 
</dt> <dt>



封裝失敗的更新、相依性或衝突驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**\_ \_ \_ \_ 磁片 \_ 空間安裝錯誤**
</dt> <dd> <dl> <dt>

15604 (0x3CF4) 
</dt> <dt>



您的電腦上沒有足夠的磁碟空間。 請釋放一些空間，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**\_安裝 \_ 網路 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

15605 (0x3CF5) 
</dt> <dt>



下載您的產品時發生問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**\_安裝 \_ 註冊 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

15606 (0x3CF6) 
</dt> <dt>



無法註冊封裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**\_安裝取消 \_ 註冊 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

15607 (0x3CF7) 
</dt> <dt>



無法取消註冊封裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**\_安裝 \_ 取消時發生錯誤**
</dt> <dd> <dl> <dt>

15608 (0x3CF8) 
</dt> <dt>



使用者已取消安裝要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**\_安裝錯誤 \_ 失敗**
</dt> <dd> <dl> <dt>

15609 (0x3CF9) 
</dt> <dt>



安裝失敗。 請洽詢您的軟體廠商。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_移除錯誤 \_ 失敗**
</dt> <dd> <dl> <dt>

15610 (0x3CFA) 
</dt> <dt>



移除失敗。 請洽詢您的軟體廠商。


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**錯誤 \_ 封裝 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

15611 (0x3CFB) 
</dt> <dt>



提供的封裝已安裝，且已封鎖重新安裝套件。 請查看 AppXDeployment-Server 事件記錄檔，以取得詳細資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**錯誤 \_ 需要 \_ 補救**
</dt> <dd> <dl> <dt>

15612 (0x3CFC) 
</dt> <dt>



無法啟動應用程式。 請嘗試重新安裝應用程式以修正問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**錯誤 \_ 安裝 \_ 先決條件 \_ 失敗**
</dt> <dd> <dl> <dt>

15613 (0x3CFD) 
</dt> <dt>



無法滿足安裝的先決條件。


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**錯誤 \_ 套件存放 \_ 庫 \_ 損毀**
</dt> <dd> <dl> <dt>

15614 (0x3CFE) 
</dt> <dt>



套件存放庫已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**\_安裝 \_ 原則 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

15615 (0x3CFF) 
</dt> <dt>



若要安裝此應用程式，您需要 Windows 開發人員授權或啟用側載功能的系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_更新錯誤套件 \_**
</dt> <dd> <dl> <dt>

15616 (0x3D00) 
</dt> <dt>



應用程式目前正在更新，所以無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_ \_ 原則封鎖錯誤 \_ 部署 \_**
</dt> <dd> <dl> <dt>

15617 (0x3D01) 
</dt> <dt>



原則封鎖了封裝部署作業。 請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_ \_ 使用中的錯誤套件 \_**
</dt> <dd> <dl> <dt>

15618 (0x3D02) 
</dt> <dt>



無法安裝封裝，因為它修改的資源目前正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**錯誤 \_ 修復 \_ 檔案 \_ 已損毀**
</dt> <dd> <dl> <dt>

15619 (0x3D03) 
</dt> <dt>



無法復原封裝，因為復原所需的資料已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**錯誤的分段簽章 \_ 無效 \_ \_**
</dt> <dd> <dl> <dt>

15620 (0x3D04) 
</dt> <dt>



簽章無效。 若要在開發人員模式下註冊，Appxsignature.p7x. appxsignature.p7x 和 AppxBlockMap.xml 必須是有效的，否則不應該存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**\_刪除 \_ 現有的 \_ APPLICATIONDATA \_ 存放區 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

15621 (0x3D05) 
</dt> <dt>



刪除封裝先前現有的應用程式資料時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**\_安裝 \_ 套件 \_ 降級時發生錯誤**
</dt> <dd> <dl> <dt>

15622 (0x3D06) 
</dt> <dt>



無法安裝封裝，因為已安裝此套件的較高版本。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**錯誤 \_ 系統 \_ 需要 \_ 補救**
</dt> <dd> <dl> <dt>

15623 (0x3D07) 
</dt> <dt>



偵測到系統二進位檔中有錯誤。 請嘗試重新整理電腦以修正問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**錯誤 \_ APPX \_ 完整性 \_ 失敗 \_ CLR \_ NGEN**
</dt> <dd> <dl> <dt>

15624 (0x3D08) 
</dt> <dt>



在系統上偵測到損毀的 CLR NGEN 二進位檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**錯誤 \_ 復原 \_ 檔案 \_ 已損毀**
</dt> <dd> <dl> <dt>

15625 (0x3D09) 
</dt> <dt>



因為復原所需的資料已損毀，所以無法繼續操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**\_安裝 \_ 防火牆 \_ 服務 \_ 未 \_ 執行時發生錯誤**
</dt> <dd> <dl> <dt>

15626 (0x3D0A) 
</dt> <dt>



無法安裝封裝，因為 Windows 防火牆服務未執行。 啟用 Windows 防火牆服務，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL \_ 錯誤 \_ 沒有 \_ 套件**
</dt> <dd> <dl> <dt>

15700 (0x3D54) 
</dt> <dt>



進程沒有套件識別。


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**已損毀的 APPMODEL \_ 錯誤 \_ 套件 \_ 運行 \_ 時間**
</dt> <dd> <dl> <dt>

15701 (0x3D55) 
</dt> <dt>



封裝執行時間資訊已損毀。


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**已損毀的 APPMODEL \_ 錯誤 \_ 套件身分 \_ 識別 \_**
</dt> <dd> <dl> <dt>

15702 (0x3D56) 
</dt> <dt>



封裝身分識別已損毀。


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL \_ 錯誤 \_ 沒有 \_ 應用程式**
</dt> <dd> <dl> <dt>

15703 (0x3D57) 
</dt> <dt>



進程沒有應用程式識別。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**錯誤 \_ 狀態 \_ 載入 \_ 存放區 \_ 失敗**
</dt> <dd> <dl> <dt>

15800 (0x3DB8) 
</dt> <dt>



載入狀態存放區失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**錯誤 \_ 狀態 \_ 取得 \_ 版本 \_ 失敗**
</dt> <dd> <dl> <dt>

15801 (0x3DB9) 
</dt> <dt>



取得應用程式的狀態版本失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**錯誤 \_ 狀態 \_ 集 \_ 版本 \_ 失敗**
</dt> <dd> <dl> <dt>

15802 (0x3DBA) 
</dt> <dt>



設定應用程式的狀態版本失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**錯誤 \_ 狀態 \_ 結構化 \_ 重設 \_ 失敗**
</dt> <dd> <dl> <dt>

15803 (0x3DBB) 
</dt> <dt>



重設應用程式的結構化狀態失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**錯誤 \_ 狀態 \_ 開啟 \_ 容器 \_ 失敗**
</dt> <dd> <dl> <dt>

15804 (0x3DBC) 
</dt> <dt>



狀態管理員無法開啟容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**錯誤 \_ 狀態 \_ 建立 \_ 容器 \_ 失敗**
</dt> <dd> <dl> <dt>

15805 (0x3DBD) 
</dt> <dt>



狀態管理員無法建立容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**錯誤 \_ 狀態 \_ 刪除 \_ 容器 \_ 失敗**
</dt> <dd> <dl> <dt>

15806 (0x3DBE) 
</dt> <dt>



狀態管理員無法刪除容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**錯誤 \_ 狀態 \_ 讀取 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15807 (0x3DBF) 
</dt> <dt>



狀態管理員無法讀取設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**錯誤 \_ 狀態 \_ 寫入 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15808 (0x3DC0) 
</dt> <dt>



狀態管理員無法寫入設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**錯誤 \_ 狀態 \_ 刪除 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15809 (0x3DC1) 
</dt> <dt>



狀態管理員無法刪除設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**錯誤 \_ 狀態 \_ 查詢 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15810 (0x3DC2) 
</dt> <dt>



狀態管理員無法查詢設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**錯誤 \_ 狀態 \_ 讀取 \_ 複合 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15811 (0x3DC3) 
</dt> <dt>



狀態管理員無法讀取複合設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**錯誤 \_ 狀態 \_ 寫入 \_ 複合 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15812 (0x3DC4) 
</dt> <dt>



狀態管理員無法寫入複合設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**錯誤 \_ 狀態 \_ 列舉 \_ 容器 \_ 失敗**
</dt> <dd> <dl> <dt>

15813 (0x3DC5) 
</dt> <dt>



狀態管理員無法列舉容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**錯誤 \_ 狀態 \_ 列舉 \_ 設定 \_ 失敗**
</dt> <dd> <dl> <dt>

15814 (0x3DC6) 
</dt> <dt>



狀態管理員無法列舉設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**已 \_ 超過錯誤狀態 \_ 複合 \_ 設定 \_ 值 \_ 大小 \_ 限制 \_**
</dt> <dd> <dl> <dt>

15815 (0x3DC7) 
</dt> <dt>



狀態管理員複合設定值的大小已超過限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 設定 \_ 值 \_ 大小 \_ 限制 \_**
</dt> <dd> <dl> <dt>

15816 (0x3DC8) 
</dt> <dt>



狀態管理員設定值的大小已超過限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 設定的 \_ 名稱 \_ 大小 \_ 限制 \_**
</dt> <dd> <dl> <dt>

15817 (0x3DC9) 
</dt> <dt>



狀態管理員設定名稱的長度已超過限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 容器 \_ 名稱 \_ 大小 \_ 限制 \_**
</dt> <dd> <dl> <dt>

15818 (0x3DCA) 
</dt> <dt>



狀態管理員容器名稱的長度已超過限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**錯誤 \_ API \_ 無法使用**
</dt> <dd> <dl> <dt>

15841 (0x3DE1) 
</dt> <dt>



此 API 無法在呼叫端的應用程式類型內容中使用。


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

 

 
