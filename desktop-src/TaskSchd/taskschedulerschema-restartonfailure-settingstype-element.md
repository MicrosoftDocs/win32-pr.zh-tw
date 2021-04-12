---
title: RestartOnFailure (settingsType) 元素
description: 指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- RestartOnFailure 元素工作排程器
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187317"
---
# <a name="restartonfailure-settingstype-element"></a>RestartOnFailure (settingsType) 元素

指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

**RestartOnFailure** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                              | 類型         | Description                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**計數**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | 指定工作排程器將嘗試重新開機工作的次數。<br/> |
| [**間隔**](taskschedulerschema-interval-restarttype-element.md) | duration     | 指定工作排程器將嘗試重新開機工作的時間長度。<br/>                 |



## <a name="remarks"></a>備註

當應用程式指定工作設定時，這項資訊會透過 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings)介面的 [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount)和 [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)屬性來存取。 針對腳本，這項資訊是透過 [**TaskSettings. RestartCount**](tasksettings-restartcount.md) 和 [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) 屬性來存取。

這兩個子專案都必須設定為指定工作排程器重新開機工作的方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





