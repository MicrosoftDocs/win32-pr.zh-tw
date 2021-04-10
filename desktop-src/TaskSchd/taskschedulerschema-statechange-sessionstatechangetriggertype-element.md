---
title: StateChange (sessionStateChangeTriggerType) 元素
description: 包含會觸發工作啟動的終端機伺服器會話變更類型。
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange 元素工作排程器
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106349"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>StateChange (sessionStateChangeTriggerType) 元素

包含會觸發工作啟動的終端機伺服器會話變更類型。

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

**StateChange** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                       | 衍生自                                                                                           | Description                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | 指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ISessionStateChangeTrigger 的 StateChange 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange)。

如需腳本開發，請參閱 [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





