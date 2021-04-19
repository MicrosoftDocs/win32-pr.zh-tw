---
description: 抓取公開金鑰的長度（以位為單位）。
ms.assetid: 02cb631a-5a5d-4d16-bdad-55263a0a53b3
title: PublicKey. Length 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Length
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9429c2ab72845324ab024005cac2da2bfaf7eec1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990759"
---
# <a name="publickeylength-property"></a>PublicKey. Length 屬性

\[[ **長度** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]

**Length** 屬性會取出公開金鑰的長度（以位為單位）。

## <a name="syntax"></a>Syntax


```VB
PublicKey.Length As Long
```



## <a name="property-value"></a>屬性值

公開金鑰的長度（以位為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
