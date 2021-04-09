---
title: StartWhenAvailable (settingsType) 元素
description: 指定工作排程器可以在經過排程的時間之後隨時啟動工作。
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- StartWhenAvailable 元素工作排程器
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934070"
---
# <a name="startwhenavailable-settingstype-element"></a>StartWhenAvailable (settingsType) 元素

指定工作排程器可以在經過排程的時間之後隨時啟動工作。

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**StartWhenAvailable** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

這個屬性只適用于計時工作。

針對 c + + 開發，請參閱 [**ITaskSettings 的 StartWhenAvailable 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable)。

如需腳本開發，請參閱 [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md)。

## <a name="examples"></a>範例

下列 XML 會定義 settings 元素，讓工作排程器在工作可用時啟動工作。


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





