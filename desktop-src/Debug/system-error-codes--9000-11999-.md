---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼9000-11999，適用于開發人員。
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: '系統錯誤碼 (9000-11999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aea735601b2c19bfc54a0841bb0150426b5c292e61dddb53473dfe41575e4337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984478"
---
# <a name="system-error-codes-9000-11999"></a>系統錯誤碼 (9000-11999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[[錯誤碼](system-error-codes.md)] 頁面上有資源清單。

下列清單描述 (錯誤9000到 11999) 的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS \_ 錯誤 \_ RCODE \_ 格式 \_ 錯誤**
</dt> <dd> <dl> <dt>

9001 (0x2329) 
</dt> <dt>



DNS 伺服器無法解讀格式。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS \_ 錯誤 \_ RCODE \_ 伺服器 \_ 失敗**
</dt> <dd> <dl> <dt>

9002 (0x232A) 
</dt> <dt>



DNS 伺服器失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS \_ 錯誤 \_ RCODE \_ 名稱 \_ 錯誤**
</dt> <dd> <dl> <dt>

9003 (0x232B) 
</dt> <dt>



DNS 名稱不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS \_ 錯誤 \_ RCODE \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

9004 (0x232C) 
</dt> <dt>



名稱伺服器不支援 DNS 要求。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_拒絕 DNS 錯誤 \_ RCODE \_**
</dt> <dd> <dl> <dt>

9005 (0x232D) 
</dt> <dt>



DNS 操作拒絕。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS \_ 錯誤 \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E) 
</dt> <dt>



存在的 DNS 名稱不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS \_ 錯誤 \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F) 
</dt> <dt>



不應該存在的 DNS RR 設定存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS \_ 錯誤 \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330) 
</dt> <dt>



應存在的 DNS RR 設定不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS \_ 錯誤 \_ RCODE \_ NOTAUTH**
</dt> <dd> <dl> <dt>

9009 (0x2331) 
</dt> <dt>



DNS 伺服器未授權區域。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS \_ 錯誤 \_ RCODE \_ NOTZONE**
</dt> <dd> <dl> <dt>

9010 (0x2332) 
</dt> <dt>



Update 或 >prereq 中的 DNS 名稱不在區域中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS \_ 錯誤 \_ RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338) 
</dt> <dt>



DNS 簽章無法驗證。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS \_ 錯誤 \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339) 
</dt> <dt>



DNS 錯誤的索引鍵。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS \_ 錯誤 \_ RCODE \_ BADTIME**
</dt> <dd> <dl> <dt>

9018 (0x233A) 
</dt> <dt>



DNS 簽名碼有效期限已過期。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**\_需要 DNS 錯誤 \_ KEYMASTER \_**
</dt> <dd> <dl> <dt>

9101 (0x238D) 
</dt> <dt>



只有作為區域金鑰主機的 DNS 伺服器，才能執行這項操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_ \_ \_ \_ \_ 簽署的 \_ 區域不允許 DNS 錯誤**
</dt> <dd> <dl> <dt>

9102 (0x238E) 
</dt> <dt>



這項作業不能用於已簽署或有簽署金鑰的區域。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS \_ 錯誤 \_ NSEC3 \_ \_ 與 \_ RSA \_ SHA1 不相容**
</dt> <dd> <dl> <dt>

9103 (0x238F) 
</dt> <dt>



NSEC3 與 RSA-SHA-1 演算法不相容。 選擇不同的演算法或使用 NSEC。

此值也稱為 **DNS \_ ERROR 無效 \_ 的 \_ NSEC3 \_ 參數**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS \_ 錯誤 \_ 沒有 \_ 足夠的 \_ 簽署 \_ 金鑰 \_ 描述元**
</dt> <dd> <dl> <dt>

9104 (0x2390) 
</dt> <dt>



區域沒有足夠的簽署金鑰。 至少必須有一個金鑰簽署金鑰 (KSK) ，以及至少一個 (ZSK) 的區域簽署金鑰。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS \_ 錯誤 \_ 不支援的 \_ 演算法**
</dt> <dd> <dl> <dt>

9105 (0x2391) 
</dt> <dt>



不支援指定的演算法。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS \_ 錯誤 \_ 的 \_ 金鑰 \_ 大小無效**
</dt> <dd> <dl> <dt>

9106 (0x2392) 
</dt> <dt>



不支援指定的金鑰大小。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_ \_ \_ \_ 無法存取 DNS 錯誤簽署 \_ 金鑰**
</dt> <dd> <dl> <dt>

9107 (0x2393) 
</dt> <dt>



DNS 伺服器無法存取區域的一或多個簽署金鑰。 在解決此錯誤之前，區域簽署將無法運作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS \_ 錯誤 \_ KSP \_ 不 \_ \_ 支援 \_ 保護**
</dt> <dd> <dl> <dt>

9108 (0x2394) 
</dt> <dt>



指定的金鑰儲存提供者不支援 DPAPI + + 資料保護。 在解決此錯誤之前，區域簽署將無法運作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS \_ 錯誤未 \_ 預期的 \_ 資料 \_ 保護 \_ 錯誤**
</dt> <dd> <dl> <dt>

9109 (0x2395) 
</dt> <dt>



遇到非預期的 DPAPI + + 錯誤。 在解決此錯誤之前，區域簽署將無法運作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS \_ 錯誤非 \_ 預期的 \_ CNG \_ 錯誤**
</dt> <dd> <dl> <dt>

