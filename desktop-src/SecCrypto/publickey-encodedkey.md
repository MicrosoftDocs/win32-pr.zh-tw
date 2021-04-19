---
description: 捕獲公開金鑰的值。
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: PublicKey. EncodedKey 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979574"
---
# <a name="publickeyencodedkey-property"></a>PublicKey. EncodedKey 屬性

\[**EncodedKey** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]

**EncodedKey** 屬性會捕獲公開金鑰的值。

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>屬性值

提供存取公開金鑰值的 [**EncodedData**](encodeddata.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
