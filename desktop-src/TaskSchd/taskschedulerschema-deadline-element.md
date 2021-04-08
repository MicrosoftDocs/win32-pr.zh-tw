---
title: 期限元素
description: 指定工作排程器在緊急自動維護期間必須啟動工作的時間（如果在定期自動維護期間無法完成）。
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- 期限元素工作排程器
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685740"
---
# <a name="deadline-element"></a>期限元素

指定工作排程器在緊急自動維護期間必須啟動工作的時間（如果在定期自動維護期間無法完成）。

此字串的格式為 *PnYnMnDTnHnMnS*，其中 *nY* 是年數，nm 是月數、 *nD* 是天、 *T* 是日期/時間分隔符號、 *nH* 是時數、 *nM* 為分鐘數，而 *nS* 是秒數 (例如，"PT5M" 指定5分鐘，而 "P1M4DT2H5M" 則指定一個月、四天、兩小時和五分鐘的) 。 最小值是一分鐘。 如需持續時間類型的詳細資訊，請參閱 [XML 架構第2部分：資料類型第二版](https://www.w3.org/TR/xmlschema-2/#duration)。 工作可以使用的最短期限為1天。 **期限** 元素的值應大於 [**Period**](taskschedulerschema-period-element.md)元素的值。 如果未指定期限，則不會在緊急自動維護期間啟動工作。

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**期限** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                                          | 衍生自                                                                               | Description                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | 指定工作排程器將在自動維護期間用來啟動工作的工作設定。<br/> |



## <a name="remarks"></a>備註

若是 c + + 程式設計，則會使用 [**IMaintenanceSettings：:D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) 屬性來指定此閒置設定。

## <a name="examples"></a>範例

下列 XML 定義在三月執行工作的月份行事曆。


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





