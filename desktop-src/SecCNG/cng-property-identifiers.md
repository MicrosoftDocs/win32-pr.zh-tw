---
description: 搭配 BCryptGetProperty 和 BCryptSetProperty 函數使用，以識別屬性。
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: '加密基本屬性識別碼 (Bcrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5452c6a55388998a08577cb19ef2fba6905faddbdf28f5f8051b7bc8d9d1c375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908219"
---
# <a name="cryptography-primitive-property-identifiers"></a>加密基本屬性識別碼

下列值會搭配 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 和 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 函數使用，以識別屬性。

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT \_ 演算法 \_ 名稱**
</dt> <dd> <dl> <dt>

L "AlgorithmName"
</dt> <dt>



以 null 終止的 Unicode 字串，其中包含演算法的名稱。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT \_ AUTH \_ TAG \_ LENGTH**
</dt> <dd> <dl> <dt>

L "AuthTagLength"
</dt> <dt>



演算法所支援的驗證標記長度。 這個屬性是 [**BCRYPT \_ AUTH \_ TAG \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) 結構。 這個屬性只適用于演算法。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT \_ 區塊 \_ 長度**
</dt> <dd> <dl> <dt>

L "BlockLength"
</dt> <dt>



演算法之加密區塊的大小（以位元組為單位）。 這個屬性只適用于區塊加密演算法。 此資料類型為 **DWORD**。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT \_ 區塊 \_ 大小 \_ 清單**
</dt> <dd> <dl> <dt>

L "BlockSizeList"
</dt> <dt>



加密演算法所支援的區塊長度清單。 此資料類型是 **dword** 的陣列。 陣列中的元素數目可以藉由將單一 **DWORD** 的大小所抓取的位元組數目進行分割來決定。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT \_ 連結 \_ 模式**
</dt> <dd> <dl> <dt>

L "ChainingMode"
</dt> <dt>



以 null 結束的 Unicode 字串指標，表示加密演算法的連結模式。 這個屬性可以在演算法控制碼或索引鍵控制碼上設定為下列其中一個值。



| 識別碼                   | 值                         | 描述                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BCRYPT \_ 鏈 \_ 模式 \_ CBC** | L "ChainingModeCBC"<br/> | 將演算法的連結模式設定為 [*加密區塊鏈*](/windows/desktop/SecGloss/c-gly)。<br/>            |
| **BCRYPT \_ 鏈 \_ 模式 \_ CCM** | L "ChainingModeCCM"<br/> | 將演算法的連結模式設定為使用 CBC (CCM) 的 MAC 模式來進行計數器。**Windows Vista：** 從 Windows Vista SP1 開始支援此值。<br/> <br/> |
| **BCRYPT \_ 鏈 \_ 模式 \_ CFB** | L "ChainingModeCFB"<br/> | 將演算法的連結模式設定為 [*加密意見*](/windows/desktop/SecGloss/c-gly)反應。<br/>                              |
| **BCRYPT \_ 鏈 \_ 模式 \_ ECB** | L "ChainingModeECB"<br/> | 將演算法的連結模式設定為 [*電子 codebook*](/windows/desktop/SecGloss/e-gly)。<br/>                  |
| **BCRYPT \_ 鏈 \_ 模式 \_ GCM** | L "ChainingModeGCM"<br/> | 將演算法的連結模式設定為 Galois/counter 模式 (GCM) 。**Windows Vista：** 從 Windows Vista SP1 開始支援此值。<br/> <br/>       |
| **BCRYPT \_ 鏈 \_ 模式 \_ NA**  | L "ChainingModeN/A"<br/> | 演算法不支援連結。<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT \_ DH \_ 參數**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



指定要搭配 Diffie-Hellman 索引鍵使用的參數。 此資料類型是 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) 結構的指標。 這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT \_ DSA \_ 參數**
</dt> <dd> <dl> <dt>

L "DSAParameters"
</dt> <dt>



指定要與 DSA 金鑰搭配使用的參數。 這個屬性是 [**BCRYPT \_ dsa \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) 或 [**BCRYPT \_ dsa \_ 參數 \_ 標頭 \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) 結構。 這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。

**Windows 8：** 從 Windows 8 開始，此屬性可以是 [**BCRYPT \_ DSA \_ 參數 \_ 標頭 \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2)結構。 如果金鑰大小超過1024個位且小於或等於3072位，請使用此結構。 如果金鑰大小大於或等於512但小於或等於1024位，請使用 [**BCRYPT \_ DSA \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) 結構。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT \_ 有效 \_ 金鑰 \_ 長度**
</dt> <dd> <dl> <dt>

L "EffectiveKeyLength"
</dt> <dt>



RC2 金鑰有效長度的大小（以位為單位）。 此資料類型為 **DWORD**。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT \_ 雜湊 \_ 區塊 \_ 長度**
</dt> <dd> <dl> <dt>

L "HashBlockLength"
</dt> <dt>



雜湊區塊的大小（以位元組為單位）。 這個屬性只適用于雜湊演算法。 此資料類型為 **DWORD**。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT \_ 雜湊 \_ 長度**
</dt> <dd> <dl> <dt>

