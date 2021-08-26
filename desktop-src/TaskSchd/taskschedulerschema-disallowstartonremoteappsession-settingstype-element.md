---
title: DisallowStartOnRemoteAppSession (settingsType) 元素
description: 指定當觸發在本機 (鐵路) 會話的遠端應用程式中執行時，工作將不會啟動。
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- DisallowStartOnRemoteAppSession 元素工作排程器
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2f7834ecd57fa10aaaabfa21945f1e908834d535d50f94b4dd21e6ca45c0a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010798"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>DisallowStartOnRemoteAppSession (settingsType) 元素

指定當觸發在本機 (鐵路) 會話的遠端應用程式中執行時，工作將不會啟動。

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**DisallowStartOnRemoteAppSession** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

此元素的預設設定為 False。

針對 c + + 開發，此資訊可透過 [**ITaskSettings2：:D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) 屬性來存取。

## <a name="examples"></a>範例

下列 XML 會定義一個設定專案，如果工作觸發在滑軌會話中執行，則不允許啟動工作。


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





