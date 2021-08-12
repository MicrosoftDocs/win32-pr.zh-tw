---
title: 'NAP 錯誤常數 (Winerror.h .h) '
description: 下列 NAP 錯誤常數定義于 Winerror.h 中。
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620837"
---
# <a name="nap-error-constants"></a>NAP 錯誤常數

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

下列 NAP 錯誤常數定義于 Winerror.h 中。

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E \_ 不正確封 \_ 包**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270001L) 
</dt> <dt>



NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包無效。


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ 遺失 \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270002L) 
</dt> <dt>



NAP 封包中缺少 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 。


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP \_ E \_ 衝突 \_ 識別碼**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270003L) 
</dt> <dt>



實體識別碼與已註冊的實體識別碼衝突。


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E 沒有快取的 \_ \_ \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270004L) 
</dt> <dt>



沒有快取的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 存在。


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ 仍系結 \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270005L) 
</dt> <dt>



實體仍系結至 NAP 系統。


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270006L) 
</dt> <dt>



實體未向 NAP 系統註冊。


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ 未 \_ 初始化**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270007L) 
</dt> <dt>



實體未使用 NAP 系統初始化。


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP \_ E 不符的 \_ \_ 識別碼**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270008L) 
</dt> <dt>



[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)要求和 **soh** 回應中的相互關聯識別碼不相符。


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ 未 \_ 擱置**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270009L) 
</dt> <dt>



在目前未暫止的要求上指出完成。


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ \_ \_ \_ 找不到 NAP E 識別碼**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000AL) 
</dt> <dt>



找不到 NAP 元件的識別碼。


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MAXSIZE \_ 太 \_ 小**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000BL) 
</dt> <dt>



連接的大小上限對於 SoH 封包而言太小。


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP \_ E \_ 服務 \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000CL) 
</dt> <dt>



NapAgent 服務未執行。


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP \_ S \_ 憑證 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x0027000DL)  
</dt> <dt>



憑證已存在於憑證存放區中。


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_ \_ \_ 已停用 NAP E 實體**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000EL) 
</dt> <dt>



已停用 NapAgent 服務的實體。


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP \_ E \_ NETSH \_ GROUPPOLICY \_ 錯誤**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000FL) 
</dt> <dt>



未設定群組原則。


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ 電子 \_ \_ 通話太多 \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270010L) 
</dt> <dt>



同時呼叫太多。


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP \_ E \_ SHV 設定已 \_ \_ 存在**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270011L) 
</dt> <dt>



SHV 設定已經存在。

> [!Note]  
> 在 Windows 7 或更新版本中支援。

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270012L) 
</dt> <dt>



找不到 SHV 設定。

> [!Note]  
> 在 Windows 7 或更新版本中支援。

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP \_ E \_ SHV \_ TIMEOUT**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270013L) 
</dt> <dt>



SHV 在要求時過期。

> [!Note]  
> 在 Windows 7 或更新版本中支援。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NAP 常數**](nap-constants.md)
</dt> </dl>

 

 





