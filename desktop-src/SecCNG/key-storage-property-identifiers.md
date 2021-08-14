---
description: 用來識別索引鍵存放區屬性。
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: '索引鍵儲存體屬性識別碼 (Ncrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907610"
---
# <a name="key-storage-property-identifiers"></a>索引鍵儲存體屬性識別碼

以下是用來識別索引鍵儲存屬性的值。

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT \_ 演算法 \_ 群組 \_ 屬性**
</dt> <dd> <dl> <dt>

L "演算法群組"
</dt> <dt>



以 null 終止的 Unicode 字串，其中包含物件之演算法群組的名稱。 這個屬性只適用于索引鍵。 以下是 Microsoft 金鑰儲存提供者所傳回的識別碼。



| 識別碼                                     | 值              | 描述                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **NCRYPT \_ RSA \_ 演算法 \_ 群組**<br/>   | 與眾不同<br/>   | RSA 演算法群組。<br/>                           |
| **NCRYPT \_ DH \_ 演算法 \_ 群組**<br/>    | DH<br/>    | Diffie-Hellman 演算法群組。<br/>                |
| **NCRYPT \_ DSA \_ 演算法 \_ 群組**<br/>   | DSA<br/>   | DSA 演算法群組。<br/>                           |
| **NCRYPT \_ ECDSA \_ 演算法 \_ 群組**<br/> | ECDSA<br/> | 橢圓曲線 DSA 演算法群組。<br/>            |
| **NCRYPT \_ ECDH \_ 演算法 \_ 群組**<br/>  | ECDH<br/>  | 橢圓曲線 Diffie-Hellman 演算法群組。<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT \_ 演算法 \_ 屬性**
</dt> <dd> <dl> <dt>

L "演算法名稱"
</dt> <dt>



以 null 終止的 Unicode 字串，其中包含物件之演算法的名稱。 這可以是其中一個預先定義的 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 或另一個已註冊的演算法識別碼。 這個屬性只適用于索引鍵。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT \_ 相關聯的 \_ ECDH \_ 金鑰**
</dt> <dd> <dl> <dt>

L "SmartCardAssociatedECDHKey"
</dt> <dt>



**LPWSTR** 值，這個值會指出橢圓曲線的容器名稱 Diffie-Hellman (ECDH) 金鑰，以在針對橢圓曲線數位簽章演算法 (ECDSA) 索引鍵的指定控制碼登入時使用。 如果卡片上沒有任何 ECDH 金鑰，則 [*金鑰儲存提供者*](/windows/desktop/SecGloss/k-gly) (KSP) 會傳回 **「 \_ 未 \_ 找到上限**」。 這個屬性會套用至 ECDSA 金鑰以用於以智慧卡登入。 Microsoft 智慧卡金鑰儲存提供者（而不是 Microsoft 軟體金鑰儲存提供者）支援此屬性。

**Windows Server 2008 和 Windows Vista：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT \_ 區塊 \_ 長度 \_ 屬性**
</dt> <dd> <dl> <dt>

L "區塊長度"
</dt> <dt>



**DWORD** ，其中包含加密區塊的長度（以位元組為單位）。 這個屬性只適用于支援加密的金鑰。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT \_ 憑證 \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardKeyCertificate"
</dt> <dt>



包含與金鑰相關聯之 x.509 憑證的 [*BLOB*](/windows/desktop/SecGloss/b-gly) 。

**Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 包含 [*智慧卡*](/windows/desktop/SecGloss/s-gly)金鑰 [*憑證*](/windows/desktop/SecGloss/c-gly)的 [*BLOB*](/windows/desktop/SecGloss/b-gly) 。 Microsoft 軟體金鑰儲存體提供者不支援此屬性。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT \_ DH \_ 參數 \_ 屬性**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



指定要搭配 Diffie-Hellman 索引鍵使用的參數。 此資料類型是 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) 結構的指標。 這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT \_ 匯出 \_ 原則 \_ 屬性**
</dt> <dd> <dl> <dt>

L 「匯出原則」
</dt> <dt>



**DWORD** ，其中包含一組旗標，可指定保存金鑰的匯出原則。 這個屬性只適用于索引鍵。 這可以包含零個或一個或多個下列值的組合。



