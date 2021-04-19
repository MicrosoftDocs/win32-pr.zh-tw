---
description: 根據指定的索引來抓取限定詞。
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: 限定詞。 Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981386"
---
# <a name="qualifiersitem-property"></a>限定詞。 Item 屬性

\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

**Item** 屬性會根據指定的索引來抓取限定詞。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

代表集合之索引限定詞的辨識 [**符號**](qualifier.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**限定詞**](qualifiers.md)
</dt> </dl>

 

 