9110 (0x2396) 
</dt> <dt>



遇到未預期的加密錯誤。 在解決此錯誤之前，區域簽署可能無法運作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS \_ 錯誤 \_ 未知的 \_ 簽署 \_ 參數 \_ 版本**
</dt> <dd> <dl> <dt>

9111 (0x2397) 
</dt> <dt>



DNS 伺服器發現具有未知版本的簽署金鑰。 在解決此錯誤之前，區域簽署將無法運作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_ \_ \_ 無法存取 DNS 錯誤 \_ KSP**
</dt> <dd> <dl> <dt>

9112 (0x2398) 
</dt> <dt>



DNS 伺服器無法開啟指定的金鑰服務提供者。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS \_ 錯誤 \_ 太 \_ 多 \_ SKD**
</dt> <dd> <dl> <dt>

9113 (0x2399) 
</dt> <dt>



DNS 伺服器無法接受具有此區域指定演算法和 KSK 旗標值的其他任何簽署金鑰。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS \_ 錯誤 \_ 的 \_ 變換 \_ 期間無效**
</dt> <dd> <dl> <dt>

9114 (0x239A) 
</dt> <dt>



指定的變換期間無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS \_ 錯誤 \_ 的 \_ 初始 \_ 變換 \_ 位移無效**
</dt> <dd> <dl> <dt>

9115 (0x239B) 
</dt> <dt>



指定的初始變換位移無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS \_ 錯誤 \_ 變換 \_ 正在 \_ 進行中**
</dt> <dd> <dl> <dt>

9116 (0x239C) 
</dt> <dt>



指定的簽署金鑰已在變換金鑰的過程中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS \_ 錯誤 \_ 待命 \_ 金鑰 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

9117 (0x239D) 
</dt> <dt>



指定的簽署金鑰沒有要撤銷的待命金鑰。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_ \_ \_ ZSK 上不允許 \_ DNS \_ 錯誤**
</dt> <dd> <dl> <dt>

9118 (0x239E) 
</dt> <dt>



 (ZSK) 的區域簽署金鑰上不允許此作業。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_ \_ \_ \_ \_ 主動 \_ SKD 上不允許 DNS 錯誤**
</dt> <dd> <dl> <dt>

9119 (0x239F) 
</dt> <dt>



使用中的簽署金鑰不允許進行這項操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS \_ 錯誤 \_ 變換 \_ 已 \_ 排入佇列**
</dt> <dd> <dl> <dt>

9120 (0x23A0) 
</dt> <dt>



指定的簽署金鑰已排入佇列進行變換。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_ \_ 未 \_ \_ \_ 簽署的 \_ 區域上不允許 DNS 錯誤**
</dt> <dd> <dl> <dt>

9121 (0x23A1) 
</dt> <dt>



不允許在未簽署的區域上執行這項操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS \_ 錯誤 \_ 錯誤 \_ KEYMASTER**
</dt> <dd> <dl> <dt>

9122 (0x23A2) 
</dt> <dt>



無法完成此操作，因為列為此區域目前金鑰主機的 DNS 伺服器已關閉或設定不正確。 請解決此區域目前金鑰主機上的問題，或使用另一部 DNS 伺服器來佔用金鑰主機角色。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS \_ 錯誤不正確簽章 \_ \_ \_ 有效 \_ 期間**
</dt> <dd> <dl> <dt>

9123 (0x23A3) 
</dt> <dt>



指定的簽章有效期間無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS \_ 錯誤 \_ 不正確 \_ NSEC3 \_ 反覆運算 \_ 計數**
</dt> <dd> <dl> <dt>

9124 (0x23A4) 
</dt> <dt>



指定的 NSEC3 反覆運算計數高於區域中使用的最小金鑰長度所允許的數目。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS \_ 錯誤 \_ DNSSEC \_ 已 \_ 停用**
</dt> <dd> <dl> <dt>

9125 (0x23A5) 
</dt> <dt>



因為 DNS 伺服器已設定為停用 DNSSEC 功能，所以無法完成此操作。 在 DNS 伺服器上啟用 DNSSEC。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS \_ 錯誤 \_ 不正確 \_ XML**
</dt> <dd> <dl> <dt>

9126 (0x23A6) 
</dt> <dt>



無法完成這項作業，因為收到的 XML 資料流程是空的或語法無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS \_ 錯誤 \_ 沒有 \_ 有效的 \_ 信任 \_ 錨點**
</dt> <dd> <dl> <dt>

9127 (0x23A7) 
</dt> <dt>



這項作業已完成，但未新增任何信任錨點，因為收到的所有信賴起點都無效、不受支援、已過期，或在30天內不會有效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS \_ 錯誤 \_ 變換 \_ 未 \_ POKEABLE**
</dt> <dd> <dl> <dt>

9128 (0x23A8) 
</dt> <dt>



指定的簽署金鑰未等候家長 DS 更新。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS \_ 錯誤 \_ NSEC3 \_ 名稱 \_ 衝突**
</dt> <dd> <dl> <dt>

9129 (0x23A9) 
</dt> <dt>



在 NSEC3 簽署期間偵測到雜湊衝突。 請指定不同的使用者提供 salt，或使用隨機產生的 salt，然後再次嘗試簽署區域。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS \_ 錯誤 \_ NSEC \_ \_ 與 \_ NSEC3 \_ RSA \_ SHA1 不相容**
</dt> <dd> <dl> <dt>