| 識別碼                                    | 值      | 描述                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ 允許 \_ 匯出 \_ 旗標**               | 0x00000001 | 您可以匯出私密金鑰。                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ 允許 \_ 純文字 \_ 匯出 \_ 旗標**    | 0x00000002 | 私密金鑰可以用純文字格式匯出。                                                                                                                                                                                                                                                               |
| **NCRYPT \_ 允許 \_ 封存 \_ 旗標**            | 0x00000004 | 私密金鑰可以匯出一次，以供封存之用。 此旗標只適用于設定它的原始金鑰控制碼。 此原則只能套用至原始金鑰控制碼。 關閉金鑰控制碼之後，就無法再匯出金鑰以供封存之用。                   |
| **NCRYPT \_ 允許 \_ 純文字封存 \_ \_ 旗標** | 0x00000008 | 私密金鑰可以用純文字格式匯出一次，以供封存之用。 此旗標只適用于設定它的原始金鑰控制碼。 此原則只能套用至原始金鑰控制碼。 關閉金鑰控制碼之後，就無法再匯出金鑰以供封存之用。 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT \_ IMPL \_ TYPE \_ 屬性**
</dt> <dd> <dl> <dt>

L "Impl Type"
</dt> <dt>



包含一組旗標的 **DWORD** ，這些旗標會定義提供者的執行詳細資料。 這個屬性只適用于金鑰儲存提供者。 這可以包含零個或一個或多個下列值的組合。



| 識別碼                            | 值      | 描述                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **NCRYPT \_ IMPL \_ 硬體 \_ 旗標**      | 0x00000001 | 提供者是以硬體為基礎。                           |
| **NCRYPT \_ IMPL \_ SOFTWARE \_ 旗標**      | 0x00000002 | 提供者是以軟體為基礎。                           |
| **NCRYPT \_ IMPL \_ 可移動 \_ 旗旗標**     | 0x00000008 | 提供者是可移動的。                                |
| **NCRYPT \_ IMPL \_ 硬體 \_ RNG \_ 旗標** | 0x00000010 | 提供者是以硬體為基礎的亂數字產生器。 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT 索引 \_ 鍵 \_ 類型 \_ 屬性**
</dt> <dd> <dl> <dt>

L "金鑰類型"
</dt> <dt>



**DWORD** ，包含定義索引鍵類型的一組旗標。 這個屬性只適用于索引鍵。 這可以包含零或下列值。



| 識別碼                     | 值      | 描述                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ 機 \_ 碼 \_ 旗標** | 0x00000001 | 金鑰適用于本機電腦。 如果不存在此旗標，則會將金鑰套用至目前的使用者。 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT \_ 金鑰 \_ 使用方式 \_ 屬性**
</dt> <dd> <dl> <dt>

L [金鑰使用方法]
</dt> <dt>



包含一組旗標的 **DWORD** ，這些旗標會定義索引鍵的使用詳細資料。 這個屬性只適用于索引鍵。 這可以包含零個或一個或多個下列值的組合。



| 識別碼                              | 值      | 描述                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ 允許 \_ 解密 \_ 旗標**        | 0x00000001 | 金鑰可以用來解密。                  |
| **NCRYPT \_ 允許 \_ 簽署 \_ 旗標**        | 0x00000002 | 金鑰可以用來簽署。                     |
| **NCRYPT \_ 允許 \_ 金鑰 \_ 合約 \_ 旗標** | 0x00000004 | 金鑰可用於秘密協定加密。 |
| **NCRYPT \_ 允許 \_ 所有 \_ 使用方式**          | 0x00ffffff | 金鑰可用於任何用途。                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT \_ 上次 \_ 修改的 \_ 屬性**
</dt> <dd> <dl> <dt>

L 「已修改」
</dt> <dt>



指出金鑰上次修改的時間。 此資料類型是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構的指標。 這個屬性只適用于保存的金鑰。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT \_ LENGTH \_ 屬性**
</dt> <dd> <dl> <dt>

L "Length"
</dt> <dt>



**DWORD** ，其中包含索引鍵的長度（以位為單位）。 這個屬性只適用于索引鍵。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT \_ 長度 \_ 屬性**
</dt> <dd> <dl> <dt>

L "長度"
</dt> <dt>



指出金鑰所支援的金鑰大小。 此資料類型是 [**NCRYPT \_ 支援 \_ 長度**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) 結構的指標，其中包含這項資訊。 這個屬性只適用于索引鍵。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT \_ MAX \_ NAME \_ LENGTH \_ 屬性**
</dt> <dd> <dl> <dt>

L "最大名稱長度"
</dt> <dt>



**DWORD** ，其中包含持續性索引鍵名稱的最大長度（以字元為單位）。 這個屬性只適用于提供者。

