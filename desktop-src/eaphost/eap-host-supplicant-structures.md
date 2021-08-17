---
title: EAPHost 要求者結構
description: 瞭解 EAPHost 要求者 API 結構，例如 EAP 認證 \_ \_ 需求和 eap \_ 方法 \_ 屬性 \_ 陣列。
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904615"
---
# <a name="eaphost-supplicant-structures"></a>EAPHost 要求者結構

EAPHost 要求者 API 結構如下所示。



| 結構                                                                        | Description                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ 認證 \_ 需求**](eap-cred-req.md)                                           | 包含認證變更作業的新舊 EAP 認證。                                    |
| [**EAP \_ 認證 \_ RESP**](eap-cred-resp.md)                                         | 包含認證變更作業的新舊 EAP 認證。                                    |
| [**EAP \_ 認證 \_ 到期 \_ 申請**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | 包含認證到期作業的舊和新 EAP 認證                                     |
| [**EAP \_ 認證 \_ 到期 \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | 包含認證到期作業的舊和新 EAP 認證。                                    |
| [**EAP 認證登入要求 \_ \_ \_**](eap-cred-logon-req.md)                              | 包含網路驗證的 EAP 認證。                                                                 |
| [**EAP \_ 認證 \_ 登入 \_ RESP**](eap-cred-logon-resp.md)                            | 包含網路驗證的 EAP 認證。                                                                 |
| [**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | 包含在 EAP 要求者上引發之互動式使用者介面元件的設定資訊。            |
| [**EAP \_ 方法 \_ 屬性**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 或更新版本：表示方法屬性。                                                                    |
| [**EAP \_ 方法 \_ 屬性 \_ 陣列**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 或更新版本：包含方法屬性結構的陣列。                                                 |
| [**EAP \_ 方法 \_ 屬性 \_ 值**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 或更新版本：包含方法屬性值。                                                                |
| [**EAP \_ 方法 \_ 屬性 \_ 值 \_ BOOL**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 或更新版本：包含 BOOL 資料類型方法屬性值。                                                 |
| [**EAP \_ 方法 \_ 屬性 \_ 值 \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 或更新版本：包含 DWORD 資料類型方法屬性值。                                                |
| [**EAP \_ 方法 \_ 屬性 \_ 值 \_ 字串**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 或更新版本：包含 string 資料類型方法屬性值。                                               |
| [**EAPHOST \_ AUTH \_ 資訊**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | 描述 EAP 驗證程式之不同階段中目前的驗證資訊。          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | 包含 EAPHost 在驗證會話期間產生的結果資料，然後傳遞給 EAP 方法。 |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 或更新版本：包含 EAP 要求者 (NAP) 資訊的網路存取保護。                   |



 

 

 