---
description: 指出使用的編碼類型。
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: 'CAPICOM_ENCODING_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999486"
---
# <a name="capicom_encoding_type-enumeration"></a>CAPICOM \_ 編碼 \_ 類型列舉

**CAPICOM \_ 編碼 \_ 類型** 列舉類型指出使用的編碼類型。

## <a name="members"></a>成員



| member                      | 描述                                                                                                                                                                                 | 值      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ 編碼 \_ 任何**    | 資料會儲存為 base64 編碼字串或純二進位序列。 此編碼類型只用于具有未知編碼類型的輸入資料。 在 CAPICOM 2.0 中引進。<br/> | 0xffffffff |
| **CAPICOM \_ 編碼 \_ BASE64** | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                        | 0          |
| **CAPICOM \_ 編碼 \_ 二進位** | 資料會儲存為純二進位序列。<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>備註

下列 CAPICOM 方法和屬性會使用這個列舉類型：

-   [**Certificate. Export**](certificate-export.md) 方法
-   [**EncodedData。 Value**](encodeddata-value.md) 屬性
-   [**A**](encrypteddata-encrypt.md) 方法
-   [**EnvelopedData**](envelopeddata-encrypt.md) 方法
-   [**ExtendedProperty。 Value**](extendedproperty-value.md) 屬性
-   [**SignedData. Sign**](signeddata-sign.md) 方法
-   [**SignedData. CoSign**](signeddata-cosign.md) 方法
-   [**Store. Export**](store-export.md) 方法
-   [**GetRandom**](utilities-getrandom.md) 方法

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




