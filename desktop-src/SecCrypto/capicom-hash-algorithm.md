---
description: CAPICOM \_ 雜湊 \_ 演算法列舉會定義雜湊演算法。
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: 'CAPICOM_HASH_ALGORITHM 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989796"
---
# <a name="capicom_hash_algorithm-enumeration"></a>CAPICOM \_ 雜湊 \_ 演算法列舉

**CAPICOM \_ 雜湊 \_ 演算法** 列舉會定義雜湊演算法。

## <a name="members"></a>成員



| member                                 | 描述                                                                                                                                                                 | 值 |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1**     |  (SHA) 的 [*安全雜湊演算法*](../secgloss/s-gly.md)，會產生160位訊息摘要。<br/> | 0     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ MD2**      | MD2 雜湊演算法。<br/>                                                                                                                                           | 1     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ MD4**      | MD4 雜湊演算法。<br/>                                                                                                                                           | 2     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ MD5**      | MD5 雜湊演算法。<br/>                                                                                                                                           | 3     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 256** | 256 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/>                                                                 | 4     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 384** | 384 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/>                                                                 | 5     |
| **CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 512** | 512 SHA-1 雜湊演算法。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。<br/>                                                                 | 6     |



## <a name="remarks"></a>備註

[**HashedData 演算法**](hasheddata-algorithm.md)屬性會使用 **CAPICOM \_ 雜湊 \_ 演算法** 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
