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
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000248"
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



 

 




