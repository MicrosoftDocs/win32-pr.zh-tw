---
description: 定義 CAPICOM 傳回的錯誤碼。
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: 'CAPICOM_ERROR_CODE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989854"
---
# <a name="capicom_error_code-enumeration"></a>CAPICOM \_ 錯誤碼 \_ 列舉

**Capicom \_ 錯誤碼 \_** 列舉型別會定義由 capicom 傳回的錯誤碼。

> [!Note]  
> Visual Basic Scripting Edition 錯誤會傳回大於零的 **Err** 數值。 針對這些錯誤，錯誤 **。描述** 值會提供錯誤原因的相關資訊。 除了 Visual Basic Scripting Edition 錯誤之外，CAPICOM 錯誤還會傳回由 **capicom \_ 錯誤碼 \_** 定義的程式碼。

 

## <a name="members"></a>成員



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>member</th>
<th>描述</th>
<th>值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></td>
<td>使用了不正確編碼類型。<br/> 下列清單顯示有效的編碼類型：
<ul>
<li>CAPICOM_ENCODE_ANY</li>
<li>CAPICOM_ENCODE_BASE64</li>
<li>CAPICOM_ENCODE_BINARY</li>
</ul>
<br/></td>
<td>0x80880100</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EKU_INVALID_OID</strong></td>
<td>無法設定<a href="eku.md"><strong>EKU</strong></a>物件的<a href="eku-oid.md"><strong>OID</strong></a>屬性，因為<a href="eku-name.md"><strong>Name</strong></a>屬性未設定為 CAPICOM_EKU_OTHER。<br/> 設定<a href="eku-oid.md"><strong>OID</strong></a>屬性之前，請先將 [<a href="eku-name.md"><strong>名稱</strong></a>] 屬性設定為 CAPICOM_EKU_OTHER。<br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td><a href="eku.md"><strong>EKU</strong></a>物件的<a href="eku-oid.md"><strong>OID</strong></a>屬性尚未初始化。 <br/> 將 [ <a href="eku-name.md"><strong>名稱</strong></a> ] 屬性設定為 [CAPICOM_EKU_OTHER 以外的任何內容，或將 [ <strong>名稱</strong> ] 屬性設定為 [CAPICOM_EKU_OTHER]，並將 [ <a href="eku-oid.md"><strong>OID</strong></a> ] 屬性設定為值。<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td><a href="certificate.md"><strong>憑證</strong></a>物件尚未初始化。<br/> 通常，當 <a href="certificate.md"><strong>憑證</strong></a> 物件具現化但未與數位憑證相關聯時，就會傳回此錯誤碼。 若要建立物件與數位憑證之間的關聯，請將它指派給現有的 <strong>憑證</strong> 物件或呼叫匯 <a href="certificate-import.md"><strong>入</strong></a> 方法。<br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRI加值稅E_KEY</strong></td>
<td><a href="certificate.md"><strong>憑證</strong></a>物件沒有相關聯的私密金鑰。<br/> 嘗試使用簽署人的私密金鑰來簽署資料時，會傳回此錯誤碼，但與<a href="signer.md"><strong>簽署者</strong></a>物件相關聯的<a href="certificate.md"><strong>憑證</strong></a>物件無法用於簽署作業。<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td><a href="chain.md"><strong>鏈</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="chain.md"><strong>Chain</strong></a> 物件，請呼叫 <a href="chain-build.md"><strong>Build</strong></a> 方法。<br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td><a href="store.md"><strong>存放區</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="store.md"><strong>存放區</strong></a> 物件，請呼叫 <a href="store-open.md"><strong>Open</strong></a> 方法。<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td><a href="store.md"><strong>存放區</strong></a>物件未包含任何<a href="certificate.md"><strong>憑證</strong></a>物件。<br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td><a href="store-open.md"><strong>Store. Open</strong></a>方法的<em>OpenMode</em>參數不包含有效的 CAPICOM_STORE_OPEN_MODE 值。<br/> 下列清單顯示 CAPICOM_STORE_OPEN_MODE 的有效值：
<ul>
<li>CAPICOM_STORE_OPEN_READ_ONLY</li>
<li>CAPICOM_STORE_OPEN_READ_WRITE</li>
<li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li>
<li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li>
<li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li>
</ul>
<br/></td>
<td>0x80880232</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></td>
<td>傳遞給<a href="store.md"><strong>Store</strong></a>物件之<a href="store-export.md"><strong>Export</strong></a>方法的<em>SaveAs</em>值無效。 <br/> 下列清單顯示有效的 <em>SaveAs</em> 值：
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>尚未初始化<a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-name.md"><strong>Name</strong></a>屬性。 <br/> 設定 [ <a href="attribute-name.md"><strong>名稱</strong></a> ] 屬性。<br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>尚未初始化<a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-value.md"><strong>Value</strong></a>屬性。 <br/> 設定 <a href="attribute-value.md"><strong>Value</strong></a> 屬性。<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td><a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-name.md"><strong>Name</strong></a>屬性無效。 <br/> 下列清單顯示有效的屬性名稱：
<ul>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li>
</ul>
<br/></td>
<td>0x80880242</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></td>
<td><a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-value.md"><strong>Value</strong></a>屬性無效，因為資料類型不符合<strong>名稱</strong>屬性所指定的資料類型。 <br/> 例如，如果 [ <a href="attribute-value.md"><strong>名稱</strong></a> ] 屬性設定為 [CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME]，則資料類型必須是 [ <strong>日期</strong>]。<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td><a href="signer.md"><strong>簽署者</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="signer.md"><strong>簽署者</strong></a> 物件，請設定 <a href="signer-certificate.md"><strong>Certificate</strong></a> 屬性。<br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>在 <a href="signeddata.md"><strong>SignedData</strong></a> 物件中找不到簽署人。 <br/> 通常不會發生這種情況，因為 <a href="signeddata.md"><strong>SignedData</strong></a> 物件是由 CAPICOM 所建立;但是，如果 <strong>SignedData</strong> 物件是由協力廠商產品所建立，則簽署者的憑證可能不會包含在 PKCS #7 結構中。<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>在<a href="signer.md"><strong>簽署人</strong></a>物件中找不到<a href="chain.md"><strong>鏈</strong></a>物件。<br/></td>
<td>0x80880252//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>嘗試以不正確方式使用簽署人。<br/></td>
<td>0x80880253 //v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td><a href="signeddata.md"><strong>SignedData</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="signeddata.md"><strong>SignedData</strong></a> 物件，請設定 <a href="signeddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="signeddata-verify.md"><strong>Verify</strong></a> 方法。<br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td><a href="signeddata.md"><strong>SignedData</strong></a>物件包含不正確類型。 <br/> 通常，這會在嘗試使用 <a href="signeddata.md"><strong>SignedData</strong></a> 物件驗證封包訊息時發生，反之亦然。<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td><a href="signeddata.md"><strong>SignedData</strong></a>物件尚未簽署。 <br/> 若要簽署 <a href="signeddata.md"><strong>SignedData</strong></a> 物件，請呼叫 <a href="signeddata-sign.md"><strong>sign</strong></a> 方法。<br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td><a href="algorithm.md"><strong>演算法</strong></a>物件的 [<a href="algorithm-name.md"><strong>名稱</strong></a>] 屬性的演算法值無效。 <br/> 下列清單顯示 <a href="algorithm-name.md"><strong>Name</strong></a> 屬性的有效演算法值：
<ul>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li>
</ul>
<br/></td>
<td>0x80880270</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></td>
<td><a href="algorithm.md"><strong>演算法</strong></a>物件之<a href="algorithm-keylength.md"><strong>KeyLength</strong></a>屬性的金鑰長度值無效。 <br/> 下列清單顯示 <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> 屬性的有效金鑰長度值：
<ul>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li>
</ul>
<br/></td>
<td>0x80880271</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></td>
<td><a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件，請設定 <a href="envelopeddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="envelopeddata-decrypt.md"><strong>解密</strong></a> 方法。<br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td><a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件包含不正確類型。 <br/> 通常，這會在嘗試使用 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件驗證已簽署的訊息時發生，反之亦然。<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>呼叫<strong>EnvelopedData</strong>物件的<a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a>方法時，不會在<a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件中指定任何收件者。 <br/> 若要加入收件者，請呼叫收件者 <a href="recipients-add.md"><strong>。 add</strong></a> 方法。<br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>在 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件中找不到收件者。 <br/> 通常不會發生這種情況，因為 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件是由 CAPICOM 所建立;但是，如果 <strong>EnvelopedData</strong> 物件是由協力廠商產品所建立，則該收件者的憑證可能不會包含在 PKCS #7 結構中。<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td><a href="encrypteddata.md"><strong>A</strong></a>物件尚未初始化。 <br/> 若要初始化 <a href="encrypteddata.md"><strong>a</strong></a> 物件，請設定 <a href="encrypteddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="encrypteddata-decrypt.md"><strong>解密</strong></a> 方法。<br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td><a href="encrypteddata.md"><strong>A</strong></a>物件不是有效的類型。 <br/> 這通常表示資料已損毀。<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td><a href="encrypteddata.md"><strong>A</strong></a>物件的密碼尚未初始化。 <br/> 若要初始化 <a href="encrypteddata.md"><strong>a</strong></a> 物件的秘密，請呼叫 <a href="encrypteddata-setsecret.md"><strong>>client.setsecret</strong></a> 方法。<br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRI加值稅E_KEY_NOT_INITIALIZED</strong></td>
<td><a href="privatekey.md"><strong>PrivateKey</strong></a>物件尚未初始化。<br/></td>
<td>0x80880300//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRI加值稅E_KEY_NOT_EXPORTABLE</strong></td>
<td>無法匯出 <a href="privatekey.md"><strong>PrivateKey</strong></a> 物件。<br/></td>
<td>0x80880301//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td><a href="encodeddata.md"><strong>EncodedData</strong></a>物件尚未初始化。<br/></td>
<td>0x80880320//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td><a href="extension.md"><strong>擴充</strong></a>物件尚未初始化。<br/></td>
<td>0x80880330//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td><a href="extendedproperty.md"><strong>ExtendedProperty</strong></a>物件的<a href="extendedproperty-propid.md"><strong>PropID</strong></a>屬性尚未初始化。<br/></td>
<td>0x80880340//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>憑證的 <em>FindType</em> 參數 <a href="certificates-find.md"><strong>。 Find</strong></a> 方法不是 <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> 列舉的值。<br/></td>
<td>0x80880350//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>針對尋找作業指定的預先定義原則無效。<br/></td>
<td>0x80880351//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td><a href="signedcode.md"><strong>SignedCode</strong></a>物件尚未初始化。<br/></td>
<td>0x80880360//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td><a href="signedcode.md"><strong>SignedCode</strong></a>物件尚未簽署。<br/> 若要簽署 <a href="signedcode.md"><strong>SignedCode</strong></a> 物件，請呼叫 <a href="signedcode-sign.md"><strong>sign</strong></a> 方法。<br/></td>
<td>0x80880361//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td><a href="signedcode.md"><strong>SignedCode</strong></a>物件的<a href="signedcode-description.md"><strong>Description</strong></a>屬性尚未初始化。<br/></td>
<td>0x80880362//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td><a href="signedcode.md"><strong>SignedCode</strong></a>物件的<a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a>屬性尚未初始化。<br/></td>
<td>0x80880363//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td><a href="signedcode-timestamp.md"><strong>SignedCode</strong></a>的<em>URL</em>參數無效。<br/></td>
<td>0x80880364//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td><a href="hasheddata.md"><strong>HashedData</strong></a>物件不包含任何資料。<br/></td>
<td>0x80880370//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>轉換類型無效。<br/></td>
<td>0x80880380//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>目前的平臺不支援要求的操作。 <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>簽署時，尚未設定<a href="signer.md"><strong>簽署者</strong></a>物件的<a href="signer-certificate.md"><strong>Certificate</strong></a>屬性，但使用者憑證的提示已停用。 <br/> 設定<a href="settings.md"><strong>[設定] 物件的</strong></a>[ <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> ] 屬性，或設定 [<a href="signer.md"><strong>簽署者</strong></a>] 物件的 [<a href="signer-certificate.md"><strong>憑證</strong></a>] 屬性，即可啟用提示。<br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>使用者已取消作業。 <br/> 當系統提示使用者執行特定作業（例如存取私密金鑰），而使用者取消作業時，就會發生這種情況。<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>不允許嘗試的操作。<br/> 例如，如果物件附加至憑證，就不允許變更<a href="extendedproperty.md"><strong>ExtendedProperty</strong></a>物件的<a href="extendedproperty-propid.md"><strong>PropID</strong></a>屬性。<br/></td>
<td>0x80880903//v2。0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>CAPICOM 的資源已用盡。<br/></td>
<td>0x80880904//v2。0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>發生內部錯誤。 <br/> 請洽詢 Microsoft 技術支援人員以取得協助。<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>發生未知的錯誤。 <br/> 盡可能收集最多的資訊，並洽詢您的廠商。<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




