---
title: EAPHost API 參考
description: 瞭解 EAPHost Api 及其元件。 請參閱各種 API 主題的參考資訊，例如 EAPHost XML 架構。
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c522698999bcb58b4e33b8e1cb0d1bb74ae64fc3b709ce672b35e7db81e85ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739098"
---
# <a name="eaphost-api-reference"></a>EAPHost API 參考

EAPHost Api 分為三個元件：要求者 Api，可從已啟用 EAP 的應用程式直接呼叫;EAP 對等方法 Api，可管理特定 EAP 驗證類型的要求者要求，並在用戶端上引發互動式元素;和 EAP 驗證器 API，可執行要求者的伺服器端驗證。

後兩個 API 元件--eap 對等方法和 eap Authenticator 方法 api--在將它們公開給 EAPHost 服務的 dll 中，需要有自訂且一致的執行。 您無法直接從應用程式程式碼呼叫它們;相反地，它們是由用戶端上的 EAPHost (的 EAP 對等方法，以及 EAP 驗證器方法的伺服器端所呼叫) 如果執行是否符合對應檔中指定的 API 簽章。 每個函式參考頁面上都會提供 API 實行的特定資訊。

## <a name="eaphost-registry-settings"></a>EAPHost Registry 設定



| 主題                                                      | 描述                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [EAPHost Registry 設定](eaphost-registry-settings.md) | 描述 EAPHost 所使用的登錄機碼。 |



 

## <a name="eaphost-xml-schema"></a>EAPHost XML 架構



| 主題                                            | 描述                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost 和舊版架構](eaphost-schemas.md) | 描述用於建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。 |



 

## <a name="common-eaphost-api-reference"></a>Common EAPHost API 參考



| 主題                                                                   | 描述                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [常見的 EAPHost API 列舉](common-eap-host-api-enumerations.md) | 列出所有 EAPHost Api 通用的常數。  |
| [常見的 EAPHost API 結構](common-eap-host-api-structures.md)     | 列出所有 EAPHost Api 通用的結構。 |
| [常見的 EAPHost API 常數](common-eap-host-error-constants.md)     | 列出所有 EAPHost Api 通用的常數。  |



 

## <a name="eaphost-api-reference"></a>EAPHost API 參考



| 主題                                                                       | 描述                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [EAPHost 要求者 API 參考](eap-host-supplicant-api-reference.md)   | 描述可讓要求者呼叫 EAPHost 的 API 元素。                                                                      |
| [EAPHost 對等方法 API 參考](eap-host-peer-method-api-reference.md) | 描述必須實作為的 API 元素，以建立可由用戶端 EAPHost 載入和呼叫的 EAP 對等方法 DLL。          |
| [EAPHost Authenticator 方法 api](eaphost-authenticator-method-apis.md)  | 描述必須執行的 API 專案，以建立可由伺服器 EAPHost 載入和呼叫的 EAP 驗證器方法 DLL。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 EAPHost](about-eap-host.md)
</dt> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> </dl>

 

 




