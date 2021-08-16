---
description: 憑證服務提供可用於要求憑證的網頁註冊頁面。
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: 自訂憑證服務網頁註冊頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767793"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>自訂憑證服務網頁註冊頁面

[*憑證服務*](../secgloss/c-gly.md) 提供可用於要求憑證的網頁註冊頁面。 系統管理員可以自訂一些可在網頁註冊頁面中查看的專案;不過，在進行任何變更之前，您應該先熟悉網頁註冊頁面和 web 腳本。 如需 web 腳本的詳細資訊，請參閱 [腳本](/previous-versions/ms950396(v=msdn.10))。

[組織]、[組織單位]、[位置]、[狀態] 和 [國家/地區] 的 [辨別名稱] 欄位的預設值是安裝憑證服務時， (CA) 的 [*憑證授權單位*](../secgloss/c-gly.md) 單位所指定的值。 這些預設值會出現在網頁中，且使用者可以在憑證註冊程式期間變更這些預設值。 However, if you want other default values to appear in the webpages, you can edit the Certdat.inc file (in the path \\*WindowsDirectory*\\System32\\Certsrv\\); specifically, you can assign custom values to the following variables provided for customization.



| 變數            | 描述                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | 預設公司 (會在 [*憑證要求*](../secgloss/c-gly.md) 中顯示為 [ [*x.509*](../secgloss/x-gly.md) 組織] 欄位) 。 |
| sDefaultOrgUnit     | 預設部門 (在憑證要求中會顯示為 [x.509 組織單位] 欄位) 。                                                                                                                                           |
| sDefaultLocality    | 預設 city (在憑證要求中會顯示為 [x.509 位置] 欄位) 。                                                                                                                                                            |
| sDefaultState       | 預設的州/省 (在憑證要求中會顯示為 [x.509 狀態] 欄位) 。                                                                                                                                                     |
| sDefaultCountry     | 預設國家/地區 (在憑證要求中會顯示為 [x.509 國家/地區] 欄位) 。                                                                                                                                            |
| nPendingTimeoutDays | 要求之後，使用者可以取得擱置中憑證的天數。                                                                                                                                          |



 

Certdat inc. 檔案中不應變更其他變數。

下列範例會將預設的組織單位設為「行銷」。


```VB
sDefaultOrgUnit="Marketing"
```



此外，您可以編輯 Certrqtp 檔案，以新增、變更或移除使用者可用的 [*憑證範本*](../secgloss/c-gly.md) 或類型。 這些範本和類型以及相關資訊都包含在名為 rgAvailReqTypes (*m*，5) 的維度陣列中。

這個陣列（如同所有 Visual Basic 腳本版本的陣列）是以零為基礎，因此，陣列的第一個維度 *m* 會配置 *m*+ 1 專案的記憶體。 因此，如果在自訂網頁時，您需要修改 rgAvailReqTypes 陣列中的專案數，請將 *m* 維度設定為小於所需專案總數的1。 例如，如果您將有七個憑證範本，請變更 rgAvailReqTypes 的宣告，如下列範例所示。


```VB
Dim rgAvailReqTypes(6,5)
```



陣列的第二個維度（一律具有值五個）會配置構成每個專案的六個欄位。 這六個欄位代表憑證範本或類型、與此範本或類型相關聯的顯示名稱，以及範本是否需要 [*安全/多用途網際網路郵件延伸*](../secgloss/s-gly.md) (S/MIME) 。

為了讓您更容易瞭解存取了哪些欄位，Certrqtp 也提供下列常數，可讓您在設定域值時使用。



| 常數                              | 描述                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **欄位 \_ OID**                        |  (適用于獨立 Ca) 索引至專案的第一個欄位;代表憑證類型 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md) 。<br/>                                                                                                           |
| **欄位 \_ 範本**                   |  (適用于企業 Ca) 索引至專案的第一個欄位;代表憑證範本。<br/>                                                                                                                                                                                                                           |
| **欄位 \_ FRIENDLYNAME**               | 專案第二個欄位的索引;表示在註冊第一個欄位中的專案) 時，使用者會看到的顯示名稱 (。                                                                                                                                                                                               |
| **欄位 \_ 請 CSPLIST**                    | 專案第三個欄位的索引。 範本允許的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 名稱清單。 清單中的每個名稱都是以問號 (？ ) 分隔。                                                    |
| **欄位 \_ CSPLIST2**                   | 專案第四個欄位的索引。 範本允許的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 名稱的次要清單。 清單中的每個名稱都是以問號 (？ ) 分隔。 此清單提供不同的預設值。 |
| **欄位可 \_ 匯出**                 | 專案第五個欄位的索引。 指出範本是否會指定應該可匯出的金鑰。 如果此欄位包含 "True"，則金鑰可匯出。 如果此欄位包含 "False"，則無法匯出金鑰。                                                                                                        |
| **FIELD \_ 需要 \_ SMIME \_ 功能** | 不支援這個常數。                                                                                                                                                                                                                                                                                                      |



 

例如，下列運算式會將1.3.6.1.5.5.7.3.2 的 OID 指派給第一個專案的第一個欄位，並將「網頁瀏覽器憑證」指派給第一個專案的第二個欄位， (陣列值為零的第一個專案) 索引。


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



這些指派的結果是使用者會在註冊時看到文字 **Web 瀏覽器憑證** ，如果使用者選取 **網頁瀏覽器憑證**， [*憑證要求*](../secgloss/c-gly.md) 將會包含 OID 1.3.6.1.5.5.7.3.2。

Certrqtp inc. 檔案也包含用於憑證範本或類型之顯示名稱的常數。 下列範例顯示格式。


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



這些常數定義于 Certrqtp inc. 檔案的區塊中，而此群組可讓您更輕鬆地將自訂值指派給每個常數。 當您將國際版網頁的顯示名稱當地語系化時，這會特別有用。

最後，Certrqtp 檔案包含的變數代表 rgAvailReqTypes 陣列中的憑證範本數目或類型。 相對於陣列的 *m* 維度，請將 nAvailReqTypes 變數的值設定為您的安裝將會使用的憑證範本或類型的實際數目。此值不能大於 *m*+ 1。 雖然在 Certrqtp inc 檔案的頂端附近宣告，但 nAvailReqTypes 會在填入 rgAvailReqTypes 陣列後指派一個值，讓您更輕鬆地查看陣列實際使用的元素數目。 NAvailReqTypes 值用於網頁註冊頁面中其他位置的反復專案中，因此，此變數必須正確地反映您想要讓使用者看到的憑證範本或類型數目。

請注意，只會將 [*憑證範本*](../secgloss/c-gly.md) 和類型新增至 Certrqtp 檔案，並不保證使用者能夠取得具有這些特性的憑證;CA 必須獲得授權，才能針對指定的憑證範本或類型發出憑證。

安裝可以建立自己的應用程式或網頁來要求和接收憑證。 [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)和 [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)物件可讓程式設計人員或腳本撰寫者建立 [*憑證要求*](../secgloss/c-gly.md)應用程式。

若要要求在 [*智慧卡*](../secgloss/s-gly.md)上發行憑證，您可以使用智慧卡註冊控制項。 如需詳細資訊和範例程式碼，請參閱 [**ISCrdEnr**](iscrdenr.md)。

 

 
