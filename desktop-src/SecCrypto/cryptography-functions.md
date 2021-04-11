---
description: 列出 CryptoAPI 提供的函數。
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: 密碼編譯函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91338c4a1cea62e2ecc4a2fa1f7254f303ef9b2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104116089"
---
# <a name="cryptography-functions"></a>密碼編譯函式

加密函式會根據使用方式進行分類，如下所示：

-   [CryptXML 函式](#cryptxml-functions)
-   [簽署者函式](#signer-functions)
-   [基礎密碼編譯功能](#base-cryptography-functions)
    -   [服務提供者函數](#service-provider-functions)
    -   [金鑰產生和交換功能](#key-generation-and-exchange-functions)
    -   [物件編碼和解碼函數](#object-encoding-and-decoding-functions)
    -   [資料加密和解密功能](#data-encryption-and-decryption-functions)
    -   [雜湊和數位簽章函式](#hash-and-digital-signature-functions)
-   [憑證和憑證存放區功能](#certificate-and-certificate-store-functions)
    -   [憑證存放區功能](#certificate-and-certificate-store-functions)
    -   [憑證和憑證存放區維護功能](#certificate-and-certificate-store-maintenance-functions)
    -   [憑證函數](#certificate-functions)
    -   [憑證撤銷清單函式](#certificate-revocation-list-functions)
    -   [憑證信任清單函式](#certificate-trust-list-functions)
    -   [擴充屬性函式](#extended-property-functions)
-   [MakeCert 函式](#makecert-functions)
-   [憑證驗證功能](#certificate-verification-functions)
    -   [使用 Ctl 的驗證函數](#verification-functions-using-ctls)
    -   [憑證鏈驗證功能](#certificate-chain-verification-functions)
-   [訊息函數](#message-functions)
    -   [低層級訊息函數](#low-level-message-functions)
    -   [簡化的訊息函數](#simplified-message-functions)
-   [輔助函式](#auxiliary-functions)
    -   [資料管理函式](#data-management-functions)
    -   [資料轉換函數](#data-conversion-functions)
    -   [增強金鑰使用方法功能](#enhanced-key-usage-functions)
    -   [金鑰識別碼函數](#key-identifier-functions)
    -   [OID 支援函式](#oid-support-functions)
    -   [遠端物件抓取函式](#remote-object-retrieval-functions)
    -   [PFX 函數](#pfx-functions)
-   [憑證服務備份和還原功能](#certificate-services-backup-and-restore-functions)
-   [回呼函式](#callback-functions)
-   [目錄定義函數](#catalog-definition-functions)
-   [目錄函式](#catalog-functions)
-   [WinTrust 函式](#wintrust-functions)
-   [物件定位器函數](#object-locator-functions)

## <a name="cryptxml-functions"></a>CryptXML 函式

密碼編譯 XML 函式提供 API，可讓您使用 XML 格式化資料來建立和表示數位簽章。 如需 XML 格式化簽章的詳細資訊，請參閱中的 XML-Signature 語法和處理規格 <https://go.microsoft.com/fwlink/p/?linkid=139649> 。



| 函式                                                                          | 描述                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SHAFinal**](a-shafinal.md)                                                 | 計算 MD5Update 函數所輸入之資料的最終雜湊。                                                                                                                                                                                                                                           |
| [**\_SHAInit**](a-shainit.md)                                                   | 起始資料流程的雜湊。                                                                                                                                                                                                                                                                       |
| [**\_SHAUpdate**](a-shaupdate.md)                                               | 將資料加入至指定的雜湊物件。                                                                                                                                                                                                                                                                            |
| [**CryptXmlCreateReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | 建立 XML 簽章的參考。                                                                                                                                                                                                                                                                         |
| [**CryptXmlAddObject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | 將 **物件** 專案加入至開啟以進行編碼的檔內容中的簽章。                                                                                                                                                                                                                        |
| [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | 關閉密碼編譯 XML 物件控制碼。                                                                                                                                                                                                                                                                        |
| [**CryptXmlDigestReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | 由應用程式用來摘要解析的參考。 此函數會在更新摘要之前套用轉換。                                                                                                                                                                                            |
| [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | 釋放 CryptXmlDllCreateDigest 函數所配置的 CRYPT \_ XML \_ 摘要。 [](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                                                                                                                                                                                               |
| [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | 為指定的方法建立摘要物件。                                                                                                                                                                                                                                                                |
| [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | 剖析 **KeyValue** 元素並建立密碼編譯 API：新一代 (CNG) BCrypt 金鑰控制碼來驗證簽章。                                                                                                                                                                                   |
| [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | 將資料放入摘要。                                                                                                                                                                                                                                                                                       |
| [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | 使用預設參數為 agile 演算法編碼 **SignatureMethod** 或 **DigestMethod** 元素。                                                                                                                                                                                                           |
| [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | 將 **KeyValue** 元素編碼。                                                                                                                                                                                                                                                                                  |
| [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | 抓取摘要值。                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | 對 XML 演算法進行解碼，並傳回演算法的相關資訊。                                                                                                                                                                                                                                           |
| [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | 針對指定的演算法抓取密碼編譯延伸模組函式的指標。                                                                                                                                                                                                                        |
| [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | 簽署資料。                                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | 驗證簽章。                                                                                                                                                                                                                                                                                            |
| [**CryptXmlEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | 使用提供的 XML 寫入器回呼函數來編碼簽章資料。                                                                                                                                                                                                                                       |
| [**CryptXmlGetAlgorithmInfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | 解碼 CRYPT \_ XML \_ 演算法結構，並傳回演算法的相關資訊。                                                                                                                                                                                                                         |
| [**CryptXmlGetDocCoNtext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | 傳回所提供之控制碼所指定的檔內容。                                                                                                                                                                                                                                                   |
| [**CryptXmlGetReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | 傳回所提供之控制碼所指定的 **參考** 元素。                                                                                                                                                                                                                                              |
| [**CryptXmlGetSignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | 傳回 XML **Signature** 元素。                                                                                                                                                                                                                                                                            |
| [**CryptXmlGetStatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | 傳回 [**CRYPT \_ XML \_ 狀態**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) 結構，其中包含有關所提供之控制碼所指定之物件的狀態資訊。                                                                                                                                                           |
| [**CryptXmlGetTransforms**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | 傳回預設轉換鏈引擎的相關資訊。                                                                                                                                                                                                                                                    |
| [**CryptXmlImportPublicKey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | 匯入所提供之控制碼所指定的公開金鑰。                                                                                                                                                                                                                                                         |
| [**CryptXmlOpenToEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | 開啟 XML 數位簽章以進行編碼，並 **傳回開啟之** 簽章元素的控制碼。 控制碼會封裝具有單一 [**CRYPT \_ XML \_**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) 簽章結構的檔內容，並保持開啟狀態，直到呼叫 [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) 函式為止。 |
| [**CryptXmlOpenToDecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | 開啟 XML 數位簽章以進行解碼，並傳回封裝 [**CRYPT \_ XML \_**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) 簽章結構的檔內容控制碼。 檔內容可以包含一個 **或多個** 簽章元素。                                                                 |
| [**CryptXmlSetHMACSecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | 在呼叫 [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) 或 [**CryptXmlVerify**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) 函式之前，先在控制碼上設定 HMAC 秘密。                                                                                                                                                        |
| [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | 建立 **SignedInfo** 元素的密碼編譯簽章。                                                                                                                                                                                                                                                   |
| [**CryptXmlVerifySignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | 執行 **SignedInfo** 元素的密碼編譯簽章驗證。                                                                                                                                                                                                                                       |
| [*PFN \_ CRYPT \_ XML \_ 寫入 \_ 回呼*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | 建立指定之資料提供者的轉換。                                                                                                                                                                                                                                                               |
| [*PFN \_ CRYPT \_ XML \_ CREATE \_ 轉換*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | 寫入密碼編譯 XML 資料。                                                                                                                                                                                                                                                                                   |
| [*PFN \_ CRYPT \_ XML \_ 資料 \_ 提供者 \_ 讀取*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | 讀取密碼編譯 XML 資料。                                                                                                                                                                                                                                                                                    |
| [*PFN \_ CRYPT \_ XML \_ 資料 \_ 提供者 \_ 關閉*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | 釋放密碼編譯 XML 資料提供者。                                                                                                                                                                                                                                                                    |
| [*PFN \_ CRYPT \_ XML \_ 列舉 \_ ALG \_ 資訊*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | 列舉預先定義和註冊的 [**CRYPT \_ XML \_ 演算法 \_ 資訊**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) 專案。                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>簽署者函式

提供函數來簽署和時間戳記資料。



| 函式                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) | 釋放先前呼叫 [**SignerSignEx**](signersignex.md)函式所配置的 [**簽署者 \_ 內容**](signer-context.md)結構。                                                                                                                                                                                                                                                                      |
| [**SignError**](signerror.md)                             | 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數，並將傳回碼轉換成 **HRESULT**。                                                                                                                                                                                                                                                                                                            |
| [**SignerSign**](signersign.md)                           | 簽署指定的檔案。                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SignerSignEx**](signersignex.md)                       | 簽署指定的檔案，並傳回已簽署資料的指標。                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | 簽署和時間戳記指定的檔案，允許多個嵌套的簽章。                                                                                                                                                                                                                                                                                                                                      |
| [**SignerTimeStamp**](signertimestamp.md)                 | 時間戳記指定的主體。 此函數支援 Authenticode 時間戳記。 若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 [**SignerTimeStampEx2**](signertimestampex2.md) 函數。                                                                                                                                                                                       |
| [**SignerTimeStampEx**](signertimestampex.md)             | 時間戳記指定的主體，並選擇性地傳回包含 [*BLOB*](../secgloss/b-gly.md)指標之 [**簽署者 \_ 內容**](signer-context.md)結構的指標。 此函數支援 Authenticode 時間戳記。 若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 [**SignerTimeStampEx2**](signertimestampex2.md) 函數。 |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | 時間戳記指定的主體，並選擇性地傳回包含 [*BLOB*](../secgloss/b-gly.md)指標之 [**簽署者 \_ 內容**](signer-context.md)結構的指標。 您可以使用此函式來執行 x.509 公開金鑰基礎結構、RFC 3161 相容的時間戳記。                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | 時間戳記指定的主體，並支援在多個簽章上設定時間戳記。                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>基礎密碼編譯功能

基底加密函式提供最具彈性的方法來開發加密應用程式。 所有與 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的通訊都是透過這些函式進行。

CSP 是執行所有密碼編譯作業的獨立模組。 每個使用密碼編譯功能的應用程式都必須至少有一個 CSP。 單一應用程式偶爾會使用一個以上的 CSP。

如果使用多個 CSP，則可以在 CryptoAPI 密碼編譯函式呼叫中指定要使用的 CSP。 其中一個 CSP （Microsoft 基底密碼編譯提供者）與 [*CryptoAPI*](../secgloss/c-gly.md)配套。 如果未指定其他 CSP，則會使用此 CSP 作為許多 CryptoAPI 函數的預設提供者。

每個 CSP 都提供針對 CryptoAPI 提供的密碼編譯支援不同的實作為。 有些提供更強的密碼編譯演算法;其他則包含硬體元件，例如 [*智慧卡*](../secgloss/s-gly.md)。 此外，某些 Csp 有時可以直接與使用者通訊，例如使用使用者的簽章 [*私密金鑰*](../secgloss/s-gly.md)來執行 [*數位簽章*](../secgloss/d-gly.md)。

基底加密函式位於下列廣泛的群組中：

-   服務提供者函數
-   金鑰產生和交換功能
-   物件編碼和解碼函數
-   資料加密和解密功能
-   雜湊和數位簽章函式

### <a name="service-provider-functions"></a>服務提供者函數

應用程式會使用下列服務功能來連接 [*加密服務提供者*](../secgloss/c-gly.md) (CSP) 並中斷連線。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireCoNtext</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 取得特定 CSP 內目前使用者 <a href="/windows/desktop/SecGloss/k-gly"><em>金鑰容器</em></a> 的控制碼。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>CryptCoNtextAddRef</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 遞增<a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a>控制碼上的<a href="/windows/desktop/SecGloss/r-gly"><em>參考計數</em></a>。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>CryptEnumProviders</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 列舉電腦上的提供者。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>CryptEnumProviderTypes</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 列舉電腦上支援的提供者類型。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>CryptGetDefaultProvider</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 針對目前使用者或電腦的指定提供者類型，決定預設的 CSP。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 抓取管理 CSP 作業的參數。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultCoNtext</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 安裝先前取得的 <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> 內容，作為預設內容使用。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>CryptReleaseCoNtext</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 釋放 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireCoNtext</strong></a> 函數所取得的控制碼。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>CryptSetProvider</strong></a>和<a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>CryptSetProviderEx</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 指定特定 CSP 類型的使用者預設 CSP。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>CryptSetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 指定 CSP 的屬性。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>CryptUninstallDefaultCoNtext</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 移除 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultCoNtext</strong></a>先前安裝的預設內容。</td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>FreeCryptProvFromCertEx</strong></a></td>
<td>將控制碼釋放給 <a href="/windows/desktop/SecGloss/c-gly"><em>密碼編譯服務提供者</em></a> (CSP) 或密碼編譯 API：新一代 (CNG) 金鑰。</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>金鑰產生和交換功能

金鑰產生和 exchange 功能會與其他使用者 [*交換金鑰*](../secgloss/e-gly.md) ，以及建立、設定和終結 [*密碼編譯金鑰*](../secgloss/c-gly.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>CryptDeriveKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 建立從密碼衍生的金鑰。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>CryptDestroyKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 終結金鑰。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>CryptDuplicateKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 建立金鑰的完整複本，包括金鑰的 <a href="/windows/desktop/SecGloss/s-gly"><em>狀態</em></a> 。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 從 CSP 將金鑰傳輸到應用程式記憶體空間中的 <a href="/windows/desktop/SecGloss/k-gly"><em>金鑰 BLOB</em></a> 。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 建立隨機索引鍵。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 產生亂數據。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>CryptGetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 捕獲金鑰的參數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 取得金鑰交換或簽章金鑰的控制碼。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>CryptImportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 從 <a href="/windows/desktop/SecGloss/k-gly"><em>金鑰 BLOB</em></a> 將金鑰傳輸至 CSP。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 指定索引鍵的參數。</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>物件編碼和解碼函數

這些是一般化的編碼和解碼功能。 它們可用來編碼和解碼 [*憑證*](../secgloss/c-gly.md)、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 、 [*憑證要求*](../secgloss/c-gly.md)和憑證延伸。

| 函式                                           | 描述                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | 解碼 *lpszStructType* 型別的結構。                                                                                                    |
| [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | 解碼 *lpszStructType* 型別的結構。 [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) 支援一次傳遞記憶體配置選項。 |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | 將 *lpszStructType* 類型的結構編碼。                                                                                                    |
| [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | 將 *lpszStructType* 類型的結構編碼。 [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) 支援一次傳遞記憶體配置選項。 |



 

### <a name="data-encryption-and-decryption-functions"></a>資料加密和解密功能

下列函數支援加密和解密作業。 [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) 和 [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) 在呼叫之前需要 [*密碼編譯金鑰*](../secgloss/c-gly.md) 。 這是使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)、 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)或 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函數來完成。 建立金鑰時，會指定加密演算法。 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 可以設定額外的加密參數。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>CryptDecrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 使用指定的加密金鑰來解密 <a href="/windows/desktop/SecGloss/c-gly"><em>加密</em></a> 文字區段。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 使用指定的加密金鑰來加密 <a href="/windows/desktop/SecGloss/p-gly"><em>純文字</em></a> 區段。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>針對 <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a> 結構中的資料執行加密。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>加密記憶體以保護機密資訊。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>在 <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a>中執行資料的解密和完整性檢查。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>解密使用 <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a>加密的記憶體。</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>雜湊和數位簽章函式

這些函數會計算資料的 [*雜湊*](../secgloss/h-gly.md) ，也會建立並驗證 [*數位簽章*](../secgloss/d-gly.md)。 雜湊也稱為訊息摘要。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 建立空的雜湊物件。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>CryptDestroyHash</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 終結雜湊物件。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>CryptDuplicateHash</strong></a></td>
<td>複製雜湊物件。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>抓取雜湊物件參數。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 雜湊資料區塊，並將其加入至指定的雜湊物件。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>CryptHashSessionKey</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 雜湊工作階段金鑰，並將它加入至指定的雜湊物件。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>CryptSetHashParam</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 設定雜湊物件參數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>CryptSignHash</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 簽署指定的雜湊物件。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a></td>
<td>顯示以數位方式簽署檔或 <a href="/windows/desktop/SecGloss/b-gly"><em>BLOB</em></a>的 wizard。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>CryptUIWizFreeDigitalSignCoNtext</strong></a></td>
<td>釋放 <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> 結構的指標。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>CryptVerifySignature</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 在指定雜湊物件的控制碼的情況下，驗證數位簽章。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>PFNCFILTERPROC</strong></a></td>
<td>篩選出現在 <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a> 函式所顯示的數位簽章 wizard 中的憑證。</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>憑證和憑證存放區功能

憑證和憑證存放區功能會管理 [*憑證*](../secgloss/c-gly.md)的使用、儲存和抓取、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) ，以及 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。 這些函數分為下列群組：

-   憑證存放區功能
-   憑證和憑證存放區維護功能
-   憑證函數
-   憑證撤銷清單函式
-   憑證信任清單函式
-   擴充屬性函式
-   MakeCert 函式

### <a name="certificate-store-functions"></a>憑證存放區功能

使用者網站可以經過一段時間，收集許多憑證。 網站通常會有網站使用者的憑證，以及其他憑證來描述使用者所傳達的個人和實體。 每個實體都可以有一個以上的憑證。 對於每個個別的憑證，都應該有一鏈驗證憑證，可提供回受信任 [*根憑證*](../secgloss/r-gly.md)的線索。 [*憑證存放區*](../secgloss/c-gly.md) 與其相關功能提供儲存、抓取、列舉、驗證和使用儲存在憑證中之資訊的功能。

| 函式                                                               | 描述                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | 將同一個憑證存放區新增至集合憑證存放區。                                                                                                                                                                                                                                                                       |
| [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | 關閉憑證存放區控制碼。                                                                                                                                                                                                                                                                                                        |
| [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | 允許應用程式在快取存放區的內容與保存到儲存體的存放區內容之間有差異時收到通知。 它也提供快取存放區的 desynchronization （如有必要），並提供將快取存放區中所做的變更認可至保存儲存體的方法。<br/> |
| [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | 藉由遞增 [*參考計數*](../secgloss/r-gly.md)來複製存放區控制碼。                                                                                                                                                                                            |
| [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | 列舉指定系統存放區的實體存放區。                                                                                                                                                                                                                                                                              |
| [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | 列舉所有可用的系統存放區。                                                                                                                                                                                                                                                                                                   |
| [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | 列舉所有具有可用系統存放區的位置。                                                                                                                                                                                                                                                                      |
| [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | 取得存放區屬性。                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | 使用指定的存放區提供者類型，開啟憑證存放區。                                                                                                                                                                                                                                                                          |
| [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | 開啟以子系統通訊協定為基礎的系統憑證存放區。                                                                                                                                                                                                                                                                           |
| [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | 將實體存放區新增至登錄系統存放區集合。                                                                                                                                                                                                                                                                              |
| [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | 註冊系統存放區。                                                                                                                                                                                                                                                                                                                 |
| [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | 從集合存放區中移除同一個憑證存放區。                                                                                                                                                                                                                                                                              |
| [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | 儲存憑證存放區。                                                                                                                                                                                                                                                                                                              |
| [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | 設定存放區屬性。                                                                                                                                                                                                                                                                                                                    |
| [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | 從指定的系統存放區集合中移除實體存放區。                                                                                                                                                                                                                                                                        |
| [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | 取消註冊指定的系統存放區。                                                                                                                                                                                                                                                                                                     |
| [**CryptUIWizExport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | 提供一個可匯出憑證、憑證信任清單 (CTL) 、憑證撤銷清單 (CRL) 或憑證存放區的 wizard。                                                                                                                                                                                                      |
| [**CryptUIWizImport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | 提供一個可匯入憑證、憑證信任清單 (CTL) 、憑證撤銷清單 (CRL) 或憑證存放區的 wizard。                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>憑證和憑證存放區維護功能

CryptoAPI 提供一組一般憑證和憑證存放區維護功能。

| 函式                                                                                                                              | 描述                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | 將序列化的憑證或 CRL 元素新增至存放區。                                   |
| [**CertCreateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | 從編碼的位元組建立指定的內容。 新的內容不會放在存放區中。 |
| [**CertEnumSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | 列舉已排序 CTL 內容中的 TrustedSubjects。                                        |
| [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | 在 CTL 中尋找指定的主體。                                                          |
| [**CertFindSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | 在排序的 CTL 中尋找指定的主體。                                                   |
| [**OpenPersonalTrustDBDialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog)和 [ **OpenPersonalTrustDBDialogEx**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | 顯示 [ **憑證** ] 對話方塊。                                                      |



 

### <a name="certificate-functions"></a>憑證函數

大部分的 [*憑證*](../secgloss/c-gly.md) 函數都有相關的函式來處理 [*crl*](../secgloss/c-gly.md) 和 [*ctl*](../secgloss/c-gly.md)。 如需相關 CRL 和 CTL 函數的詳細資訊，請參閱憑證撤銷清單函式和憑證信任清單函式。

| 函式                                                                             | 描述                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCertificateCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | 將憑證內容新增至憑證存放區。                                                                                                                                                                                            |
| [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | 將憑證存放區中的連結新增至不同存放區中的憑證內容。                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | 將編碼的憑證轉換成憑證內容，然後將內容新增至憑證存放區。                                                                                                                                  |
| [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | 遞增 **HCERT \_ 伺服器 \_ OCSP \_ 回應** 控制碼的參考計數。                                                                                                                                                                 |
| [**CertAddRefServerOcspResponseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | 遞增 [**CERT \_ SERVER \_ OCSP \_ 回應 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context) 結構的參考計數。                                                                                                              |
| [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | 關閉 [*線上憑證狀態通訊協定*](../secgloss/o-gly.md) (OCSP) server 回應控制碼。                                               |
| [**CertCreateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | 從編碼的憑證建立憑證內容。 建立的內容不會放在憑證存放區中。                                                                                                                               |
| [**CertCreateSelfSignCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | 建立自我簽署憑證。                                                                                                                                                                                                              |
| [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | 從憑證存放區刪除憑證。                                                                                                                                                                                               |
| [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | 藉由遞增其 [*參考計數*](../secgloss/r-gly.md)來複製憑證內容。                                                                                           |
| [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | 列舉憑證存放區中的憑證內容。                                                                                                                                                                                   |
| [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | 在憑證存放區中尋找符合搜尋準則的第一個或下一個憑證內容。                                                                                                                                           |
| [**CertFreeCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | 釋出憑證內容。                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | 從憑證存放區取得指定之主體憑證的第一個或下一個發行者的憑證內容。                                                                                                                      |
| [**CertGetServerOcspResponseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | 抓取未封鎖、時間有效的 [*線上憑證狀態通訊協定*](../secgloss/o-gly.md) (指定之控制碼的 OCSP) 回應內容。 |
| [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | 從憑證存放區取得主體憑證內容，此內容是由其簽發者和序號來唯一識別。                                                                                                                  |
| [**CertGetValidUsages**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | 傳回使用方式的陣列，其中包含憑證陣列中所有憑證的有效使用方式交集。                                                                                                               |
| [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | 開啟 [*線上憑證狀態通訊協定*](../secgloss/o-gly.md) 的控制碼， (與伺服器憑證鏈相關聯的 OCSP) 回應。       |
| [**CertRetrieveLogoOrBiometricInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | 針對 **szOID \_ 商標 \_ ext** 或 **szOID \_ 生物特徵辨識 \_ EXT** 憑證延伸模組中指定的標誌或生物特徵辨識資訊執行 URL 抓取。                                                                                  |
| [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | 提供一個對話方塊，可讓使用者從符合指定準則的一組憑證中選取憑證。                                                                                                                       |
| [**CertSelectCertificateChains**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | 根據指定的選取準則來抓取證書鏈。                                                                                                                                                                             |
| [**CertSelectionGetSerializedBlob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Helper 函式，用來從 [**CERT \_ SELECTUI \_ 輸入**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input)結構中取出序列化的憑證 [*BLOB*](../secgloss/b-gly.md) 。                                               |
| [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | 序列化憑證內容的編碼憑證，以及其屬性的編碼標記法。                                                                                                                                         |
| [**CertVerifySubjectCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | 使用簽發者對主體憑證執行啟用的驗證檢查。                                                                                                                                                           |
| [**CryptUIDlgCertMgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | 顯示允許使用者管理憑證的對話方塊。                                                                                                                                                                              |
| [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)                   | 顯示允許使用者選取憑證的對話方塊。                                                                                                                                                                               |
| [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | 顯示允許從指定的存放區選取憑證的對話方塊。                                                                                                                                                        |
| [**CryptUIDlgViewCertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | 提供顯示指定憑證的對話方塊。                                                                                                                                                                                    |
| [**CryptUIDlgViewCoNtext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | 顯示憑證、CRL 或 CTL。                                                                                                                                                                                                            |
| [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)                         | 顯示對話方塊，其中包含已簽署訊息的簽署者資訊。                                                                                                                                                                |
| [**GetFriendlyNameOfCert**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | 捕獲憑證的顯示名稱。                                                                                                                                                                                                   |
| [**RKeyCloseKeyService**](rkeyclosekeyservice.md)                                   | 關閉金鑰服務控制碼。                                                                                                                                                                                                                    |
| [**RKeyOpenKeyService**](rkeyopenkeyservice.md)                                     | 在遠端電腦上開啟金鑰服務控制碼。                                                                                                                                                                                                |
| [**RKeyPFXInstall**](rkeypfxinstall.md)                                             | 在遠端電腦上安裝憑證。                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>憑證撤銷清單函式

這些函式會管理 (Crl) 的 [*憑證撤銷清單*](../secgloss/c-gly.md) 的儲存和抓取。

| 函式                                                             | 描述                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCRLCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | 將 CRL 內容新增至憑證存放區。                                                                                                                                          |
| [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | 將存放區中的連結新增至不同存放區中的 CRL 內容。                                                                                                                         |
| [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | 將編碼的 CRL 轉換成 CRL 內容，然後將內容新增至憑證存放區。                                                                                        |
| [**CertCreateCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | 從編碼的 CRL 建立 CRL 內容。 建立的內容不會放在憑證存放區中。                                                                                     |
| [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | 刪除憑證存放區中的 CRL。                                                                                                                                             |
| [**CertDuplicateCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | 藉由遞增 [*參考計數*](../secgloss/r-gly.md)來複製 CRL 內容。                                         |
| [**CertEnumCRLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | 列舉存放區中的 CRL 內容。                                                                                                                                               |
| [**CertFindCertificateInCRL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | 搜尋指定憑證 (CRL) 的 [*憑證撤銷清單*](../secgloss/c-gly.md) 。 |
| [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | 在憑證存放區中尋找符合特定準則的第一個或下一個 CRL 內容。                                                                                     |
| [**CertFreeCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | 釋放 CRL 內容。                                                                                                                                                                  |
| [**CertGetCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | 針對指定的簽發者憑證，取得憑證存放區中的第一個或下一個 CRL 內容。                                                                                 |
| [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | 序列化 CRL 內容的編碼 CRL 和其屬性。                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>憑證信任清單函式

這些函式會管理 [*憑證信任清單*](../secgloss/c-gly.md) (ctl) 的儲存和抓取。

| 函式                                                               | 描述                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**CertAddCTLCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | 將 CTL 內容新增至憑證存放區。                                                                         |
| [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | 將存放區中的連結新增至不同存放區中的 CRL 內容。                                                        |
| [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | 將編碼的 CTL 轉換為 CTL 內容，然後將內容新增至憑證存放區。                       |
| [**CertCreateCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | 從編碼的憑證信任清單建立 CTL 內容。 建立的內容不會放在憑證存放區中。 |
| [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | 從憑證存放區刪除 CTL。                                                                            |
| [**CertDuplicateCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | 藉由遞增參考計數來複製 CTL 內容。                                                        |
| [**CertEnumCTLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | 列舉憑證存放區中的 CTL 內容。                                                                |
| [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | 在憑證存放區中尋找符合特定準則的第一個或下一個 CTL 內容。                     |
| [**CertFreeCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | 釋出 CTL 內容。                                                                                                 |
| [**CertModifyCertificatesToTrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | 針對特定用途修改 CTL 中的憑證集。                                                       |
| [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | 將 CTL 內容的編碼 CTL 和其屬性序列化。                                                         |



 

### <a name="extended-property-functions"></a>擴充屬性函式

下列函式適用于憑證、Crl 和 Ctl 的擴充屬性。

| 函式                                                                             | 描述                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**CertEnumCertificateCoNtextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | 列舉指定之憑證內容的屬性。 |
| [**CertEnumCRLCoNtextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | 列舉指定之 CRL 內容的屬性。         |
| [**CertEnumCTLCoNtextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | 列舉所指定 CTL 內容的屬性。         |
| [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | 捕獲憑證屬性。                                |
| [**CertGetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | 捕獲 CRL 屬性。                                        |
| [**CertGetCTLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | 抓取 CTL 屬性。                                        |
| [**CertSetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | 設定憑證屬性。                                     |
| [**CertSetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | 設定 CRL 屬性。                                             |
| [**CertSetCTLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | 設定 CTL 屬性。                                             |



 

## <a name="makecert-functions"></a>MakeCert 函式

下列函數支援 [MakeCert](makecert.md) 工具。



| 函式                                                                               | 描述                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCryptProvFromCert**](freecryptprovfromcert.md)                                 | 將 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 的控制碼釋放 (CSP) ，並選擇性地刪除 [**GetCryptProvFromCert**](getcryptprovfromcert.md) 函式所建立的暫存容器。 |
| [**GetCryptProvFromCert**](getcryptprovfromcert.md)                                   | 取得 CSP 的控制碼和憑證內容的金鑰規格。                                                                                                                                                                                                                                |
| [**PvkFreeCryptProv**](pvkfreecryptprov.md)                                           | 釋放 CSP 的控制碼，並選擇性地刪除 [**PvkGetCryptProv**](pvkgetcryptprov.md) 函式所建立的暫存容器。                                                                                                                                                          |
| [**PvkGetCryptProv**](pvkgetcryptprov.md)                                             | 根據 [*私密金鑰*](../secgloss/p-gly.md) 檔案名或金鑰容器名稱，取得 CSP 的控制碼。                                                                                                                                          |
| [**PvkPrivateKeyAcquireCoNtextFromMemory**](pvkprivatekeyacquirecontextfrommemory.md) | 在 CSP 中建立暫存容器，並從記憶體將私密金鑰載入至容器。                                                                                                                                                                                                         |
| [**PvkPrivateKeySave**](pvkprivatekeysave.md)                                         | 將私密金鑰和其對應的 [*公開金鑰*](../secgloss/p-gly.md) 儲存至指定的檔案。                                                                                                                                                          |
| [**SignError**](signerror.md)                                                         | 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ，並將傳回碼轉換成 **HRESULT**。                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>憑證驗證功能

憑證會使用 [*ctl*](../secgloss/c-gly.md) 或憑證鏈進行驗證。 這兩個函式都有提供：

-   使用 Ctl 的驗證函數
-   憑證鏈驗證功能

### <a name="verification-functions-using-ctls"></a>使用 Ctl 的驗證函數

這些函數會在驗證程式中使用 Ctl。 您可以在憑證信任清單函式和擴充屬性函式中，找到使用 Ctl 的其他函數。

下列函式會直接使用 Ctl 進行驗證。

| 函式                                                         | 描述                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | 驗證 CTL 的使用方式。                 |
| [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | 將 CTL 編碼並簽署為訊息。        |
| [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | 從訊息中抓取和驗證 CTL。 |
| [**CryptMsgSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | 簽署包含 CTL 的訊息。         |



 

### <a name="certificate-chain-verification-functions"></a>憑證鏈驗證功能

建立憑證鏈，以提供有關個別憑證的信任資訊。

| 函數名稱                                                                                                    | Description                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | 為應用程式建立新的非預設的鏈引擎。                                                                                                                                                          |
| [**CertCreateCTLEntryFromCertificateCoNtextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | 建立 CTL 專案，其屬性為憑證內容的屬性。                                                                                                                                      |
| [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | 藉由遞增鏈的 [*參考計數*](../secgloss/r-gly.md) ，並將指標傳回給鏈，來複製憑證鏈。                    |
| [**CertFindChainInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | 尋找存放區中的第一個或下一個憑證連結內容。                                                                                                                                                     |
| [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | 藉由減少其參考計數來釋出憑證鏈。                                                                                                                                                          |
| [**CertFreeCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | 釋出非預設的憑證鏈引擎。                                                                                                                                                                        |
| [**CertFreeCertificateChainList**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | 釋放鏈內容指標的陣列。                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | 在可能的情況下，從結束憑證開始並回到受信任的 [*根憑證*](../secgloss/r-gly.md)。                |
| [**CertIsValidCRLForCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | 檢查 [*CRL*](../secgloss/c-gly.md) 來判斷是否要在憑證被撤銷時包含特定的憑證。 |
| [**CertSetCertificateCoNtextPropertiesFromCTLEntry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | 使用 CTL 專案中的屬性，設定憑證內容上的屬性。                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | 檢查憑證鏈來確認其有效性，包括其符合任何指定的有效原則準則。                                                                                            |



 

## <a name="message-functions"></a>訊息函數

[*CryptoAPI*](../secgloss/c-gly.md) 訊息函式包含兩個函式群組：低層級訊息函數和 [*簡化的訊息函數*](../secgloss/s-gly.md)。

低層級的訊息函式會直接建立並使用 PKCS \# 7 訊息。 這些函式會編碼 PKCS \# 7 資料，以傳輸和解碼收到的 pkcs \# 7 資料。 它們也會解密並驗證已接收訊息的簽章。 如需 PKCS \# 7 標準和低層級訊息的總覽，請參閱 [低層級的訊息](low-level-messages.md)。

簡化的訊息函式在較高的層級，並將數個低層級的訊息函式和憑證函式包裝成單一函式，以特定方式執行特定工作。 這些函式可減少完成工作所需的函式呼叫數目，進而簡化 CryptoAPI 的使用。 如需簡化訊息的總覽，請參閱 [簡化的訊息](simplified-messages.md)。

-   低層級訊息函數
-   簡化的訊息函數

### <a name="low-level-message-functions"></a>低層級訊息函數

低層級訊息函式提供將資料編碼以進行傳輸，以及解碼所收到的 PKCS 7 訊息所需的功能 \# 。 也提供功能來解密和驗證已接收訊息的簽章。 不建議在大部分的應用程式中使用這些低層級的訊息函數。 針對大部分的應用程式，最好使用簡化的訊息函式，將數個低層級訊息函式包裝成單一函式呼叫。

| 函式                                                                                   | 描述                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | 計算編碼的密碼編譯訊息的長度。                                                                                                                                                                     |
| [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | 關閉密碼編譯訊息的控制碼。                                                                                                                                                                                    |
| [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | 在最後 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 已編碼或已解碼的密碼編譯訊息之後，執行特殊的控制函數。                                                                                   |
| [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | 來副署已存在於訊息中的簽章。                                                                                                                                                                       |
| [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | 來副署已存在的簽章 (編碼 SignerInfo，如 PKCS \# 7) 所定義。                                                                                                                                       |
| [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | 藉由遞增 [*參考計數*](../secgloss/r-gly.md)來複製密碼編譯訊息控制碼。 參考計數會持續追蹤訊息的存留期。 |
| [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | 在編碼或解碼密碼編譯訊息之後取得參數。                                                                                                                                                       |
| [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | 開啟解碼的密碼編譯訊息。                                                                                                                                                                                    |
| [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | 開啟編碼的密碼編譯訊息。                                                                                                                                                                                    |
| [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | 更新密碼編譯訊息的內容。                                                                                                                                                                               |
| [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | 依據 PKCS 7) 所定義 (SignerInfo 結構來驗證 [*副署*](../secgloss/c-gly.md) \# 。                                                   |
| [**CryptMsgVerifyCountersignatureEncodedEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | 確認 *pbSignerInfoCounterSignature* 參數包含 *pbSignerInfo* 參數結構之 **encryptedDigest** 欄位的加密 [*雜湊*](../secgloss/h-gly.md)。   |



 

### <a name="simplified-message-functions"></a>簡化的訊息函數

[*簡化的訊息*](../secgloss/s-gly.md) 函式會將低層級的訊息函式包裝成單一函式，以完成指定的工作。

| 函式                                                                               | 描述                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | 解碼密碼編譯訊息。                                                                                                                                                                                                                                             |
| [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | 解密指定的訊息，並驗證簽署人。                                                                                                                                                                                                                     |
| [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | 解密指定的訊息。                                                                                                                                                                                                                                              |
| [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | 加密收件者或收件者的訊息。                                                                                                                                                                                                                        |
| [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | 傳回包含訊息憑證和 [*crl*](../secgloss/c-gly.md)的 [*憑證存放區*](../secgloss/c-gly.md)。 |
| [**CryptGetMessageSignerCount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | 傳回已簽署訊息中的簽署者計數。                                                                                                                                                                                                                          |
| [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | 建立訊息的雜湊。                                                                                                                                                                                                                                               |
| [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | 簽署訊息，然後針對收件者或收件者進行加密。                                                                                                                                                                                                     |
| [**CryptSignMessageWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | 使用函式的參數中指定的 CSP 私密金鑰來簽署訊息。                                                                                                                                                                                       |
| [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | 簽署訊息。                                                                                                                                                                                                                                                           |
| [**CryptVerifyDetachedMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | 驗證封裝含已卸離之雜湊的雜湊訊息。                                                                                                                                                                                                                     |
| [**CryptVerifyDetachedMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | 驗證封裝含已卸離之簽章或簽章的已簽署訊息。                                                                                                                                                                                                  |
| [**CryptVerifyMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | 確認雜湊的訊息。                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | 驗證已簽署的訊息。                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignatureWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | 使用指定的公開金鑰資訊來驗證已簽署訊息的簽章。                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>輔助函式

協助工具的分組方式如下：

-   資料管理函式
-   資料轉換函數
-   增強金鑰使用方法功能
-   金鑰識別碼函數
-   OID 支援函式
-   遠端物件抓取函式
-   PFX 函數

### <a name="data-management-functions"></a>資料管理函式

下列 CryptoAPI 函數會管理資料和憑證。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>CertCompareCertificate</strong></a></td>
<td>比較兩個憑證，以判斷它們是否相同。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>CertCompareCertificateName</strong></a></td>
<td>比較兩個憑證名稱，以判斷它們是否相同。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>CertCompareIntegerBlob</strong></a></td>
<td>比較兩個整數 <a href="/windows/desktop/SecGloss/b-gly"><em>blob</em></a>。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>CertComparePublicKeyInfo</strong></a></td>
<td>比較兩個 <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰</em></a> ，判斷它們是否相同。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>CertFindAttribute</strong></a></td>
<td>尋找 (OID) 的 <a href="/windows/desktop/SecGloss/o-gly"><em>物件識別碼</em></a> 所識別的第一個屬性。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>CertFindExtension</strong></a></td>
<td>尋找其 OID 所識別的第一個延伸模組。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>CertFindRDNAttr</strong></a></td>
<td>在<em>相對分辨名稱</em>的名稱清單中尋找其 OID 所識別的第一個<a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a>屬性。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>CertGetIntendedKeyUsage</strong></a></td>
<td>從憑證取得預定的金鑰使用方式位元組。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>CertGetPublicKeyLength</strong></a></td>
<td>從 <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰 BLOB</em></a>取得公開/私用金鑰的位長度。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>CertIsRDNAttrsInCertificateName</strong></a></td>
<td>將 <a href="/windows/desktop/SecGloss/c-gly"><em>憑證名稱</em></a> 中的屬性與指定的 <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>CERT_RDN</strong></a> 進行比較，以判斷是否在其中包含所有屬性。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>CertIsStrongHashToSign</strong></a></td>
<td>判斷指定的雜湊演算法和簽署憑證中的公開金鑰是否可以用來執行強式簽署。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>CertVerifyCRLRevocation</strong></a></td>
<td>確認主體憑證不在 (CRL) 的 <a href="/windows/desktop/SecGloss/c-gly"><em>憑證撤銷清單</em></a> 中。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>CertVerifyCRLTimeValidity</strong></a></td>
<td>確認 CRL 的時間有效性。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>CertVerifyRevocation</strong></a></td>
<td>確認主體憑證不在 CRL 上。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>CertVerifyTimeValidity</strong></a></td>
<td>確認憑證的時間有效性。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>CertVerifyValidityNesting</strong></a></td>
<td>確認主體的時間有效性會嵌套在簽發者的時間有效性內。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a>函式會取代此函數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>以 PKCS #8 格式匯出私密金鑰。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>匯出與提供者對應之私密金鑰相關聯的公開金鑰資訊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>CryptExportPublicKeyInfoEx</strong></a></td>
<td>匯出與提供者對應之私密金鑰相關聯的公開金鑰資訊。 此函式與 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> 不同之處在于，使用者可以指定公開金鑰演算法，進而覆寫 CSP 所提供的預設值。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>CryptExportPublicKeyInfoFromBCryptKeyHandle</strong></a></td>
<td>匯出與提供者對應之私密金鑰相關聯的公開金鑰資訊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>CryptFindCertificateKeyProvInfo</strong></a></td>
<td>列舉密碼編譯提供者及其 <a href="/windows/desktop/SecGloss/k-gly"><em>金鑰容器</em></a> ，以尋找與憑證公開金鑰對應的私密金鑰。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>CryptFindLocalizedName</strong></a></td>
<td>尋找指定名稱的當地語系化名稱，例如，尋找根系統存放區名稱的當地語系化名稱。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>CryptHashCertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 雜湊編碼的內容。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>使用密碼編譯 API：新一代 (CNG) 雜湊提供者來雜湊資料區塊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>CryptHashPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 計算已編碼公開金鑰資訊的雜湊。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>CryptHashToBeSigned</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 將的雜湊計算 &quot; 為編碼的 &quot; 已簽署內容 (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>) 中簽署的資訊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 將 PKCS #8 格式的 <a href="/windows/desktop/SecGloss/p-gly"><em>私密金鑰</em></a> 匯入至 <a href="/windows/desktop/SecGloss/c-gly"><em>密碼編譯服務提供者</em></a> (CSP) 。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 將公開金鑰資訊轉換並匯入提供者，並傳回公開金鑰的控制碼。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 將公開金鑰資訊轉換並匯入提供者，並傳回公開金鑰的控制碼。 您可以使用 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a>) 所指定的其他參數 (，這些參數可用來覆寫預設值，以提供補充 <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>將公開金鑰匯入至 CNG 非對稱提供者。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a></td>
<td>配置緩衝區的記憶體。 所有傳回已配置緩衝區的 Crypt32.dll .lib 函數都會使用此記憶體。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>CryptMemFree</strong></a></td>
<td>釋放 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a> 或 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a>所配置的記憶體。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a></td>
<td>釋出目前為緩衝區配置的記憶體，並為新的緩衝區配置記憶體。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 捕獲 BLOB 或檔案內容的相關資訊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>將編碼 &quot; 為簽署的資訊 &quot; 、簽署此編碼的資訊，然後將產生的帶正負號編碼資訊編碼。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>CryptSignCertificate</strong></a></td>
<td>將簽署的 &quot; 資訊簽 &quot; 入已編碼、簽署的內容中。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a></td>
<td>將主體介面套件新增 (SIP) 。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>CryptSIPCreateIndirectData</strong></a></td>
<td>傳回<a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a>結構，其中包含提供的<a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>結構、摘要演算法和編碼屬性的<a href="/windows/desktop/SecGloss/h-gly"><em>雜湊</em></a>。 雜湊可以當做資料的間接參考使用。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>CryptSIPGetCaps</strong></a></td>
<td>捕獲 SIP 的功能。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>CryptSIPGetSignedDataMsg</strong></a></td>
<td>從檔案抓取 Authenticode 簽章。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>CryptSIPLoad</strong></a></td>
<td>載入動態連結程式庫，此程式庫會執行主體介面套件，並將適當的程式庫匯出函數指派給 <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> 結構。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>CryptSIPPutSignedDataMsg</strong></a></td>
<td>將 Authenticode 簽章儲存在目標檔案中。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>CryptSIPRemoveProvider</strong></a></td>
<td>移除先前對 <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a> 函式的呼叫所加入的 SIP。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>CryptSIPRemoveSignedDataMsg</strong></a></td>
<td>移除指定的 Authenticode 簽章。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>CryptSIPRetrieveSubjectGuid</strong></a></td>
<td>根據指定檔案中的標頭資訊來抓取 GUID。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>CryptSIPRetrieveSubjectGuidForCatalogFile</strong></a></td>
<td>抓取與指定檔案相關聯的主體 GUID。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>CryptSIPVerifyIndirectData</strong></a></td>
<td>針對提供的主體驗證間接雜湊資料。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>CryptUpdateProtectedState</strong></a></td>
<td>在使用者的 <a href="/windows/desktop/SecGloss/s-gly"><em>安全識別碼</em></a> (SID) 變更之後，遷移目前使用者的主要金鑰。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a></td>
<td>使用公開金鑰資訊來驗證主體憑證或 <a href="/windows/desktop/SecGloss/c-gly"><em>CRL</em></a> 的簽章。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>CryptVerifyCertificateSignatureEx</strong></a></td>
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a>的擴充版本。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>GetEncSChannel</strong></a></td>
<td>將加密的 Schannel DLL 內容儲存在記憶體中。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pCryptSIPGetCaps</strong></a></td>
<td>由 SIP 執行以報告功能。</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>資料轉換函數

下列 CryptoAPI 函數會將憑證結構成員轉換成不同的表單。

| 函式                                           | 描述                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAlgIdToOID**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | 將 CryptoAPI 演算法識別碼 (ALG 識別碼 \_) 轉換成 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) ([*asn.1)*](../secgloss/o-gly.md) OID (字串。 |
| [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | 從憑證取得主體或簽發者名稱，並將其轉換為以 null 結束的字元字串。                                                                                                                                                                                                               |
| [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | 將憑證名稱 [*BLOB*](../secgloss/b-gly.md) 轉換為以零結尾的字串。                                                                                                                                                                                                      |
| [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | 將 ASN. 1 物件識別碼字串轉換為 CSP 演算法識別碼。                                                                                                                                                                                                                                                 |
| [**CertRDNValueToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | 將名稱值轉換為以 null 結束的字串。                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | 將以 null 終止的 [*X. 500*](../secgloss/x-gly.md) 字串轉換成編碼的憑證名稱。                                                                                                                                                                                          |
| [**CryptBinaryToString**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | 將二進位序列轉換成格式化的字串。                                                                                                                                                                                                                                                                          |
| [**CryptFormatObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | 格式化編碼的資料，並傳回 Unicode 字串。                                                                                                                                                                                                                                                                          |
| [**CryptStringToBinary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | 將格式化字串轉換成二進位序列。                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>增強金鑰使用方法功能

下列函式會處理 [*增強金鑰使用*](../secgloss/e-gly.md) 方法 (EKU) 擴充功能和憑證的 eku 擴充屬性。 EKU 延伸模組和擴充屬性指定並限制憑證的有效使用。 延伸模組是憑證本身的一部分。 它們是由憑證的簽發者所設定，而且是唯讀的。 憑證擴充的屬性是與可以在應用程式中設定的憑證相關聯的值。

| 函式                                                                             | 描述                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CertAddEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | 將使用識別碼新增至憑證的 EKU 屬性。                       |
| [**CertGetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | 從憑證取得 EKU 延伸模組或屬性的相關資訊。 |
| [**CertRemoveEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | 從憑證的 EKU 擴充屬性移除使用識別碼。       |
| [**CertSetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | 設定憑證的 EKU 屬性。                                       |



 

### <a name="key-identifier-functions"></a>金鑰識別碼函數

金鑰識別碼函數可讓使用者建立、設定、抓取或尋找金鑰識別碼或其屬性。

金鑰識別碼是 [*公開/私密金鑰*](../secgloss/p-gly.md)組的唯一識別碼。 它可以是任何唯一的識別碼，但通常是編碼憑證 [**\_ 公開金鑰 \_ \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) 結構的20位元組 SHA1 雜湊。 金鑰識別碼可透過憑證的憑證 \_ 金鑰 \_ 識別碼識別碼（ID）來取得 \_ \_ 。 金鑰識別碼可讓您使用該 [*金鑰*](../secgloss/k-gly.md) 組來加密或解密訊息，而不需要使用憑證。

金鑰識別碼未與 [*crl*](../secgloss/c-gly.md) 或 [*ctl*](../secgloss/c-gly.md)相關聯。

金鑰識別碼可擁有與憑證內容相同的屬性。 如需詳細資訊，請參閱 [**CertCreateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>CryptCreateKeyIdentifierFromCSP</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 從 CSP 的 <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰 BLOB</em></a>建立金鑰識別碼。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>CryptEnumKeyIdentifierProperties</strong></a></td>
<td>列舉金鑰識別碼及其屬性。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>CryptGetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 從指定的金鑰識別碼取得特定屬性。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>CryptSetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
此 API 即將淘汰。 新的和現有的軟體應該開始使用 <a href="/windows/desktop/SecCNG/cng-portal">新一代密碼編譯 api。</a> Microsoft 可能會在未來的版本中移除此 API。
</blockquote>
<br/> 設定指定之金鑰識別碼的屬性。</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>OID 支援函式

這些函式會提供 [*物件識別碼*](../secgloss/o-gly.md) (OID) 支援。 這些函式會安裝、註冊和分派至 OID，以及編碼類型特定的函式。

下列 CryptoAPI 函數會使用這些 OID 支援函式：

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

如需此流程的總覽，請參閱 [擴充 CryptoAPI 功能](extending-cryptoapi-functionality.md)。

下列函式適用于 Oid。

| 函式                                                                       | 描述                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | 列舉以其編碼類型、函式名稱和 OID 識別的已註冊 OID 函數。                                                                                                                 |
| [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | 列舉其群組識別的已註冊 OID 資訊，並呼叫 *pfnEnumOIDInfo* 以取得相符專案。                                                                                                       |
| [**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | 使用指定的索引鍵和群組來尋找 OID 資訊。                                                                                                                                                          |
| [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | 釋放 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) 或 [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)所遞增和傳回的控制碼計數。 |
| [**CryptGetDefaultOIDDllList**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | 取得指定之函式集和編碼類型的已註冊預設 DLL 專案清單。                                                                                                              |
| [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | 取得第一個或下一個安裝的預設函數，或載入包含預設函式的 DLL。                                                                                                 |
| [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | 搜尋已安裝的函式清單，以取得編碼類型和 OID 相符的功能。 如果找不到相符的結果，則會搜尋相符的登錄。                                                                  |
| [**CryptGetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | 取得指定之編碼類型、函式名稱、OID 和值名稱的值。                                                                                                                            |
| [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | 初始化並傳回由提供的函式名稱所識別之 OID 函數集的控制碼。                                                                                                                 |
| [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | 安裝一組可呼叫的 OID 函數位址。                                                                                                                                                                 |
| [**CryptRegisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | 註冊包含要針對指定的編碼類型和函式名稱呼叫之預設函式的 DLL。                                                                                               |
| [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | 註冊包含要針對指定的編碼類型、函式名稱和 OID 呼叫之函式的 DLL。                                                                                                 |
| [**CryptRegisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | 註冊 [**CRYPT \_ oid \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) 結構中指定的 oid 資訊，並將其保存到登錄中。                                                                                |
| [**CryptSetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | 設定指定之編碼類型、函式名稱、OID 和值名稱的值。                                                                                                                                |
| [**CryptUnregisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | 移除包含要針對指定的編碼類型和函式名稱呼叫之預設函式之 DLL 的註冊。                                                                            |
| [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | 移除包含要針對指定的編碼類型、函式名稱和 OID 呼叫之函式之 DLL 的註冊。                                                                              |
| [**CryptUnregisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | 移除指定之 OID 資訊的註冊。                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>遠端物件抓取函式

下列函式可讓使用者 (PKI) 物件取得公開金鑰基礎結構、取得憑證、CTL 或 CRL 的 URL，或從物件解壓縮 URL。

| 函式                                                     | 描述                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**CryptGetObjectUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | 從憑證、CTL 或 CRL 取得遠端物件的 URL。 |
| [**CryptRetrieveObjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | 從 URL 指定的位置抓取 PKI 物件。           |



 

### <a name="pfx-functions"></a>PFX 函數

下列功能支援 (PFX) 格式 [*blob*](../secgloss/b-gly.md)的個人資訊交換。

| 函式                                             | 描述                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFXExportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | 從參考的 [*憑證存放區*](../secgloss/c-gly.md) 匯出憑證，以及其相關聯的 [*私密金鑰*](../secgloss/p-gly.md)（如果有的話）。 |
| [**PFXExportCertStoreEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | 從參考的憑證存放區匯出憑證，以及其相關聯的私密金鑰（如果有的話）。                                                                                                                                                             |
| [**PFXImportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | 匯入 PFX BLOB，並傳回存放區的控制碼，其中包含憑證和任何相關聯的私密金鑰。                                                                                                                                                            |
| [**PFXIsPFXBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | 嘗試將 BLOB 的外部層解碼為 PFX 封包。                                                                                                                                                                                                                |
| [**PFXVerifyPassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | 嘗試將 BLOB 的外部層解碼為 PFX 封包，並使用指定的密碼將它解密。                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>憑證服務備份和還原功能

憑證服務包含用來備份和還原憑證服務資料庫的功能。 這些憑證服務備份和還原功能都包含在 Certadm.dll 中。 不同于與憑證服務相關聯的其他 API 元素，這些函式不會封裝在可以用來呼叫類別方法的物件中。 相反地，藉由呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，然後藉由呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)來判斷函式的位址，藉 Certadm.dll 以呼叫備份和還原 api。 當您完成呼叫憑證服務備份和還原函式時，請呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) ，以從記憶體釋放 Certadm.dll 資源。

> [!Note]
> Certadm.dll 所提供的備份和還原功能不會備份或還原憑證服務的 [*私密金鑰*](../secgloss/p-gly.md)。 如需備份憑證服務私密金鑰的詳細資訊，請參閱 [備份和還原憑證服務私密金鑰](backing-up-and-restoring-the-certificate-services-private-key.md)。
> 
> 若要呼叫備份和還原功能，您必須擁有備份和還原 [*許可權*](../secgloss/p-gly.md)。 如需詳細資訊，請參閱 [設定備份和還原許可權](setting-the-backup-and-restore-privileges.md)。

 

> [!Note]  
> 如果先前是在用來呼叫憑證服務備份和還原 Api 的相同執行緒中呼叫 **CoInitializeEx** ，則必須將 COINIT \_ APARTMENTTHREADED 旗標傳遞到 **CoInitializeEx**。 也就是說，當您使用相同的執行緒時，如果執行緒先前在呼叫 CoInitializeEx 時傳入了 COINIT \_ 多執行緒旗標，您就無法呼叫憑證服務備份和還原API。

 

憑證服務備份 Api 定義于 Certbcli 中。 但是，當您建立程式時，請使用 Certsrv 作為 include 檔。

Certadm.dll 會匯出下列 Api。

| 函式                                                                         | 描述                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | 關閉開啟的檔案。                                                                                                |
| [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | 結束備份會話。                                                                                                |
| [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | 釋放由備份和還原 Api 所配置的緩衝區。                                                              |
| [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | 傳回需要備份的記錄檔清單。                                                                |
| [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | 傳回需要備份的資料庫檔案清單。                                                           |
| [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | 抓取需要針對指定的備份內容備份的憑證服務動態檔案名清單。 |
| [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | 開啟檔案以準備進行備份。                                                                        |
| [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | 準備資料庫以進行線上備份。                                                                          |
| [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | 讀取已開啟檔案的內容。                                                                                 |
| [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | 截斷記錄檔。                                                                                              |
| [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | 判斷憑證服務伺服器是否在線上 (主動執行) 。                                        |
| [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | 結束還原會話。                                                                                               |
| [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | 取得 (用於備份和還原案例) 的資料庫位置。                                            |
| [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | 開始還原會話。                                                                                             |
| [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | 註冊還原作業。                                                                                        |
| [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | 完成先前註冊的還原作業。                                                                  |
| [**CertSrvRestoreRegisterThroughFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | 註冊還原作業。                                                                                        |
| [**CertSrvServerControl**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | 將控制命令傳送到憑證服務實例。                                                         |



 

## <a name="callback-functions"></a>回呼函式

本節中的回呼函式是用來註冊或安裝應用程式定義的 [*憑證存放區*](../secgloss/c-gly.md) 提供者，以及透過回呼函式提供相關的功能。 回呼函式是由應用程式所執行，而且是由 [*CryptoAPI*](../secgloss/c-gly.md) 函式所呼叫。 回呼函數可讓應用程式控制 CryptoAPI 函式運算元據的方式。

| 回呼函數                                                                                                        | 使用                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertChainFindByIssuerCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | 應用程式定義的回呼函式，可讓應用程式篩選可能會新增至憑證鏈的憑證。                                                                                                                                                                                                     |
| [**CertDllOpenStoreProv**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | 定義存放區提供者 open 函數。                                                                                                                                                                                                                                                                                                     |
| [**CertEnumPhysicalStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)函式所使用的回呼函式，用來格式化和呈現每個找到的實體存放區的資訊。                                                                                                                                                                                 |
| [**CertEnumSystemStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)函式所使用的回呼函式，用來格式化和呈現每個找到的實體存放區的資訊。                                                                                                                                                                                     |
| [**CertEnumSystemStoreLocationCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)函式所使用的回呼函式，用來格式化和呈現每個找到的實體存放區的資訊。                                                                                                                                                                     |
| [**CertStoreProvCloseCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | 決定當開啟存放區的 [*參考計數*](../secgloss/r-gly.md) 變成零時，會發生什麼事。                                                                                                                                                                                    |
| [**CertStoreProvControl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | 允許應用程式在使用中的快取存放區內容和存放區保存儲存時的內容有差異時，收到通知。                                                                                                                                                                   |
| [**CertStoreProvDeleteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | 決定從憑證存放區刪除憑證之前所要採取的動作。                                                                                                                                                                                                                                                      |
| [**CertStoreProvDeleteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | 決定從憑證存放區刪除 [*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) 之後要採取的動作。                                                                                                                        |
| [**CertStoreProvDeleteCTL**](certstoreprovdeletectl.md)                                                                 | 判斷是否可刪除 CTL。                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvFindCert**](certstoreprovfindcert.md)                                                                   | 在存放區中尋找符合指定準則的第一個或下一個憑證。                                                                                                                                                                                                                                                             |
| [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)                                                                     | 在存放區中尋找符合指定準則的第一個或下一個 CRL。                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFindCTL**](certstoreprovfindctl.md)                                                                     | 在存放區中尋找符合指定準則的第一個或下一個 CTL。                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFreeFindCert**](certstoreprovfreefindcert.md)                                                           | 釋出先前找到的憑證內容。                                                                                                                                                                                                                                                                                                 |
| [**CertStoreProvFreeFindCRL**](certstoreprovfreefindcrl.md)                                                             | 釋出先前找到的 CRL 內容。                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvFreeFindCTL**](certstoreprovfreefindctl.md)                                                             | 釋放先前找到的 CTL 內容。                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvGetCertProperty**](certstoreprovgetcertproperty.md)                                                     | 抓取憑證的指定屬性。                                                                                                                                                                                                                                                                                              |
| [**CertStoreProvGetCRLProperty**](certstoreprovgetcrlproperty.md)                                                       | 抓取 CRL 的指定屬性。                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvGetCTLProperty**](certstoreprovgetctlproperty.md)                                                       | 抓取 CTL 的指定屬性。                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | 目前未使用，但可能會匯出至未來的 Csp。                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | 目前未使用，但可能會匯出至未來的 Csp。                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCTL**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | 讀取提供者的 CTL 內容複本，如果存在，請建立新的 CTL 內容。                                                                                                                                                                                                                                                     |
| [**CertStoreProvSetCertPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | 決定在呼叫 [**CertSetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) 或 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)之前所要採取的動作。                                                                                                                             |
| [**CertStoreProvSetCRLPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | 決定在呼叫 [**CertSetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) 或 [**CertGetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)之前所要採取的動作。                                                                                                                                                             |
| [**CertStoreProvSetCTLProperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | 判斷是否可以在 CTL 上設定屬性。                                                                                                                                                                                                                                                                                            |
| [**CertStoreProvWriteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | 決定將憑證新增至存放區之前所要採取的動作。                                                                                                                                                                                                                                                                        |
| [**CertStoreProvWriteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | 決定將 CRL 新增至存放區之前所要採取的動作。                                                                                                                                                                                                                                                                                |
| [**CertStoreProvWriteCTL**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | 判斷是否可以將 CTL 新增至存放區。                                                                                                                                                                                                                                                                                           |
| [**CRYPT \_ 列舉 \_ KEYID \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | [**CryptEnumKeyIdentifierProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties)函式所使用的回呼函數。                                                                                                                                                                                                                          |
| [**CRYPT \_ 列舉 \_ OID \_ 函數**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)函式所使用的回呼函數。                                                                                                                                                                                                                                                  |
| [**CRYPT \_ 列舉 \_ OID \_ 資訊**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)函式所使用的回呼函數。                                                                                                                                                                                                                                                          |
| [**CryptGetSignerCertificateCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | 搭配 [**CRYPT \_ 驗證 \_ 訊息 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) 結構使用的回呼函式，以取得並驗證訊息簽署者的憑證。                                                                                                                                                                                 |
| [**PCRYPT \_ 解密 \_ 私用 \_ 金鑰 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8)函式所使用的回呼函數。                                                                                                                                                                                                                                                          |
| [**PCRYPT \_ 加密 \_ 私用 \_ 金鑰 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | 建立 [**CRYPT \_ 加密的 \_ 私密金鑰 \_ \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) 結構時所使用的回呼函數。                                                                                                                                                                                                          |
| [**PCRYPT \_ RESOLVE \_ HCRYPTPROV \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8)函式所使用的回呼函數。                                                                                                                                                                                                                                                          |
| [**PFN \_ CDF \_ 剖析 \_ 錯誤 \_ 回呼**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | 剖析目錄定義檔 (CDF) 時，針對目錄定義函式所呼叫的使用者定義函數錯誤。                                                                                                                                                                                                                          |
| [**PFN \_ CERT \_ CREATE \_ 內容 \_ 排序 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | 在建立內容時針對每個已排序的內容專案呼叫。                                                                                                                                                                                                                                                                               |
| [**PFN \_ CMSG \_ CNG 匯 \_ 入 \_ 內容 \_ 加密 \_ 金鑰**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | CNG [*物件識別碼*](../secgloss/o-gly.md) (OID) 可安裝的函式，以匯入已解密的內容加密金鑰 (CEK) 。                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG 匯 \_ 入 \_ 金鑰 \_ 同意**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | 匯入封包訊息的金鑰傳輸收件者的內容加密金鑰。                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG 匯 \_ 入 \_ 金鑰 \_ 交易**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | CNG OID 可安裝的函式，用於匯入和 [*解密*](../secgloss/d-gly.md) 金鑰-傳輸-收件者、加密、內容 [*加密*](../secgloss/e-gly.md) 金鑰 (CEK) 。                                                                   |
| [**PFN \_ CMSG \_ 匯出 \_ 金鑰 \_ 同意**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | 針對封包訊息的重要合約收件者，加密及匯出內容加密金鑰。                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ 匯出 \_ 金鑰 \_ 交易**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | 為封包訊息的金鑰傳輸收件者加密及匯出內容加密金鑰。                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ 匯出 \_ 郵寄清單 \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | 為封包訊息的郵寄清單收件者加密及匯出內容加密金鑰。                                                                                                                                                                                                                                         |
| [**PFN \_ CMSG \_ GEN \_ CONTENT \_ 加密 \_ 金鑰**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | 產生用來加密封包訊息之內容的 [*對稱金鑰*](../secgloss/s-gly.md) 。                                                                                                                                                                                     |
| [**PFN \_ CMSG 匯 \_ 入 \_ 金鑰 \_ 同意**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | 匯入封包訊息的金鑰傳輸收件者的內容加密金鑰。                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG 匯 \_ 入 \_ 金鑰 \_ 交易**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | 匯入封包訊息的金鑰傳輸收件者的內容加密金鑰。                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ 匯 \_ 入 \_ 郵寄清單**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | 匯入封包訊息的金鑰傳輸收件者的內容加密金鑰。                                                                                                                                                                                                                                                       |
| [**PFN \_ CRYPT \_ 匯出 \_ 公開金鑰 \_ \_ 資訊 \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | 由 [**CryptExportPublicKeyInfoEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) 呼叫，以匯出公開金鑰 BLOB 並進行編碼。                                                                                                                                                                                                                         |
| [**PFN CRYPT 將編碼的簽章 \_ \_ \_ \_ \_ 參數 \_ FUNC 解壓縮**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | 呼叫以解碼和傳回雜湊演算法識別碼，並選擇性地傳回簽章參數。                                                                                                                                                                                                                                            |
| [**PFN \_ CRYPT \_ 正負號 \_ 和 \_ 編碼 \_ 雜湊 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | 呼叫以簽署及編碼計算的雜湊。                                                                                                                                                                                                                                                                                                    |
| [**PFN \_ CRYPT \_ 驗證編碼的簽章 \_ \_ \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | 呼叫以解密編碼的簽章，並將其與計算的雜湊進行比較。                                                                                                                                                                                                                                                                     |
| [**PFN \_ 匯 \_ 入 \_ 公開金鑰 \_ 資訊 \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | 由 [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) 呼叫以解碼 [*公開金鑰演算法*](../secgloss/p-gly.md) 識別碼、載入演算法提供者，以及匯入 [*金鑰*](../secgloss/k-gly.md)組。 |
| [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)                                                                       | 使用者定義的回呼函式，可讓 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) 函式的呼叫者處理使用者選取要查看的憑證顯示。                                                                                                                               |
| [**PFNCMFILTERPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | 篩選每個憑證，以決定它是否會顯示在 [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) 函式所顯示的憑證選取對話方塊中。                                                                                                                                                                |
| [**PFNCMHOOKPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | 在 [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) 函式所產生的憑證選取對話方塊處理訊息之前呼叫。                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>目錄定義函數

這些函數用來建立目錄。 所有這些函式都是由 [MakeCat](makecat.md)呼叫。

| 函式                                                                           | 描述                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATCDFClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | 關閉目錄定義檔，並釋放對應 [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) 結構的記憶體。 |
| [**CryptCATCDFEnumAttributesWithCDFTag**](cryptcatcdfenumattributeswithcdftag.md) | 列舉 CDF **CatalogFiles** 區段中成員檔案的屬性。                                       |
| [**CryptCATCDFEnumCatAttributes**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | 列舉 CDF **CatalogHeader** 區段內的目錄層級屬性。                                        |
| [**CryptCATCDFEnumMembersByCDFTagEx**](cryptcatcdfenummembersbycdftagex.md)       | 列舉 CDF **CatalogFiles** 區段中的個別檔案成員。                                          |
| [**CryptCATCDFOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | 開啟現有的 CDF 以讀取和初始化 [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) 結構。                         |



 

## <a name="catalog-functions"></a>目錄函式

這些函數用來管理目錄。

| 函式                                                                             | 描述                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATAdminAcquireCoNtext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | 取得目錄管理員內容的控制碼。 後續呼叫 [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)、 [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)和 [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) 函式時，可以使用這個控制碼。 |
| [**CryptCATAdminAcquireCoNtext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | 取得指定雜湊演算法和雜湊原則的目錄管理員內容控制碼。                                                                                                                                                                                                                                   |
| [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | 將目錄新增至目錄資料庫。                                                                                                                                                                                                                                                                                            |
| [**CryptCATAdminCalcHashFromFileHandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | 計算檔案的雜湊。                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | 使用指定的演算法來計算檔案的雜湊。                                                                                                                                                                                                                                                                   |
| [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | 列舉包含指定雜湊的目錄。                                                                                                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCatalogCoNtext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | 釋放 [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) 函式先前所傳回的目錄內容控制碼。                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCoNtext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | 釋放 [**CryptCATAdminAcquireCoNtext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) 函式先前所指派的控制碼。                                                                                                                                                                                                        |
| [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | 刪除類別目錄檔案，並從 Windows 目錄資料庫移除該目錄的專案。                                                                                                                                                                                                                                         |
| [**CryptCATAdminResolveCatalogPath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | 抓取指定之目錄的完整路徑。                                                                                                                                                                                                                                                                       |
| [**CryptCATCatalogInfoFromCoNtext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | 從指定的目錄內容抓取目錄資訊。                                                                                                                                                                                                                                                                    |
| [**CryptCATClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | 關閉 [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) 函數先前開啟的目錄控制碼。                                                                                                                                                                                                                                    |
| [**CryptCATEnumerateAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | 列舉與目錄成員相關聯的屬性。                                                                                                                                                                                                                                                                   |
| [**CryptCATEnumerateCatAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | 列舉與目錄相關聯的屬性。                                                                                                                                                                                                                                                                               |
| [**CryptCATEnumerateMember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | 列舉目錄的成員。                                                                                                                                                                                                                                                                                               |
| [**CryptCATGetAttrInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | 抓取目錄成員之屬性的相關資訊。                                                                                                                                                                                                                                                                 |
| [**CryptCATGetMemberInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | 從目錄的 PKCS 7 捕獲成員資訊 \# 。 除了針對指定的參考標記來取得成員資訊之外，此函式也會開啟成員內容。                                                                                                                                                    |
| [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | 開啟目錄，並將內容控制碼傳回至開啟的目錄。                                                                                                                                                                                                                                                                 |
| [**IsCatalogFile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | 抓取布林值，指出指定的檔案是否為類別目錄檔案。                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>WinTrust 函式

下列函式可用來執行各種信任作業。

| 函式                                                                               | 描述                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | 將信任提供者動作加入使用者的系統中。                                                                                                                   |
| [**WintrustGetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | 捕獲原則提供者的原則旗標。                                                                                                                        |
| [**WintrustAddDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | 指定提供者的預設使用識別碼和回呼資訊                                                                                       |
| [**WintrustGetDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | 抓取預設使用識別碼和回呼資訊。                                                                                                     |
| [**WintrustLoadFunctionPointers**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | 載入指定動作 GUID 的函式進入點。                                                                                                             |
| [**WintrustRemoveActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | 移除 [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) 函數所加入的動作。                                                                          |
| [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | 設定預設設定，這個設定會決定建立主體介面封裝時是否包含分頁雜湊， (SIP) 可攜式可執行檔的間接資料。 |
| [**WintrustSetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | 設定原則提供者的原則旗標。                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | 在指定的物件上執行信任驗證動作。                                                                                                          |
| [**WinVerifyTrustEx**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | 在指定的物件上執行信任驗證動作，並採用 WINTRUST \_ 資料結構的指標。                                                        |
| [**WTHelperCertCheckValidSignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | 檢查簽章是否有效。                                                                                                                                 |
| [**WTHelperCertFindIssuerCertificate**](wthelpercertfindissuercertificate.md)         | 從指定的憑證存放區尋找符合指定主體憑證的簽發者憑證。                                                    |
| [**WTHelperCertIsSelfSigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | 檢查憑證是否為自我簽署。                                                                                                                         |
| [**WTHelperGetFileHash**](wthelpergetfilehash.md)                                     | 驗證已簽署檔案的簽章，並取得檔案的雜湊值和演算法識別碼。                                                            |
| [**WTHelperGetProvCertFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | 從憑證鏈抓取信任提供者憑證。                                                                                                   |
| [**WTHelperGetProvPrivateDataFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | 使用提供者識別碼，從連結收 [**CRYPT \_ 提供者 \_ PRIVDATA**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) 結構。                                           |
| [**WTHelperGetProvSignerFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | 從鏈中依索引抓取簽署者或 countersigner。                                                                                                         |
| [**WTHelperProvDataFromStateData**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | 從指定的控制碼抓取信任提供者資訊。                                                                                                        |



 

## <a name="object-locator-functions"></a>物件定位器函數

下列回呼函式可以由安全通道所要呼叫的自訂提供者來執行 (Schannel) 安全性封裝以取得憑證。



| 函式                                                                                                             | 描述                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ 排清**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | 指定物件已經變更。                   |
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ GET**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | 抓取物件。                                    |
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ 版本**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | 釋放提供者。                                  |
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ 可用 \_ 密碼**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | 釋放用來加密 PFX 位元組陣列的密碼。 |
| [**PFN \_ CRYPT \_ OBJECT \_ 定位器 \_ PROVIDER \_ FREE**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | 釋放提供者所傳回的物件。           |
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ 可用 \_ 識別碼**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | 釋放物件識別碼的記憶體。               |
| [**PFN \_ CRYPT \_ 物件 \_ 定位器 \_ 提供者 \_ 初始化**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | 將提供者初始化。                               |



 

 

 
