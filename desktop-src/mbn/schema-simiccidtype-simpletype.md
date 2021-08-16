---
description: 定義行動寬頻設定檔之 SimIccID 元素的類型。
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: simIccIDType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035756"
---
# <a name="simiccidtype-simple-type"></a>simIccIDType 簡單類型

**SimIccIDType** 簡單類型會定義行動寬頻設定檔的 [**SimIccID**](schema-simiccid-mbnprofile-element.md)元素類型。 此類型是數位和/或大寫和小寫字母的集合，至少一個字元長，最多20個字元。

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**SimIccIDType** 簡單類型是以下列模式限制的標記：

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




