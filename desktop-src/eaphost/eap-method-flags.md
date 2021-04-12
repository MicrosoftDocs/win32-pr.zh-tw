---
title: 'EAP 方法旗標 (Eaptypes .h) '
description: EAP 方法旗標用於要求者、驗證器和對等函式中，以指定 EAP 驗證會話的行為。
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464177"
---
# <a name="eap-method-flags"></a>EAP 方法旗標

EAP 方法旗標用於要求者、驗證器和對等函式中，以指定 EAP 驗證會話的行為。

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP \_ 旗標 \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP \_ 旗標 \_ 非 \_ 互動式**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



請勿顯示 (UI) 的使用者介面。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP \_ 旗標 \_ 登入**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



使用者資料是從 Windows 登入取得的。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP \_ 旗標 \_ 預覽**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



在驗證之前顯示認證 UI，即使快取的認證存在也一樣。


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_旗標 \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP \_ 旗標 \_ 電腦 \_ 驗證**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



使用機器層級驗證;未設定此旗標表示正在使用使用者層級驗證。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP \_ 旗標 \_ 來賓 \_ 存取**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



表示提供來賓存取權的要求。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP \_ 旗標 \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_旗標 \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP \_ 旗 \_ 標 \_ 從 \_ 休眠狀態繼續**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



表示這是機器活動從休眠期間繼續進行的第一次呼叫。


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_旗標 \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP \_ 旗標 \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP \_ 旗標 \_ 完整 \_ 驗證**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



表示通道方法應該執行完整驗證，而不是簡短版本，例如 [受保護的 EAP (PEAP) 快速重新](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10))連線。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP \_ 旗標 \_ 偏好 \_ 替換 \_ 認證**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



指出所有其他形式的認證抓取都偏好傳遞至 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 的認證，即使傳遞到目前函式的設定資料要求不同的認證抓取模式也是一樣。

> [!Note]  
> 此旗標僅供 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)使用。

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP \_ 旗標 \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP \_ 對等 \_ 旗標 \_ 健全狀況 \_ 狀態 \_ 變更**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



指出重新驗證的原因是 (NAP) 回呼的 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) ;因為健全狀況狀態變更，所以 NAP 起始了驗證會話。 只有當先前呼叫這個函式所提供的 NAP 特定 [*NotificationHandler*](/previous-versions/windows/desktop/api) 回呼呼叫這個函式時，才必須傳送此旗標。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP \_ 旗標 \_ 抑制 \_ UI**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



繼續以可用資訊進行驗證。 如果驗證無法繼續，則會失敗。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP \_ 旗標 \_ 預先 \_ 登入**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



表示 EAPHost 應該提供單一登入 (SSO) 。 如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP \_ 旗標 \_ 使用者 \_ 驗證**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



表示無法設定 **EAP \_ 旗標 \_ 電腦 \_ 驗證** 之舊版方法的使用者層級驗證。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP \_ 旗標 \_ SAMPLEPAGE.DLL.CONFG \_ READONLY**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



表示可查看但未更新的設定。


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP \_ 旗標 \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



請勿使用。 保留供未來使用。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常見的 EAPHost 常數](common-eap-host-error-constants.md)
</dt> </dl>

