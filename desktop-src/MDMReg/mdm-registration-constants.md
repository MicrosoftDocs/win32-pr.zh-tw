---
title: 'MDM 註冊錯誤值 (MDMRegistration .h) '
description: 下列是 MDM 註冊的錯誤值。
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff5c73941b0235788772522f5551f73faea30d06e91e582dcdbe97433ca85c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638458"
---
# <a name="mdm-registration-error-values"></a>MDM 註冊錯誤值

下列是 MDM 註冊的錯誤值。

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DATATYPE \_ 不符**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



資料類型不符合預期的資料類型。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER \_ E \_ 裝置 \_ 訊息 \_ 格式 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



不正確架構，來自伺服器的訊息格式錯誤。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**MENROLL \_ E \_ 裝置 \_ 訊息 \_ 格式 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



不正確架構，來自伺服器的訊息格式錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER \_ E \_ 裝置 \_ 驗證 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



伺服器無法驗證使用者。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**MENROLL \_ E \_ 裝置 \_ 驗證 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



伺服器無法驗證使用者。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MREGISTER \_ E \_ 裝置 \_ 授權 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



使用者沒有註冊的授權。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**MENROLL \_ E \_ 裝置 \_ 授權 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



使用者沒有註冊的授權。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER \_ E \_ 裝置 \_ CERTIFCATEREQUEST \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



使用者沒有憑證範本的許可權，或無法連線到憑證授權單位單位。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL \_ E \_ 裝置 \_ CERTIFCATEREQUEST \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



使用者沒有憑證範本的許可權，或無法連線到憑證授權單位單位。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER \_ E \_ 裝置 \_ CONFIGMGRSERVER \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



管理伺服器發生錯誤，例如資料庫存取錯誤。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL \_ E \_ 裝置 \_ CONFIGMGRSERVER \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



管理伺服器發生錯誤，例如資料庫存取錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER \_ E \_ 裝置 \_ INTERNALSERVICE \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



伺服器上發生未處理的例外狀況。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL \_ E \_ 裝置 \_ INTERNALSERVICE \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



伺服器上發生未處理的例外狀況。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER \_ E \_ 裝置 \_ INVALIDSECURITY \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



伺服器上發生未處理的例外狀況。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL \_ E \_ 裝置 \_ INVALIDSECURITY \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



伺服器上發生未處理的例外狀況。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**MREGISTER \_ E \_ 裝置 \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



未知的伺服器錯誤。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**MENROLL \_ E \_ 裝置 \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



未知的伺服器錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MREGISTER \_ E \_ 註冊 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



目前正在進行另一項註冊作業。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**MENROLL \_ E \_ 註冊 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



目前正在進行另一項註冊作業。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER \_ E \_ 裝置 \_ 已 \_ 註冊**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



不再使用。

**Windows 8.1：** 裝置已註冊。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**MENROLL \_ E \_ 裝置 \_ 已 \_ 註冊**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



已註冊該裝置。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER \_ E \_ 裝置 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



不再使用。

**Windows 8.1：** 裝置未註冊。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**MENROLL \_ E \_ 裝置 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



裝置未註冊。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ DISCOVERY 重新 \_ 導向**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



不再使用。

**Windows 8.1：** 需要重新導向。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER \_ E \_ 裝置 \_ 未 \_ 註冊 AD 的 \_ \_ 錯誤**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



不再使用。

**Windows 8.1：** 裝置未向 Active Directory 註冊。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL \_ E \_ DISCOVERY \_ SEC \_ CERT \_ 日期 \_ 無效**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



在探索期間，sec cert 日期無效。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MREGISTER \_ E \_ 探索 \_ 失敗**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



不再使用。

**Windows 8.1：** 探索失敗;需要重新導向。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_需要 MENROLL E \_ 密碼 \_**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



需要密碼，但未提供。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**MENROLL \_ E \_ WAB \_ 錯誤**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



在 WAB 註冊期間發生錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL \_ E 連線 \_ 能力**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



發生網路錯誤，例如 DNS 或網路延遲。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**已 \_ 暫停 MENROLL 的 \_ 註冊 \_**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



註冊已暫止。 不再支援。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



SSL 憑證無效。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ >DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



使用者已註冊太多裝置。 刪除或取消註冊舊的舊版本，以修正此錯誤。 請注意，使用者可以在沒有系統管理員協助的情況下解決此錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

顯示0x80180014
</dt> <dt>



不支援特定平臺 (例如 Windows) 或版本。 此錯誤的一般修正是升級裝置。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



此裝置通常不支援行動裝置管理-使用者可以呼叫系統管理員，但不太可能會解決此問題。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



裝置正在嘗試更新，但伺服器已拒絕要求。 檢查裝置上的時間。 使用者可以藉由重新註冊來解決此錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ INMAINTENANCE**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



帳戶正在進行維護;請稍後重試。 使用者可以稍後重試。 不過，使用者可以選擇呼叫系統管理員來決定維護排程。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



使用者的授權處於不正確的狀態封鎖註冊;使用者必須呼叫系統管理員。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



伺服器已拒絕註冊資料;伺服器可能未正確設定。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



伺服器要求 HTTP 而非 HTTPS，但不接受。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**MENROLL \_ E \_ 平臺 \_ 錯誤 \_ 狀態**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



嘗試的作業無效，例如嘗試註冊相同的裝置兩次或取消註冊不明的裝置。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**MENROLL \_ E \_ PLATFORM \_ 授權 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



用戶端上安裝的 Windows 版本不支援此註冊類型。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**MENROLL \_ E \_ 平臺 \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



用戶端上發生未知的錯誤。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ >PROV \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



憑證存放區 CSP 中的布建失敗。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ >prov \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



在 W7/DMAcc CPP 中布建失敗。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ >PROV \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



在 DM 用戶端 CSP 中布建失敗。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ >PROV \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Passport for Work CSP 中的布建失敗。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ >PROV \_ CSP \_ 其他**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



在未列于上面的 CSP 中布建失敗。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ >PROV \_ 不明**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



布建失敗，但未指出特定的 CSP。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ >PROV \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



嘗試系結公開憑證/私密金鑰時，找不到公用憑證：嘗試系結公用憑證/私密金鑰時，或在查看布建承載時 (可能以錯誤的存放區) 為目標。

**Windows 8.1：** Windows 10 之前無法使用這個常數。


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ >PROV \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



EnterpriseAppManagement CSP 中的布建失敗。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**MENROLL \_ E \_ 裝置 \_ 管理已 \_ 封鎖**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



已封鎖行動裝置管理 (MDM) ，可能是群組原則或 [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) 函數。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL \_ E \_ CERTPOLICY \_ PRI加值稅EKEYCREATION \_ 失敗**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



無法建立私密金鑰。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ 無法 \_ \_ 找到 \_ CERT**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



已要求憑證驗證，但無法找到要使用的憑證。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ EMPTY \_ MESSAGE**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



伺服器已回應 HTTP 200，但訊息是空的。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ 使用者 \_ 已取消** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



使用者已取消操作。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**\_ \_ \_ 未設定 MENROLL 電子 \_ MDM**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



未設定 (MDM) 的 Mobile 裝置管理。

> [!Note]  
> 在 Windows 10 1709 版之前無法使用這個常數。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                    |
| 標頭<br/>                   | <dl> <dt>MDMRegistration。h</dt> </dl> |



 

 