9130 (0x23AA) 
</dt> <dt>



NSEC 與 NSEC3-RSA-SHA-1 演算法不相容。 選擇不同的演算法或使用 NSEC3。


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS \_ 資訊 \_ 沒有 \_ 記錄**
</dt> <dd> <dl> <dt>

9501 (0x251D) 
</dt> <dt>



沒有找到指定的 DNS 查詢記錄。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS \_ 錯誤的封 \_ \_ 包錯誤**
</dt> <dd> <dl> <dt>

9502 (0x251E) 
</dt> <dt>



錯誤的 DNS 封包。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS \_ 錯誤的封 \_ \_ 包**
</dt> <dd> <dl> <dt>

9503 (0x251F) 
</dt> <dt>



沒有 DNS 封包。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS \_ 錯誤 \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520) 
</dt> <dt>



DNS 錯誤，請檢查 rcode。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS \_ 錯誤不安全的封 \_ \_ 包**
</dt> <dd> <dl> <dt>

9505 (0x2521) 
</dt> <dt>



不安全的 DNS 封包。


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS \_ 要求 \_ 擱置中**
</dt> <dd> <dl> <dt>

9506 (0x2522) 
</dt> <dt>



DNS 查詢要求正在擱置中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS \_ 錯誤 \_ 的 \_ 類型無效**
</dt> <dd> <dl> <dt>

9551 (0x254F) 
</dt> <dt>



DNS 類型無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS \_ 錯誤 \_ 不正確 \_ IP \_ 位址**
</dt> <dd> <dl> <dt>

9552 (0x2550) 
</dt> <dt>



IP 位址無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS \_ 錯誤 \_ 的 \_ 屬性無效**
</dt> <dd> <dl> <dt>

9553 (0x2551) 
</dt> <dt>



屬性無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS \_ 錯誤 \_ 稍後再試一次 \_ \_**
</dt> <dd> <dl> <dt>

9554 (0x2552) 
</dt> <dt>



請稍後再試一次 DNS 操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS \_ 錯誤 \_ 不是 \_ 唯一的**
</dt> <dd> <dl> <dt>

9555 (0x2553) 
</dt> <dt>



指定名稱和類型的記錄不是唯一的。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS \_ 錯誤 \_ 非 \_ RFC \_ 名稱**
</dt> <dd> <dl> <dt>

9556 (0x2554) 
</dt> <dt>



DNS 名稱不符合 RFC 規格。


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS \_ 狀態 \_ FQDN**
</dt> <dd> <dl> <dt>

9557 (0x2555) 
</dt> <dt>



DNS 名稱是完整的 DNS 名稱。


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS \_ 狀態 \_ 點 \_ 名稱**
</dt> <dd> <dl> <dt>

9558 (0x2556) 
</dt> <dt>



DNS 名稱是點 (多標籤) 。


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS \_ 狀態 \_ 單一 \_ 部分 \_ 名稱**
</dt> <dd> <dl> <dt>

9559 (0x2557) 
</dt> <dt>



DNS 名稱是單一部分的名稱。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS \_ 錯誤 \_ 不正確 \_ 名稱 \_ 字元**
</dt> <dd> <dl> <dt>

9560 (0x2558) 
</dt> <dt>



DNS 名稱包含不正確字元。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS \_ 錯誤 \_ 數值 \_ 名稱**
</dt> <dd> <dl> <dt>

9561 (0x2559) 
</dt> <dt>



DNS 名稱完全是數位。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_ \_ \_ \_ \_ 根 \_ 伺服器上不允許 DNS 錯誤**
</dt> <dd> <dl> <dt>

9562 (0x255A) 
</dt> <dt>



DNS 根伺服器上不允許所要求的操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_ \_ \_ 委派下不允許 \_ DNS \_ 錯誤**
</dt> <dd> <dl> <dt>

9563 (0x255B) 
</dt> <dt>



因為 DNS 命名空間的這個部分已委派給另一部伺服器，所以無法建立記錄。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS \_ 錯誤找 \_ 不 \_ 到 \_ 根 \_ 提示**
</dt> <dd> <dl> <dt>

9564 (0x255C) 
</dt> <dt>



DNS 伺服器找不到一組根提示。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS \_ 錯誤 \_ 的 \_ 根 \_ 提示不一致**
</dt> <dd> <dl> <dt>

9565 (0x255D) 
</dt> <dt>



DNS 伺服器找到根目錄提示，但它們在所有介面卡之間都不一致。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS \_ 錯誤 \_ DWORD \_ 值 \_ 太 \_ 小**
</dt> <dd> <dl> <dt>

9566 (0x255E) 
</dt> <dt>



指定的值對此參數而言太小。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS \_ 錯誤 \_ DWORD \_ 值 \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

9567 (0x255F) 
</dt> <dt>



指定的值對此參數而言太大。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS \_ 錯誤 \_ 背景 \_ 載入**
</dt> <dd> <dl> <dt>

9568 (0x2560) 
</dt> <dt>



當 DNS 伺服器在背景中載入區域時，不允許此操作。 請稍後再試一次。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_ \_ \_ RODC 上不允許 \_ DNS \_ 錯誤**
</dt> <dd> <dl> <dt>

9569 (0x2561) 
</dt> <dt>



針對在唯讀 DC 上執行的 DNS 伺服器，不允許所要求的操作。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_ \_ \_ \_ 在 DNAME 下不允許 DNS 錯誤 \_**
</dt> <dd> <dl> <dt>

