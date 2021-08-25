---
description: 設定或抓取用於簽署、封套和加密作業的演算法。 這是預設屬性。
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4d9860e9a3f04f2f17ebcda08a4ec2610c5af3cbb5fbb5e7afa98227264992b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880148"
---
# <a name="algorithmname-property"></a>Algorithm.Name 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Name** 屬性會設定或抓取用於簽署、封套和加密作業的演算法。 這是預設屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>屬性值

[**CAPICOM \_ 加密 \_ 演算法**](capicom-encryption-algorithm.md)列舉的值，可指定要使用的演算法。 下表顯示可能的值。



| 值                                                                                                                                                                                                                       | 意義                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**CAPICOM \_ 加密 \_ 演算法 \_ RC2**</dt> </dl>    | 使用 RC2 加密。<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**CAPICOM \_ 加密 \_ 演算法 \_ RC4**</dt> </dl>    | 使用 RC4 加密。<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**CAPICOM \_ 加密 \_ 演算法 \_ DES**</dt> </dl>    | 使用 DES 加密。<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**CAPICOM \_ 加密 \_ 演算法 \_ 3des**</dt> </dl> | 使用三重 DES 加密。<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**CAPICOM \_ 加密 \_ 演算法 \_ AES**</dt> </dl>    | 使用 AES 演算法。<br/>     |



 

## <a name="remarks"></a>備註

當這個屬性的值是直接或間接重設時，會重設物件的整個狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
