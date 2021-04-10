---
title: 延遲 (sessionStateChangeTriggerType) 元素
description: 包含值，指出當偵測到終端機伺服器會話狀態變更時，工作開始時間的延遲長度。
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Delay 元素工作排程器
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106379"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>延遲 (sessionStateChangeTriggerType) 元素

包含值，指出當偵測到終端機伺服器會話狀態變更時，工作開始時間的延遲長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**Delay** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                       | 衍生自                                                                                           | Description                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | 指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。 <br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**SessionStateChangeTrigger**](sessionstatechangetrigger-delay.md) 屬性來指定會話狀態變更觸發程式延遲。

針對 c + + 開發，會使用 [**ISessionStateChangeTrigger 的 delay 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay)指定會話狀態變更觸發程式延遲。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





