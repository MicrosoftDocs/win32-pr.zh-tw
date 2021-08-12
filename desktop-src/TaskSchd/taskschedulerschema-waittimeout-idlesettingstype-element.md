---
title: WaitTimeout (idleSettingsType) 元素
description: 指定工作排程器將等候閒置條件發生的時間量。
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- WaitTimeout 元素工作排程器
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d078acecf39f9bd4848cabaa8b203787049ca8a66e565e6183b8b1998389ad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610393"
---
# <a name="waittimeout-idlesettingstype-element"></a>WaitTimeout (idleSettingsType) 元素

指定工作排程器將等候閒置條件發生的時間量。 如果未指定這個專案的值，工作排程器服務將會無限期地等候閒置的情況發生。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。 允許的最小時間是1分鐘。

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | 描述                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，此閒置設定是使用 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性來指定。

針對 c + + 開發，此閒置設定是使用 [**IIdleSettings：： WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 會定義閒置設定，以等候24小時進行閒置的條件。


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





