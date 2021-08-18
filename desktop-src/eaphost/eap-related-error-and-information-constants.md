---
title: 'EAP 相關的錯誤和資訊常數 (Eaphosterror .h) '
description: 所有 EAPHost API 技術通用的 EAP 相關錯誤和資訊常數的個別群組。
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4140444d1b5c3ae99c90c2447e165a4143b042dcc7567104e4b5f0063b645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984238"
---
# <a name="eap-related-error-and-information-constants"></a>EAP 相關的錯誤和資訊常數

所有 EAPHost API 技術通用的 EAP 相關錯誤和資訊常數的個別群組。

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ EAPHost \_ FIRST** 和 **eap \_ e \_ EAPHost \_** 之間，會發生任何 EAPHost 相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST \_ LAST** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ EAPHost \_ FIRST** 和 **eap \_ e \_ EAPHost \_** 之間，會發生任何 EAPHost 相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST \_ FIRST** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



定義資訊報告的界限;所有 EAPHost 相關的資訊事件記錄都會出現在 **EAP \_ i \_ EAPHost \_ FIRST** 和 **eap EAPHost 的 \_ \_ \_ 最後**。


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**\_ \_ EAPHOST \_ 前的 EAP**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



定義資訊報告的界限;所有 EAPHost 相關的資訊事件記錄都會出現在 **EAP \_ i \_ EAPHost \_ FIRST** 和 **eap EAPHost 的 \_ \_ \_ 最後**。


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_無法存取 EAP E \_ CERT \_ STORE \_**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



驗證者或對等都不能存取證書存儲。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ 未安裝 EAP E EAPHOST \_ 方法**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



未安裝要求的 EAP 方法。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHOST \_ THIRDPARTY \_ 方法 \_ 主機 \_ 重設**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



協力廠商方法的主機沒有回應，且已自動重新開機。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**\_無法存取 EAP E \_ EAPHOST \_ EAPQEC \_**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost 無法與 EAP [隔離強制用戶端](/windows/desktop/NAP/nap-client-architecture) 通訊 (QEC) 在 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) 上 (NAP) 啟用的用戶端。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP \_ E \_ EAPHOST 身分 \_ 識別 \_ 不明**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



如果驗證器在送出對等身分識別之後驗證失敗，EAPHost 就會傳回這個錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP \_ E \_ 驗證 \_ 失敗**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost 會在驗證失敗時傳回這個錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP \_ I \_ EAPHOST \_ EAP \_ 協商 \_ 失敗**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



當用戶端和伺服器未設定相容的 EAP 類型時，EAPHost 會記錄此資訊事件。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP \_ E \_ EAPHOST \_ 方法 \_ 不正確封 \_ 包**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



EAP 方法收到無法處理的 EAP 封包。 **Eap \_ E \_ EAPHOST \_ 方法 \_ \_** 的另一個名稱不正確封包是 **eap \_ 方法 \_ 無效 \_** 的封包。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP \_ E \_ EAPHOST \_ 遠端 \_ 不正確封 \_ 包**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost 收到無法處理的封包。 **Eap \_ E \_ EAPHOST \_ 遠端 \_ 無效封 \_ 包** 的另一個名稱是 **eap \_ 無效 \_** 的封包。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHOST \_ XML \_ 格式不正確** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



EAPHost 設定架構驗證失敗。


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP \_ E \_ 方法設定不 \_ \_ \_ \_ 支援 \_ SSO**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 或更新版本： EAP 方法不支援提供的設定 (SSO) 的單一登入。


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_ \_ 不支援 EAP E EAPHOST \_ 方法 \_ 操作 \_ \_**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



當設定的 EAP 方法不支援要求的作業時，EAPHost 會傳回此錯誤 (程序呼叫) 。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ 電子 \_ 使用者 \_ 第一**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 第一次** 與 **eap \_ e \_ 使用者 \_** 之間，會發生任何使用者相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ 使用者 \_ 上次** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 第一次** 與 **eap \_ e \_ 使用者 \_** 之間，會發生任何使用者相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ 使用者 \_ 優先**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



定義資訊報告的界限;任何 EAP 相關的資訊事件記錄都會出現在 **eap \_ i \_ 使用者 \_ 第一次** 與 **eap \_ i \_ 使用者 \_** 之間。


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**最近的 EAP \_ \_ 使用者 \_**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



