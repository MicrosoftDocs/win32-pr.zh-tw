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
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965318"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





