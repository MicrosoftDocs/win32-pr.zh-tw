---
title: 'EAP \_ 認證 \_ 登入 \_ RESP (Eaptypes .h) '
description: '在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。 |EAP \_ 認證 \_ 登入 \_ RESP (Eaptypes .h) '
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000552"
---
# <a name="eap_cred_logon_resp"></a>EAP \_ 認證 \_ 登入 \_ RESP

**Eap 認證 \_ 登 \_ 入 \_ RESP** 結構會在 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中儲存 eap 安全性認證。


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**EAP \_ 認證 \_ 登入 \_ RESP**
</dt> <dd>

Eap [**\_ 互動式 \_ ui \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證要求類型時， **eap 認證登入 \_ \_ \_ RESP** 結構會儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的 eap 安全性認證。 此結構中的輸入欄位會與 [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)所傳回的輸入欄位相同。 **EAP \_認證 \_ 登入 \_ RESP** 用於初始認證要求中，而 [**EAP \_ 認證 \_ RESP**](eap-cred-resp.md) 則用於驗證期間的認證重試要求。

</dd> </dl>

## <a name="remarks"></a>備註

**EAP 認證 \_ 登 \_ 入 \_ RESP** 結構是用來支援單一登入 (SSO) 。

**Eap 認證 \_ 登 \_ 入 \_ RESP** 結構等同于 eap 認證 [**\_ \_ 登 \_**](eap-cred-logon-req.md)入要求結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP 認證登入要求 \_ \_ \_**](eap-cred-logon-req.md)
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





