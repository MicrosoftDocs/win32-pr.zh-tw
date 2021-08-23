---
description: 抓取布林值，指出是否已設定 decipherOnly 位。
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: KeyUsage. IsDecipherOnlyEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e46a2d5fb04b54922081bc7c15ab4cfdcbe7536974720d39472ac0af8c64fca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622308"
---
# <a name="keyusageisdecipheronlyenabled-property"></a>KeyUsage. IsDecipherOnlyEnabled 屬性

\[**IsDecipherOnlyEnabled** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsDecipherOnlyEnabled** 屬性會抓取布林值，指出是否已設定 decipherOnly 位。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則會設定 decipherOnly 位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