L "HashDigestLength"
</dt> <dt>



雜湊提供者雜湊值的大小（以位元組為單位）。 此資料類型為 **DWORD**。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT \_ 雜湊 \_ OID \_ 清單**
</dt> <dd> <dl> <dt>

L "HashOIDList"
</dt> <dt>



以 [*DER*](/windows/desktop/SecGloss/d-gly)編碼的雜湊 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) 清單 (oid) 。 這個屬性是 [**BCRYPT 的 \_ OID \_ 清單**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) 結構。 只能讀取這個屬性。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT \_ 初始化 \_ 向量**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



包含金鑰的 [*初始化向量*](/windows/desktop/SecGloss/i-gly) (IV) 。 這個屬性只適用于索引鍵。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT \_ 金鑰 \_ 長度**
</dt> <dd> <dl> <dt>

L "KeyLength"
</dt> <dt>



對稱金鑰提供者之金鑰值的大小（以位為單位）。 此資料類型為 **DWORD**。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT \_ 金鑰 \_ 長度**
</dt> <dd> <dl> <dt>

L "KeyLengths"
</dt> <dt>



演算法所支援的金鑰長度。 這個屬性是 BCRYPT 的索引 [**\_ 鍵 \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) 結構。 這個屬性只適用于演算法。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT 索引 \_ 鍵 \_ 物件 \_ 長度**
</dt> <dd> <dl> <dt>

L "KeyObjectLength"
</dt> <dt>



不會使用此屬性。 **BCRYPT \_ 物件 \_ 長度** 屬性是用來取得此資訊。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT \_ 金鑰 \_ 強度**
</dt> <dd> <dl> <dt>

L "KeyStrength"
</dt> <dt>



機碼中的位數。 此資料類型為 **DWORD**。 這個屬性只適用于索引鍵。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT \_ 訊息 \_ 區塊 \_ 長度**
</dt> <dd> <dl> <dt>

L "MessageBlockLength"
</dt> <dt>



這可以在已設定 CFB 連結模式的任何索引鍵控制碼上進行設定。 根據預設，這個屬性會設定為1，以進行8位 CFB。 將它設定為區塊大小（以位元組為單位）會導致使用完整區塊 CFB。 針對 XTS 索引鍵，它是用來設定 XTS 資料單位的大小（以位元組為單位）， (通常是512或 4096) 。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ 多 \_ 物件 \_ 長度**
</dt> <dd> <dl> <dt>

L "MultiObjectLength"
</dt> <dt>



這個屬性會傳回 [**BCRYPT \_ 多 \_ 物件 \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)，其中包含計算物件緩衝區大小所需的資訊。 只有支援 [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) 函式的作業系統版本才支援此屬性。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT \_ 物件 \_ 長度**
</dt> <dd> <dl> <dt>

L "ObjectLength"
</dt> <dt>



提供者之子物件的大小（以位元組為單位）。 此資料類型為 **DWORD**。 目前，雜湊和對稱式加密演算法提供者會使用呼叫端配置的緩衝區來儲存其子服務。 例如，雜湊提供者要求您針對以 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數取得的雜湊物件配置記憶體。 這個屬性會提供提供者物件的緩衝區大小，讓您可以為提供者所建立的物件配置記憶體。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT \_ 填補 \_ 配置**
</dt> <dd> <dl> <dt>

L "PaddingSchemes"
</dt> <dt>



代表 RSA 演算法提供者的填補配置。 此資料類型為 **DWORD**。 這可以是下列其中一個值。



| 識別碼                             | 值      | 描述                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **BCRYPT \_ 支援的 \_ PAD \_ 路由器**     | 0x00000001 | 提供者支援由路由器新增的填補。         |
| **BCRYPT \_ 支援的 \_ PAD \_ PKCS1 \_ ENC** | 0x00000002 | 提供者支援 PKCS1 加密填補配置。 |
| **BCRYPT \_ 支援的 \_ PAD \_ PKCS1 \_ SIG** | 0x00000004 | 提供者支援 PKCS1 簽章填補配置。  |
| **BCRYPT \_ 支援的 \_ PAD \_ OAEP**       | 0x00000008 | 提供者支援 OAEP 填補配置。             |
| **BCRYPT \_ 支援的 \_ PAD \_ PSS**        | 0x00000010 | 提供者支援 PSS 填補配置。              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT \_ 提供者 \_ 控制碼**
</dt> <dd> <dl> <dt>

L "ProviderHandle"
</dt> <dt>



CNG 提供者的控制碼，它會建立在 *hObject* 參數中傳遞的物件。 此資料類型是 **BCRYPT \_ ALG \_ 控制碼**。 只能抓取此屬性;無法設定。


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT \_ 簽名 \_ 長度**
</dt> <dd> <dl> <dt>

L "SignatureLength"
</dt> <dt>



金鑰簽章長度的大小（以位元組為單位）。 此資料類型為 **DWORD**。 這個屬性只適用于索引鍵。 只能抓取此屬性;無法設定。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Bcrypt。h</dt> </dl> |



 

