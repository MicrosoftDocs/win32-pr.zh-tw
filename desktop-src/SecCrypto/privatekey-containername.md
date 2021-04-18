---
description: 抓取私密金鑰容器名稱。
ms.assetid: ecc0b4ba-4e2b-49e9-8358-8c498e1d6ae0
title: PrivateKey 容器屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ContainerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0e9506b9390dc8b09e6326232e53c72d01749f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976286"
---
# <a name="privatekeycontainername-property"></a>PrivateKey 容器屬性

\[[ **容器** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**容器** 屬性會抓取私密金鑰容器名稱。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
PrivateKey.ContainerName As String
```



## <a name="property-value"></a>屬性值

包含私密金鑰容器名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
