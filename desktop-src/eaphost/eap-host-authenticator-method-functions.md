---
title: EAPHost Authenticator 方法函數
description: 瞭解 EAPHost Authenticator 方法 API 函式，例如 EapMethodAuthenticatorFreeErrorMemory。
ms.assetid: 319516ee-b21d-4375-8c90-e3abe0a457e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cc21d636c2a1b107897c3b000fca3f279288e13c14d1219f5b13515c2e8a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984268"
---
# <a name="eaphost-authenticator-method-functions"></a>EAPHost Authenticator 方法函數

EAPHost Authenticator 方法 API 函數如下所示。



| 函式                                                                                               | 描述                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession)                       | 在伺服器 EAPHost 上建立新的 EAP 驗證會話。                                                                                                                             |
| [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession)                           | 關閉伺服器 EAPHost 上的 EAP 驗證會話。                                                                                                                                 |
| [**EapMethodAuthenticatorFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory)                 | 釋放 EAP 驗證器方法所配置的錯誤特定記憶體。                                                                                                                   |
| [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)                     | 從 EAP 驗證器方法取得 EAP 驗證屬性的陣列。                                                                                                        |
| [**EapMethodAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetinfo)                                 | 取得一組函式指標，以進行載入的 EAP 驗證器方法的執行。                                                                                            |
| [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult)                             | 從 EAP 驗證器方法取得驗證結果。                                                                                                                        |
| [**EapMethodAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize)                           | 初始化伺服器 EAPHost 的 EAP 驗證器方法。                                                                                                                             |
| [**EapMethodAuthenticatorInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui)                   | 定義函式，此函式會在用戶端上引發 EAP 方法的連接設定使用者介面對話方塊。                                                                           |
| [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)                     | 處理伺服器 EAPHost 所接收的 EAP 驗證封包，並傳迴響應動作。                                                                                        |
| [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)                           | 從 EAP 驗證器方法取得要傳送給要求者的驗證封包。                                                                                               |
| [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)                     | 提供在 EAP 驗證器方法上設定的更新 EAP 驗證屬性。                                                                                                      |
| [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown)                               | 關閉 EAP 驗證器方法，並準備將它從伺服器 EAPHost 卸載。                                                                                                  |
| [**EapMethodAuthenticatorUpdateInnerMethodParams**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams) | 從伺服器 EAPHost 更新 [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) 的呼叫之前所建立的 EAP 驗證會話設定。 |



 

 

 