定義資訊報告的界限;任何 EAP 相關的資訊事件記錄都會出現在 **eap \_ i \_ 使用者 \_ 第一次** 與 **eap \_ i \_ 使用者 \_** 之間。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ \_ \_ \_ 找不到 EAP 電子使用者憑證**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost 找不到使用者憑證進行驗證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E \_ 使用者 \_ 憑證 \_ 無效**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



要驗證使用者的使用者憑證沒有適當的擴充金鑰使用方法 (EKU) 集。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E \_ 使用者憑證已 \_ \_ 過期**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost 找到過期的使用者憑證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP \_ E \_ 使用者憑證已 \_ \_ 撤銷**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



用於驗證的使用者憑證已撤銷。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP \_ E \_ 使用者 \_ 憑證 \_ 其他 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



使用使用者認證進行驗證時發生未知的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_拒絕 EAP 電子 \_ 使用者憑證 \_ \_** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



驗證者拒絕了使用者認證。


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP \_ 我的 \_ 使用者 \_ 帳戶 \_ 其他 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



識別交換之後收到 EAP 失敗，指出驗證使用者帳戶發生問題的可能性。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_拒絕 EAP 電子 \_ 使用者 \_ 認證 \_**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



驗證器已拒絕驗證的使用者認證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**拒絕的 EAP \_ 電子 \_ 使用者 \_ 名稱 \_ 密碼 \_**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 或更新版本：驗證失敗。 驗證者拒絕了使用者認證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ 電子 \_ 沒有 \_ 智慧 \_ 卡 \_ 讀卡機**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 或更新版本：找不到智慧卡讀卡機。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ SERVER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ Server \_ FIRST** 與 **eap \_ e \_ server \_** 之間，會發生任何伺服器相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ Server \_ FIRST** 與 **eap \_ e \_ server \_** 之間，會發生任何伺服器相關錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ \_ \_ \_ 找不到 EAP 電子伺服器憑證**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost 找不到伺服器憑證以進行驗證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E \_ 伺服器 \_ 證書 \_ 無效**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



用來驗證使用者的伺服器憑證沒有適當的擴充金鑰使用方式 (EKU) 集。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP \_ E \_ 伺服器 \_ 證書已 \_ 過期**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost 找到過期的伺服器憑證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E \_ 伺服器 \_ 證書已 \_ 撤銷**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



用於驗證的伺服器憑證已撤銷。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP \_ E \_ SERVER \_ CERT \_ 其他 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



伺服器憑證發生未知的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 根憑證 \_ \_ 第一** 次與 **eap \_ e \_ 使用者 \_ 跟 \_ 證書 \_** 之間，會發生任何使用者根憑證相關的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ LAST**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 根憑證 \_ \_ 第一** 次與 **eap \_ e \_ 使用者 \_ 跟 \_ 證書 \_** 之間，會發生任何使用者根憑證相關的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 EAP E 使用者根憑證**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost 在受信任的根憑證存放區中找不到用於使用者認證驗證的憑證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ 無效**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



驗證失敗，因為用於此網路的根憑證無效。


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書已 \_ 過期**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



使用者憑證驗證所需的受信任根憑證已過期。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 第一個**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



定義錯誤報表的界限;系統會先將 **eap \_ e \_ server \_ 根憑證 \_ \_ 第一個** 與 **eap \_ e \_ server \_ 跟 \_ \_** 證書之間發生任何伺服器根憑證相關的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 最後**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



定義錯誤報表的界限;系統會先將 **eap \_ e \_ server \_ 根憑證 \_ \_ 第一個** 與 **eap \_ e \_ server \_ 跟 \_ \_** 證書之間發生任何伺服器根憑證相關的錯誤。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 EAP E 伺服器根憑證**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost 在伺服器憑證驗證的受信任根憑證存放區中找不到根憑證。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 無效** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



驗證失敗，因為伺服器電腦上此網路所需的伺服器憑證無效。


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_需要 EAP E \_ 伺服器 \_ 跟 \_ 證書 \_ 名稱 \_**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



驗證失敗，因為伺服器電腦上的憑證未指定伺服器名稱。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

某些錯誤有替代名稱：

-   **Eap \_ E \_ EAPHOST \_ 方法 \_ \_** 的另一個名稱不正確封包是 **eap \_ 方法 \_ 無效 \_** 的封包。
-   **Eap \_ E \_ EAPHOST \_ 遠端 \_ 無效封 \_ 包** 的另一個名稱是 **eap \_ 無效 \_** 的封包。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Eaphosterror。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常見的 EAPHost 常數](common-eap-host-error-constants.md)
</dt> </dl>

 

