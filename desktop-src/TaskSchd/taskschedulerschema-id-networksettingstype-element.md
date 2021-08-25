---
title: Id (networkSettingsType) 元素
description: 包含可識別網路設定檔的 GUID 值。
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Id 元素工作排程器
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125838"
---
# <a name="id-networksettingstype-element"></a>Id (networkSettingsType) 元素

包含可識別網路設定檔的 GUID 值。

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

**Id** 元素是由 [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                            | 衍生自                                                                       | 描述                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | 包含工作排程器服務用來取得網路設定檔的設定。 當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**INetworkSettings 的 Id 屬性**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id)。

如需腳本開發，請參閱 [**NetworkSettings.Id**](networksettings-id.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





