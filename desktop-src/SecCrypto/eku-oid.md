---
description: 設定或抓取包含 EKU OID 字串值的字串，如 Wincrypt 中所定義。
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: IEKU：： OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 49a35cb223c338573ba0a52288a1e5528820dcbd4c7589548ce31f9df46dc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875248"
---
# <a name="iekuoid-property"></a>IEKU：： OID 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**OID** 屬性會設定或抓取包含 EKU OID 字串值的字串，如 Wincrypt 中所定義。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EKU.OID As String
```



## <a name="property-value"></a>屬性值

包含 Wincrypt 中所定義之 EKU OID 字串值的字串。

## <a name="remarks"></a>備註

此屬性不會使用在 CAPICOM 2.0 中引進的 [**OID**](oid.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
