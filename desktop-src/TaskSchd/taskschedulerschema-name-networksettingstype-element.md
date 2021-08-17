---
title: NetworkSettingsType) 專案的名稱 (
description: 包含網路設定檔的名稱。 此名稱會用於顯示用途。
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name 元素工作排程器
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758498"
---
# <a name="name-networksettingstype-element"></a>NetworkSettingsType) 專案的名稱 (

包含網路設定檔的名稱。 此名稱會用於顯示用途。

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

**Name** 元素是由 [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                            | 衍生自                                                                       | 描述                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | 包含工作排程器服務用來取得網路設定檔的設定。 當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**INetworkSettings 的 Name 屬性**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name)。

如需腳本開發，請參閱 [**NetworkSettings.Name**](networksettings-name.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





