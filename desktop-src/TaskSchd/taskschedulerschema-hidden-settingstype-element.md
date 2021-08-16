---
title: 隱藏的 (settingsType) 元素
description: 指定預設情況下，工作將不會顯示在 UI 中。
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Hidden 元素工作排程器
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9820008ead01930eff23a50408f4952d08e9190984432f65c3d9e5f4eedbef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658908"
---
# <a name="hidden-settingstype-element"></a>隱藏的 (settingsType) 元素

指定預設情況下，工作將不會顯示在 UI 中。 不過，系統管理員可以使用「主要交換器」來覆寫這項設定，讓所有工作都顯示在 UI 中。

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**Hidden** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 Hidden 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden)。

如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-hidden.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





