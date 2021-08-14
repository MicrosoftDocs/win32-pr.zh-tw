---
title: versionType 簡單類型
description: 定義指定工作版本的模式。
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- versionType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ad30f5ea14a447e2a08151ef2803b0577066e147e29673d373ce87eee033f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355034"
---
# <a name="versiontype-simple-type"></a>versionType 簡單類型

定義指定工作版本的模式。

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**VersionType** 簡單類型是以下列模式限制的 **字串**：

-   `\d+(\.\d+){1,3}`

    後面接著一、二或三個雙精度浮點數的雙精度浮點數。 例如，1.2 或1.2.3。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





