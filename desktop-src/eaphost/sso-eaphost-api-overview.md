---
title: SSO EAPHost API 總覽
description: 提供支援單一登入 (SSO) 的 EAPHost Api 總覽。
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023427"
---
# <a name="sso-eaphost-api-overview"></a>SSO EAPHost API 總覽

本主題提供支援單一登入 (SSO) 的 EAPHost Api 總覽。 如需特定的 SSO 案例，請參閱 [Sso EAPHost 案例](why-eaphost-sso.md)。

## <a name="eaphost-enumerations"></a>EAPHost 列舉

下列列舉支援 SSO。



| 名稱                                                                    | 目的                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | 定義在查詢使用者認證時可使用的一組可能的輸入欄位類型。    |
| [**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | 指定提供給特定要求者 API 呼叫的互動式 UI 內容資料類型。 |



 

## <a name="eaphost-structures"></a>EAPHost 結構

下列資料結構支援 SSO。



| 名稱                                                                     | 目的                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | 包含與單一輸入欄位相關聯的資料。                                                                                                                         |
| [**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | 包含一組 [**EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) 結構，其中共同包含從使用者取得的使用者輸入欄位資料。 |
| [**EAP \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | 包含在 EAP 要求者上引發之互動式 UI 元件的設定資訊。                                                                                   |
| [**EAP \_ 認證 \_ 需求**](eap-cred-req.md)                                   | 包含認證變更作業的新舊 EAP 認證。                                                                                               |
| [**EAP \_ 認證 \_ RESP**](eap-cred-resp.md)                                 | 包含認證變更作業的新舊 EAP 認證。                                                                                               |
| [**EAP \_ 認證 \_ 到期 \_ 申請**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | 包含認證到期作業的舊和新 EAP 認證。                                                                                                 |
| [**EAP \_ 認證 \_ 到期 \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | 包含認證到期作業的舊和新 EAP 認證。                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>EAPHost 對等 (要求者) Api

下列要求者函數支援 SSO。

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)和 [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)函式是 SSO 專屬的。



| 名稱                                                                                                             | 目的                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 呼叫的順序 |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | 取得要在要求者上引發之互動式 UI 元件的輸入欄位。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | 可讓使用者判斷在 SSO 案例中執行驗證的方法需要何種認證。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | 將使用者資訊轉換成可供 EAPHost 執行時間函式使用的使用者 BLOB。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | 取得可用來從 SSO UI 接收的使用者輸入啟動驗證的認證 BLOB。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | 要求者使用 **EAP \_ 旗標 \_ 預先 \_ 登** 入旗標來指出 EAPHost 應該提供 SSO。 如果傳回 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) 動作碼，EAPHost 會呼叫 [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)，然後呼叫 [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> 如果未傳回 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) 動作碼，EAPHost 會繼續進行一般的非 SSO 呼叫順序。 如需詳細資訊，請參閱 [要求者 API 呼叫順序](supplicant-api-call-sequence.md)。<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>EAPHost 對等方法 Api

下列對等函數支援 SSO。

[**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)和 [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)函式是 SSO 專屬的。



| 名稱                                                                                                      | 目的                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 呼叫的順序 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | 定義 EAP 方法 API 的執行，以提供要在要求者上引發之互動式 UI 元件的輸入欄位。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | 定義 EAP 方法特定函式的執行，此函式會取得該 EAP 方法的 EAP SSO 認證輸入欄位。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | 將使用者資訊轉換成可供 EAPHost 執行時間函式使用的使用者 BLOB。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | 定義 EAP 方法函式的執行，此函式會取得要求者上引發的互動式 SSO UI 所提供的使用者 BLOB 資料。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | **EAP \_ 旗標 \_ 預先 \_ 登** 入旗標表示 EAPHost 應該提供 SSO。 在 SSO 案例中，如果傳回 **EapPeerResponseInvokeUI** 動作碼，EAPHost 會呼叫 [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)，然後呼叫 [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> 如果未傳回 **EapPeerResponseInvokeUI** 動作碼，EAPHost 會繼續進行一般的非 SSO 呼叫順序。 如需詳細資訊，請參閱 [對等方法 API 呼叫順序](peer-method-api-call-sequence.md)。<br/> | 3            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[SSO EAPHost 案例](why-eaphost-sso.md)
</dt> </dl>

 