9570 (0x2562) 
</dt> <dt>



在 DNAME 記錄下不允許有任何資料存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_需要 DNS 錯誤 \_ 委派 \_**
</dt> <dd> <dl> <dt>

9571 (0x2563) 
</dt> <dt>



此操作需要認證委派。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS \_ 錯誤 \_ 不正確 \_ 原則 \_ 資料表**
</dt> <dd> <dl> <dt>

9572 (0x2564) 
</dt> <dt>



名稱解析原則資料表已損毀。 在修正之前，DNS 解析將會失敗。 請連絡網路系統管理員。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS \_ 錯誤 \_ 區域 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

9601 (0x2581) 
</dt> <dt>



DNS 區域不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS \_ 錯誤 \_ 沒有 \_ 區域 \_ 資訊**
</dt> <dd> <dl> <dt>

9602 (0x2582) 
</dt> <dt>



DNS 區域資訊無法使用。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS \_ 錯誤 \_ 不正確 \_ 區域 \_ 操作**
</dt> <dd> <dl> <dt>

9603 (0x2583) 
</dt> <dt>



DNS 區域的操作無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS \_ 錯誤 \_ 區域 \_ 設定 \_ 錯誤**
</dt> <dd> <dl> <dt>

9604 (0x2584) 
</dt> <dt>



DNS 區域設定無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS \_ 錯誤 \_ 區域 \_ \_ 沒有 \_ SOA \_ 記錄**
</dt> <dd> <dl> <dt>

9605 (0x2585) 
</dt> <dt>



DNS 區域沒有 (SOA) 記錄的授權啟動。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS \_ 錯誤 \_ 區域 \_ \_ 沒有 \_ NS \_ 記錄**
</dt> <dd> <dl> <dt>

9606 (0x2586) 
</dt> <dt>



DNS 區域沒有 (NS) 記錄的名稱伺服器。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS \_ 錯誤 \_ 區域已 \_ 鎖定**
</dt> <dd> <dl> <dt>

9607 (0x2587) 
</dt> <dt>



DNS 區域已鎖定。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_建立 DNS \_ 錯誤 \_ 區域 \_ 失敗**
</dt> <dd> <dl> <dt>

9608 (0x2588) 
</dt> <dt>



DNS 區域建立失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS \_ 錯誤 \_ 區域 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9609 (0x2589) 
</dt> <dt>



DNS 區域已存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS \_ 錯誤 \_ AUTOZONE \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9610 (0x258A) 
</dt> <dt>



DNS 自動區域已經存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS \_ 錯誤 \_ 不正確 \_ 區域 \_ 類型**
</dt> <dd> <dl> <dt>

9611 (0x258B) 
</dt> <dt>



DNS 區欄位型別無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS \_ 錯誤 \_ 次要 \_ 需要 \_ 主要 \_ IP**
</dt> <dd> <dl> <dt>

9612 (0x258C) 
</dt> <dt>



次要 DNS 區域需要主要 IP 位址。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS \_ 錯誤 \_ 區域 \_ 不是 \_ 次要**
</dt> <dd> <dl> <dt>

9613 (0x258D) 
</dt> <dt>



DNS 區域不是次要。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS \_ 錯誤 \_ 需要 \_ 次要 \_ 位址**
</dt> <dd> <dl> <dt>

9614 (0x258E) 
</dt> <dt>



需要次要 IP 位址。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS \_ 錯誤 \_ WINS \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

9615 (0x258F) 
</dt> <dt>



WINS 初始化失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS \_ 錯誤 \_ 需要 \_ WINS \_ 伺服器**
</dt> <dd> <dl> <dt>

9616 (0x2590) 
</dt> <dt>



需要 WINS 伺服器。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS \_ 錯誤 \_ NBSTAT \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

9617 (0x2591) 
</dt> <dt>



NBTSTAT 初始化呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS \_ 錯誤 \_ SOA \_ 刪除 \_ 無效**
</dt> <dd> <dl> <dt>

9618 (0x2592) 
</dt> <dt>



不正確 (SOA) 刪除授權啟動。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS \_ 錯誤轉寄站 \_ \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9619 (0x2593) 
</dt> <dt>



該名稱已有條件式轉送區域存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS \_ 錯誤 \_ 區域 \_ 需要 \_ 主要 \_ IP**
</dt> <dd> <dl> <dt>

9620 (0x2594) 
</dt> <dt>



此區域必須設定一或多個主要 DNS 伺服器 IP 位址。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS \_ 錯誤 \_ 區域 \_ 已 \_ 關閉**
</dt> <dd> <dl> <dt>

9621 (0x2595) 
</dt> <dt>



無法執行操作，因為此區域已關閉。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**已 \_ 鎖定 DNS 錯誤 \_ 區域 \_ \_ 進行 \_ 簽署**
</dt> <dd> <dl> <dt>

9622 (0x2596) 
</dt> <dt>



因為目前正在簽署區域，所以無法執行此作業。 請稍後再試一次。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS \_ 錯誤 \_ 主要 \_ 需要 \_ 資料檔案**
</dt> <dd> <dl> <dt>

9651 (0x25B3) 
</dt> <dt>



主要 DNS 區域需要資料檔案。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS \_ 錯誤 \_ 不正確 \_ 資料檔案 \_ 名稱**
</dt> <dd> <dl> <dt>

9652 (0x25B4) 
</dt> <dt>



