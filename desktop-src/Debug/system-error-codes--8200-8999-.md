---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼8200-8999，適用于開發人員。
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: '系統錯誤碼 (8200-8999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187727"
---
# <a name="system-error-codes-8200-8999"></a>系統錯誤碼 (8200-8999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述錯誤8200到8999的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**\_ \_ 未安裝錯誤 \_ DS**
</dt> <dd> <dl> <dt>

8200 (0x2008) 
</dt> <dt>



安裝目錄服務時發生錯誤。 如需詳細資訊，請參閱事件記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**在 \_ \_ 本機評估 DS 成員資格的 \_ 錯誤 \_**
</dt> <dd> <dl> <dt>

8201 (0x2009) 
</dt> <dt>



目錄服務會在本機評估群組成員資格。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**錯誤 \_ DS \_ 沒有 \_ 屬性 \_ 或 \_ 值**
</dt> <dd> <dl> <dt>

8202 (0x200A) 
</dt> <dt>



指定的目錄服務屬性或值不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**錯誤 \_ DS \_ 不正確 \_ 屬性 \_ 語法**
</dt> <dd> <dl> <dt>

8203 (0x200B) 
</dt> <dt>



指定給目錄服務的屬性語法無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**錯誤 \_ DS \_ 屬性 \_ 類型 \_ 未定義**
</dt> <dd> <dl> <dt>

8204 (0x200C) 
</dt> <dt>



未定義指定給目錄服務的屬性類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**\_DS \_ 屬性 \_ 或 \_ 值 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

8205 (0x200D) 
</dt> <dt>



指定的目錄服務屬性或值已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**\_DS \_ 忙碌時發生錯誤**
</dt> <dd> <dl> <dt>

8206 (0x200E) 
</dt> <dt>



目錄服務忙碌中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**\_ \_ 無法使用錯誤 DS**
</dt> <dd> <dl> <dt>

8207 (0x200F) 
</dt> <dt>



目錄服務無法使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**錯誤 \_ DS \_ 未配置 \_ RID \_**
</dt> <dd> <dl> <dt>

8208 (0x2010) 
</dt> <dt>



目錄服務無法配置相關的識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**錯誤 \_ DS \_ 不再 \_ 有 \_ RID**
</dt> <dd> <dl> <dt>

8209 (0x2011) 
</dt> <dt>



目錄服務已用盡相對識別碼的集區。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**錯誤 \_ DS 錯誤的 \_ \_ 角色 \_ 擁有者**
</dt> <dd> <dl> <dt>

8210 (0x2012) 
</dt> <dt>



無法執行要求的作業，因為目錄服務不是該類型作業的主要。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**錯誤 \_ DS \_ RIDMGR \_ 初始化 \_ 錯誤**
</dt> <dd> <dl> <dt>

8211 (0x2013) 
</dt> <dt>



目錄服務無法初始化配置相對識別碼的子系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**\_DS \_ OBJ \_ 類別 \_ 違規錯誤**
</dt> <dd> <dl> <dt>

8212 (0x2014) 
</dt> <dt>



要求的作業無法滿足一或多個與物件類別相關聯的條件約束。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**\_ \_ \_ 無法在非分 \_ \_ 葉上進行錯誤 DS**
</dt> <dd> <dl> <dt>

8213 (0x2015) 
</dt> <dt>



目錄服務只能對分葉物件執行要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**錯誤 \_ DS \_ 無法 \_ 在 \_ RDN 上進行**
</dt> <dd> <dl> <dt>

8214 (0x2016) 
</dt> <dt>



目錄服務無法在物件的 RDN 屬性上執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ OBJ \_ 類別**
</dt> <dd> <dl> <dt>

8215 (0x2017) 
</dt> <dt>



目錄服務偵測到嘗試修改物件的物件類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**錯誤 \_ DS \_ 跨 \_ DOM \_ 移動 \_ 錯誤**
</dt> <dd> <dl> <dt>

8216 (0x2018) 
</dt> <dt>



無法執行要求的跨網域移動操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**錯誤 \_ DS \_ GC \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

8217 (0x2019) 
</dt> <dt>



無法連絡通用類別目錄伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**錯誤 \_ 共用 \_ 原則**
</dt> <dd> <dl> <dt>

8218 (0x201A) 
</dt> <dt>



原則物件是共用的，只能在根修改。


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ \_ 找不到錯誤原則物件**
</dt> <dd> <dl> <dt>

8219 (0x201B) 
</dt> <dt>



原則物件不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_ \_ 只有 \_ DS 中的錯誤原則 \_**
</dt> <dd> <dl> <dt>

8220 (0x201C) 
</dt> <dt>



要求的原則資訊只會在目錄服務中。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**使用中的錯誤 \_ 提升 \_**
</dt> <dd> <dl> <dt>

8221 (0x201D) 
</dt> <dt>



網域控制站升級目前為使用中狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**錯誤 \_ 沒有任何 \_ 促銷 \_ 活動**
</dt> <dd> <dl> <dt>

8222 (0x201E) 
</dt> <dt>



網域控制站升級目前未啟用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**錯誤 \_ DS \_ 作業 \_ 錯誤**
</dt> <dd> <dl> <dt>

8224 (0x2020) 
</dt> <dt>



發生作業錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**錯誤 \_ DS \_ 通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

8225 (0x2021) 
</dt> <dt>



發生了通訊協定錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**\_超過錯誤 DS \_ TIMELIMIT \_**
</dt> <dd> <dl> <dt>

8226 (0x2022) 
</dt> <dt>



超過此要求的時間限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**\_超過錯誤 DS \_ SIZELIMIT \_**
</dt> <dd> <dl> <dt>

8227 (0x2023) 
</dt> <dt>



超過此要求的大小限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_超過 DS 系統 \_ 管理員 \_ 限制 \_ 錯誤**
</dt> <dd> <dl> <dt>

8228 (0x2024) 
</dt> <dt>



超過此要求的管理限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**錯誤 \_ DS \_ 比較 \_ FALSE**
</dt> <dd> <dl> <dt>

8229 (0x2025) 
</dt> <dt>



比較回應為 false。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**錯誤 \_ DS \_ 比較 \_ TRUE**
</dt> <dd> <dl> <dt>

8230 (0x2026) 
</dt> <dt>



比較回應為 true。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**\_ \_ \_ \_ 不支援錯誤 DS 驗證 \_ 方法**
</dt> <dd> <dl> <dt>

8231 (0x2027) 
</dt> <dt>



伺服器不支援要求的驗證方法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**\_需要 DS \_ 強 \_ 身份驗證 \_ 的錯誤**
</dt> <dd> <dl> <dt>

8232 (0x2028) 
</dt> <dt>



此伺服器需要更安全的驗證方法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**錯誤 \_ DS \_ 不當 \_ 驗證**
</dt> <dd> <dl> <dt>

8233 (0x2029) 
</dt> <dt>



不適當的驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**錯誤 \_ DS \_ 驗證 \_ 不明**
</dt> <dd> <dl> <dt>

8234 (0x202A) 
</dt> <dt>



驗證機制未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**錯誤 \_ DS \_ 參考**
</dt> <dd> <dl> <dt>

8235 (0x202B) 
</dt> <dt>



已從伺服器傳回轉介。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**錯誤 \_ DS \_ 無法使用 \_ 臨界 \_ 延伸模組**
</dt> <dd> <dl> <dt>

8236 (0x202C) 
</dt> <dt>



伺服器不支援要求的重要延伸模組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**\_需要 DS \_ 機密性 \_ 錯誤**
</dt> <dd> <dl> <dt>

8237 (0x202D) 
</dt> <dt>



此要求需要安全連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**錯誤 \_ DS 不 \_ 適當的 \_ 相符**
</dt> <dd> <dl> <dt>

8238 (0x202E) 
</dt> <dt>



不適當的相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**錯誤 \_ DS \_ 條件約束 \_ 違規**
</dt> <dd> <dl> <dt>

8239 (0x202F) 
</dt> <dt>



發生條件約束違規。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**錯誤 \_ DS \_ 沒有 \_ 這類 \_ 物件**
</dt> <dd> <dl> <dt>

8240 (0x2030) 
</dt> <dt>



伺服器上沒有此類物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**錯誤 \_ DS \_ 別名 \_ 問題**
</dt> <dd> <dl> <dt>

8241 (0x2031) 
</dt> <dt>



有別名問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**錯誤 \_ DS \_ 不正確 \_ DN \_ 語法**
</dt> <dd> <dl> <dt>

8242 (0x2032) 
</dt> <dt>



指定了不正確 dn 語法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**錯誤 \_ DS \_ 是分 \_ 葉**
</dt> <dd> <dl> <dt>

8243 (0x2033) 
</dt> <dt>



物件是分葉物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**錯誤 \_ DS \_ 別名 \_ DEREF \_ 問題**
</dt> <dd> <dl> <dt>

8244 (0x2034) 
</dt> <dt>



有一個別名參考問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**\_DS 不 \_ 願意 \_ \_ 執行的錯誤 DS**
</dt> <dd> <dl> <dt>

8245 (0x2035) 
</dt> <dt>



伺服器不願意處理要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**\_DS \_ 迴圈偵測 \_ 錯誤**
</dt> <dd> <dl> <dt>

8246 (0x2036) 
</dt> <dt>



偵測到迴圈。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**\_DS \_ 命名 \_ 違規時發生錯誤**
</dt> <dd> <dl> <dt>

8247 (0x2037) 
</dt> <dt>



發生命名違規。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**錯誤 \_ DS \_ 物件 \_ 結果 \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

8248 (0x2038) 
</dt> <dt>



結果集太大。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**錯誤 \_ DS \_ 會影響 \_ 多個 \_ DSA**
</dt> <dd> <dl> <dt>

8249 (0x2039) 
</dt> <dt>



作業會影響多個 Dsa。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**錯誤 \_ DS \_ 伺服器 \_ 關閉**
</dt> <dd> <dl> <dt>

8250 (0x203A) 
</dt> <dt>



無法操作伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**錯誤 \_ DS \_ 本機 \_ 錯誤**
</dt> <dd> <dl> <dt>

8251 (0x203B) 
</dt> <dt>



發生本機錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**錯誤 \_ DS \_ 編碼 \_ 錯誤**
</dt> <dd> <dl> <dt>

8252 (0x203C) 
</dt> <dt>



發生了編碼錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**錯誤 \_ DS \_ 解碼 \_ 錯誤**
</dt> <dd> <dl> <dt>

8253 (0x203D) 
</dt> <dt>



發生解碼錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**錯誤 \_ DS \_ 篩選器 \_ 未知**
</dt> <dd> <dl> <dt>

8254 (0x203E) 
</dt> <dt>



無法辨認搜尋篩選準則。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**錯誤 \_ DS \_ 參數 \_ 錯誤**
</dt> <dd> <dl> <dt>

8255 (0x203F) 
</dt> <dt>



一或多個參數不合法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**\_ \_ 不支援錯誤 \_ DS**
</dt> <dd> <dl> <dt>

8256 (0x2040) 
</dt> <dt>



不支援指定的方法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**錯誤 \_ DS \_ 沒有 \_ 傳回任何結果 \_**
</dt> <dd> <dl> <dt>

8257 (0x2041) 
</dt> <dt>



未傳回任何結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**\_ \_ \_ 找不到 DS \_ 控制項錯誤**
</dt> <dd> <dl> <dt>

8258 (0x2042) 
</dt> <dt>



伺服器不支援指定的控制項。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**錯誤 \_ DS \_ 用戶端 \_ 迴圈**
</dt> <dd> <dl> <dt>

8259 (0x2043) 
</dt> <dt>



