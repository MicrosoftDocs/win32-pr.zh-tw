---
description: 代表單一數位憑證。
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Certificate 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6c19acc094426f99599b9e4aa9ea3968414c7de1d99377b2ce0bd2e8e3fde05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877988"
---
# <a name="certificate-object"></a>Certificate 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**憑證** 物件代表單一 [*數位憑證*](../secgloss/d-gly.md)。

**憑證** 物件會公開下列介面：

-   **ICertificate** ：在 CAPICOM 1.0 中引進。
-   **ICertificate2** ：在 CAPICOM 2.0 中引進。

## <a name="when-to-use"></a>使用時機

**憑證** 物件是用來執行下列工作：

-   從檔案載入憑證資料（包括私密金鑰）。
-   從憑證取得資訊。
-   傳回與憑證相關聯的基本條件約束、EKU、擴充屬性、延伸模組、金鑰使用方法、公開金鑰和範本物件。
-   判斷憑證是否有效，並檢查憑證主體私密金鑰的存取可用性。
-   顯示憑證。
-   匯入及匯出憑證。
-   將憑證儲存至檔案。
-   取得或設定描述憑證的屬性。

## <a name="members"></a>成員

**憑證** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**憑證** 物件有這些方法。



| 方法                                                       | 描述                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | 傳回 [**BasicConstraints**](basicconstraints.md) 物件，這個物件表示憑證的基本條件約束延伸。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                    |
| [**顯示**](certificate-display.md)                       | 顯示憑證。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                                                                                                                              |
| [**匯出**](certificate-export.md)                         | 將憑證複製到編碼的字串。 編碼的字串可以寫入檔案或匯入至新的 **憑證** 物件。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | 傳回 [**ExtendedKeyUsage**](extendedkeyusage.md) 物件，這個物件會指出有效的憑證擴充金鑰使用。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                        |
| [**ExtendedProperties**](certificate-extendedproperties.md) | 傳回憑證擴充屬性的集合。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                              |
| [**延伸模組**](certificate-extensions.md)                 | 傳回與憑證相關聯的延伸模組集合。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                          |
| [**GetInfo**](certificate-getinfo.md)                       | 從憑證抓取資訊。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                                                                                                          |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | 判斷憑證是否有與其相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                     |
| [**匯入**](certificate-import.md)                         | 從字串將先前編碼的憑證匯入到 **憑證** 物件中。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                                                              |
| [**IsValid**](certificate-isvalid.md)                       | 建立憑證的憑證驗證鏈，並傳回包含憑證有效狀態的 [**CertificateStatus**](certificatestatus.md) 物件。<br/>  (繼承自 **CertificateICertificate2ICertificate**)  |
| [**KeyUsage**](certificate-keyusage.md)                     | 傳回 [**KeyUsage**](keyusage.md) 物件，這個物件表示憑證的有效金鑰使用方式。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                                                                 |
| [**載入**](certificate-load.md)                             | 從檔案匯入憑證。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                                                               |
| [**PublicKey**](certificate-publickey.md)                   | 傳回 [**PublicKey**](publickey.md) 物件。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                                                 |
| [**儲存**](certificate-save.md)                             | 將憑證儲存至檔案。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                                                                 |
| [**範本**](certificate-template.md)                     | 傳回與憑證相關聯的範本。<br/>  (繼承自 **CertificateICertificate2**)                                                                                                                                            |



 

### <a name="properties"></a>屬性

**憑證** 物件具有這些屬性。



| 屬性                                                      | 存取類型           | 描述                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**封存**](certificate-archived.md)<br/>           | 讀取/寫入<br/> | 設定或抓取布林值，指出憑證是否已封存。<br/>  (繼承自 **CertificateICertificate2**)        |
| [**IssuerName**](certificate-issuername.md)<br/>       | 唯讀<br/>  | 抓取包含憑證簽發者名稱的字串。<br/>  (繼承自 **CertificateICertificate2ICertificate**)             |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | 讀取/寫入<br/> | 設定或抓取與憑證相關聯的私密金鑰。<br/>  (繼承自 **CertificateICertificate2**)                           |
| [**SerialNumber**](certificate-serialnumber.md)<br/>   | 唯讀<br/>  | 抓取包含憑證序號的字串。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                  |
| [**SubjectName**](certificate-subjectname.md)<br/>     | 唯讀<br/>  | 抓取包含憑證主體名稱的字串。<br/>  (繼承自 **CertificateICertificate2ICertificate**)            |
| [**指紋**](certificate-thumbprint.md)<br/>       | 唯讀<br/>  | 抓取包含憑證之 SHA-1 雜湊的十六進位字串。<br/>  (繼承自 **CertificateICertificate2ICertificate**)  |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | 唯讀<br/>  | 捕獲憑證有效性的開始日期。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | 唯讀<br/>  | 捕獲憑證有效性的結束日期。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                   |
| [**版本**](certificate-version.md)<br/>             | 唯讀<br/>  | 捕獲憑證的版本號碼。<br/>  (繼承自 **CertificateICertificate2ICertificate**)                                 |



 

## <a name="remarks"></a>備註

您可以建立 **憑證** 物件，並且可以安全地進行腳本處理。 **憑證** 物件的 ProgID 是「CAPICOM」。Certificate. 2 "。

**CAPICOM 1。*x*：** **憑證** 物件的 ProgID 是「CAPICOM」。Certificate. 1 "。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
