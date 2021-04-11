---
description: 名稱屬性是憑證和憑證要求的屬性，代表主體的相關資料，也就是憑證的擁有者或要求憑證的個人。
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: 名稱屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c5978b3fe5ab7c6ead39840dfb1793372c5feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194738"
---
# <a name="name-properties"></a>名稱屬性

名稱屬性是憑證和憑證要求的屬性，代表主體的相關資料，也就是憑證的擁有者或要求憑證的個人。 每個名稱屬性都是以屬性名稱來識別。 這些名稱無法當地語系化;不過，[名稱] 屬性通常會對應至 [憑證服務] 資料庫資料行，而且您可以使用 [憑證授權單位單位] MMC 嵌入式管理單元、命令列工具 [certutil-schema] 或 [**IEnumCERTVIEWCOLUMN：： GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) 方法來顯示資料庫資料行名稱的當地語系化版本。

屬性名稱 (但不是別名) 可能有 "Subject"。 作為選擇性的前置詞。 例如，若要參考主體的一般名稱，您可以使用 "CommonName" 或 "Subject. CommonName"。

除了其名稱之外，每個屬性都有一些別名，憑證服務會將其辨識為屬性的替代名稱。 請注意， (oid) 的 [*物件識別碼*](../secgloss/o-gly.md)是可接受的別名，就像 **szOID \_ \* *_ 常數一樣。這些常數是 Wincrypt 中的定義， (在代表 Oid 的) 中。例如，_* szOID \_ 一般 \_ 名稱** 定義為 "2.5.4.3"。 因此，您可以使用 **szOID \_ \** _ 常數作為別名來取代它們所代表的 oid。