用戶端偵測到參考迴圈。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_超過錯誤 DS \_ 參考 \_ 限制 \_**
</dt> <dd> <dl> <dt>

8260 (0x2044) 
</dt> <dt>



超過預設的參考限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**\_缺少 DS \_ 排序 \_ 控制項 \_ 錯誤**
</dt> <dd> <dl> <dt>

8261 (0x2045) 
</dt> <dt>



搜尋需要 SORT 控制項。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**錯誤 \_ DS \_ 位移 \_ 範圍 \_ 錯誤**
</dt> <dd> <dl> <dt>

8262 (0x2046) 
</dt> <dt>



搜尋結果超過指定的位移範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**錯誤 \_ DS \_ RIDMGR \_ 已停用**
</dt> <dd> <dl> <dt>

8263 (0x2047) 
</dt> <dt>



目錄服務偵測到配置相對識別碼的子系統已停用。 當系統判斷 (Rid) 已用盡之相對識別碼的重要部分時，就會發生這種保護機制。 如需 <https://go.microsoft.com/fwlink/p/?linkid=228610> 建議的診斷步驟和重新啟用帳戶建立的程式，請參閱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**錯誤 \_ DS \_ 根 \_ 必須 \_ 是 \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D) 
</dt> <dt>



根物件必須是命名內容的標頭。 根物件不能有具現化的父系。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**禁止 \_ DS \_ 新增 \_ 複本 \_**
</dt> <dd> <dl> <dt>

8302 (0x206E) 
</dt> <dt>



無法執行新增複本作業。 命名內容必須是可寫入的，才能建立複本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**\_ \_ \_ \_ \_ 架構中的錯誤 DS ATT 不是 DEF \_**
</dt> <dd> <dl> <dt>

8303 (0x206F) 
</dt> <dt>



未在架構中定義之屬性的參考發生。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_超過錯誤 DS 的 \_ 最大 \_ OBJ \_ 大小 \_**
</dt> <dd> <dl> <dt>

8304 (0x2070) 
</dt> <dt>



已超過物件的大小上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**錯誤 \_ DS \_ OBJ \_ 字串 \_ 名稱 \_ 存在**
</dt> <dd> <dl> <dt>

8305 (0x2071) 
</dt> <dt>



嘗試使用已在使用中的名稱，將物件新增至目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**錯誤 \_ DS \_ \_ \_ \_ 在架構中未定義 RDN \_**
</dt> <dd> <dl> <dt>

8306 (0x2072) 
</dt> <dt>



嘗試加入類別的物件，而該類別沒有定義在架構中的 RDN。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**錯誤 \_ DS \_ RDN \_ 不 \_ 符合 \_ 架構**
</dt> <dd> <dl> <dt>

8307 (0x2073) 
</dt> <dt>



嘗試使用不是在架構中定義之 RDN 的 RDN 來新增物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**錯誤 \_ DS \_ \_ 找不到要求的 \_ ATTS \_**
</dt> <dd> <dl> <dt>

8308 (0x2074) 
</dt> <dt>



在物件上找不到任何要求的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**錯誤 \_ DS \_ 使用者 \_ 緩衝區 \_ 至 \_ 小型**
</dt> <dd> <dl> <dt>

8309 (0x2075) 
</dt> <dt>



使用者緩衝區太小。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**錯誤 \_ DS \_ ATT \_ \_ 不 \_ 在 \_ OBJ 上**
</dt> <dd> <dl> <dt>

8310 (0x2076) 
</dt> <dt>



在作業中指定的屬性不存在於物件中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**錯誤 \_ DS 不 \_ 合法的 \_ MOD \_ 運算**
</dt> <dd> <dl> <dt>

8311 (0x2077) 
</dt> <dt>



不合法的修改作業。 不允許修改的某些層面。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**錯誤 \_ DS \_ OBJ \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

8312 (0x2078) 
</dt> <dt>



指定的物件太大。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**錯誤 \_ DS 錯誤的 \_ \_ 實例 \_ 類型**
</dt> <dd> <dl> <dt>

8313 (0x2079) 
</dt> <dt>



指定的實例類型無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**\_需要錯誤 DS \_ MASTERDSA \_**
</dt> <dd> <dl> <dt>

8314 (0x207A) 
</dt> <dt>



此操作必須在主要 DSA 上執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_需要 ERROR DS \_ 物件 \_ 類別 \_**
</dt> <dd> <dl> <dt>

8315 (0x207B) 
</dt> <dt>



必須指定物件類別屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**錯誤 \_ DS \_ 遺失 \_ 必要的 \_ ATT**
</dt> <dd> <dl> <dt>

8316 (0x207C) 
</dt> <dt>



遺漏必要的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**錯誤 \_ DS \_ ATT \_ NOT \_ \_ 類別的 \_ DEF**
</dt> <dd> <dl> <dt>

8317 (0x207D) 
</dt> <dt>



嘗試修改物件以包含對其類別而言不合法的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**錯誤 \_ DS \_ ATT \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

8318 (0x207E) 
</dt> <dt>



物件上已經有指定的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**錯誤 \_ DS \_ 無法 \_ 新增 \_ ATT \_ 值**
</dt> <dd> <dl> <dt>

8320 (0x2080) 
</dt> <dt>



指定的屬性不存在，或沒有任何值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR \_ DS \_ 單一 \_ 值 \_ 條件約束**
</dt> <dd> <dl> <dt>

8321 (0x2081) 
</dt> <dt>



針對只能有一個值的屬性，指定了多個值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**錯誤 \_ DS \_ 範圍 \_ 條件約束**
</dt> <dd> <dl> <dt>

8322 (0x2082) 
</dt> <dt>



屬性的值不在可接受的值範圍內。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**錯誤 \_ DS \_ ATT \_ VAL \_ 已經 \_ 存在**
</dt> <dd> <dl> <dt>

8323 (0x2083) 
</dt> <dt>



指定的值已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**錯誤 \_ DS \_ 無法 \_ REM \_ 遺失 \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084) 
</dt> <dt>



無法移除屬性，因為該屬性不存在於物件上。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**錯誤 \_ DS \_ 無法 \_ REM \_ 遺漏 \_ ATT \_ VAL**
</dt> <dd> <dl> <dt>

8325 (0x2085) 
</dt> <dt>



無法移除屬性值，因為它不存在於物件上。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**\_ \_ \_ \_ 無法 \_ SUBREF 錯誤 DS 根目錄**
</dt> <dd> <dl> <dt>

8326 (0x2086) 
</dt> <dt>



指定的根物件不可以是 subref。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**錯誤 \_ DS \_ 沒有 \_ 連結**
</dt> <dd> <dl> <dt>

8327 (0x2087) 
</dt> <dt>



不允許使用連結。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**錯誤 \_ DS \_ 沒有 \_ 連結的 \_ 評估**
</dt> <dd> <dl> <dt>

8328 (0x2088) 
</dt> <dt>



不允許連鎖的評估。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**錯誤 \_ DS \_ 沒有 \_ 父 \_ 物件**
</dt> <dd> <dl> <dt>

8329 (0x2089) 
</dt> <dt>



無法執行操作，因為物件的父系可能無法建立例項或已被刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**錯誤 \_ DS \_ 父系 \_ 是 \_ \_ 別名**
</dt> <dd> <dl> <dt>

8330 (0x208A) 
</dt> <dt>



不允許擁有別名的父系。 別名是分葉物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**錯誤 \_ DS \_ 無法 \_ 混合 \_ 主機 \_ 和 \_ 代表**
</dt> <dd> <dl> <dt>

8331 (0x208B) 
</dt> <dt>



物件和父系必須屬於相同類型，不論是 master 或兩個複本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**\_DS \_ 子系 \_ 存在錯誤**
</dt> <dd> <dl> <dt>

8332 (0x208C) 
</dt> <dt>



無法執行操作，因為子物件存在。 此作業只能在分葉物件上執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**\_ \_ \_ 找不到 DS \_ OBJ 錯誤**
</dt> <dd> <dl> <dt>

8333 (0x208D) 
</dt> <dt>



找不到目錄物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_缺少錯誤 DS \_ 別名的 \_ OBJ \_**
</dt> <dd> <dl> <dt>

8334 (0x208E) 
</dt> <dt>



遺漏了別名的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**錯誤 \_ DS \_ 錯誤 \_ 名稱 \_ 語法**
</dt> <dd> <dl> <dt>

8335 (0x208F) 
</dt> <dt>



物件名稱的語法不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**錯誤 \_ DS \_ 別名 \_ 指向 \_ \_ 別名**
</dt> <dd> <dl> <dt>

8336 (0x2090) 
</dt> <dt>



別名不允許參考另一個別名。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**錯誤 \_ DS 無法進行 \_ \_ DEREF \_ 別名**
</dt> <dd> <dl> <dt>

8337 (0x2091) 
</dt> <dt>



別名無法取值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**錯誤 \_ DS \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

8338 (0x2092) 
</dt> <dt>



作業超出範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**\_ \_ \_ 移除的 DS 物件 \_ 錯誤**
</dt> <dd> <dl> <dt>

8339 (0x2093) 
</dt> <dt>



無法繼續操作，因為物件正在移除中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**錯誤 \_ DS \_ 無法 \_ 刪除 \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8340 (0x2094) 
</dt> <dt>



無法刪除 DSA 物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**錯誤 \_ DS \_ 一般 \_ 錯誤**
</dt> <dd> <dl> <dt>

8341 (0x2095) 
</dt> <dt>



發生目錄服務錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**錯誤 \_ DS \_ DSA \_ 必須 \_ 是 \_ INT \_ 主機**
</dt> <dd> <dl> <dt>

8342 (0x2096) 
</dt> <dt>



此操作只能在內部主要 DSA 物件上執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**錯誤 \_ DS \_ 類別 \_ 不是 \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097) 
</dt> <dt>



物件必須是類別 DSA。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**錯誤 \_ DS \_ INSUFF \_ 訪問 \_ 許可權**
</dt> <dd> <dl> <dt>

8344 (0x2098) 
</dt> <dt>



許可權不足，無法執行此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**錯誤 \_ DS 不 \_ 合法的 \_ 高階**
</dt> <dd> <dl> <dt>

8345 (0x2099) 
</dt> <dt>



無法加入物件，因為父系不在可能的 superiors 清單中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_ \_ \_ SAM 所擁有 \_ 的 \_ 錯誤 DS 屬性**
</dt> <dd> <dl> <dt>

8346 (0x209A) 
</dt> <dt>



因為屬性是由安全性帳戶管理員 (SAM) 所擁有，所以不允許存取屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**錯誤 \_ DS \_ 名稱 \_ 太 \_ 多 \_ 部分**
</dt> <dd> <dl> <dt>

8347 (0x209B) 
</dt> <dt>



名稱具有太多部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**錯誤 \_ DS \_ 名稱 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

8348 (0x209C) 
</dt> <dt>



名稱太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**錯誤 \_ DS \_ 名稱 \_ 值 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

8349 (0x209D) 
</dt> <dt>



名稱值太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**錯誤 \_ DS \_ 名稱無法 \_ 分析**
</dt> <dd> <dl> <dt>

8350 (0x209E) 
</dt> <dt>



目錄服務剖析名稱時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**錯誤 \_ DS \_ 名稱 \_ 類型 \_ 未知**
</dt> <dd> <dl> <dt>

8351 (0x209F) 
</dt> <dt>



目錄服務無法取得名稱的屬性類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**錯誤 \_ DS \_ 不 \_ 是 \_ 物件**
</dt> <dd> <dl> <dt>

8352 (0x20A0) 
</dt> <dt>



