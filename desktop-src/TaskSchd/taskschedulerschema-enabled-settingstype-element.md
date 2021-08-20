---
title: 已啟用 (settingsType) 元素
description: 指定已啟用工作。 只有當這項設定為 True 時，才能執行此工作。
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Enabled 元素工作排程器
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131867"
---
# <a name="enabled-settingstype-element"></a>已啟用 (settingsType) 元素

指定已啟用工作。 只有當這項設定為 True 時，才能執行此工作。

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

**Enabled** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 Enabled 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled)。

如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-enabled.md)

## <a name="examples"></a>範例

如需已啟用之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





