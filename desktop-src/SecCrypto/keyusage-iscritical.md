---
description: 抓取布林值，指出 KeyUsage 延伸模組是否標記為重大。
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage. IsCritical 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983943"
---
# <a name="keyusageiscritical-property"></a>KeyUsage. IsCritical 屬性

\[**IsCritical** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsCritical** 屬性會抓取布林值，指出 KeyUsage 延伸模組是否標記為重大。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則表示 KeyUsage 延伸模組標示為「重大」。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
