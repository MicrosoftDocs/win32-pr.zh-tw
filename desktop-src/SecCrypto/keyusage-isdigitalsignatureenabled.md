---
description: 抓取布林值，指出是否已設定 digitalSignature 位。
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: KeyUsage. IsDigitalSignatureEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 963fc78243cf235fe0975fae203e17d1d4f6e71bb909259c7c83acc4fe9e5f07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080648"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a>KeyUsage. IsDigitalSignatureEnabled 屬性

\[**IsDigitalSignatureEnabled** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsDigitalSignatureEnabled** 屬性會抓取布林值，指出是否已設定 digitalSignature 位。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則會設定 digitalSignature 位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
