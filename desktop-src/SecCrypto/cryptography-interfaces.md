---
description: 列出 CryptoAPI 提供的介面。
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: 密碼編譯介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5284f5c2107e741fd91e2936ff3dea0853e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318228"
---
# <a name="cryptography-interfaces"></a>密碼編譯介面

密碼編譯介面會根據使用方式進行分類，如下所示：

-   [伺服器引擎匯出介面](#server-engine-export-interfaces)
-   [伺服器引擎匯入介面](#server-engine-import-interfaces)
-   [編碼介面](#encoding-interfaces)
-   [憑證註冊介面](#certificate-enrollment-interfaces)
-   [CAPICOM 互通性介面](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>伺服器引擎匯出介面

下列參考主題描述由伺服器引擎匯出並由外部物件呼叫的介面。



| 介面                                                                | 描述                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | 管理程式用來管理要求、憑證及撤銷。                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | 管理程式用來管理要求、憑證及撤銷。 取代 [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)。                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | 供用戶端用來取得可用伺服器的相關資訊。                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | 供用戶端用來取得可用伺服器的相關資訊。 取代 [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)。                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | 提供用來抓取 [*憑證服務*](../secgloss/c-gly.md) 伺服器的用戶端安裝) 期間所指定之公用設定資料 (的功能。                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | 用來將要求傳送至伺服器，並取得要求的結果。                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | 用來將要求傳送至伺服器，並取得要求的結果。 取代 [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)。                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | 由結束 [模組](exit-modules.md) 用來取得憑證和要求屬性。                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | [原則模組](policy-modules.md)用來取得和設定憑證和要求屬性。                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | 供用戶端用來 [查看憑證服務資料庫](viewing-the-certificate-services-database.md)。                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | 供用戶端用來查看憑證服務資料庫。 取代 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)。                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | 用戶端用來存取憑證服務視圖中某個資料列的憑證屬性。                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | 用戶端用來存取憑證服務視圖中資料列的資料行。                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | 用戶端用來存取憑證服務視圖中某個資料列的憑證延伸資料。                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | 用戶端用來列舉憑證服務視圖的資料列。                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | 管理程式用來設定線上憑證狀態通訊協定 (OCSP) 回應程式伺服器。                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | 提供設定 OCSP 回應程式服務的功能，以處理特定 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 的狀態要求。<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | 提供功能來管理 OCSP 回應程式服務可以處理要求的 CA 設定。                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | 提供設定 OCSP 回應程式伺服器屬性的功能。                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | 管理程式用來管理 OCSP 回應者伺服器屬性。                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>伺服器引擎匯入介面

下列參考主題描述伺服器引擎所匯入的介面。



| 介面                                      | 描述                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | 由結束模組匯出。 由伺服器引擎用來傳遞完成的憑證和撤銷資訊。                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | 將 [**GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) 方法加入至 [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)。                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | 由原則或結束模組匯出。 用來顯示模組資訊，或顯示用於設定模組的使用者介面。 |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | 由原則模組匯出。 伺服器引擎用來檢查要求以及取得憑證的屬性。                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | 將 [**GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) 方法加入至 [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)。                         |



 

## <a name="encoding-interfaces"></a>編碼介面

下列參考主題描述可由 [擴充處理常式](writing-custom-extension-handlers.md) 匯出並由原則模組匯入的介面。



| 介面                                                | 描述                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | [原則模組](policy-modules.md)用來處理替代名稱延伸模組。                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | 原則模組用來處理憑證延伸中使用的位字串。                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | 原則模組用來處理憑證延伸中使用的 CRL) 散發資訊陣列 (CRL 的 [*憑證撤銷清單*](../secgloss/c-gly.md) 。 |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | 原則模組用來處理憑證延伸中使用的 **日期** 陣列。                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | 原則模組用來處理憑證延伸中使用的 **長** 陣列。                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | 原則模組用來處理憑證延伸中使用的 **字串** 陣列。                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>憑證註冊介面

本節說明憑證註冊控制項的物件、方法和屬性，以及智慧卡註冊控制項中可用的物件、方法和屬性。 這些包含下列介面。



| 介面                                                                                  | 描述                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，這主要是很重要的。                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，這主要是很重要的。                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，這主要是很重要的。                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | 代表 Active Directory 憑證服務 (ADC) 內 (CEP) Web 服務的憑證註冊原則。 服務可讓使用者和電腦取得憑證註冊原則資訊。 |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | 代表 ADC 中 (CES) 的憑證註冊 Web 服務。 服務可讓使用者和電腦註冊及更新憑證。                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，這主要是很重要的。                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，則此介面主要是很重要的。                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，則此介面主要是很重要的。                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | 代表憑證註冊控制項的數個介面之一。 如果您不是使用自動化，則此介面主要是很重要的。                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | 代表智慧卡註冊控制項。 如果您不是使用自動化，這主要是很重要的。                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>CAPICOM 互通性介面

下列參考主題描述的介面，可讓 CryptoAPI 衍生與 CAPICOM 2.0 一起運作。



| 介面                              | 描述                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertCoNtext**](icertcontext.md)   | 提供 CAPICOM x.509v3 [**憑證**](certificate.md) 物件內容的存取權。 此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。 |
| [**ICertStore**](icertstore.md)       | 提供 CAPICOM [**存放區**](store.md) 物件內容的存取權。 此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。               |
| [**IChainCoNtext**](ichaincontext.md) | 提供 CAPICOM [**鏈**](chain.md) 物件內容的存取權。 此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。         |



 

 

 
