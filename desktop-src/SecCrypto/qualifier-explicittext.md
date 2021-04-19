---
description: 抓取使用者通知的內容。
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: ExplicitText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989568"
---
# <a name="qualifierexplicittext-property"></a>ExplicitText 屬性

\[**ExplicitText** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

**ExplicitText** 屬性會抓取使用者通知的內容。 這個屬性可以是空的。

## <a name="syntax"></a>Syntax


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>屬性值

使用者通知的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
