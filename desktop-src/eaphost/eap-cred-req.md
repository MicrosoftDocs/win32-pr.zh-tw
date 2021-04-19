---
title: 'EAP \_ 認證 \_ 需求 (Eaptypes .h) '
description: '在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。 |EAP \_ 認證 \_ 需求 (Eaptypes .h) '
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000217"
---
# <a name="eap_cred_req"></a>EAP \_ 認證 \_ 需求

**Eap 認證 \_ \_ 需求** 結構會在 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中儲存 eap 安全性認證。


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**EAP \_ 認證 \_ 需求**
</dt> <dd>

Eap [**\_ 互動式 \_ ui \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證要求類型時， **eap 認證 \_ \_ 需求** 結構會儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的舊和新 EAP 安全性認證。

</dd> </dl>

## <a name="remarks"></a>備註

**EAP 認證 \_ \_ 需求** 結構是用來支援單一登入 (SSO) 。

**Eap 認證 \_ \_ 需求** 結構與 [**eap 認證 \_ \_ RESP**](eap-cred-resp.md)結構相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 要求者結構](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ 認證 \_ RESP**](eap-cred-resp.md)
</dt> <dt>

[**EAP \_ 認證 \_ 到期 \_ 申請**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ 認證 \_ 到期 \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

