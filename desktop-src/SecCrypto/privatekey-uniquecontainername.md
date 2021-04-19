---
description: 抓取唯一的私密金鑰容器名稱。
ms.assetid: 2f1315b7-0b12-45d6-8dac-80331bd84ffd
title: PrivateKey. UniqueContainerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.UniqueContainerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9db721f8d3cc67bd8ec9252f299bffa6e077f086
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977603"
---
# <a name="privatekeyuniquecontainername-property"></a>PrivateKey. UniqueContainerName 屬性

\[**UniqueContainerName** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**UniqueContainerName** 屬性會抓取唯一的私密金鑰容器名稱。

## <a name="syntax"></a>Syntax


```VB
PrivateKey.UniqueContainerName As String
```



## <a name="property-value"></a>屬性值

包含唯一私用金鑰容器名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
