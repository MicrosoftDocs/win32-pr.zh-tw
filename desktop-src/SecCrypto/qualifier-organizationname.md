---
description: 抓取與辨識符號相關聯的組織名稱。
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: OrganizationName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f082a821779cc6e2182e88cf9742c87de0417e7ac297fda2f799ca5878d4ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975768"
---
# <a name="qualifierorganizationname-property"></a>OrganizationName 屬性

\[**OrganizationName** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

**OrganizationName** 屬性會抓取與辨識符號相關聯的組織名稱。 這個屬性可以是空的。

## <a name="syntax"></a>Syntax


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a>屬性值

與辨識符號相關聯的組織名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