DNS 區域的資料檔案名稱無效。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS \_ 錯誤 \_ 資料檔案 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

9653 (0x25B5) 
</dt> <dt>



無法開啟 DNS 區域的資料檔案。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS \_ 錯誤 \_ 檔案 \_ 回寫 \_ 失敗**
</dt> <dd> <dl> <dt>

9654 (0x25B6) 
</dt> <dt>



無法寫入 DNS 區域的資料檔案。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS \_ 錯誤 \_ 資料檔案 \_ 剖析**
</dt> <dd> <dl> <dt>

9655 (0x25B7) 
</dt> <dt>



讀取 DNS 區域的資料檔案時失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS \_ 錯誤 \_ 記錄 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

9701 (0x25E5) 
</dt> <dt>



DNS 記錄不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS \_ 錯誤 \_ 記錄 \_ 格式**
</dt> <dd> <dl> <dt>

9702 (0x25E6) 
</dt> <dt>



DNS 記錄格式錯誤。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_建立 DNS \_ 錯誤 \_ 節點 \_ 失敗**
</dt> <dd> <dl> <dt>

9703 (0x25E7) 
</dt> <dt>



DNS 中的節點建立失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS \_ 錯誤 \_ 未知的 \_ 記錄 \_ 類型**
</dt> <dd> <dl> <dt>

9704 (0x25E8) 
</dt> <dt>



未知的 DNS 記錄類型。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS \_ 錯誤 \_ 記錄 \_ 超時 \_**
</dt> <dd> <dl> <dt>

9705 (0x25E9) 
</dt> <dt>



DNS 記錄超時。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS \_ 錯誤 \_ 名稱 \_ 不 \_ 在 \_ 區域中**
</dt> <dd> <dl> <dt>

9706 (0x25EA) 
</dt> <dt>



名稱不在 DNS 區域中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS \_ 錯誤 \_ CNAME \_ 迴圈**
</dt> <dd> <dl> <dt>

9707 (0x25EB) 
</dt> <dt>



偵測到 CNAME 迴圈。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS \_ 錯誤 \_ 節點 \_ 為 \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC) 
</dt> <dt>



Node 是 CNAME DNS 記錄。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS \_ 錯誤 \_ CNAME \_ 衝突**
</dt> <dd> <dl> <dt>

9709 (0x25ED) 
</dt> <dt>



已有指定名稱的 CNAME 記錄。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ \_ 只有 \_ 在 \_ 區域 \_ 根目錄的 DNS 錯誤記錄**
</dt> <dd> <dl> <dt>

9710 (0x25EE) 
</dt> <dt>



只記錄在 DNS 區域根。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS \_ 錯誤 \_ 記錄 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9711 (0x25EF) 
</dt> <dt>



DNS 記錄已經存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS \_ 錯誤的 \_ 次要 \_ 資料**
</dt> <dd> <dl> <dt>

9712 (0x25F0) 
</dt> <dt>



次要 DNS 區域資料錯誤。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS \_ 錯誤 \_ 沒有 \_ CREATE \_ CACHE \_ 資料**
</dt> <dd> <dl> <dt>

9713 (0x25F1) 
</dt> <dt>



無法建立 DNS 快取資料。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS \_ 錯誤 \_ 名稱 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

9714 (0x25F2) 
</dt> <dt>



DNS 名稱不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS \_ 警告 \_ PTR \_ 建立 \_ 失敗**
</dt> <dd> <dl> <dt>

9715 (0x25F3) 
</dt> <dt>



無法 (PTR) 記錄建立指標。


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS \_ 警告 \_ 網域取消 \_ 刪除**
</dt> <dd> <dl> <dt>

9716 (0x25F4) 
</dt> <dt>



DNS 網域已取消刪除。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_ \_ 無法使用 DNS 錯誤 DS \_**
</dt> <dd> <dl> <dt>

9717 (0x25F5) 
</dt> <dt>



目錄服務無法使用。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS \_ 錯誤 \_ DS \_ 區域 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9718 (0x25F6) 
</dt> <dt>



DNS 區域已存在於目錄服務中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_ \_ \_ \_ 如果 \_ DS \_ 區域，DNS 錯誤無 BOOTFILE**
</dt> <dd> <dl> <dt>

9719 (0x25F7) 
</dt> <dt>



DNS 伺服器不會建立或讀取目錄服務整合式 DNS 區域的開機檔案。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS \_ 錯誤 \_ 節點 \_ 是 \_ DNAME**
</dt> <dd> <dl> <dt>

9720 (0x25F8) 
</dt> <dt>



Node 是 DNAME DNS 記錄。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS \_ 錯誤 \_ DNAME \_ 衝突**
</dt> <dd> <dl> <dt>

9721 (0x25F9) 
</dt> <dt>



已有指定名稱的 DNAME 記錄存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS \_ 錯誤 \_ 別名 \_ 迴圈**
</dt> <dd> <dl> <dt>

9722 (0x25FA) 
</dt> <dt>



偵測到具有 CNAME 或 DNAME 記錄的別名迴圈。


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS \_ 資訊 \_ AXFR \_ 完成**
</dt> <dd> <dl> <dt>

9751 (0x2617) 
</dt> <dt>



DNS AXFR (區域轉送) 完成。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS \_ 錯誤 \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618) 
</dt> <dt>



DNS 區域傳輸失敗。


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS \_ 資訊 \_ 已新增 \_ 本機 \_ WINS**
</dt> <dd> <dl> <dt>

