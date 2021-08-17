---
description: 設定或抓取索引鍵的長度。
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: KeyLength 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c5ce8f906628df06ef506a0f57c33db4bed7c5980bb78ab2e0094d0443b5646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773662"
---
# <a name="algorithmkeylength-property"></a>KeyLength 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**KeyLength** 屬性會設定或抓取索引鍵的長度。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>屬性值

指定金鑰長度之 [**CAPICOM \_ 加密 \_ 金鑰 \_ 長度**](capicom-encryption-key-length.md) 列舉的值。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                        | 意義                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 上限**</dt> </dl>     | 使用指定的加密演算法所提供的最大金鑰長度。<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 40 \_ 位**</dt> </dl>    | 使用40位的金鑰。<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 56 \_ 位**</dt> </dl>    | 使用56位金鑰（如果有的話）。<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 128 \_ 位**</dt> </dl> | 使用128位金鑰（如果有的話）。<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 192 \_ 位**</dt> </dl> | 使用192位的金鑰。 此金鑰長度僅適用于 AES。<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 256 \_ 位**</dt> </dl> | 使用256位的金鑰。 此金鑰長度僅適用于 AES。<br/>                  |



 

## <a name="remarks"></a>備註

使用 DES 和3DES 加密演算法時，金鑰長度是標準的，而且會忽略 **KeyLength** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**演算法**](algorithm.md)
</dt> </dl>

 

 
