---
title: EAPHost 對等方法結構
description: 瞭解 EAPHost 對等方法 API 結構，例如 EapCertificateCredential 和 EapSimCredential。
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968119"
---
# <a name="eaphost-peer-method-structures"></a>EAPHost 對等方法結構

EAPHost 對等方法 API 結構如下所示。



| 結構                                                              | Description                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | 包含 EAP 方法用來進行驗證之憑證的相關資訊。                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | 包含認證類型和適當認證的相關資訊。 這會以輸入的形式傳遞至 [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API。 |
| [**EAP \_ 對等 \_ 方法 \_ 常式**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | 包含一組指向 EAPHost 對等方法 Api 的函式指標。                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | 包含 EAP 對等方法所傳回的動作資訊。                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | 包含驗證期間 EAP 方法所產生的結果資料。                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | 包含 EAP 方法用來進行驗證之 SIM 的相關資訊。                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | 包含 EAP 方法用來驗證使用者的使用者名稱和密碼。                                                                                                     |



 

 

 