名稱不會識別物件;名稱會識別虛設專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR \_ DS \_ SEC \_ DESC \_ 太 \_ 短**
</dt> <dd> <dl> <dt>

8353 (0x20A1) 
</dt> <dt>



安全描述項太短。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR \_ DS \_ SEC \_ DESC \_ 無效**
</dt> <dd> <dl> <dt>

8354 (0x20A2) 
</dt> <dt>



安全描述項無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**錯誤 \_ DS \_ 未 \_ 刪除 \_ 名稱**
</dt> <dd> <dl> <dt>

8355 (0x20A3) 
</dt> <dt>



無法建立已刪除之物件的名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**錯誤 \_ DS \_ SUBREF \_ 必須 \_ 有 \_ 父系**
</dt> <dd> <dl> <dt>

8356 (0x20A4) 
</dt> <dt>



新 subref 的父系必須存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**錯誤 \_ DS \_ NCNAME \_ 必須 \_ 是 \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5) 
</dt> <dt>



物件必須是命名內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**錯誤 \_ DS \_ 無法 \_ 新增 \_ 系統 \_**
</dt> <dd> <dl> <dt>

8358 (0x20A6) 
</dt> <dt>



不允許新增系統所擁有的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR \_ DS \_ 類別 \_ 必須 \_ 是 \_ 具體的**
</dt> <dd> <dl> <dt>

8359 (0x20A7) 
</dt> <dt>



物件的類別必須是結構化的。您無法具現化抽象類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**錯誤 \_ DS \_ 不正確 \_ DMD**
</dt> <dd> <dl> <dt>

8360 (0x20A8) 
</dt> <dt>



找不到架構物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**錯誤 \_ DS \_ OBJ \_ GUID \_ 存在**
</dt> <dd> <dl> <dt>

8361 (0x20A9) 
</dt> <dt>



具有這個 GUID)  (的本機物件已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**錯誤 \_ DS \_ 不 \_ 在 \_ BACKLINK 上**
</dt> <dd> <dl> <dt>

8362 (0x20AA) 
</dt> <dt>



無法在後置連結上執行此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**錯誤 \_ DS \_ 沒有 \_ \_ NC 的交叉引用 \_**
</dt> <dd> <dl> <dt>

8363 (0x20AB) 
</dt> <dt>



找不到指定之命名內容的交互參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**錯誤 \_ DS \_ 關機 \_**
</dt> <dd> <dl> <dt>

8364 (0x20AC) 
</dt> <dt>



無法執行操作，因為目錄服務正在關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**錯誤 \_ DS \_ 不明 \_ 操作**
</dt> <dd> <dl> <dt>

8365 (0x20AD) 
</dt> <dt>



目錄服務要求無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**錯誤 \_ DS \_ 不正確 \_ 角色 \_ 擁有者**
</dt> <dd> <dl> <dt>

8366 (0x20AE) 
</dt> <dt>



無法讀取角色擁有者屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**錯誤 \_ DS \_ 無法 \_ 聯絡 \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF) 
</dt> <dt>



要求的 FSMO 作業失敗。 無法連絡目前的 FSMO 持有人。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**錯誤 \_ DS \_ 跨 \_ NC \_ DN \_ 重新命名**
</dt> <dd> <dl> <dt>

8368 (0x20B0) 
</dt> <dt>



不允許在命名內容中修改 DN。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ 系統 \_**
</dt> <dd> <dl> <dt>

8369 (0x20B1) 
</dt> <dt>



因為屬性是由系統所擁有，所以無法修改。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**\_ \_ 僅限錯誤 DS 複寫器 \_**
</dt> <dd> <dl> <dt>

8370 (0x20B2) 
</dt> <dt>



只有複寫器可以執行此功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**\_ \_ \_ \_ 未定義錯誤 DS OBJ \_ 類別**
</dt> <dd> <dl> <dt>

8371 (0x20B3) 
</dt> <dt>



未定義指定的類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR \_ DS \_ OBJ \_ 類別 \_ 不 \_ 是子類別**
</dt> <dd> <dl> <dt>

8372 (0x20B4) 
</dt> <dt>



指定的類別不是子類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**錯誤 \_ DS \_ 名稱 \_ 參考 \_ 無效**
</dt> <dd> <dl> <dt>

8373 (0x20B5) 
</dt> <dt>



名稱參考無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**錯誤 \_ DS \_ 交互 \_ 參照 \_ 存在**
</dt> <dd> <dl> <dt>

8374 (0x20B6) 
</dt> <dt>



交叉參考已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**錯誤 \_ DS \_ 無法 \_ DEL \_ 主機 \_ 交叉引用**
</dt> <dd> <dl> <dt>

8375 (0x20B7) 
</dt> <dt>



不允許刪除主要交互參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**錯誤 \_ DS \_ 子樹 \_ 通知 \_ NOT \_ NC \_ HEAD**
</dt> <dd> <dl> <dt>

8376 (0x20B8) 
</dt> <dt>



只有 NC 標頭才支援子樹通知。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**錯誤 \_ DS \_ 通知 \_ 篩選 \_ 太 \_ 複雜**
</dt> <dd> <dl> <dt>

8377 (0x20B9) 
</dt> <dt>



通知篩選太複雜。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20BA) 
</dt> <dt>



架構更新失敗：重複的 RDN。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR \_ DS \_ DUP \_ OID**
</dt> <dd> <dl> <dt>

8379 (0x20BB) 
</dt> <dt>



架構更新失敗：重複的 OID。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**錯誤 \_ DS \_ DUP \_ MAPI \_ 識別碼**
</dt> <dd> <dl> <dt>

8380 (0x20BC) 
</dt> <dt>



架構更新失敗：重複的 MAPI 識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR \_ DS \_ DUP \_ 架構 \_ 識別碼 \_ GUID**
</dt> <dd> <dl> <dt>

8381 (0x20BD) 
</dt> <dt>



架構更新失敗：重複的架構識別碼 GUID。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR \_ DS \_ DUP \_ LDAP \_ 顯示 \_ 名稱**
</dt> <dd> <dl> <dt>

8382 (0x20BE) 
</dt> <dt>



架構更新失敗：重複的 LDAP 顯示名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**錯誤 \_ DS \_ 語義 \_ ATT \_ 測試**
</dt> <dd> <dl> <dt>

8383 (0x20BF) 
</dt> <dt>



架構更新失敗：範圍-低於範圍上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**錯誤 \_ DS \_ 語法 \_ 不相符**
</dt> <dd> <dl> <dt>

8384 (0x20C0) 
</dt> <dt>



架構更新失敗：語法不相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ 必須 \_ 有**
</dt> <dd> <dl> <dt>

8385 (0x20C1) 
</dt> <dt>



架構刪除失敗：屬性在必須包含的中使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ 可能 \_ 的**
</dt> <dd> <dl> <dt>

8386 (0x20C2) 
</dt> <dt>



架構刪除失敗：在可能包含的屬性中使用屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_ \_ 不存在的 DS 錯誤 \_ 可能 \_ 有**
</dt> <dd> <dl> <dt>

8387 (0x20C3) 
</dt> <dt>



架構更新失敗：可能包含的屬性不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_ \_ 不存在的錯誤 DS \_ 必須 \_ 有**
</dt> <dd> <dl> <dt>

8388 (0x20C4) 
</dt> <dt>



架構更新失敗： in 必須包含的屬性不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**錯誤 \_ DS \_ AUX \_ CLS \_ 測試 \_ 失敗**
</dt> <dd> <dl> <dt>

8389 (0x20C5) 
</dt> <dt>



架構更新失敗： aux 類別清單中的類別不存在或不是輔助類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**錯誤 \_ DS 不 \_ 存在 \_ POSS \_ SUP**
</dt> <dd> <dl> <dt>

8390 (0x20C6) 
</dt> <dt>



架構更新失敗： poss-superiors 中的類別不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**錯誤 \_ DS \_ 子 \_ CLS \_ 測試 \_ 失敗**
</dt> <dd> <dl> <dt>

8391 (0x20C7) 
</dt> <dt>



架構更新失敗： subclassof 清單中的類別不存在或無法滿足階層規則。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**錯誤 \_ DS 錯誤的 \_ \_ RDN \_ ATT \_ 識別碼 \_ 語法**
</dt> <dd> <dl> <dt>

8392 (0x20C8) 
</dt> <dt>



架構更新失敗： Rdn-Att 識別碼的語法錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_ \_ \_ \_ AUX \_ CLS 中存在錯誤 DS**
</dt> <dd> <dl> <dt>

8393 (0x20C9) 
</dt> <dt>



架構刪除失敗：類別會當做輔助類別使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ SUB \_ CLS 中**
</dt> <dd> <dl> <dt>

8394 (0x20CA) 
</dt> <dt>



架構刪除失敗：類別用做為子類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_ \_ \_ \_ POSS \_ SUP 中有錯誤 DS**
</dt> <dd> <dl> <dt>

8395 (0x20CB) 
</dt> <dt>



架構刪除失敗：類別用來做為 poss 高階。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**錯誤 \_ DS \_ RECALCSCHEMA \_ 失敗**
</dt> <dd> <dl> <dt>

8396 (0x20CC) 
</dt> <dt>



重新計算驗證快取時架構更新失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**錯誤 \_ DS \_ 樹 \_ 刪除 \_ 未 \_ 完成**
</dt> <dd> <dl> <dt>

8397 (0x20CD) 
</dt> <dt>



未完成刪除樹狀結構。 您必須重新建立要求，才能繼續刪除樹狀目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**錯誤 \_ DS \_ 無法 \_ 刪除**
</dt> <dd> <dl> <dt>

8398 (0x20CE) 
</dt> <dt>



無法執行要求的刪除操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**錯誤 \_ DS \_ ATT \_ 架構 \_ 要求 \_ 識別碼**
</dt> <dd> <dl> <dt>

8399 (0x20CF) 
</dt> <dt>



無法讀取架構記錄的管理類別識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**錯誤 \_ DS \_ 錯誤 \_ ATT \_ 架構 \_ 語法**
</dt> <dd> <dl> <dt>

8400 (0x20D0) 
</dt> <dt>



屬性架構的語法不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**錯誤 DS 無法快取 \_ \_ \_ \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1) 
</dt> <dt>



無法快取屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**錯誤 DS 無法快取 \_ \_ \_ \_ 類別**
</dt> <dd> <dl> <dt>

8402 (0x20D2) 
</dt> <dt>



無法快取類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**錯誤 \_ DS \_ 無法 \_ 移除 \_ ATT 快取 \_**
</dt> <dd> <dl> <dt>

8403 (0x20D3) 
</dt> <dt>



無法從快取中移除屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**錯誤 \_ DS \_ 無法 \_ 移除 \_ 類別快取 \_**
</dt> <dd> <dl> <dt>

8404 (0x20D4) 
</dt> <dt>



無法從快取中移除類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5) 
</dt> <dt>



無法讀取分辨名稱屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**錯誤 \_ DS \_ 遺失 \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6) 
</dt> <dt>



尚未為目錄服務設定上層參照。 因此，目錄服務無法對這個樹系外的物件發出參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ 實例**
</dt> <dd> <dl> <dt>

8407 (0x20D7) 
</dt> <dt>



無法取出實例型別屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**錯誤 \_ DS 程式 \_ 代碼不 \_ 一致**
</dt> <dd> <dl> <dt>

8408 (0x20D8) 
</dt> <dt>



發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**錯誤 \_ DS \_ 資料庫 \_ 錯誤**
</dt> <dd> <dl> <dt>

8409 (0x20D9) 
</dt> <dt>



發生資料庫錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**錯誤 \_ DS \_ GOVERNSID \_ 遺失**
</dt> <dd> <dl> <dt>

