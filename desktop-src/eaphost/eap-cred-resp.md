---
title: 'EAP \_ 認證 \_ RESP (Eaptypes .h) '
description: '在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。 |EAP \_ 認證 \_ RESP (Eaptypes .h) '
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b9bda55ed1b4aee9a9847740b25d46418c6ec3544dfdd6ba71b2c282042b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904635"
---
# <a name="eap_cred_resp"></a>EAP \_ 認證 \_ RESP

**Eap 認證 \_ \_ RESP** 結構會在 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中儲存 eap 安全性認證。


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**EAP \_ 認證 \_ RESP**
</dt> <dd>

Eap [**\_ 互動式 \_ ui \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證回應類型時， **eap 認證 \_ \_ RESP** 結構會儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的舊和新 EAP 安全性認證。

</dd> </dl>

## <a name="remarks"></a>備註

**EAP 認證 \_ \_ RESP** 結構是用來支援單一登入 (SSO) 。

**Eap 認證 \_ \_ RESP** 結構與 [**eap 認證 \_ \_ 需求**](eap-cred-req.md)結構相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 要求者結構](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ 認證 \_ 需求**](eap-cred-req.md)
</dt> <dt>

[**EAP \_ 認證 \_ 到期 \_ 申請**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ 認證 \_ 到期 \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

