---
description: 定義要用於加密和解密的演算法。
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: 'CAPICOM_ENCRYPTION_ALGORITHM 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977520"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>CAPICOM \_ 加密 \_ 演算法列舉

**CAPICOM \_ 加密 \_ 演算法** 列舉型別會定義要用於加密和解密的演算法。

## <a name="members"></a>成員



| member                                   | 描述                                                                                                                                                                                              | 值     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **CAPICOM \_ 加密 \_ 演算法 \_ RC2**  | 使用 RSA RC2 加密。<br/>                                                                                                                                                                       | 0         |
| **CAPICOM \_ 加密 \_ 演算法 \_ RC4**  | 使用 RSA RC4 加密。<br/>                                                                                                                                                                       | 1         |
| **CAPICOM \_ 加密 \_ 演算法 \_ DES**  | 使用 DES 加密。<br/>                                                                                                                                                                           | 2         |
| **CAPICOM \_ 加密 \_ 演算法 \_ 3des** | 使用三重 DES 加密。<br/>                                                                                                                                                                    | 3         |
| **CAPICOM \_ 加密 \_ 演算法 \_ AES**  | 使用 [*進階加密標準*](../secgloss/a-gly.md) (AES) 演算法。 此值只對 [**a**](encrypteddata.md) 物件有效。<br/> | 4//v 2。0 |



## <a name="remarks"></a>備註

[**Algorithm.Name**](algorithm-name.md)屬性使用了 **CAPICOM \_ 加密 \_ 演算法** 列舉型別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
