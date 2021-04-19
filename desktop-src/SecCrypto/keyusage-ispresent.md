---
description: 抓取布林值，指出 KeyUsage 延伸是否存在。
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986143"
---
# <a name="keyusageispresent-property"></a>KeyUsage. IsPresent 屬性

\[**IsPresent** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsPresent** 屬性會抓取布林值，指出 [**KeyUsage**](keyusage.md)延伸是否存在。

這個屬性是 [**KeyUsage**](keyusage.md) 物件的預設屬性。

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則表示 KeyUsage 延伸模組存在。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
