---
description: 演算法屬性會抓取識別公開金鑰所使用之演算法的 OID 物件。 這是預設屬性。
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey 演算法屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978758"
---
# <a name="publickeyalgorithm-property"></a>PublicKey 演算法屬性

\[[ **演算法]** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]

**演算法** 屬性會抓取識別公開金鑰所使用之演算法的 [**OID**](oid.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>屬性值

識別公開金鑰所使用之演算法的 [**OID**](oid.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