8410 (0x20DA) 
</dt> <dt>



遺漏屬性 GOVERNSID。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**錯誤 \_ DS \_ 遺失 \_ 預期的 \_ ATT**
</dt> <dd> <dl> <dt>

8411 (0x20DB) 
</dt> <dt>



遺漏預期的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**\_DS \_ NCNAME \_ 缺少 \_ CR \_ REF 時發生錯誤**
</dt> <dd> <dl> <dt>

8412 (0x20DC) 
</dt> <dt>



指定的命名內容缺少交互參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**錯誤 \_ DS \_ 安全性 \_ 檢查 \_ 錯誤**
</dt> <dd> <dl> <dt>

8413 (0x20DD) 
</dt> <dt>



發生安全性檢查錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_ \_ \_ 未載入錯誤 DS \_ 架構**
</dt> <dd> <dl> <dt>

8414 (0x20DE) 
</dt> <dt>



未載入架構。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**錯誤 \_ DS \_ 架構 \_ 配置 \_ 失敗**
</dt> <dd> <dl> <dt>

8415 (0x20DF) 
</dt> <dt>



架構配置失敗。 請檢查電腦是否記憶體不足。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**錯誤 \_ DS \_ ATT \_ 架構 \_ 要求 \_ 語法**
</dt> <dd> <dl> <dt>

8416 (0x20E0) 
</dt> <dt>



無法取得屬性架構的必要語法。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**錯誤 \_ DS \_ GCVERIFY \_ 錯誤**
</dt> <dd> <dl> <dt>

8417 (0x20E1) 
</dt> <dt>



通用類別目錄驗證失敗。 通用類別目錄無法使用，或不支援此操作。 目錄的某些部分目前無法使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**\_DS \_ DRA 架構 \_ 錯誤 \_ 不相符**
</dt> <dd> <dl> <dt>

8418 (0x20E2) 
</dt> <dt>



複寫作業失敗，因為相關伺服器之間的架構不相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**錯誤 \_ DS \_ \_ 找不到 \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8419 (0x20E3) 
</dt> <dt>



找不到 DSA 物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**錯誤 \_ DS \_ \_ 找不到 \_ 預期的 \_ NC**
</dt> <dd> <dl> <dt>

8420 (0x20E4) 
</dt> <dt>



找不到命名內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**錯誤 \_ DS \_ 在快取 \_ 中找不到 \_ NC \_ \_**
</dt> <dd> <dl> <dt>

8421 (0x20E5) 
</dt> <dt>



在快取中找不到命名內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ 子系**
</dt> <dd> <dl> <dt>

8422 (0x20E6) 
</dt> <dt>



無法取出子物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**錯誤 \_ DS \_ 安全性不 \_ 合法的 \_ 修改**
</dt> <dd> <dl> <dt>

8423 (0x20E7) 
</dt> <dt>



基於安全性考慮，不允許進行修改。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**錯誤 \_ DS \_ 無法 \_ 取代 \_ 隱藏的 \_ REC**
</dt> <dd> <dl> <dt>

8424 (0x20E8) 
</dt> <dt>



作業無法取代隱藏的記錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**錯誤 DS 錯誤的階層 \_ \_ \_ \_ 檔**
</dt> <dd> <dl> <dt>

8425 (0x20E9) 
</dt> <dt>



階層檔案無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**錯誤 \_ DS \_ 組建 \_ 階層 \_ 資料表 \_ 失敗**
</dt> <dd> <dl> <dt>

8426 (0x20EA) 
</dt> <dt>



嘗試建立階層資料表失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**\_缺少 DS \_ 設定 \_ 參數 \_ 的錯誤**
</dt> <dd> <dl> <dt>

8427 (0x20EB) 
</dt> <dt>



登錄中遺漏目錄設定參數。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**錯誤 \_ DS \_ 計數 \_ AB \_ 索引 \_ 失敗**
</dt> <dd> <dl> <dt>

8428 (0x20EC) 
</dt> <dt>



嘗試計算通訊錄索引失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**錯誤 \_ DS \_ 階層 \_ 表 \_ MALLOC \_ 失敗**
</dt> <dd> <dl> <dt>

8429 (0x20ED) 
</dt> <dt>



階層資料表的配置失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**錯誤 \_ DS \_ 內部 \_ 失敗**
</dt> <dd> <dl> <dt>

8430 (0x20EE) 
</dt> <dt>



目錄服務發生內部失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**錯誤 \_ DS \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

8431 (0x20EF) 
</dt> <dt>



目錄服務發生未知的錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**錯誤 \_ DS \_ 根目錄 \_ 需要 \_ 類別 \_ TOP**
</dt> <dd> <dl> <dt>

8432 (0x20F0) 
</dt> <dt>



根物件需要 ' top ' 的類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**\_DS \_ 拒絕 \_ FSMO \_ 角色錯誤**
</dt> <dd> <dl> <dt>

8433 (0x20F1) 
</dt> <dt>



此目錄伺服器正在關機，無法取得新浮動單一主機操作角色的擁有權。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**錯誤 \_ DS \_ 遺失 \_ FSMO \_ 設定**
</dt> <dd> <dl> <dt>

8434 (0x20F2) 
</dt> <dt>



目錄服務遺失必要的設定資訊，而且無法判斷浮動單一主機作業角色的擁有權。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**錯誤 \_ DS \_ 無法 \_ \_ 時須交回 \_ 角色**
</dt> <dd> <dl> <dt>

8435 (0x20F3) 
</dt> <dt>



目錄服務無法將一或多個浮動單一主機作業角色的擁有權轉移給其他伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**錯誤 \_ DS \_ DRA \_ 泛型**
</dt> <dd> <dl> <dt>

8436 (0x20F4) 
</dt> <dt>



複寫操作失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**\_DS \_ DRA 錯誤 \_ \_ 參數無效**
</dt> <dd> <dl> <dt>

8437 (0x20F5) 
</dt> <dt>



為此複寫作業指定了不正確參數。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**\_DS \_ DRA \_ 忙碌時發生錯誤**
</dt> <dd> <dl> <dt>

8438 (0x20F6) 
</dt> <dt>



目錄服務太忙碌，無法完成複寫作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**\_DS \_ DRA DRA \_ 錯誤 \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7) 
</dt> <dt>



為此複寫作業指定的辨別名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**\_DS \_ DRA DRA \_ 錯誤 \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8) 
</dt> <dt>



為此複寫作業指定的命名內容無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**錯誤 \_ DS \_ DRA \_ DN \_ 存在**
</dt> <dd> <dl> <dt>

8441 (0x20F9) 
</dt> <dt>



為此複寫作業指定的辨別名稱已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**錯誤 \_ DS \_ DRA \_ 內部 \_ 錯誤**
</dt> <dd> <dl> <dt>

8442 (0x20FA) 
</dt> <dt>



複寫系統發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**\_DS \_ DRA DRA \_ 不一致的 \_ DIT**
</dt> <dd> <dl> <dt>

8443 (0x20FB) 
</dt> <dt>



複寫作業發生資料庫不一致的情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**錯誤 \_ DS \_ DRA \_ 連接 \_ 失敗**
</dt> <dd> <dl> <dt>

8444 (0x20FC) 
</dt> <dt>



無法連絡為此複寫作業指定的伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**\_DS \_ DRA DRA 錯誤的 \_ \_ 實例 \_ 類型**
</dt> <dd> <dl> <dt>

8445 (0x20FD) 
</dt> <dt>



複寫作業遇到具有無效實例類型的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**\_ \_ \_ \_ 記憶體中的 DS DRA \_ 錯誤**
</dt> <dd> <dl> <dt>

8446 (0x20FE) 
</dt> <dt>



複寫操作無法配置記憶體。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**錯誤 \_ DS \_ DRA \_ 郵件 \_ 問題**
</dt> <dd> <dl> <dt>

8447 (0x20FF) 
</dt> <dt>



複寫作業在郵件系統發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**錯誤 \_ DS \_ DRA \_ 參考 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

8448 (0x2100) 
</dt> <dt>



目標伺服器的複寫參考資訊已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**\_ \_ \_ \_ \_ 找不到 DS DRA 參考錯誤**
</dt> <dd> <dl> <dt>

8449 (0x2101) 
</dt> <dt>



目標伺服器的複寫參考資訊不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR \_ DS \_ DRA \_ OBJ \_ 是 \_ REP \_ 來源**
</dt> <dd> <dl> <dt>

8450 (0x2102) 
</dt> <dt>



因為命名內容已複寫到另一部伺服器，所以無法移除。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**錯誤 \_ DS \_ DRA \_ 資料庫 \_ 錯誤**
</dt> <dd> <dl> <dt>

8451 (0x2103) 
</dt> <dt>



複寫作業發生資料庫錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**錯誤 \_ DS \_ DRA \_ 沒有 \_ 複本**
</dt> <dd> <dl> <dt>

8452 (0x2104) 
</dt> <dt>



命名內容正在移除，或未從指定的伺服器複寫。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**\_拒絕 DS \_ DRA \_ 存取 \_ 錯誤**
</dt> <dd> <dl> <dt>

8453 (0x2105) 
</dt> <dt>



複寫存取被拒。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**\_ \_ \_ 不支援的 DS DRA 錯誤 \_**
</dt> <dd> <dl> <dt>

8454 (0x2106) 
</dt> <dt>



此版本的目錄服務不支援要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**錯誤 \_ DS \_ DRA \_ RPC 已 \_ 取消**
</dt> <dd> <dl> <dt>

8455 (0x2107) 
</dt> <dt>



複寫遠端程序呼叫已取消。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**\_ \_ \_ 停用 DS DRA 來源 \_ 錯誤**
</dt> <dd> <dl> <dt>

8456 (0x2108) 
</dt> <dt>



來源伺服器目前拒絕複寫要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**\_ \_ \_ 停用 DS DRA 接收 \_ 錯誤**
</dt> <dd> <dl> <dt>

8457 (0x2109) 
</dt> <dt>



目的地伺服器目前拒絕複寫要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**\_DS \_ DRA \_ 名稱 \_ 衝突錯誤**
</dt> <dd> <dl> <dt>

8458 (0x210A) 
</dt> <dt>



複寫作業失敗，因為物件名稱發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**\_ \_ \_ 重新安裝 DS DRA 來源 \_ 錯誤**
</dt> <dd> <dl> <dt>

8459 (0x210B) 
</dt> <dt>



已重新安裝複寫來源。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**錯誤 \_ DS \_ DRA \_ 遺失 \_ 父系**
</dt> <dd> <dl> <dt>

8460 (0x210C) 
</dt> <dt>



複寫作業失敗，因為遺漏必要的父物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**\_DS \_ DRA DRA \_ 錯誤**
</dt> <dd> <dl> <dt>

8461 (0x210D) 
</dt> <dt>



複寫作業已被佔用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**\_DS \_ DRA \_ 放棄 \_ 同步錯誤**
</dt> <dd> <dl> <dt>

8462 (0x210E) 
</dt> <dt>



因為缺少更新，所以已放棄複寫同步處理嘗試。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**\_DS \_ DRA \_ 關機錯誤**
</dt> <dd> <dl> <dt>

8463 (0x210F) 
</dt> <dt>



複寫作業已終止，因為系統正在關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**\_DS \_ DRA \_ 不相容的 \_ 部分 \_ 集合錯誤**
</dt> <dd> <dl> <dt>

8464 (0x2110) 
</dt> <dt>



因為目的地 DC 目前正在等候從來源同步處理新的部分屬性，所以同步處理嘗試失敗。 如果最近的架構變更修改了部分屬性集，這就是正常情況。 目的地部分屬性集不是來源部分屬性集的子集。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**錯誤 \_ DS \_ DRA \_ 來源 \_ 為 \_ 部分 \_ 複本**
</dt> <dd> <dl> <dt>

