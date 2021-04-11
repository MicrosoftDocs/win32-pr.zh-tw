---
description: 定義 Mobile 寬頻設定檔的 ProviderID 元素類型。
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: providerIdType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112892"
---
# <a name="provideridtype-simple-type"></a>providerIdType 簡單類型

**ProviderIdType** simple type 會定義 Mobile 寬頻設定檔的 [**ProviderID**](schema-providerid-providertype-element.md)元素類型。 此類型是至少一個數位的集合，且長度最多為6位數。

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**ProviderIdType** 簡單類型是以下列模式限制的標記：

-   `\d{1,6}`

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




