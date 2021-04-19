---
description: 抓取布林值，指出是否已設定 keyAgreement 位。
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: KeyUsage. IsKeyAgreementEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992363"
---
# <a name="keyusageiskeyagreementenabled-property"></a>KeyUsage. IsKeyAgreementEnabled 屬性

\[**IsKeyAgreementEnabled** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsKeyAgreementEnabled** 屬性會抓取布林值，指出是否已設定 keyAgreement 位。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則會設定 keyAgreement 位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
