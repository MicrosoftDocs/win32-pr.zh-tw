---
title: 主體 (taskType) 元素
description: 指定可以用來執行工作的安全性內容。
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- 主體元素工作排程器
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934014"
---
# <a name="principals-tasktype-element"></a>主體 (taskType) 元素

指定可以用來執行工作的安全性內容。

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

**主體** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 定義工作排程器服務所執行的工作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                  | 類型                                                                   | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

您最多可以為工作指定32主體。

針對開發腳本，工作的主體是使用 [**TaskDefinition**](taskdefinition-principal.md) 屬性來指定。

針對 c + + 開發，工作的主體是使用 ITaskDefinition 的 [**Principal 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)來指定。

## <a name="examples"></a>範例

下列 XML 會定義兩個主體：工作的使用者識別碼和群組識別碼主體。


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





