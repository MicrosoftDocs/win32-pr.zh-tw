---
description: CryptXML 可讓開發人員藉由註冊整個系統的密碼編譯延伸模組 DLL，擴充原生支援的密碼編譯演算法。
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: XML 數位簽章密碼編譯延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf0f2d99b34d59e9817f8568b03be20e72dda1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474934"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>XML 數位簽章密碼編譯延伸模組

CryptXML 可讓開發人員藉由註冊整個系統的密碼編譯延伸模組 DLL，擴充原生支援的密碼編譯演算法。 擴充 Dll 會擴充 **SignatureMethod** 和 **DigestMethod** XML 元素所支援的演算法。 延伸模組 Dll 可支援將其他參數編碼成 XML 數位簽章的演算法。

所有延伸模組 Dll 都必須支援 [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) 函式，此函式會傳回 [**CRYPT \_ XML 密碼編譯 \_ \_ 介面**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) 結構的指標。 此結構提供函式指標來執行密碼編譯延伸模組函式。 支援的函式取決於支援的密碼編譯演算法類型，以及演算法是否必須將參數編碼為 XML 數位簽章。

密碼編譯延伸模組函式包含下列函式指標：

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>必要函數
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest 方法函數
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature 方法函數
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>針對具有預設編碼參數的演算法
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

密碼編譯延伸模組 Dll 是以全系統為基礎進行註冊。 需要系統管理員許可權才能註冊密碼編譯延伸模組 DLL。

所有 CryptXML 的密碼編譯延伸模組都是由 **SignatureMethod** 或 **DigestMethod** 元素的演算法屬性欄位中設定的 URI 值所註冊。

擴充 Dll 的登錄路徑如下所示：

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>bit.msi
</dt> <dd>

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bit.msi
</dt> <dd>

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{uri}*

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **WOW6432NODE** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> </dl>

每個金鑰都包含下列設定。




| 名稱 | 類型 | 資料 | 
|------|------|------|
| DLL<br /> | 可擴充的字串<br /> | 必要。<br />XML 密碼編譯提供者 DLL 的絕對路徑。<blockquote><p><b>注意： </b>建議您在只能由具有系統管理許可權的應用程式寫入的目錄中，使用密碼編譯延伸模組 Dll。</p><p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> 用來載入密碼編譯延伸模組 DLL。<br /></p></blockquote><br /> | 
| 名稱<br /> | <strong>String</strong> | 選擇性。<br /> 與此 URI 相關聯的顯示名稱。<br /> | 
| GroupId<br /> | <strong>DWORD</strong> | 必要。<br /> 與此密碼編譯演算法相關聯的群組識別碼。 可能的值包括下列各項：<strong>CRYPT_XML_GROUP_ID_HASH</strong> \<strong> </strong> = 1<br /><strong></strong> \<strong> CRYPT_XML_GROUP_ID_SIGN </strong>= 2<br /> | 
| CNGAlgid<br /> | <strong>String</strong> | 必要。<br /> 要傳遞給 BCrypt 或 NCrypt 函數的 CNG 演算法名稱。<br /> | 
| CNGExtraAlgid<br /> | <strong>String</strong> | 選擇性。<br /> 額外的演算法字串，而非 CNGAlgid 成員中的字串，可以傳遞給 CNG 函數。<br /> 針對 (CRYPT_XML_GROUP_ID_SIGN) 的簽章演算法，此成員是要傳遞至 CNG 函數的公開金鑰演算法字串。<br /> 對於 GroupId 的其他值，請將 <strong>pwszCNGExtraAlgid</strong> 成員設定為空字串 ""。 <br /> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>


</dt> <dt>

[XML 數位簽章密碼編譯演算法](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