這個屬性主要是供金鑰儲存提供者使用，這些提供者會將金鑰儲存在具有有限可用記憶體數量（例如智慧卡）的裝置上。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT \_ NAME \_ 屬性**
</dt> <dd> <dl> <dt>

L "Name"
</dt> <dt>



以 null 終止的 Unicode 字串指標，其中包含物件的名稱。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT \_ PIN \_ 提示 \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardPinPrompt"
</dt> <dt>



不支援這個值。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT \_ 釘選 \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardPin"
</dt> <dt>



以 null 終止的 Unicode 字串指標，其中包含 PIN。 PIN 可用於智慧卡金鑰或儲存在以軟體為基礎的 KSP 中的密碼保護金鑰密碼。 只能設定這個屬性。 Microsoft Ksp 會快取此值，因此每個進程只會提示使用者一次。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT \_ 提供者 \_ 控制碼 \_ 屬性**
</dt> <dd> <dl> <dt>

L 「提供者控制碼」
</dt> <dt>



**NCRYPT \_ >prov \_ 控制碼**，其中包含 CNG 金鑰儲存提供者的控制碼。 當您完成使用控制碼時，您必須呼叫 [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) 來釋放它。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT \_ 讀取器 \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardReader"
</dt> <dt>



以 null 終止的 Unicode 字串指標，其中包含智慧卡讀取器的名稱。 只能設定這個屬性。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT \_ 根 \_ CERTSTORE \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartcardRootCertStore"
</dt> <dt>



代表智慧卡根憑證存放區的 **HCERTSTORE** 。


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_捨棄 \_ PIN \_ 識別碼**
</dt> <dd> <dl> <dt>

L "SmartCardPinId"
</dt> <dt>



與 [*智慧卡*](/windows/desktop/SecGloss/s-gly)上指定之 [*密碼編譯金鑰*](/windows/desktop/SecGloss/c-gly)相關聯的 **PIN \_ 識別碼** 值指標。 這是一個唯讀屬性。 **PIN \_ 識別碼** 資料類型定義于 cardmod.h 中。

**Windows Server 2008 和 Windows Vista：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT \_ 捨棄 \_ PIN \_ 資訊**
</dt> <dd> <dl> <dt>

L "SmartCardPinInfo"
</dt> <dt>



[**Pin 碼 \_ 資訊**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info)結構的指標，該 pin 與智慧卡上指定的密碼編譯金鑰相關聯。 呼叫端會提供金鑰控制碼。 這個屬性是唯讀屬性。 **PIN \_ 資訊** 結構定義于 cardmod.h 中。

**Windows Server 2008 和 Windows Vista：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT \_ 安全 \_ PIN \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardSecurePin"
</dt> <dt>



以 null 終止的 Unicode 字串指標，其中包含智慧卡會話 PIN。 只能設定這個屬性。

**Windows Vista：** 不支援這個屬性。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT \_ 安全性 \_ 描述 \_ 屬性**
</dt> <dd> <dl> <dt>

L "Security 描述"
</dt> <dt>



[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構的指標，其中包含索引鍵的存取控制資訊。 這個屬性只適用于持續性索引鍵。 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)或 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)函數的 *dwFlags* 參數會識別要取得或設定的安全描述項部分。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT \_ SECURITY \_ 描述 \_ SUPPORT \_ 屬性**
</dt> <dd> <dl> <dt>

L "Security 描述 Support"
</dt> <dt>



指出提供者是否支援金鑰的安全描述項。 如果提供者支援索引鍵的安全描述項，則這個屬性是包含1的 **DWORD** 。 如果此屬性包含任何其他值，或如果 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式傳回 **\_ 不 \_ 支援的上限**，則提供者不支援金鑰的安全描述項。 這個屬性只適用于提供者。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT \_ 智慧卡 \_ GUID \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardGuid"
</dt> <dt>



包含智慧卡識別碼的 BLOB。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT \_ UI \_ 原則 \_ 屬性**
</dt> <dd> <dl> <dt>

L "UI 原則"
</dt> <dt>



如果搭配 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) 或 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式使用，這是 [**NCRYPT \_ UI \_ 原則**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) 結構的指標，其中包含索引鍵的強式金鑰使用者介面原則。 這個屬性只適用于持續性索引鍵。 只有在產生金鑰時，才能設定這個屬性。 針對此索引鍵呼叫 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) 函式之後，這個屬性會變成隻讀。