8465 (0x2111) 
</dt> <dt>



複寫同步處理嘗試失敗，因為主要複本嘗試從部分複本進行同步處理。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**錯誤 \_ DS \_ DRA \_ EXTN \_ 連接 \_ 失敗**
</dt> <dd> <dl> <dt>

8466 (0x2112) 
</dt> <dt>



已連線到為此複寫作業指定的伺服器，但該伺服器無法連線到完成此作業所需的其他伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**錯誤 \_ DS \_ 安裝 \_ 架構 \_ 不符**
</dt> <dd> <dl> <dt>

8467 (0x2113) 
</dt> <dt>



來源樹系的目錄服務架構版本與這部電腦上的目錄服務版本不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_DS \_ DUP \_ 連結 \_ 識別碼錯誤**
</dt> <dd> <dl> <dt>

8468 (0x2114) 
</dt> <dt>



架構更新失敗：已有具有相同連結識別碼的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**錯誤 \_ 的 \_ DS \_ 名稱 \_ 解析錯誤**
</dt> <dd> <dl> <dt>

8469 (0x2115) 
</dt> <dt>



名稱轉譯：一般處理錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**\_ \_ \_ \_ \_ 找不到 DS 名稱錯誤**
</dt> <dd> <dl> <dt>

8470 (0x2116) 
</dt> <dt>



名稱轉譯：找不到名稱或許可權不足，無法查看名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 不是 \_ 唯一的**
</dt> <dd> <dl> <dt>

8471 (0x2117) 
</dt> <dt>



名稱轉譯：輸入名稱對應至一個以上的輸出名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 沒有 \_ 對應**
</dt> <dd> <dl> <dt>

8472 (0x2118) 
</dt> <dt>



名稱轉譯：找到輸入名稱，但沒有相關聯的輸出格式。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 網域 \_**
</dt> <dd> <dl> <dt>

8473 (0x2119) 
</dt> <dt>



名稱轉譯：無法完全解析，只找到網域。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 沒有 \_ 語法 \_ 對應**
</dt> <dd> <dl> <dt>

8474 (0x211A) 
</dt> <dt>



名稱轉譯：無法在用戶端上執行純粹的語法對應，而不需要連線到網路。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**錯誤 \_ DS \_ 結構 \_ ATT \_ MOD**
</dt> <dd> <dl> <dt>

8475 (0x211B) 
</dt> <dt>



不允許修改已建立的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**錯誤 \_ DS 錯誤的 \_ \_ OM \_ OBJ \_ 類別**
</dt> <dd> <dl> <dt>

8476 (0x211C) 
</dt> <dt>



針對具有指定語法的屬性，指定的 OM 物件類別不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**錯誤 \_ DS \_ DRA \_ 複寫 \_ 暫止**
</dt> <dd> <dl> <dt>

8477 (0x211D) 
</dt> <dt>



複寫要求已公佈;正在等候回復。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**\_需要 ERROR DS \_ DS \_**
</dt> <dd> <dl> <dt>

8478 (0x211E) 
</dt> <dt>



要求的作業需要目錄服務，而且沒有可用的。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**錯誤 \_ DS \_ 不正確 \_ LDAP \_ 顯示 \_ 名稱**
</dt> <dd> <dl> <dt>

8479 (0x211F) 
</dt> <dt>



類別或屬性的 LDAP 顯示名稱包含非 ASCII 字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**錯誤 \_ DS \_ 非 \_ 基底 \_ 搜尋**
</dt> <dd> <dl> <dt>

8480 (0x2120) 
</dt> <dt>



只有基底搜尋支援要求的搜尋作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ ATTS**
</dt> <dd> <dl> <dt>

8481 (0x2121) 
</dt> <dt>



搜尋無法從資料庫取出屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**\_ \_ \_ 沒有連結的 DS BACKLINK 錯誤 \_**
</dt> <dd> <dl> <dt>

8482 (0x2122) 
</dt> <dt>



架構更新作業嘗試加入沒有對應轉寄連結的反向連結屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**\_DS \_ EPOCH 錯誤 \_**
</dt> <dd> <dl> <dt>

8483 (0x2123) 
</dt> <dt>



跨網域移動的來源和目的地不同意物件的 epoch 號碼。 來源或目的地都沒有最新版本的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**\_DS \_ SRC \_ 名稱 \_ 不符錯誤**
</dt> <dd> <dl> <dt>

8484 (0x2124) 
</dt> <dt>



跨網域移動的來源和目的地不同意物件的目前名稱。 來源或目的地都沒有最新版本的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**錯誤 \_ DS \_ SRC \_ 和 \_ DST \_ NC \_ 相同**
</dt> <dd> <dl> <dt>

8485 (0x2125) 
</dt> <dt>



跨網域移動作業的來源和目的地相同。 呼叫端應該使用本機移動作業，而不是跨網域的移動操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**錯誤 \_ DS \_ DST \_ NC \_ 不符**
</dt> <dd> <dl> <dt>

8486 (0x2126) 
</dt> <dt>



樹系中的命名內容不會有跨網域移動的來源和目的地。 來源或目的地都沒有最新版本的分割區容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**\_ \_ \_ \_ 適用于 \_ DST \_ NC 的錯誤 DS 未 AUTHORITIVE**
</dt> <dd> <dl> <dt>

8487 (0x2127) 
</dt> <dt>



跨網域移動的目的地不是目的地命名內容的授權。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**錯誤 \_ DS \_ SRC \_ GUID \_ 不符**
</dt> <dd> <dl> <dt>

8488 (0x2128) 
</dt> <dt>



跨網域移動的來源和目的地不同意來源物件的身分識別。 來源或目的地都沒有最新版本的來源物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 已刪除的 \_ 物件**
</dt> <dd> <dl> <dt>

8489 (0x2129) 
</dt> <dt>



目的地伺服器已知道要將跨網域移動的物件刪除。 來源伺服器沒有最新版本的來源物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**\_ \_ \_ \_ 進行中的 DS PDC 操作時發生錯誤 \_**
</dt> <dd> <dl> <dt>

8490 (0x212A) 
</dt> <dt>



另一項需要獨佔存取 PDC FSMO 的作業已在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**錯誤 \_ DS \_ 跨 \_ 網域 \_ 清除 \_ REQD**
</dt> <dd> <dl> <dt>

8491 (0x212B) 
</dt> <dt>



跨網域移動作業失敗，因此移動物件的兩個版本都存在，也就是來源和目的地網域中的每一個。 必須移除目的地物件，才能將系統還原成一致的狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**錯誤 \_ DS 不 \_ 合法的 \_ XDOM \_ 移動 \_ 操作**
</dt> <dd> <dl> <dt>

8492 (0x212C) 
</dt> <dt>



因為不允許此類別的跨網域移動，或物件具有某些特殊特性，例如： trust 帳戶或限制 RID （防止其移動），所以這個物件可能不會跨網域界限移動。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**\_ \_ \_ 使用 \_ 帳戶 \_ 群組 \_ MEMBERSHPS 時發生錯誤 DS**
</dt> <dd> <dl> <dt>

8493 (0x212D) 
</dt> <dt>



一旦移動後，就無法移動具有網域界限成員資格的物件，這會違反帳戶群組的成員資格條件。 請從任何帳戶群組成員資格中移除該物件，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**錯誤 \_ DS \_ NC \_ 必須 \_ 有 \_ NC \_ 父系**
</dt> <dd> <dl> <dt>

8494 (0x212E) 
</dt> <dt>



命名內容標頭必須是另一個命名內容標頭的直屬子系，而非內部節點的子系。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**\_ \_ \_ 無法驗證 DS CR \_ 的 \_ 錯誤**
</dt> <dd> <dl> <dt>

8495 (0x212F) 
</dt> <dt>



目錄無法驗證建議的命名內容名稱，因為它不會在建議的命名內容上方保留命名內容的複本。 請確定網網域命名主機角色是由設定為通用類別目錄伺服器的伺服器所持有，而且伺服器與複寫協力電腦是最新的。  (僅適用于 Windows 2000 網網域命名主機。 ) 


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**錯誤 \_ DS \_ DST \_ 網域 \_ 不是 \_ 原生**
</dt> <dd> <dl> <dt>

8496 (0x2130) 
</dt> <dt>



目的地網域必須處於原生模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**錯誤 \_ DS \_ 遺失 \_ 基礎結構 \_ 容器**
</dt> <dd> <dl> <dt>

8497 (0x2131) 
</dt> <dt>



無法執行作業，因為伺服器上沒有感興趣網域中的基礎結構容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 帳戶 \_ 群組**
</dt> <dd> <dl> <dt>

8498 (0x2132) 
</dt> <dt>



不允許跨網域移動非空白的帳戶群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 資源 \_ 群組**
</dt> <dd> <dl> <dt>

8499 (0x2133) 
</dt> <dt>



不允許跨網域移動非空白的資源群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標**
</dt> <dd> <dl> <dt>

8500 (0x2134) 
</dt> <dt>



屬性的搜尋旗標無效。 ANR 位只適用于 Unicode 或 Teletex 字串的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**錯誤 \_ DS \_ 未 \_ 在 \_ \_ NC 上 \_ 刪除任何樹狀結構**
</dt> <dd> <dl> <dt>

8501 (0x2135) 
</dt> <dt>



不允許從具有 NC 標頭的物件開始刪除樹狀結構。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**\_ \_ \_ \_ \_ 用於 \_ 刪除的錯誤 DS 無法鎖定樹**
</dt> <dd> <dl> <dt>

8502 (0x2136) 
</dt> <dt>



目錄服務無法鎖定樹狀結構，以準備刪除樹狀結構，因為該樹狀結構正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**錯誤 \_ DS \_ 無法 \_ 識別 \_ \_ 用於 \_ 樹系 \_ 刪除的物件**
</dt> <dd> <dl> <dt>

8503 (0x2137) 
</dt> <dt>



目錄服務無法識別在嘗試刪除樹狀結構時要刪除的物件清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**\_DS \_ SAM \_ 初始化 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

8504 (0x2138) 
</dt> <dt>



安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。 錯誤狀態： 0x %2。 請關閉此系統並重新啟動至目錄服務還原模式，檢查事件記錄檔以取得詳細資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**錯誤 \_ DS \_ 敏感性 \_ 群組 \_ 違規**
</dt> <dd> <dl> <dt>

8505 (0x2139) 
</dt> <dt>



只有系統管理員可以修改系統管理群組的成員資格清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A) 
</dt> <dt>



無法變更網域控制站帳戶的主要群組識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**錯誤 \_ DS 不 \_ 合法的 \_ 基底 \_ 架構 \_ MOD**
</dt> <dd> <dl> <dt>

8507 (0x213B) 
</dt> <dt>



嘗試修改基底架構。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**錯誤 \_ DS \_ NONSAFE \_ 架構 \_ 變更**
</dt> <dd> <dl> <dt>

8508 (0x213C) 
</dt> <dt>



將新的強制屬性加入至現有的類別、從現有的類別中刪除強制屬性，或將選擇性屬性新增至不是 backlink 屬性的特殊類別 Top (直接或透過繼承，例如，藉由新增或刪除輔助類別) 則不允許。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**不 \_ 允許的 DS \_ 架構 \_ 更新 \_ 錯誤**
</dt> <dd> <dl> <dt>

8509 (0x213D) 
</dt> <dt>



因為 DC 不是架構 FSMO 角色擁有者，所以不允許在此 DC 上進行架構更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**無法 \_ \_ \_ \_ 在架構下建立錯誤 DS \_**
</dt> <dd> <dl> <dt>

