---
title: EAPHost 對等方法設定函數
description: 深入瞭解 EAPHost 對等方法設定函數。 查看設定函數的清單，並查看其他可用的資源。
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968305"
---
# <a name="eaphost-peer-method-configuration-functions"></a>EAPHost 對等方法設定函數

EAP 對等方法 API 設定函數如下所示。



| 函式                                                                                                  | 描述                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | 將設定 blob 轉換為 XML。                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | 將 XML 轉換成設定 blob。                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | 將 XML 認證轉換為 BLOB。                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | 釋放 EapHost 對等 Api 所傳回的所有 EAP 錯誤特定記憶體。                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | 釋放 EAP 方法輸出參數所配置的所有記憶體。                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | 在用戶端上引發 EAP 方法的特定連接設定使用者介面對話方塊。                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | 引發自訂互動式使用者介面對話方塊，以取得用戶端上 EAP 方法的使用者識別資訊。                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | 針對用戶端上的 EAP 方法，引發自訂互動式使用者介面對話方塊。                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | 定義 EAP 方法特定函式的執行，此函式會取得該 EAP 方法的 EAP 單一登入 (SSO) 認證輸入欄位                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | 定義 EAP 要求者函式的執行，此函式會取得要在要求者上引發之互動式使用者介面元件的輸入欄位。                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | 將使用者資訊轉換成可供 EAPHost 執行時間函式使用的使用者 BLOB。                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | 定義 EAP 方法特定函式的執行，此函式會從 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) 結構產生 eap 使用者認證 blob，其中包含要求者使用者所提供的認證資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 對等方法 Run-Time 函式](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