9753 (0x2619) 
</dt> <dt>



已新增本機 WINS 伺服器。


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_ \_ 需要繼續進行 DNS 狀態 \_**
</dt> <dd> <dl> <dt>

9801 (0x2649) 
</dt> <dt>



安全更新呼叫需要繼續更新要求。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS \_ 錯誤 \_ 沒有 \_ TCPIP**
</dt> <dd> <dl> <dt>

9851 (0x267B) 
</dt> <dt>



未安裝 TCP/IP 網路通訊協定。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS \_ 錯誤 \_ 沒有 \_ DNS \_ 伺服器**
</dt> <dd> <dl> <dt>

9852 (0x267C) 
</dt> <dt>



未針對本機系統設定任何 DNS 伺服器。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS \_ 錯誤 \_ DP \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

9901 (0x26AD) 
</dt> <dt>



指定的目錄分割不存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS \_ 錯誤 \_ DP \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

9902 (0x26AE) 
</dt> <dt>



指定的目錄分割已存在。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS \_ 錯誤 \_ DP \_ 未 \_ 登記**
</dt> <dd> <dl> <dt>

9903 (0x26AF) 
</dt> <dt>



此 DNS 伺服器未登錄于指定的目錄分割中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS \_ 錯誤 \_ DP \_ 已 \_ 登記**
</dt> <dd> <dl> <dt>

9904 (0x26B0) 
</dt> <dt>



此 DNS 伺服器已登錄于指定的目錄分割中。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS \_ 錯誤 \_ DP \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

9905 (0x26B1) 
</dt> <dt>



目錄分割目前無法使用。 請稍候幾分鐘，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS \_ 錯誤 \_ DP \_ FSMO \_ 錯誤**
</dt> <dd> <dl> <dt>

9906 (0x26B2) 
</dt> <dt>



因為無法連線到網網域命名主機 FSMO 角色，所以操作失敗。 持有網網域命名主機 FSMO 角色的網域控制站已關閉或無法服務要求，或 Windows Server 2003 或更新版本中無法執行。


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714) 
</dt> <dt>



呼叫 WSACancelBlockingCall 時，封鎖作業中斷。


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**
</dt> <dd> <dl> <dt>

10009 (0x2719) 
</dt> <dt>



提供的檔案控制代碼無效。


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271D) 
</dt> <dt>



嘗試以存取權限禁止的方式存取通訊端。


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**
</dt> <dd> <dl> <dt>

10014 (0x271E) 
</dt> <dt>



系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**
</dt> <dd> <dl> <dt>

10022 (0x2726) 
</dt> <dt>



提供的引數無效。


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**
</dt> <dd> <dl> <dt>

10024 (0x2728) 
</dt> <dt>



開啟的通訊端太多。


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733) 
</dt> <dt>



無法立即完成非封鎖通訊端作業。


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**
</dt> <dd> <dl> <dt>

10036 (0x2734) 
</dt> <dt>



正在執行封鎖作業。


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**
</dt> <dd> <dl> <dt>

10037 (0x2735) 
</dt> <dt>



嘗試在操作中的非封鎖通訊端上執行操作。


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**
</dt> <dd> <dl> <dt>

10038 (0x2736) 
</dt> <dt>



嘗試對不是通訊端的某個作業進行作業。


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737) 
</dt> <dt>



已從通訊端上的作業省略必要的位址。


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**
</dt> <dd> <dl> <dt>

10040 (0x2738) 
</dt> <dt>



資料包通訊端上傳送的郵件超過內部郵件緩衝區容量或其他一些網路限制，或用來接收資料包的緩衝區容量小於資料包本身。


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739) 
</dt> <dt>



在通訊端函數呼叫中指定的通訊協定不支援所要求之通訊端類型的語法。


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**
</dt> <dd> <dl> <dt>

10042 (0x273A) 
</dt> <dt>



在 getsockopt 或 setsockopt 呼叫中指定了未知、無效或不支援的選項或層級。


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**
</dt> <dd> <dl> <dt>

10043 (0x273B) 
</dt> <dt>



要求的通訊協定尚未設定到系統中，或其不存在。


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**
</dt> <dd> <dl> <dt>

10044 (0x273C) 
</dt> <dt>



這個地址家族中不存在對指定通訊端類型的支援。


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273D) 
</dt> <dt>



所參考的物件類型不支援所嘗試的操作。


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**
</dt> <dd> <dl> <dt>

10046 (0x273E) 
</dt> <dt>



通訊協定系列尚未設定為系統，或其不存在。


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273F) 
</dt> <dt>



使用的位址與要求的通訊協定不相容。


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (錯誤碼為 0x2740) 
</dt> <dt>



Only one usage of each socket address (protocol/network address/port) is normally permitted.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**
</dt> <dd> <dl> <dt>

10049 (0x2741) 
</dt> <dt>



要求的位址在它的內容中無效。


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**
</dt> <dd> <dl> <dt>

10050 (0x2742) 
</dt> <dt>



通訊端作業遇到停止的網路。


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**
</dt> <dd> <dl> <dt>

10051 (0x2743) 
</dt> <dt>



已嘗試對無法連線的網路進行通訊端作業。


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**
</dt> <dd> <dl> <dt>

10052 (0x2744) 
</dt> <dt>



連接已中斷，因為在作業進行時偵測到失敗。


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745) 
</dt> <dt>



您主機機器中的軟體已中止建立的連接。


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746) 
</dt> <dt>