8510 (0x213E) 
</dt> <dt>



此類別的物件無法在架構容器底下建立。 您只能在架構容器底下建立屬性架構和類別架構物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**錯誤 \_ DS \_ 安裝 \_ 沒有 \_ SRC \_ .SCH \_ 版本**
</dt> <dd> <dl> <dt>

8511 (0x213F) 
</dt> <dt>



複本/子系安裝無法取得來源 DC 上架構容器上的 objectVersion 屬性。 架構容器上缺少屬性，或提供的認證沒有讀取權限。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**錯誤 \_ DS \_ \_ \_ \_ \_ 在 INIFILE 中安裝沒有 .SCH 版本 \_**
</dt> <dd> <dl> <dt>

8512 (0x2140) 
</dt> <dt>



在 system32 目錄的檔案 schema.ini 的 [架構] 區段中，複本/子安裝無法讀取 objectVersion 屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**錯誤 \_ DS \_ 不正確 \_ 群組 \_ 類型**
</dt> <dd> <dl> <dt>

8513 (0x2141) 
</dt> <dt>



指定的群組類型無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有任何嵌套 GLOBALGROUP \_**
</dt> <dd> <dl> <dt>

8514 (0x2142) 
</dt> <dt>



如果群組已啟用安全性，您就無法在混合網域中嵌套全域群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有任何嵌套 LOCALGROUP \_**
</dt> <dd> <dl> <dt>

8515 (0x2143) 
</dt> <dt>



如果群組已啟用安全性，您就無法將本機群組嵌套在混合網域中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ 本地 \_ 成員**
</dt> <dd> <dl> <dt>

8516 (0x2144) 
</dt> <dt>



全域群組不能有本機群組做為成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ 通用 \_ 成員**
</dt> <dd> <dl> <dt>

8517 (0x2145) 
</dt> <dt>



全域群組不能有萬用群組作為成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**錯誤 \_ DS \_ 通用 \_ 不 \_ 可以有 \_ 本地 \_ 成員**
</dt> <dd> <dl> <dt>

8518 (0x2146) 
</dt> <dt>



萬用群組不能將本機群組作為成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ MICROSOFT.AZURE.MOBILE.SERVER.CROSSDOMAIN \_ 成員**
</dt> <dd> <dl> <dt>

8519 (0x2147) 
</dt> <dt>



全域群組不能有跨網域成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**錯誤 \_ DS \_ 本機 \_ 無法 \_ 具有 \_ MICROSOFT.AZURE.MOBILE.SERVER.CROSSDOMAIN \_ 本地 \_ 成員**
</dt> <dd> <dl> <dt>

8520 (0x2148) 
</dt> <dt>



本機群組不能有另一個跨網網域本機群組做為成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**錯誤 \_ DS \_ 有 \_ 主要 \_ 成員**
</dt> <dd> <dl> <dt>

8521 (0x2149) 
</dt> <dt>



具有主要成員的群組不能變更為安全性停用的群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**錯誤 \_ DS \_ 字串 \_ SD \_ 轉換 \_ 失敗**
</dt> <dd> <dl> <dt>

8522 (0x214A) 
</dt> <dt>



架構快取載入無法轉換類別架構物件上的字串預設 SD。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**\_DS \_ 命名 \_ 主機 \_ GC 錯誤**
</dt> <dd> <dl> <dt>

8523 (0x214B) 
</dt> <dt>



只有設定為通用類別目錄伺服器的設定為通用類別目錄伺服器的設定，才應允許持有網網域命名主機 FSMO 角色。  (僅適用于 Windows 2000 伺服器。 ) 


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**\_DS \_ DNS \_ 查閱 \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

8524 (0x214C) 
</dt> <dt>



因為 DNS 查閱失敗，所以 DSA 操作無法繼續。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**錯誤 \_ DS \_ 無法 \_ 更新 \_ SPN**
</dt> <dd> <dl> <dt>

8525 (0x214D) 
</dt> <dt>



處理物件的 DNS 主機名稱變更時，服務主體的名稱值無法保持同步。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E) 
</dt> <dt>



無法讀取安全描述項屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**錯誤 \_ DS \_ 金鑰 \_ 不是 \_ 唯一的**
</dt> <dd> <dl> <dt>

8527 (0x214F) 
</dt> <dt>



找不到要求的物件，但找到具有該索引鍵的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**錯誤 \_ DS \_ \_ 連結的 \_ ATT \_ 語法錯誤**
</dt> <dd> <dl> <dt>

8528 (0x2150) 
</dt> <dt>



所加入之連結屬性的語法不正確。 轉寄連結只能有語法2.5.5.1、2.5.5.7 和2.5.5.14，而 backlinks 只能有語法2.5.5.1。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**錯誤 \_ DS \_ SAM \_ 需要 \_ BOOTKEY \_ 密碼**
</dt> <dd> <dl> <dt>

8529 (0x2151) 
</dt> <dt>



安全性帳戶管理員需要取得開機密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**錯誤 \_ DS \_ SAM \_ 需要 \_ BOOTKEY \_ 軟碟**
</dt> <dd> <dl> <dt>

8530 (0x2152) 
</dt> <dt>



安全性帳戶管理員需要從磁片磁碟機取得開機金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**錯誤 \_ DS \_ 無法 \_ 啟動**
</dt> <dd> <dl> <dt>

8531 (0x2153) 
</dt> <dt>



無法啟動目錄服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**錯誤 \_ DS \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

8532 (0x2154) 
</dt> <dt>



無法啟動目錄服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**錯誤 \_ DS \_ 沒有 \_ \_ \_ 連接的 PKT \_ 隱私權**
</dt> <dd> <dl> <dt>

8533 (0x2155) 
</dt> <dt>



用戶端與伺服器之間的連線需要封包隱私權或更好的資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**\_樹系 \_ \_ \_ 中的 DS 來源網域 \_ 錯誤**
</dt> <dd> <dl> <dt>

8534 (0x2156) 
</dt> <dt>



來源網域可能不在與目的地相同的樹系中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**錯誤 \_ DS \_ 目的地 \_ 網域 \_ 不 \_ 在 \_ 樹系中**
</dt> <dd> <dl> <dt>

8535 (0x2157) 
</dt> <dt>



目的地網域必須在樹系中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_ \_ \_ \_ 未啟用 DS 目的地審核 \_ 錯誤**
</dt> <dd> <dl> <dt>

8536 (0x2158) 
</dt> <dt>



作業需要啟用目的地網域審核。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**錯誤 \_ DS \_ \_ 找不 \_ 到 \_ \_ SRC \_ 網域的 DC**
</dt> <dd> <dl> <dt>

8537 (0x2159) 
</dt> <dt>



操作找不到來源網域的 DC。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**錯誤 \_ DS \_ SRC \_ OBJ \_ 非 \_ 群組 \_ 或 \_ 使用者**
</dt> <dd> <dl> <dt>

8538 (0x215A) 
</dt> <dt>



來源物件必須是群組或使用者。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ DS SRC SID 錯誤**
</dt> <dd> <dl> <dt>

8539 (0x215B) 
</dt> <dt>



來源物件的 SID 已存在於目的地樹系中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**\_DS \_ SRC \_ 和 \_ DST \_ 物件 \_ 類別 \_ 不符的錯誤**
</dt> <dd> <dl> <dt>

8540 (0x215C) 
</dt> <dt>



來源和目的地物件必須是相同的類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**錯誤 \_ SAM \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

8541 (0x215D) 
</dt> <dt>



安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。 錯誤狀態： 0x %2。 按一下 [確定] 關閉系統，然後重新開機進入安全模式。 請檢查事件記錄檔以取得詳細資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**\_傳送的 DS \_ DRA \_ 架構 \_ 資訊 \_ 錯誤**
</dt> <dd> <dl> <dt>

8542 (0x215E) 
</dt> <dt>



無法在複寫要求中包含架構資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**\_DS \_ DRA \_ 架構 \_ 衝突錯誤**
</dt> <dd> <dl> <dt>

8543 (0x215F) 
</dt> <dt>



因為架構不相容，所以無法完成複寫作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**錯誤 \_ DS \_ DRA \_ 先前的 \_ 架構 \_ 衝突**
</dt> <dd> <dl> <dt>

8544 (0x2160) 
</dt> <dt>



因為先前的架構不相容，所以無法完成複寫作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**錯誤 \_ DS \_ DRA 的 \_ OBJ \_ NC \_ 不相符**
</dt> <dd> <dl> <dt>

8545 (0x2161) 
</dt> <dt>



無法套用複寫更新，因為來源或目的地尚未收到有關最近跨網域移動作業的資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**錯誤 \_ DS \_ NC \_ 仍 \_ 具有 \_ DSA**
</dt> <dd> <dl> <dt>

8546 (0x2162) 
</dt> <dt>



無法刪除要求的網域，因為存在仍裝載此網域的網域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**\_需要錯誤 DS \_ GC \_**
</dt> <dd> <dl> <dt>

8547 (0x2163) 
</dt> <dt>



要求的作業只能在通用類別目錄伺服器上執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**\_ \_ \_ \_ 本機的錯誤 \_ DS 本機成員 \_**
</dt> <dd> <dl> <dt>

8548 (0x2164) 
</dt> <dt>



本機群組只能是相同網域中其他本機群組的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**錯誤 \_ DS \_ \_ \_ 在 \_ 萬用群組中 \_ 沒有任何 FPO**
</dt> <dd> <dl> <dt>

8549 (0x2165) 
</dt> <dt>



外部安全性主體不可以是萬用群組的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**錯誤 \_ DS \_ \_ 無法新增 \_ 至 \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166) 
</dt> <dt>



基於安全性考慮，不允許將屬性複寫至 GC。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**錯誤 \_ DS \_ 沒有 \_ \_ PDC 的檢查點 \_**
</dt> <dd> <dl> <dt>

8551 (0x2167) 
</dt> <dt>



因為目前正在處理太多修改，所以無法取得具有 PDC 的檢查點。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**\_ \_ \_ \_ 未啟用錯誤 DS 來源 \_ 審核**
</dt> <dd> <dl> <dt>

8552 (0x2168) 
</dt> <dt>



作業需要啟用來源網域審核。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**無法 \_ 在非網域 \_ \_ \_ \_ NC 中 \_ 建立錯誤 DS**
</dt> <dd> <dl> <dt>

8553 (0x2169) 
</dt> <dt>



安全性主體物件只能在網域命名內容內建立。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**\_ \_ \_ \_ SPN 的錯誤 DS 名稱 \_ 無效**
</dt> <dd> <dl> <dt>

8554 (0x216A) 
</dt> <dt>



因為提供的主機名稱不是所需的格式，所以無法建立服務主體名稱 (SPN) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**錯誤 \_ DS \_ 篩選器 \_ 使用 \_ 效果 \_ ATTRS**
</dt> <dd> <dl> <dt>

8555 (0x216B) 
</dt> <dt>



傳遞的篩選會使用已建立的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**錯誤 \_ DS \_ UNICODEPWD \_ 不 \_ 在 \_ 引號中**
</dt> <dd> <dl> <dt>

8556 (0x216C) 
</dt> <dt>



UnicodePwd 屬性值必須用雙引號括住。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**\_超出 DS \_ 電腦 \_ 帳戶 \_ 配額 \_ 的錯誤**
</dt> <dd> <dl> <dt>

8557 (0x216D) 
</dt> <dt>



您的電腦無法加入網域。 您已超過允許在此網域中建立的電腦帳戶數目上限。 請洽詢您的系統管理員，以重設或增加此限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ 必須 \_ \_ \_ 在 \_ DST \_ DC 上執行錯誤 DS**
</dt> <dd> <dl> <dt>

