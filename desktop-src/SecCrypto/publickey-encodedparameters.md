---
description: 捕獲公開金鑰演算法的參數。
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: PublicKey. EncodedParameters 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984110"
---
# <a name="publickeyencodedparameters-property"></a>PublicKey. EncodedParameters 屬性

\[**EncodedParameters** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]

**EncodedParameters** 屬性會捕獲公開金鑰演算法的參數。

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>屬性值

[**EncodedData**](encodeddata.md)物件，可存取公開金鑰演算法的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