| 屬性名稱                 | 別名                                                                                                                                                        | 資料類型                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject. CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> _ * szOID \_ 一般 \_ 名稱 * *<br/>                                                                           | **字串** (最大64個字元)   | 針對使用者憑證，該人員的完整名稱。 若為電腦憑證，*網域名稱系統中使用的完整主機名稱 * **/** _路徑_ (DNS) 查閱 (例如 *主機名稱 ***。**_範例_*_.com_*) 。<br/>                                                                                                                                                                                                                                                                        |
| "Subject. Country"             | 「國家/地區」 "C"<br/> "2.5.4.6"<br/> **szOID \_ 國家/地區 \_ 名稱**<br/>                                                                              | **字串** (最多2個字元)     | 主體的國家或地區。 這是 [*X. 500*](../secgloss/x-gly.md) 兩個字元的國家/地區代碼 (例如美國或加拿大) 的 CA。<br/> 這兩個字元的程式碼中有許多是以 ISO 3166 標準定義。 此外，目前地區設定的程式碼可透過呼叫 Windows 函式 [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (，方法是指定地區設定 \_ SISO3166CTRYNAME) 的 LCType。<br/> |
| "Subject. DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **szOID \_ 裝置 \_ 序號 \_**<br/>                                                                         | **字串** (最大1024個字元)  | 裝置序號。                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **szOID \_ 網域 \_ 元件**<br/>                                              | **字串** (最大128個字元)   | 網域名稱系統的元件 (DNS) 名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "EMail" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **字串** (最大128個字元)   | 電子郵件地址 (例如「」 someone@example.com ) 。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. GivenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **szOID \_ 指定的 \_ 名稱**<br/>                                                                             | **字串** (最多16個字元)    | 主體的名字。                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | 「縮寫」 "I"<br/> "2.5.4.43"<br/> **szOID \_ 縮寫**<br/>                                                                                 | **字串** (最多5個字元)     | 主題 (選用) 的縮寫。                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject"            | "位置" "L"<br/> "2.5.4.7"<br/> **szOID \_ 位置 \_ 名稱**<br/>                                                                            | **字串** (最大128個字元)   | 主體城市的名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject"        | 「組織」 "Org"<br/> 輸出<br/> "2.5.4.10"<br/> **szOID \_ 組織 \_ 名稱**<br/>                                                  | **字串** (最大64個字元)    | 主體組織的法定名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. OrgUnit"             | "OrgUnit" "OrganizationUnit"<br/> OrganizationalUnit<br/> /OU<br/> 2.5.4.11<br/> **szOID \_ 組織 \_ 單位 \_ 名稱**<br/> | **字串** (最大64個字元)    | 主體的子組織或部門的名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. State"               | "State" "ST"<br/> ！<br/> "2.5.4.8"<br/> **szOID \_ 州 \_ 或 \_ 省 \_ 名稱**<br/>                                                    | **字串** (最大128個字元)   | 主體的州或省的全名 (例如加州) 。                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject. StreetAddress"       | "StreetAddress" "街道"<br/> "2.5.4.9"<br/> **szOID \_ 街道 \_ 位址**<br/>                                                                 | **字串** (最多30個字元)    | 主旨的街道位址或 PO 方塊。                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject"             | "姓氏" "SN"<br/> "2.5.4.4"<br/> **szOID \_ SUR \_ 名稱**<br/>                                                                                 | **字串** (最大40個字元)    | 主體的姓氏。                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. Title"               | "Title" "T"<br/> "2.5.4.12"<br/> **szOID \_ 標題**<br/>                                                                                       | **字串** (最大64個字元)    | 要求憑證之個人的標題 (選擇性) 。                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject. UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **字串** (最大1024個字元)  | 非結構化位址。                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. UnstructuredName"    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **字串** (最大1024個字元)  | 非結構化名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

下列屬性與主旨相關，雖然它們不是名稱屬性。 原則模組無法直接設定這些屬性。



| 屬性                    | 資料類型                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "DistinguishedName" | **字串** (最大8192個字元)  | 要求的 [*相對辨別名稱*](../secgloss/r-gly.md) ，這是要求中主旨的文字標記法。 此標記法由名稱屬性組成，例如 "CN = MyName，OU = MyOrgUnit，C = US"。 憑證服務應用程式會在呼叫原則模組之前設定這個屬性，方法是使用 RawRequest 的主體來呼叫 [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) 。 |
| "RawName"           | **Binary** (最大4096位元組)  | [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 從要求中解壓縮的二進位主體 [*BLOB*](../secgloss/b-gly.md) 。 憑證服務應用程式會先設定這個屬性，然後再呼叫原則模組。其值取決於 RawRequest 的主體。                                                                                     |
| DistinguishedName         | **字串** (最大8192個字元)  | 憑證的相對辨別名稱，即憑證中主體的文字標記法。 此標記法由名稱屬性組成，例如 "CN = MyName，OU = MyOrgUnit，C = US"。 憑證服務應用程式會在呼叫原則模組之後，藉由使用 RawName 呼叫 [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) 來設定這個屬性。                                                                                                               |
| "RawName"                   | **Binary** (最大4096位元組)  | 用來建立憑證的 asn.1 二進位主體 [*BLOB*](../secgloss/b-gly.md) 。 憑證服務應用程式會在呼叫原則模組之後設定此屬性;其值取決於特定名稱屬性的值 (CommonName 等) ，如同 SubjectTemplate 所指示。                                                                                                                                        |



 

DistinguishedName 屬性中會出現哪些 [*相對辨別名稱*](../secgloss/r-gly.md) 元件，而且它們出現的順序是由下列登錄機碼中包含的 "SubjectTemplate" 登錄值所控制：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

當憑證服務剖析 [*屬性*](../secgloss/a-gly.md) 名稱時，會忽略空格、連字號 (減號) 和大小寫。 例如，"AttributeName1"、"Attribute Name1" 和 "Attribute-Name1" 都是相等的。 若為屬性值，憑證服務會忽略開頭和尾端空白字元。

除了 DistinguishedName、RawName 和 Subject 以外，上述所有屬性都支援使用分行符號的多重值語法。 無法停用或變更分行符號分隔符號。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[憑證屬性](certificate-properties.md)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 
