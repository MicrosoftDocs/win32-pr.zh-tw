---
title: EAPHost 要求者設定函數
description: 瞭解 EAPHost 要求者設定函數，例如 EapHostPeerConfigBlob2Xml 和 EapHostPeerGetMethods。
ms.assetid: 92a1df11-10f9-4e55-a7ec-db026aaf5c24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e535b423f1d28afe72dbe52b0dc000d612977f85f325da8821858fe6d2326be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785495"
---
# <a name="eaphost-supplicant-configuration-functions"></a>EAPHost 要求者設定函數

EAP 要求者 API 設定函數如下所示。



| 函式                                                                                                           | 描述                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigblob2xml)                                                 | 將設定 blob 轉換為 XML。                                                                                                                                                                                                                                              |
| [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)                                                 | 將 XML 轉換成設定 blob。                                                                                                                                                                                                                                            |
| [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)                                       | 產生認證 BLOB。                                                                                                                                                                                                                                                      |
| [**EapHostPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory)                                               | 釋出配置給 [**EAP \_ 錯誤**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error) 結構的記憶體。                                                                                                                                                                                                              |
| [**EapHostPeerFreeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                                                         | 釋出設定 Api 所傳回的記憶體。 此函數不能用來釋放錯誤記憶體。 若要釋放錯誤記憶體，請使用 [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) 或 [**EapHostPeerFreeErrrorMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) 函數。 |
| [**EapHostPeerGetMethodProperties**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethodproperties)                                           | 取得指定連接和使用者資料的 EAP 方法屬性。                                                                                                                                                                                                            |
| [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods)                                                         | 列舉所有已安裝且可供使用的 EAP 方法，包括舊版的 EAP 方法。                                                                                                                                                                                            |
| [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)                                                     | 啟動指定 EAP 方法的設定使用者介面。                                                                                                                                                                                                                 |
| [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui)                                                 | 啟動身分識別使用者介面。                                                                                                                                                                                                                                                  |
| [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)                                       | 提供使用者的認證互動，例如智慧卡和 PIN。                                                                                                                                                                                            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                             | 可讓使用者判斷執行驗證的方法所需的認證類型。 它也會取得要在使用者介面中顯示的欄位。                                                                                                       |
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                       | 取得要在要求者上引發之互動式使用者介面元件的輸入欄位。                                                                                                                                                                                       |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)       | 將使用者資訊轉換成可由 EAPHost 執行時間函數取用的使用者 BLOB。                                                                                                                                                                                          |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) | 從單一登入使用者介面收到使用者輸入之後，取得可使用的認證 BLOB 開始驗證。                                                                                                                                 |



 

 

 