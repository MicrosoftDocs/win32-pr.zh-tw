---
title: AllowHardTerminate (settingsType) 元素
description: 指定可以使用 TerminateProcess 終止工作。
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- AllowHardTerminate (settingsType) 元素工作排程器
- AllowHardTerminate 元素工作排程器
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d7a143dfb0024cced8a67595e17b12fba9d037b335b425272e1ad2a7999e0b11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010918"
---
# <a name="allowhardterminate-settingstype-element"></a>AllowHardTerminate (settingsType) 元素

指定可以使用 TerminateProcess 終止工作。

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

**AllowHardTerminate** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                 | 描述                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 AllowHardTerminate 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate)。

如需腳本開發，請參閱 [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md)。

## <a name="examples"></a>範例

如需允許硬終止之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





