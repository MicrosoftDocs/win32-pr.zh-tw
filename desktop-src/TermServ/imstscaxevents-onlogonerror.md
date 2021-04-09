---
title: IMsTscAxEvents OnLogonError 方法
description: 發生登入錯誤或其他登入事件時呼叫。
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- OnLogonError 方法遠端桌面服務
- OnLogonError 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnLogonError 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686062"
---
# <a name="imstscaxeventsonlogonerror-method"></a>IMsTscAxEvents：： OnLogonError 方法

發生登入錯誤或其他登入事件時呼叫。

## <a name="syntax"></a>語法


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lError* \[在\]
</dt> <dd>

登入錯誤碼。 這份程式代碼清單並不詳盡。

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**仲裁 \_程式碼的 \_ \_ 選項** (-5 (0xFFFFFFFB) ) 


</dt> <dd>

Winlogon 正在顯示 **會話競爭** 對話方塊。

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**仲裁 \_程式碼 \_ 繼續 \_ 登** 入 (-2 (0xFFFFFFFE) ) 


</dt> <dd>

Winlogon 正在繼續進行登入程式。

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**仲裁 \_程式碼 \_ 繼續 \_ 終止** (-3 (0xFFFFFFFD) ) 


</dt> <dd>

Winlogon 以無訊息方式結束。

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**仲裁 \_程式碼 \_ NOPERM \_ 對話方塊** (-6 (0xFFFFFFFA) ) 


</dt> <dd>

Winlogon 正在顯示 [ **無許可權** ] 對話方塊。

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**仲裁 \_程式碼 \_ 拒絕 \_ 對話方塊** (-7 (0xFFFFFFF9) ) 


</dt> <dd>

Winlogon 顯示 [ **拒絕中斷** 連線] 對話方塊。

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**仲裁 \_程式碼 \_ RECONN \_ 選項** (-4 (0xFFFFFFFC) ) 


</dt> <dd>

Winlogon 正在顯示 [ **重新連接** ] 對話方塊。

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**錯誤 \_\_ \_ 拒絕程式碼存取** (-1 (0xffffffff) ) 


</dt> <dd>

使用者被拒絕存取。

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**登 \_ 入失敗 \_ 的 \_ 密碼錯誤** (0 (0x0) ) 


</dt> <dd>

登入失敗，因為登入認證無效。

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**登 \_ 入失敗的 \_ 其他** (2 (0x2) ) 


</dt> <dd>

發生另一個登入或後置登入錯誤。 遠端桌面用戶端會向使用者顯示登入畫面。

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**登 \_ 入無法 \_ 更新 \_ 密碼** (1 (0x1) ) 


</dt> <dd>

密碼已過期。 使用者必須更新其密碼，才能繼續登入。

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**登 \_ 入警告** (3 (0x3) ) 


</dt> <dd>

遠端桌面用戶端會顯示一個對話方塊，其中包含使用者的重要資訊。

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**狀態 \_帳戶 \_ 限制** (-1073741714 (0xC000006E) ) 


</dt> <dd>

使用者名稱和驗證資訊是有效的，但因為使用者帳戶的限制，而導致驗證遭到封鎖，例如時間限制。

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**狀態 \_登入 \_ 失敗** (-1073741715 (0xC000006D) ) 


</dt> <dd>

嘗試的登入無效。 這是因為使用者名稱不正確或驗證資訊不正確。

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**狀態 \_密碼 \_ 必須 \_ 變更** (-1073741276 (0xC0000224) ) 


</dt> <dd>

密碼已過期。 使用者必須更新其密碼，才能繼續登入。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在事件接收中執行此方法，以接收已發生登入錯誤的通知。

這份程式代碼清單並不詳盡。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