遠端主機已強制關閉一個現有連線。


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747) 
</dt> <dt>



無法執行通訊端上的作業，因為系統缺乏足夠的緩衝區空間，或佇列已滿。


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748) 
</dt> <dt>



已連線的通訊端上提出了 connect 要求。


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**
</dt> <dd> <dl> <dt>

10057 (0x2749) 
</dt> <dt>



因為未連接通訊端且 (使用 sendto 呼叫在資料包通訊端上傳送時) 未提供位址，所以不允許傳送或接收資料的要求。


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274A) 
</dt> <dt>



因為先前的關閉呼叫已將該方向的通訊端關閉，所以不允許傳送或接收資料的要求。


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**
</dt> <dd> <dl> <dt>

10059 (0x274B) 
</dt> <dt>



某些核心物件的參考太多。


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274C) 
</dt> <dt>



連接嘗試失敗，因為連線的合作物件在一段時間後未正確回應，或建立的連線失敗，因為連線的主機無法回應。


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D) 
</dt> <dt>



無法進行連接，因為目的電腦主動拒絕連線。


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E) 
</dt> <dt>



無法轉譯名稱。


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F) 
</dt> <dt>



名稱元件或名稱太長。


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750) 
</dt> <dt>



通訊端作業失敗，因為目的地主機已關閉。


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**
</dt> <dd> <dl> <dt>

10065 (0x2751) 
</dt> <dt>



已嘗試對無法連接的主機進行通訊端作業。


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**
</dt> <dd> <dl> <dt>

10066 (0x2752) 
</dt> <dt>



無法移除非空白的目錄。


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**
</dt> <dd> <dl> <dt>

10067 (0x2753) 
</dt> <dt>



Windows 通訊端執行可能會限制可同時使用它的應用程式數目。


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**
</dt> <dd> <dl> <dt>

10068 (0x2754) 
</dt> <dt>



配額不足。


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755) 
</dt> <dt>



磁片配額已用盡。


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756) 
</dt> <dt>



無法再使用檔案控制代碼參考。


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**
</dt> <dd> <dl> <dt>

10071 (0x2757) 
</dt> <dt>



專案無法在本機使用。


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**
</dt> <dd> <dl> <dt>

10091 (0x276B) 
</dt> <dt>



WSAStartup 目前無法運作，因為它用來提供網路服務的基礎系統目前無法使用。


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C) 
</dt> <dt>



不支援要求的 Windows 通訊端版本。


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D) 
</dt> <dt>



可能是應用程式未呼叫 WSAStartup，或 WSAStartup 失敗。


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**
</dt> <dd> <dl> <dt>

10101 (0x2775) 
</dt> <dt>



由 WSARecv 或 WSARecvFrom 傳回，表示遠端方已起始正常關機順序。


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**
</dt> <dd> <dl> <dt>

10102 (0x2776) 
</dt> <dt>



WSALookupServiceNext 不會傳回任何結果。


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**
</dt> <dd> <dl> <dt>

10103 (0x2777) 
</dt> <dt>



呼叫 WSALookupServiceEnd 是在這個呼叫仍在處理時進行。 呼叫已取消。


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**
</dt> <dd> <dl> <dt>

10104 (0x2778) 
</dt> <dt>



程序呼叫資料表無效。


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**
</dt> <dd> <dl> <dt>

10105 (0x2779) 
</dt> <dt>



要求的服務提供者無效。


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**
</dt> <dd> <dl> <dt>

10106 (0x277A) 
</dt> <dt>



無法載入或初始化要求的服務提供者。


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B) 
</dt> <dt>



系統呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**\_找不 \_ 到 WSASERVICE**
</dt> <dd> <dl> <dt>

10108 (0x277C) 
</dt> <dt>



沒有已知的服務。 在指定的命名空間中找不到服務。


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**\_找不 \_ 到 WSATYPE**
</dt> <dd> <dl> <dt>

10109 (0x277D) 
</dt> <dt>



找不到指定的類別。


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ 否 \_ 其他**
</dt> <dd> <dl> <dt>

10110 (0x277E) 
</dt> <dt>



WSALookupServiceNext 不會傳回任何結果。


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E 已 \_ 取消**
</dt> <dd> <dl> <dt>

10111 (0x277F) 
</dt> <dt>



呼叫 WSALookupServiceEnd 是在這個呼叫仍在處理時進行。 呼叫已取消。


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780) 
</dt> <dt>



資料庫查詢失敗，因為它已被主動拒絕。


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**\_找不 \_ 到 WSAHOST**
</dt> <dd> <dl> <dt>

11001 (0x2AF9) 
</dt> <dt>



沒有已知的此類主機。


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**\_再次 WSATRY**
</dt> <dd> <dl> <dt>

11002 (0x2AFA) 
</dt> <dt>



這通常為主機名稱解析期間的暫時錯誤，表示本機伺服器未收到授權伺服器的回應。


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO \_ 復原**
</dt> <dd> <dl> <dt>

11003 (0x2AFB) 
</dt> <dt>



資料庫查閱期間發生無法復原的錯誤。


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO \_ 資料**
</dt> <dd> <dl> <dt>

11004 (0x2AFC) 
</dt> <dt>



要求的名稱有效，但是找不到要求類型的資料。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA \_ QOS \_ 接收者**
</dt> <dd> <dl> <dt>

11005 (0x2AFD) 
</dt> <dt>



