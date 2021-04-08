---
title: NetworkProfileName (settingsType) 元素
description: 包含網路設定檔的名稱。 當 RunOnlyIfNetworkAvailable 元素設定為 True 時，工作排程器服務會檢查此網路的可用性。 此名稱會用於顯示用途。
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- NetworkProfileName 元素工作排程器
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686072"
---
# <a name="networkprofilename-settingstype-element"></a>NetworkProfileName (settingsType) 元素

包含網路設定檔的名稱。 當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。 此名稱會用於顯示用途。

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

**NetworkProfileName** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                      | 衍生自                                                         | Description                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**設定 (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 指定工作排程器用來執行工作的設定。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





