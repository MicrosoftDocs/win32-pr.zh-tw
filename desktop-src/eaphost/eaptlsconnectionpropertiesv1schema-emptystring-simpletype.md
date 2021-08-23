---
title: emptyString 簡單類型
description: 深入瞭解未使用的 emptyString 簡單類型。 查看需求並查看其他可用的資源。
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptyString 簡單類型 EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f210fadeb0097ffd7a11d80dd47b252dbbfdc614950af0ac07d612b44edd0aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948208"
---
# <a name="emptystring-simple-type"></a>emptyString 簡單類型

**EmptyString** 簡單類型未使用中。

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|-------------------------------------|------------------------------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構簡單類型](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





