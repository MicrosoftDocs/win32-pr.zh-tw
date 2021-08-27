---
title: 'EAP 認證登入要求 \_ \_ \_ (Eaptypes .h) '
description: 在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719abbed6c16deb6d3bfd61811f3f24253181364fe89f5823ee682bafef001e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785621"
---
# <a name="eap_cred_logon_req"></a>EAP 認證登入要求 \_ \_ \_

**Eap 認證 \_ \_ 登 \_** 入要求結構會將 Eap 安全性認證儲存在 [**eap \_ CONFIG \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中。


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**EAP 認證登入要求 \_ \_ \_**
</dt> <dd>

Eap **驗證 \_ \_ 登 \_** 入要求結構會在 eap 互動式 ui [**\_ \_ \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證要求類型時，儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的 eap 安全性認證。 此結構中的輸入欄位與 [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)所傳回的輸入欄位相同。 **EAP \_認證 \_ 登 \_** 入要求用於初始認證要求中，而 [**EAP \_ \_**](eap-cred-req.md) 認證要求則用於驗證期間的認證重試要求。

</dd> </dl>

## <a name="remarks"></a>備註

**EAP 認證 \_ \_ 登 \_** 入要求結構是用來支援單一登入 (SSO) 。

**Eap 認證 \_ \_ 登 \_** 入要求結構與 [**eap 認證登入 \_ \_ \_ RESP**](eap-cred-logon-resp.md)結構相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP \_ 認證 \_ 需求**](eap-cred-req.md)
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





