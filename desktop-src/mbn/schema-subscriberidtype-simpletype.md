---
description: 定義行動寬頻設定檔之 SubscriberID 元素的類型。
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: subscriberIdType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881362"
---
# <a name="subscriberidtype-simple-type"></a>subscriberIdType 簡單類型

**SubscriberIdType** 簡單類型會定義行動寬頻設定檔的 [**SubscriberID**](schema-subscriberid-mbnprofile-element.md)元素類型。 此類型是一或多個字元的集合。

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




