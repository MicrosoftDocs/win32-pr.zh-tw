---
description: 抓取代表集合之索引憑證的憑證物件。 這是預設屬性。
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificate. Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927f52570b515c6699458cfb802b5c315201d401e9bcf5e0be76ab41863bd47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770537"
---
# <a name="certificatesitem-property"></a>Certificate. Item 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]

**Item** 屬性會抓取代表集合之索引憑證的 [**憑證**](certificate.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

表示已編制索引之憑證的 [**憑證**](certificate.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificates.md)
</dt> </dl>

 

 
