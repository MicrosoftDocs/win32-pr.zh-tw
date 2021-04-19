---
description: 抓取代表索引的擴充金鑰使用方式 (EKU) 屬性的 EKU 物件。
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: IEKUs：： Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978436"
---
# <a name="iekusitem-property"></a>IEKUs：： Item 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]

**Item** 屬性會抓取代表索引的擴充金鑰使用方式 (eku) 屬性的 [**eku**](eku.md)物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

[**Eku**](eku.md)物件，代表索引的擴充金鑰使用方式 (eku) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Eku**](ekus.md)
</dt> </dl>

 

 