金鑰儲存提供者可以透過 [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) 回呼函式接收此參數。 參數值是 NCRYPT \_ UI \_ 原則 \_ BLOB 結構，其中包含相同的資訊。 同樣地，當應用程式透過 NCryptSetPropertyFn 對提供者提出要求以傳回此屬性時，提供者應該會傳回 NCRYPT \_ UI \_ 原則 \_ BLOB 結構。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT \_ 唯一 \_ 名稱 \_ 屬性**
</dt> <dd> <dl> <dt>

L 「唯一名稱」
</dt> <dt>



以 null 終止的 Unicode 字串指標，其中包含物件的唯一名稱。 這是存取金鑰時可使用的替代名稱。 當您認為原本傳遞給 [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) 的索引鍵名稱不是唯一的，而無法可靠地識別保存的金鑰時，就會使用這個屬性。 Microsoft 金鑰儲存提供者將會以這個屬性傳回金鑰的檔案名。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ 使用 \_ 上下文 \_ 屬性**
</dt> <dd> <dl> <dt>

L 「使用內容」
</dt> <dt>



以 null 結束的 Unicode 字串指標，描述作業的內容。 這個屬性不是持續性的，而且可以在提供者或索引鍵上進行設定。 索引鍵無法存取提供者的 **NCRYPT \_ USE \_ CONTEXT \_ property** 屬性，因為該屬性只是針對它所設定的控制碼所特有。

在提供者的內容中使用此屬性的範例，就是在呼叫 ([**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 時需要提示使用者的金鑰儲存提供者，例如「在讀取器中插入您的智慧卡」。) 。 由於在 **NCryptOpenKey** 傳回之前無法使用金鑰控制碼，因此應用程式應該在呼叫 **NCryptOpenKey** 之前，在提供者控制碼上設定此屬性。

在金鑰控制碼的內容中使用此屬性的範例是金鑰儲存提供者，需要在使用 (金鑰的作業期間提示使用者，例如「此應用程式必須使用此金鑰來簽署檔」。) 。 然後，提供者可以將此內容資訊轉送至作業期間所顯示之任何使用者介面中的使用者。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT \_ USE \_ COUNT \_ ENABLED \_ 屬性**
</dt> <dd> <dl> <dt>

L 「啟用的使用計數」
</dt> <dt>



指出提供者是否支援索引鍵的使用計數。 如果提供者支援索引鍵的使用計數，則這個屬性是包含1的 **DWORD** 。 如果此屬性包含任何其他值，或如果 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式傳回 **\_ 不 \_ 支援的上限**，則提供者不支援索引鍵的使用計數。 這個屬性只適用于提供者。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT \_ USE \_ COUNT \_ 屬性**
</dt> <dd> <dl> <dt>

L 「使用計數」
</dt> <dt>



[**ULARGE \_ 整數**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1)變數，其中包含指定的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)已執行的作業數目。 這個屬性是選擇性的，並非所有提供者都支援。 在索引鍵上支援此屬性的提供者，也應該支援提供者控制碼上的 **NCRYPT \_ USE \_ COUNT \_ ENABLED \_ 屬性** 屬性。 Microsoft 金鑰儲存提供者不支援此屬性。 這個屬性只適用于持續性索引鍵。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT \_ 使用者 \_ CERTSTORE \_ 屬性**
</dt> <dd> <dl> <dt>

L "SmartCardUserCertStore"
</dt> <dt>



**HCERTSTORE** ，代表智慧卡使用者憑證存放區。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT \_ VERSION \_ 屬性**
</dt> <dd> <dl> <dt>

L "Version"
</dt> <dt>



**DWORD** ，其中包含提供者的軟體版本。 最大的單字包含主要版本，而低字組則包含次要版本。 例如，0x00030033 = 3.51。 這個屬性只適用于提供者。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT \_ 視窗 \_ 控制碼 \_ 屬性**
</dt> <dd> <dl> <dt>

L "HWND 控制碼"
</dt> <dt>



視窗控制碼的指標 (**HWND**) 要做為顯示之任何使用者介面的父系。

由於使用父系的 **Null** 視窗控制碼來顯示使用者介面時可能會發生不必要的行為，因此強烈建議您不要在設定這個屬性的情況下，將金鑰儲存提供者顯示為使用者介面。


</dt> </dl> </dd> </dl>

以下是用來定義屬性資料限制的值。



| 常數/值                                                                                                                                                                                                                                                 | Description                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_最大 \_ 屬性 \_ 資料**</dt> <dt>0x100000</dt> </dl> | 指定屬性值的大小上限（以位元組為單位）。<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_最大 \_ 屬性 \_ 名稱**</dt> <dt>64</dt> </dl>       | 指定屬性名稱的大小上限（以字元為單位）。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Ncrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

