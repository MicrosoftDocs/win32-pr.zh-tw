---
title: 二元 (EventDataType) 元素
description: 使用事件記錄撰寫之事件的二進位資料 blob。
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- 二元元素 EventLog
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024606"
---
# <a name="binary-eventdatatype-element"></a>二元 (EventDataType) 元素

使用 [事件記錄](/windows/desktop/EventLog/event-logging)撰寫之事件的二進位資料 blob。

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

**二元** 元素是由 [**EventDataType**](eventschema-eventdatatype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**EventData (的事件)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

