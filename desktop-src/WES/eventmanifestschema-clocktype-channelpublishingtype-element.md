---
title: clockType (ChannelPublishingType) 元素
description: 記錄每個事件的時間戳記時，所要使用的時鐘解析。
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- clockType 元素 EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384029"
---
# <a name="clocktype-channelpublishingtype-element"></a>clockType (ChannelPublishingType) 元素

記錄每個事件的時間戳記時，所要使用的時鐘解析。

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**ClockType** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**發行 (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





