---
title: sidType (ChannelPublishingType) 元素
description: 決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- sidType 元素 EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589149"
---
# <a name="sidtype-channelpublishingtype-element"></a>sidType (ChannelPublishingType) 元素

決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**SidType** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**發行 (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





