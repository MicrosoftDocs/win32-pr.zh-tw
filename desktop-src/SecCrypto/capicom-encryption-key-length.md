---
description: 定義要用於加密的金鑰長度。
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: 'CAPICOM_ENCRYPTION_KEY_LENGTH 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2957bd644fdf405fec7e82a487bf83af2cbae35ae305f10b9b168628a30b0749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772473"
---
# <a name="capicom_encryption_key_length-enumeration"></a>CAPICOM \_ 加密 \_ 金鑰 \_ 長度列舉

**CAPICOM \_ 加密 \_ 金鑰 \_ 長度** 列舉類型會定義要在加密中使用的 [*金鑰長度*](../secgloss/k-gly.md)。

## <a name="members"></a>成員



| member                                          | 描述                                                                               | 值     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 上限**   | 使用指定的加密演算法所提供的最大金鑰長度。<br/> | 0         |
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 40 \_ 位**  | 使用40位的索引鍵。<br/>                                                              | 1         |
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 56 \_ 位**  | 使用56位金鑰（如果有的話）。<br/>                                                 | 2         |
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 128 \_ 位** | 使用128位金鑰（如果有的話）。<br/>                                                | 3         |
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 192 \_ 位** | 使用192位的索引鍵。 此金鑰長度僅適用于 AES。<br/>                  | 4//v 2。0 |
| **CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 256 \_ 位** | 使用256位的索引鍵。 此金鑰長度僅適用于 AES。<br/>                  | 5//v 2。0 |



## <a name="remarks"></a>備註

[**KeyLength**](algorithm-keylength.md)屬性使用了 **CAPICOM \_ 加密 \_ 金鑰 \_ 長度** 列舉類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