至少有一個保留已抵達。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA \_ QOS \_ 寄件者**
</dt> <dd> <dl> <dt>

11006 (0x2AFE) 
</dt> <dt>



至少有一個路徑已抵達。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ QOS \_ 無 \_ 寄件者**
</dt> <dd> <dl> <dt>

11007 (0x2AFF) 
</dt> <dt>



沒有任何寄件者。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA \_ QOS \_ 無 \_ 接收者**
</dt> <dd> <dl> <dt>

11008 (0x2B00) 
</dt> <dt>



沒有任何接收者。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**已 \_ 確認 WSA QOS \_ 要求 \_**
</dt> <dd> <dl> <dt>

11009 (0x2B01) 
</dt> <dt>



保留已確認。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA \_ QOS \_ 許可 \_ 失敗**
</dt> <dd> <dl> <dt>

11010 (0x2B02) 
</dt> <dt>



因為缺少資源而發生錯誤。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA \_ QOS \_ 原則 \_ 失敗**
</dt> <dd> <dl> <dt>

11011 (0x2B03) 
</dt> <dt>



因為系統管理原因而遭到拒絕-不正確的認證。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA \_ QOS \_ 不良 \_ 樣式**
</dt> <dd> <dl> <dt>

11012 (0x2B04) 
</dt> <dt>



未知或衝突的樣式。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA \_ QOS \_ 不良 \_ 物件**
</dt> <dd> <dl> <dt>

11013 (0x2B05) 
</dt> <dt>



一般 filterspec 或 providerspecific 緩衝區的部分問題。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA \_ QOS \_ 流量 \_ CTRL \_ 錯誤**
</dt> <dd> <dl> <dt>

11014 (0x2B06) 
</dt> <dt>



Flowspec 某些部分的問題。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA \_ QOS \_ 一般 \_ 錯誤**
</dt> <dd> <dl> <dt>

11015 (0x2B07) 
</dt> <dt>



一般 QOS 錯誤。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ QOS \_ ESERVICETYPE**
</dt> <dd> <dl> <dt>

11016 (0x2B08) 
</dt> <dt>



在 flowspec 中找到無效或無法辨識的服務類型。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA \_ QOS \_ EFLOWSPEC**
</dt> <dd> <dl> <dt>

11017 (0x2B09) 
</dt> <dt>



在 QOS 結構中發現無效或不一致的 flowspec。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ QOS \_ EPROVSPECBUF**
</dt> <dd> <dl> <dt>

11018 (0x2B0A) 
</dt> <dt>



QOS 提供者特定的緩衝區無效。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ QOS \_ EFILTERSTYLE**
</dt> <dd> <dl> <dt>

11019 (0x2B0B) 
</dt> <dt>



使用了不正確 QOS 篩選樣式。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA \_ QOS \_ EFILTERTYPE**
</dt> <dd> <dl> <dt>

11020 (0x2B0C) 
</dt> <dt>



使用了不正確 QOS 篩選類型。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA \_ QOS \_ EFILTERCOUNT**
</dt> <dd> <dl> <dt>

11021 (0x2B0D) 
</dt> <dt>



在 FLOWDESCRIPTOR 中指定了不正確的 QOS FILTERSPECs 數目。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA \_ QOS \_ EOBJLENGTH**
</dt> <dd> <dl> <dt>

11022 (0x2B0E) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中指定了 ObjectLength 欄位不正確物件。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA \_ QOS \_ EFLOWCOUNT**
</dt> <dd> <dl> <dt>

11023 (0x2B0F) 
</dt> <dt>



QOS 結構中指定了不正確數目的流程描述項。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ QOS \_ EUNKOWNPSOBJ**
</dt> <dd> <dl> <dt>

11024 (0x2B10) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到無法辨識的物件。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ QOS \_ EPOLICYOBJ**
</dt> <dd> <dl> <dt>

11025 (0x2B11) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到不正確原則物件。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ QOS \_ EFLOWDESC**
</dt> <dd> <dl> <dt>

11026 (0x2B12) 
</dt> <dt>



在流程描述項清單中找到不正確 QOS 流程描述項。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ QOS \_ EPSFLOWSPEC**
</dt> <dd> <dl> <dt>

11027 (0x2B13) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到無效或不一致的 flowspec。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ QOS \_ EPSFILTERSPEC**
</dt> <dd> <dl> <dt>

11028 (0x2B14) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到不正確 FILTERSPEC。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ QOS \_ ESDMODEOBJ**
</dt> <dd> <dl> <dt>

11029 (0x2B15) 
</dt> <dt>



在 QOS 提供者特定緩衝區中找到不正確圖形捨棄模式物件。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ QOS \_ ESHAPERATEOBJ**
</dt> <dd> <dl> <dt>

11030 (0x2B16) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到不正確成形率物件。


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA \_ QOS \_ 保留的 \_ PETYPE**
</dt> <dd> <dl> <dt>

11031 (0x2B17) 
</dt> <dt>



在 QOS 提供者特定的緩衝區中找到保留的原則元素。


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ \_ 找不到 WSA 安全主機**
</dt> <dd> <dl> <dt>

11032 (0x2B18) 
</dt> <dt>



無法安全地得知這類主機。


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA \_ IPSEC \_ 名稱 \_ 原則 \_ 錯誤**
</dt> <dd> <dl> <dt>

11033 (0x2B19) 
</dt> <dt>



無法新增以名稱為基礎的 IPSEC 原則。


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




