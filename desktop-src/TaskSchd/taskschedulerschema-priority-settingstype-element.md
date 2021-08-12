---
title: 優先權 (settingsType) 元素
description: 指定工作的優先權層級。
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Priority 元素工作排程器
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611890"
---
# <a name="priority-settingstype-element"></a>優先權 (settingsType) 元素

指定工作的優先權層級。

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

**Priority** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

優先權層級0是最高優先順序，而優先順序層級10是最低優先順序。 預設值為 7。 最小值和最大值是由 [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) 簡單類型所設定。 優先權層級7和8用於背景工作，而優先順序層級4、5和6則用於互動式工作。

工作的動作會在具有以優先權類別值為基礎之優先權的進程中啟動。 優先權層級值 (執行緒優先順序) 用於 COM 處理常式、訊息方塊，以及電子郵件工作動作。 如需優先順序類別和優先權層級值的詳細資訊，請參閱 [排程優先順序](/windows/desktop/ProcThread/scheduling-priorities)。 下表列出 **priority** 元素的可能值，以及對應的 priority 類別和優先權層級值。



| 工作優先順序 | Priority 類別                 | 優先權層級                   |
|---------------|--------------------------------|----------------------------------|
| 0             | 即時 \_ 優先權 \_ 類別      | 執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足 |
| 1             | 高 \_ 優先順序 \_ 類別          | 執行緒 \_ 優先順序 \_ 最高        |
| 2             | 高於 \_ 一般 \_ 優先順序 \_ 類別 | \_ \_ 高於 \_ 一般的執行緒優先順序  |
| 3             | 高於 \_ 一般 \_ 優先順序 \_ 類別 | \_ \_ 高於 \_ 一般的執行緒優先順序  |
| 4             | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 5             | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 6             | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 7             | 低於 \_ 一般 \_ 優先順序 \_ 類別 | 一般的執行緒 \_ 優先順序 \_ \_  |
| 8             | 低於 \_ 一般 \_ 優先順序 \_ 類別 | 一般的執行緒 \_ 優先順序 \_ \_  |
| 9             | 閒置 \_ 優先權 \_ 類別          | 執行緒 \_ 優先順序 \_ 最低         |
| 10            | 閒置 \_ 優先權 \_ 類別          | 執行緒 \_ 優先順序 \_ 閒置           |



 

針對 c + + 開發，請參閱 [**ITaskSettings 的 Priority 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority)。

如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-priority.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