8558 (0x216E) 
</dt> <dt>



基於安全性考慮，必須在目的地 DC 上執行作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**錯誤 \_ DS \_ SRC \_ DC \_ 必須 \_ 是 \_ SP4 \_ 或 \_ 更高版本**
</dt> <dd> <dl> <dt>

8559 (0x216F) 
</dt> <dt>



基於安全性理由，來源 DC 必須是 NT4SP4 或更高的版本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**錯誤 \_ DS \_ 無法 \_ \_ 刪除 \_ 重要的 \_ OBJ**
</dt> <dd> <dl> <dt>

8560 (0x2170) 
</dt> <dt>



在樹系刪除作業期間，無法刪除重要目錄服務系統物件。 樹狀目錄刪除可能已部分執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**錯誤 \_ DS \_ 初始化 \_ 失敗 \_ 主控台**
</dt> <dd> <dl> <dt>

8561 (0x2171) 
</dt> <dt>



目錄服務無法啟動，因為發生下列錯誤： %1。 錯誤狀態： 0x %2。 請按一下 [確定] 以關閉系統。 您可以使用 [修復主控台] 進一步診斷系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**錯誤 \_ DS \_ SAM \_ 初始化 \_ 失敗 \_ 主控台**
</dt> <dd> <dl> <dt>

8562 (0x2172) 
</dt> <dt>



安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。 錯誤狀態： 0x %2。 請按一下 [確定] 以關閉系統。 您可以使用 [修復主控台] 進一步診斷系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**錯誤 \_ DS \_ 樹系 \_ 版本 \_ 過 \_ 高**
</dt> <dd> <dl> <dt>

8563 (0x2173) 
</dt> <dt>



作業系統的版本與目前的 AD DS 樹系功能等級或 AD LDS 設定集功能等級不相容。 您必須升級為新版的作業系統，此伺服器才能成為 AD DS 網域控制站，或在此 AD DS 樹系或 AD LDS 設定集中新增 AD LDS 實例。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**錯誤 \_ DS \_ 網域 \_ 版本 \_ 過 \_ 高**
</dt> <dd> <dl> <dt>

8564 (0x2174) 
</dt> <dt>



安裝的作業系統版本與目前的網域功能等級不相容。 您必須先升級為新版的作業系統，此伺服器才能成為此網域中的網域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**錯誤 \_ DS \_ 樹系 \_ 版本 \_ 太 \_ 低**
</dt> <dd> <dl> <dt>

8565 (0x2175) 
</dt> <dt>



安裝在這部伺服器上的作業系統版本不再支援目前的 AD DS 樹系功能等級或 AD LDS 設定集功能等級。 您必須提高 AD DS 樹系功能等級或 AD LDS 設定集功能等級，此伺服器才能成為此樹系或設定集中的 AD DS 網域控制站或 AD LDS 實例。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**錯誤 \_ DS \_ 網域 \_ 版本 \_ 太 \_ 低**
</dt> <dd> <dl> <dt>

8566 (0x2176) 
</dt> <dt>



安裝在此伺服器上的作業系統版本不再支援目前的網域功能等級。 您必須提高網域功能等級，此伺服器才能成為此網域中的網域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**錯誤 \_ DS \_ 不相容的 \_ 版本**
</dt> <dd> <dl> <dt>

8567 (0x2177) 
</dt> <dt>



此伺服器上安裝的作業系統版本與網域或樹系的功能等級不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**錯誤 \_ DS \_ 低 \_ DSA \_ 版本**
</dt> <dd> <dl> <dt>

8568 (0x2178) 
</dt> <dt>



網域 (或樹系) 的功能等級無法提高為要求的值，因為網域 (或樹系) 中有一或多個網域控制站位於較不相容的功能等級。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有行為版本 \_**
</dt> <dd> <dl> <dt>

8569 (0x2179) 
</dt> <dt>



樹系功能等級無法提高為要求的值，因為有一或多個網域仍處於混合網域模式。 樹系中的所有網域必須處於原生模式，您才能提高樹系功能等級。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**錯誤 \_ DS \_ 不 \_ 支援的 \_ 排序 \_ 順序**
</dt> <dd> <dl> <dt>

8570 (0x217A) 
</dt> <dt>



不支援要求的排序次序。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**錯誤 \_ DS \_ 名稱 \_ 不是 \_ 唯一的**
</dt> <dd> <dl> <dt>

8571 (0x217B) 
</dt> <dt>



要求的名稱已存在為唯一識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**\_PRENT4 建立的 DS \_ 電腦 \_ 帳戶 \_ \_ 錯誤**
</dt> <dd> <dl> <dt>

8572 (0x217C) 
</dt> <dt>



電腦帳戶是在 NT4 之前建立的。 需要重新建立帳戶。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**\_ \_ \_ \_ 版本 \_ 存放區發生錯誤 DS**
</dt> <dd> <dl> <dt>

8573 (0x217D) 
</dt> <dt>



資料庫不在版本存放區中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**\_使用了 DS \_ 不相容的錯誤 \_ 控制項 \_**
</dt> <dd> <dl> <dt>

8574 (0x217E) 
</dt> <dt>



因為使用了多個衝突的控制項，所以無法繼續操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**錯誤 \_ DS \_ 沒有任何 \_ REF \_ 網域**
</dt> <dd> <dl> <dt>

8575 (0x217F) 
</dt> <dt>



找不到此分割區的有效安全描述項參考網域。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_DS \_ 保留 \_ 連結 \_ 識別碼錯誤**
</dt> <dd> <dl> <dt>

8576 (0x2180) 
</dt> <dt>



架構更新失敗：連結識別碼已保留。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**錯誤 \_ DS \_ 連結 \_ 識別碼 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

8577 (0x2181) 
</dt> <dt>



架構更新失敗：沒有可用的連結識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**錯誤 \_ DS \_ AG \_ 不 \_ 能有 \_ 通用 \_ 成員**
</dt> <dd> <dl> <dt>

8578 (0x2182) 
</dt> <dt>



帳戶群組不能有萬用群組作為成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**\_ \_ \_ \_ \_ 實例類型不允許的 DS \_ MODIFYDN 錯誤**
</dt> <dd> <dl> <dt>

8579 (0x2183) 
</dt> <dt>



不允許對命名內容標頭或唯讀物件進行重新命名或移動作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 \_ 架構 \_ NC 中沒有物件移動**
</dt> <dd> <dl> <dt>

8580 (0x2184) 
</dt> <dt>



不允許對架構命名內容中的物件進行移動作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**\_旗標 \_ 不 \_ 允許 \_ 的 \_ 錯誤 DS MODIFYDN**
</dt> <dd> <dl> <dt>

8581 (0x2185) 
</dt> <dt>



物件上已設定系統旗標，且不允許移動或重新命名物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**錯誤 \_ DS \_ MODIFYDN \_ 錯誤的 \_ 祖系**
</dt> <dd> <dl> <dt>

8582 (0x2186) 
</dt> <dt>



此物件不允許變更其祖系容器。 在此物件上不禁止移動，但受限於同級容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 信任 \_ 參考**
</dt> <dd> <dl> <dt>

8583 (0x2187) 
</dt> <dt>



無法完全解決，會產生對另一個樹系的參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**\_ \_ \_ \_ 標準伺服器不支援的 \_ 錯誤**
</dt> <dd> <dl> <dt>

8584 (0x2188) 
</dt> <dt>



標準伺服器不支援要求的動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**錯誤 \_ DS \_ 無法 \_ 存取 \_ \_ \_ AD 的遠端 \_ 部分**
</dt> <dd> <dl> <dt>

8585 (0x2189) 
</dt> <dt>



無法存取位於遠端伺服器上目錄服務的磁碟分割。 請確定至少有一部伺服器正在針對有問題的分割區執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**\_ \_ \_ 無法 \_ \_ 驗證 \_ V2 的 DS CR 錯誤**
</dt> <dd> <dl> <dt>

8586 (0x218A) 
</dt> <dt>



目錄無法驗證建議的命名內容 (或分割區) 名稱，因為它不會保存複本，也不能在建議的命名內容上方連接命名內容的複本。 請確定已在 DNS 中正確註冊父命名內容，且網網域命名主機至少可以連線到此命名內容的一個複本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_超過錯誤 DS \_ 執行緒 \_ 限制 \_**
</dt> <dd> <dl> <dt>

8587 (0x218B) 
</dt> <dt>



已超過此要求的執行緒限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**錯誤 \_ DS \_ 未 \_ 最接近**
</dt> <dd> <dl> <dt>

8588 (0x218C) 
</dt> <dt>



通用類別目錄伺服器不在最接近的網站。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**錯誤 \_ DS 無法在 \_ \_ \_ \_ 沒有 \_ 伺服器 \_ REF 的情況下衍生 SPN**
</dt> <dd> <dl> <dt>

8589 (0x218D) 
</dt> <dt>



DS 無法衍生服務主體名稱 (SPN) 用來相互驗證目標伺服器，因為本機 DS 資料庫中對應的伺服器物件沒有 serverReference 屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**錯誤 \_ DS \_ 單一 \_ 使用者 \_ 模式 \_ 失敗**
</dt> <dd> <dl> <dt>

8590 (0x218E) 
</dt> <dt>



目錄服務無法進入單一使用者模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**錯誤 \_ DS \_ NTDSCRIPT \_ 語法 \_ 錯誤**
</dt> <dd> <dl> <dt>

8591 (0x218F) 
</dt> <dt>



由於語法錯誤，目錄服務無法剖析腳本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**錯誤 \_ DS \_ NTDSCRIPT \_ 進程 \_ 錯誤**
</dt> <dd> <dl> <dt>

8592 (0x2190) 
</dt> <dt>



目錄服務無法處理腳本，因為發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**錯誤 \_ DS \_ 不同的複寫 \_ \_ EPOCH**
</dt> <dd> <dl> <dt>

8593 (0x2191) 
</dt> <dt>



目錄服務無法執行要求的作業，因為涉及的伺服器屬於不同的複寫 epoch (這通常與進行中的網域重新命名相關) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**錯誤 \_ DS \_ DRS \_ 擴充功能 \_ 已變更**
</dt> <dd> <dl> <dt>

8594 (0x2192) 
</dt> <dt>



因為伺服器擴充功能資訊的變更，所以必須重新協商目錄服務系結。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**\_ \_ \_ \_ \_ \_ \_ \_ 停用的 CR 上不允許 \_ 發生錯誤 DS 複本集變更**
</dt> <dd> <dl> <dt>

8595 (0x2193) 
</dt> <dt>



不允許在停用的交叉參考上進行操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**錯誤 \_ DS \_ 無 \_ \_ INTID**
</dt> <dd> <dl> <dt>

8596 (0x2194) 
</dt> <dt>



架構更新失敗：無法使用 IntId 的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**錯誤 \_ DS \_ DUP \_ \_ INTID**
</dt> <dd> <dl> <dt>

8597 (0x2195) 
</dt> <dt>



架構更新失敗：重複的 INtId。 重試作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_ \_ \_ RDNATTID 中有錯誤 \_ DS**
</dt> <dd> <dl> <dt>

8598 (0x2196) 
</dt> <dt>



架構刪除失敗：屬性在 rDNAttID 中使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**錯誤 \_ DS \_ 授權 \_ 失敗**
</dt> <dd> <dl> <dt>

8599 (0x2197) 
</dt> <dt>



目錄服務無法授權要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**錯誤 \_ DS \_ 不正確 \_ 腳本**
</dt> <dd> <dl> <dt>

8600 (0x2198) 
</dt> <dt>



