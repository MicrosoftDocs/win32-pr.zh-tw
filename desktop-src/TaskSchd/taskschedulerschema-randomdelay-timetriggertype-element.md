---
title: RandomDelay (timeTriggerType) 元素
description: 包含隨機新增至觸發程式開始時間的延遲時間。 |RandomDelay (timeTriggerType) 元素
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- RandomDelay 元素工作排程器
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c4c9fde8a0f88ed7e87b5a0d3ccc252f141f6b677f535adf853ef0aca9499b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611504"
---
# <a name="randomdelay-timetriggertype-element"></a>RandomDelay (timeTriggerType) 元素

包含隨機新增至觸發程式開始時間的延遲時間。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

元素是由 [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                    | 衍生自                                                               | 描述                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | 指定啟動觸發程式時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITimeTrigger 的 RandomDelay 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)。

如需腳本開發，請參閱 [**TimeTrigger. RandomDelay**](timetrigger-randomdelay.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





