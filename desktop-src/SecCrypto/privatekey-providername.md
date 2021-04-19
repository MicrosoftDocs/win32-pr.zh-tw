---
description: 抓取 (CSP) 的密碼編譯服務提供者的名稱。
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990819"
---
# <a name="privatekeyprovidername-property"></a>PrivateKey. ProviderName 屬性

\[[ **ProviderName** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**ProviderName** 屬性會抓取 (CSP) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的名稱。

## <a name="syntax"></a>Syntax


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a>屬性值

包含 CSP 名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
