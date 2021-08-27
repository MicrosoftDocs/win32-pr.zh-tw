---
title: runLevelType 簡單類型
description: 定義 RunLevel (principalType) 元素的可能值。
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- runLevelType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991068"
---
# <a name="runleveltype-simple-type"></a>runLevelType 簡單類型

定義 [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) 元素的可能值。

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**RunLevelType** 簡單類型會定義下列值。



| 值            | 描述                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | 工作會以最少的許可權執行， (LUA) 。<br/> |
| HighestAvailable | 工作是以最高許可權執行。<br/>     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





