---
title: NetworkSettings (settingsType) 元素
description: 包含工作排程器服務用來取得網路設定檔的設定。 當 RunOnlyIfNetworkAvailable 元素設定為 True 時，工作排程器服務會檢查此網路的可用性。
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- NetworkSettings 元素工作排程器
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465805"
---
# <a name="networksettings-settingstype-element"></a>NetworkSettings (settingsType) 元素

包含工作排程器服務用來取得網路設定檔的設定。 當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

**NetworkSettings** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                      | 衍生自                                                         | Description                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**設定 (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 指定工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 NetworkSettings 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings)。

如需腳本開發，請參閱 [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





