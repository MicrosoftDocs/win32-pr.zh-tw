---
title: MaintenanceSettings (maintenanceSettingsType) 元素
description: 指定工作排程器在自動維護期間如何執行工作。
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- MaintenanceSettings 元素工作排程器
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5724a5dff942377af783970e5d011e8f8a1ce9123039112917a3f652372495d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309338"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>MaintenanceSettings (maintenanceSettingsType) 元素

指定工作排程器在自動維護期間如何執行工作。

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

**MaintenanceSettings** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                    | 類型    | 描述                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**期限**](taskschedulerschema-deadline-element.md)   |         | 指定當工作排程器在正常維護期間無法完成時，在緊急自動維護期間，工作排程器將嘗試啟動工作的時間量。 <br/> |
| [**獨佔**](taskschedulerschema-exclusive-element.md) | boolean | 如果設定為 true，則工作將會在其他維護工作中以獨佔方式啟動。 <br/>                                                                                                 |
| [**期間**](taskschedulerschema-period-element.md)       |         | 指定在自動維護期間必須啟動工作的頻率。 <br/>                                                                                                      |



## <a name="remarks"></a>備註

針對 c + + 程式設計，此閒置設定是使用 [**ITaskSettings3：： MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 定義的設定元素，會指示工作排程器在定期自動維護期間的5天內執行工作一次，如果在15天內失敗，則在緊急自動維護期間開始嘗試工作。


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





