---
title: 安全性認證
description: 安全性認證是通訊物件所擁有的一項辨識項，可用來建立或取得安全性權杖。
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Windows 的安全性認證 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5703d9f58e7fee57f1ce8465e0413a7ca3c246590b816e84f7419e80f6efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192759"
---
# <a name="security-credentials"></a>安全性認證

安全性認證是通訊物件所擁有的一項辨識項，可用來建立或取得安全性權杖。 因此，認證通常比安全性權杖長，且安全性權杖可視為安全性認證的運行時程表現。 認證的範例包括電腦憑證 (可在執行時間將其轉換成 x.509 安全性權杖) 或在網域的使用者名稱/密碼組 (，可用來取得) 的 Kerberos 安全性權杖。


認證會指定為 [安全性](security-bindings.md)系結的一部分。

下列 API 元素會搭配安全性認證使用。

| 回呼                                                                  | Description                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**WS \_ GET \_ CERT \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | 提供憑證給安全性執行時間。          |
| [**WS \_ 驗證 \_ 密碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | 驗證接收者端的使用者名稱/密碼組。 |



 



| 列舉型別                                                                                           | 描述                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**WS \_ CERT \_ 認證 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | 憑證認證的類型。                       |
| [**WS 使用者 \_ 名稱 \_ 認證 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | 使用者名稱/密碼認證的類型。                 |
| [**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Windows 整合式驗證認證的類型。 |



 



| 結構                                                                                                   | Description                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**WS \_ CERT \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | 所有憑證認證類型的抽象基底類型。                                                          |
| [**WS \_ 自 \_ 定義 \_ 憑證認證**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | 型別，用來指定要由回呼提供給應用程式的憑證認證。             |
| [**WS \_ 預設 \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | 輸入，以根據目前的執行緒 token 提供 Windows 整合式驗證認證。                  |
| [**WS 不 \_ 透明的 \_ WINDOWS 整合式 \_ \_ 驗證 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | 提供 Windows 整合式驗證認證的類型。                                                    |
| [**WS \_ 字串使用者 \_ 名稱 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | 提供以字串形式提供使用者名稱/密碼組的型別。                                                           |
| [**WS \_ 字串 \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | 以使用者名稱、密碼、網域字串提供 Windows 認證的類型。                                        |
| [**WS \_ 主體 \_ 名稱 \_ \_ 憑證認證**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | 使用憑證的主體名稱、存放區位置和存放區名稱來指定憑證認證的型別。 |
| [**WS \_ 指紋 \_ \_ 憑證認證**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | 類型，用來指定使用憑證指紋的憑證認證、儲存位置和存放區名稱。   |
| [**WS 使用者 \_ 名稱 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | 所有使用者名稱/密碼認證的抽象基底類型。                                                         |
| [**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | 所有與 Windows 整合式驗證搭配使用之認證類型的抽象基底類型。                          |



 

 

 