目錄服務無法處理腳本，因為它無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**錯誤 \_ DS \_ 遠端 \_ 交叉交叉操作作業 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

8601 (0x2199) 
</dt> <dt>



網網域命名主機 FSMO 上的遠端建立交互參照操作失敗。 作業的錯誤是在擴充的資料中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**錯誤 \_ DS \_ 交互 \_ 參照 \_ 忙碌**
</dt> <dd> <dl> <dt>

8602 (0x219A) 
</dt> <dt>



交互參照在本機使用相同的名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**錯誤 \_ DS \_ 無法 \_ 衍生 \_ \_ \_ 已刪除 \_ 網域的 SPN**
</dt> <dd> <dl> <dt>

8603 (0x219B) 
</dt> <dt>



因為伺服器的網域已從樹系中刪除，所以 DS 無法衍生服務主體名稱 (SPN) 用來相互驗證目標伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**無法 \_ \_ 使用可 \_ \_ \_ 寫入 NC 降級 \_ 的 DS 錯誤**
</dt> <dd> <dl> <dt>

8604 (0x219C) 
</dt> <dt>



可寫入的 Nc 會防止此 DC 降級。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_發現錯誤 DS \_ 重複 \_ 識別碼 \_**
</dt> <dd> <dl> <dt>

8605 (0x219D) 
</dt> <dt>



要求的物件具有非唯一的識別碼，因此無法抓取。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**錯誤 \_ DS \_ 沒有 \_ 足夠 \_ 的 ATTR 可 \_ 建立 \_ 物件**
</dt> <dd> <dl> <dt>

8606 (0x219E) 
</dt> <dt>



提供的屬性不足，無法建立物件。 此物件可能已被刪除且已進行垃圾收集，因此可能不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**錯誤 \_ DS \_ 群組 \_ 轉換 \_ 錯誤**
</dt> <dd> <dl> <dt>

8607 (0x219F) 
</dt> <dt>



因為要求的群組類型上的屬性限制，所以無法轉換群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 應用程式 \_ 基本 \_ 群組**
</dt> <dd> <dl> <dt>

8608 (0x21A0) 
</dt> <dt>



不允許跨網域移動非空白的基本應用程式群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 應用程式 \_ 查詢 \_ 群組**
</dt> <dd> <dl> <dt>

8609 (0x21A1) 
</dt> <dt>



不允許跨網域移動非空白的查詢應用程式群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**\_ \_ \_ 未驗證 DS 角色 \_ 錯誤**
</dt> <dd> <dl> <dt>

8610 (0x21A2) 
</dt> <dt>



無法驗證 FSMO 角色擁有權，因為它的目錄分割未成功地複寫至少一個複寫協力的複本。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**錯誤 \_ DS \_ WKO \_ 容器 \_ 不可 \_ 為 \_ 特殊**
</dt> <dd> <dl> <dt>

8611 (0x21A3) 
</dt> <dt>



已知物件容器重新導向的目標容器不可以是特殊的容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**錯誤 \_ DS \_ 網域 \_ 重新 \_ 命名 \_ 進行中**
</dt> <dd> <dl> <dt>

8612 (0x21A4) 
</dt> <dt>



目錄服務無法執行要求的作業，因為網域重新命名操作正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**錯誤 \_ DS \_ 現有的 \_ AD \_ 子 \_ NC**
</dt> <dd> <dl> <dt>

8613 (0x21A5) 
</dt> <dt>



目錄服務在要求的分割區名稱底下偵測到子磁碟分割。 您必須在由上而下的方法中建立資料分割階層。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_超過錯誤 DS 複寫 \_ \_ 存留期 \_**
</dt> <dd> <dl> <dt>

8614 (0x21A6) 
</dt> <dt>



目錄服務無法與此伺服器複寫，因為與此伺服器進行最後一次複寫以來的時間已超過標記存留期。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**\_ \_ \_ \_ 系統容器中不允許的 DS 錯誤 \_**
</dt> <dd> <dl> <dt>

8615 (0x21A7) 
</dt> <dt>



系統容器下的物件不允許要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**錯誤 \_ DS \_ LDAP \_ 傳送 \_ 佇列已 \_ 滿**
</dt> <dd> <dl> <dt>

8616 (0x21A8) 
</dt> <dt>



LDAP 伺服器網路傳送佇列已填滿，因為用戶端未處理其要求的結果速度夠快。 在用戶端趕上之前，將不會再處理任何要求。 如果用戶端未趕上，則會中斷連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**錯誤 \_ DS \_ DRA \_ 出 \_ 排程 \_ 視窗**
</dt> <dd> <dl> <dt>

8617 (0x21A9) 
</dt> <dt>



因為系統太忙碌而無法在 [排程] 視窗內執行要求，所以未進行排程的複寫。 複寫佇列已超載。 請考慮減少夥伴數目或減少排程的複寫頻率。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**錯誤 \_ DS \_ 原則 \_ 未知 \_**
</dt> <dd> <dl> <dt>

8618 (0x21AA) 
</dt> <dt>



目前無法判斷是否可在中樞網域控制站上使用分支複寫原則。 請稍後再試一次，以考慮複寫延遲。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**錯誤 \_ 的 \_ 網站 \_ 設定 \_ 物件**
</dt> <dd> <dl> <dt>

8619 (0x21AB) 
</dt> <dt>



指定網站的網站設定物件不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**錯誤 \_ 的 \_ 秘密**
</dt> <dd> <dl> <dt>

8620 (0x21AC) 
</dt> <dt>



本機帳戶存放區未包含指定之帳戶的秘密內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**錯誤 \_ ， \_ 找不到可寫入 \_ DC \_**
</dt> <dd> <dl> <dt>

8621 (0x21AD) 
</dt> <dt>



在網域中找不到可寫入的網域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**錯誤 \_ DS \_ 沒有 \_ 伺服器 \_ 物件**
</dt> <dd> <dl> <dt>

8622 (0x21AE) 
</dt> <dt>



網域控制站的伺服器物件不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**錯誤 \_ DS \_ 沒有 \_ NTDSA \_ 物件**
</dt> <dd> <dl> <dt>

8623 (0x21AF) 
</dt> <dt>



網域控制站的 NTDS 設定物件不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**錯誤 \_ DS \_ 非 \_ ASQ \_ 搜尋**
</dt> <dd> <dl> <dt>

8624 (0x21B0) 
</dt> <dt>



ASQ 搜尋不支援要求的搜尋作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**錯誤 \_ DS \_ 審核 \_ 失敗**
</dt> <dd> <dl> <dt>

8625 (0x21B1) 
</dt> <dt>



無法為作業產生必要的 audit 事件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標 \_ 子樹**
</dt> <dd> <dl> <dt>

8626 (0x21B2) 
</dt> <dt>



屬性的搜尋旗標無效。 子樹索引位只適用于單一值屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標 \_ 元組**
</dt> <dd> <dl> <dt>

8627 (0x21B3) 
</dt> <dt>



屬性的搜尋旗標無效。 元組索引位只有在 Unicode 字串的屬性上才有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**錯誤 \_ DS \_ 階層 \_ 資料表 \_ 太 \_ 深**
</dt> <dd> <dl> <dt>

8628 (0x21B4) 
</dt> <dt>



通訊錄的嵌套太深。 無法建立階層資料表。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**\_DS DRA 損毀 \_ \_ \_ UTD \_ 向量錯誤**
</dt> <dd> <dl> <dt>

8629 (0x21B5) 
</dt> <dt>



指定的最新性質向量已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**\_拒絕 DS \_ DRA \_ 秘密 \_ 的錯誤**
</dt> <dd> <dl> <dt>

8630 (0x21B6) 
</dt> <dt>



複寫秘密的要求遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**錯誤 \_ DS \_ 保留的 \_ MAPI \_ 識別碼**
</dt> <dd> <dl> <dt>

8631 (0x21B7) 
</dt> <dt>



架構更新失敗：已保留 MAPI 識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**\_ \_ \_ \_ 無法使用錯誤 DS MAPI \_ 識別碼**
</dt> <dd> <dl> <dt>

8632 (0x21B8) 
</dt> <dt>



架構更新失敗：沒有可用的 MAPI 識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**錯誤 \_ DS \_ DRA \_ 遺失 \_ KRBTGT \_ 秘密**
</dt> <dd> <dl> <dt>

8633 (0x21B9) 
</dt> <dt>



複寫作業失敗，因為遺漏本機 krbtgt 物件的必要屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ 錯誤 DS 功能變數名稱**
</dt> <dd> <dl> <dt>

8634 (0x21BA) 
</dt> <dt>



樹系中已經有受信任網域的功能變數名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ 錯誤 DS 一般名稱**
</dt> <dd> <dl> <dt>

8635 (0x21BB) 
</dt> <dt>



受信任網域的一般名稱已存在於樹系中。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**錯誤 \_ 不正確 \_ 使用者 \_ 主體 \_ 名稱**
</dt> <dd> <dl> <dt>

8636 (0x21BC) 
</dt> <dt>



 (UPN) 的使用者主體名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**錯誤 \_ DS \_ OID \_ 對應 \_ 群組 \_ 不 \_ 能有 \_ 成員**
</dt> <dd> <dl> <dt>

8637 (0x21BD) 
</dt> <dt>



OID 對應的群組不能有成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 DS OID**
</dt> <dd> <dl> <dt>

8638 (0x21BE) 
</dt> <dt>



找不到指定的 OID。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**\_DS \_ DRA \_ 回收 \_ 目標錯誤**
</dt> <dd> <dl> <dt>

8639 (0x21BF) 
</dt> <dt>



複寫作業失敗，因為連結值所參考的目標物件已回收。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**錯誤 \_ DS 不 \_ 允許的 NC 重新 \_ \_ 導向**
</dt> <dd> <dl> <dt>

8640 (0x21C0) 
</dt> <dt>



重新導向作業失敗，因為目標物件位於與目前網域控制站的網域 NC 不同的 NC 中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR \_ DS \_ HIGH \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1) 
</dt> <dt>



AD LDS 設定集的功能等級無法降到要求的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**錯誤 \_ DS \_ 高 \_ DSA \_ 版本**
</dt> <dd> <dl> <dt>

8642 (0x21C2) 
</dt> <dt>



網域 (或樹系) 的功能等級無法降到要求的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**錯誤 \_ DS \_ 低 \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3) 
</dt> <dt>



因為有一或多個 ADLDS 實例位於較不相容的功能等級，所以無法將 AD LDS 設定集的功能層級提升為要求的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ \_ \_ 與 \_ 本機工作站相同的 \_ 網域 SID 錯誤**
</dt> <dd> <dl> <dt>

8644 (0x21C4) 
</dt> <dt>



無法完成加入網域，因為您嘗試加入的網域 SID 等同于這部電腦的 SID。 這是作業系統安裝未正確複製的徵兆。 您應該在這部電腦上執行 sysprep，才能產生新的電腦 SID。 請參閱 <https://go.microsoft.com/fwlink/p/?linkid=168895> 以取得詳細資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**錯誤 \_ DS 取消 \_ 刪除 \_ SAM \_ 驗證 \_ 失敗**
</dt> <dd> <dl> <dt>

8645 (0x21C5) 
</dt> <dt>



取消刪除作業失敗，因為正在刪除之物件的 Sam 帳戶名稱或其他 Sam 帳戶名稱與現有的即時物件相衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**錯誤 \_ 的 \_ 帳戶 \_ 類型不正確**
</dt> <dd> <dl> <dt>

8646 (0x21C6) 
</dt> <dt>



系統不是指定帳戶的授權，因此無法完成操作。 請使用與此帳戶相關聯的提供者重試操作。 如果這是線上提供者，請使用提供者的線上網站。


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

 

 




