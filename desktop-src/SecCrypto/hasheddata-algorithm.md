---
description: 設定或抓取所使用的雜湊演算法類型。
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData 演算法屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993980"
---
# <a name="hasheddataalgorithm-property"></a>HashedData 演算法屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]

**演算法** 屬性會設定或抓取所使用的雜湊演算法類型。

## <a name="syntax"></a>Syntax


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>屬性值

定義雜湊演算法之 [**CAPICOM \_ 雜湊 \_ 演算法**](capicom-hash-algorithm.md) 列舉的值。 預設值為 [CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1]。 下表顯示可能的值。



| 值                                                                                                                                                                                                               | 意義                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1**</dt> </dl>           | SHA1 雜湊演算法。<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD2**</dt> </dl>              | MD2 雜湊演算法。<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD4**</dt> </dl>              | MD4 雜湊演算法。<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD5**</dt> </dl>              | MD5 雜湊演算法。<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 256**</dt> </dl> | 256 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 384**</dt> </dl> | 384 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 512**</dt> </dl> | 512 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
