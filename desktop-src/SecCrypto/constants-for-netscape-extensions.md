---
description: 用於編碼和解碼作業。
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Netscape 延伸模組的常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103853959"
---
# <a name="constants-for-netscape-extensions"></a>Netscape 延伸模組的常數

下列 Netscape 延伸模組可搭配編碼和解碼作業使用。 Netscape 預先定義的常數和物件識別碼字串不能直接搭配編碼或解碼函數、 [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject)、 [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)、 [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate)、 [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)或 [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)使用。 相反地，這些擴充功能需要使用所示的 *lpszStructType* 。

如需適用于某些 Netscape 延伸模組的其他詳細資料，請參閱下表中的備註。



| Netscape 憑證延伸物件識別碼                      | *lpszStructType*                                           | 對應的 *pvStructInfo*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szOID \_ NETSCAPE \_ 基底 \_ URL "2.16.840.1.113730.1.2"<br/>           | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>pbdata** 成員會指向 \_ 附加到憑證中所有相對 URL 位址開頭的 IA5 字串。 您可以將此延伸模組視為優化，以縮減 URL 延伸模組的大小。                                                                                                       |
| szOID \_ NETSCAPE \_ CA \_ 原則 \_ URL "2.16.840.1.113730.1.8"<br/>     | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>pbdata** 成員會指向 IA5 \_ 字串，也就是網頁的相對或絕對 URL，描述憑證發出時所用的原則。                                                                                                                                                            |
| szOID \_ NETSCAPE \_ CA \_ 撤銷 \_ URL "2.16.840.1.113730.1.4"<br/> | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>pbdata** 成員會指向一個 IA5 \_ 字串，此字串是用來檢查目前憑證所屬 [*憑證授權單位*](../secgloss/c-gly.md)單位所簽署憑證撤銷狀態的相對或絕對 URL。 |
| szOID \_ NETSCAPE \_ CERT \_ 更新 \_ URL "2.16.840.1.113730.1.7"<br/>  | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>pbdata** 成員指向的 IA5 \_ 字串，是憑證更新表單的相對或絕對 URL。                                                                                                                                                                                                     |
| szOID \_ NETSCAPE \_ CERT \_ SEQUENCE "2.16.840.1.113730.2.5"<br/>      | \_任何的 PKCS 內容 \_ 資訊 \_ 序列 \_ \_                     | [**CRYPT \_ \_ 的內容 \_ 資訊 \_ 順序 \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ NETSCAPE \_ CERT \_ TYPE "2.16.840.1.113730.1.1"<br/>          | X509 \_ 位                                                 | [**CRYPT \_ 位 \_ BLOB**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ NETSCAPE \_ 批註 "2.16.840.1.113730.1.13"<br/>            | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>PBDATA** 成員指向 IA5 \_ 字串，這個字串是在查看憑證時要顯示的批註。                                                                                                                                                                                                         |
| szOID \_ NETSCAPE \_ 撤銷 \_ URL "2.16.840.1.113730.1.3"<br/>     | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>pbdata** 成員會指向 IA5 \_ 字串，此字串是用來檢查憑證撤銷狀態的相對或絕對 URL。                                                                                                                                                                              |
| szOID \_ NETSCAPE \_ SSL \_ 伺服器 \_ 名稱 "2.16.840.1.113730.1.12"<br/>  | X509 任何字串 \_ \_ 或 x509 \_ UNICODE \_ 任何 \_ 字串<br/> | [**CERT \_名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)。 **DwValueType** 成員設定為 CERT \_ RDN \_ IA5 \_ 字串。 **值** 成員的 **>PBDATA** 成員指向 IA5 \_ 字串，此字串是用來比對使用此憑證的 SSL 伺服器之主機名稱的命令介面運算式。                                                                                                                                                                       |



 

針對所有使用 X509 \_ any \_ 字串或 X5O9 \_ UNICODE 任何字串 lpszStructType 的編碼函數 \_ \_ ，  \_ \_ 如果 **值** 成員的 **>pbdata** 成員中的字串格式為 [*ASCII*](../secgloss/a-gly.md)，則會使用任何字串，如果 \_ \_ \_ 字串格式為 UNICODE，則會使用 x509 UNICODE 任何字串。 在 Unicode 案例中，您必須先將憑證 \_ [**\_ 名稱 \_ 值**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value)結構的 **dwValueType** 成員設定為 cert \_ RDN IA5 字串，才能將字串轉換成 IA5 字串，然後再進行編碼 \_ \_ 。

針對解碼函數，使用者會選取輸出字串的格式。 如果所 \_ \_ 需的字串格式為 ASCII，請使用 x509 any 字串 \_ ， \_ 如果所 \_ 需的字串格式為 unicode，則使用 x509 UNICODE 任何字串。

針對 szOID \_ NETSCAPE \_ CERT \_ 更新 \_ url 延伸模組，資料結構包含指向憑證更新表單的相對或絕對 url。 更新表單會使用 HTTP GET 方法來存取，該 URL 是更新 URL 和憑證序號的串連。 憑證-序號會編碼為 ASCII 十六進位數位的字串。 例如，如果 netscape-base-url 是 HTTPs://*憑證授權單位單位 url*/，netscape-憑證-續約 url 為 cgi-bin/check-renew，而憑證序號為173420，則產生的 url 會是： HTTPs://*憑證授權單位單位 url*/cgi-bin/check-renew.cgi？02a56c。 傳回的檔應該是 HTML 格式，可讓使用者要求更新其憑證。

若是 \_ \_ \_ 使用 X509 ASN 編碼的 szOID NETSCAPE CERT SEQUENCE 延伸模組 \_ \_ ，則會將憑證編碼為一種 \_ \_ 包裝任何順序的 PKCS 內容資訊結構。 **ContentType** 成員的值為 **pszObjId**，而 content 欄位為下列結構：

SequenceOfAny：： = ANY 的序列

任何 **rgValue** 成員指向編碼 X509 憑證 [**\_ 之 CRYPT \_ 內容 \_ 資訊 \_ 序列 \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)中的 [**CRYPT \_ DER \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))s。

針對 szOID \_ NETSCAPE \_ 憑證 \_ 類型延伸，會定義下列位。



| 位元值 | 對應的類型                      |
|-----------|-----------------------------------------|
| 0x80      | NETSCAPE \_ SSL \_ 用戶端 \_ 驗證憑證 \_ \_ 類型 |
| 0x40      | NETSCAPE \_ SSL \_ 伺服器 \_ 驗證 \_ 憑證 \_ 類型 |
| 0x04      | NETSCAPE \_ SSL \_ CA \_ 憑證 \_ 類型           |



 

針對 szOID \_ NETSCAPE \_ 撤銷 \_ url 延伸模組，您可以使用相對或絕對 url 來檢查憑證的撤銷狀態。 撤銷檢查將會以 HTTP GET 方法的形式執行，其使用的 URL 是撤銷 URL 和憑證序號的串連。 憑證-序號會編碼為 ASCII 十六進位數位的字串。 例如，如果 netscape-base-url 是 HTTPs： \/ /www.certs-r-us.com/，則 netscape-撤銷 url 是 cgi-bin/check-rev，而憑證序號是173420，則產生的 url 會是： HTTPs： \/ /www.certs-r-us.com/cgi-bin/check-rev.cgi?02a56c。

伺服器應傳回檔，其內容類型為 application/x-netscape-撤銷。 如果憑證目前無效，檔應該包含單一 ASCII 數位 "1"，如果目前有效則為 "0"。

請注意，對於包含憑證序號的所有 Url，序號將會編碼為包含偶數個十六進位數位的字串。 如果有效位數的數目是奇數，則字串會有單一前置零，以確保產生偶數的數位。

 

 
