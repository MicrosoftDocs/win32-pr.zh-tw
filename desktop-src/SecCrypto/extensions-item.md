---
description: Item 屬性會依據索引，從集合中抓取延伸。 這是預設屬性。
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extension. Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989753"
---
# <a name="extensionsitem-property"></a>Extension. Item 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]

**Item** 屬性會依據索引，從集合中抓取延伸。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

代表集合之索引憑證延伸的 [**擴充**](extension.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**延伸模組**](extensions.md)
</dt> </dl>

 

 
