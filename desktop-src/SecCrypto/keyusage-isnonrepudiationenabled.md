---
description: 抓取布林值，指出是否已設定 nonRepudiationEnabled 位。
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: KeyUsage. IsNonRepudiationEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b5ba81aad49a33a987b2c16c072a6666776b665bf1bd936086a25d1ddd542f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408728"
---
# <a name="keyusageisnonrepudiationenabled-property"></a>KeyUsage. IsNonRepudiationEnabled 屬性

\[**IsNonRepudiationEnabled** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsNonRepudiationEnabled** 屬性會抓取布林值，指出是否已設定 nonRepudiationEnabled 位。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則會設定 nonRepudiationEnabled 位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
