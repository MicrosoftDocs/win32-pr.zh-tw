---
title: FilterListType 複雜類型
description: 定義 ETW 控制器可傳遞給提供者的篩選清單，以進一步限制它所寫入的事件。
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589623"
---
# <a name="filterlisttype-complex-type"></a>FilterListType 複雜類型

定義 ETW 控制器可傳遞給提供者的篩選清單，以進一步限制它所寫入的事件。

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素    | 類型                                                             | 描述                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | 篩選準則的清單。<br/> |



## <a name="remarks"></a>備註

ETW 控制器是一種應用程式，可呼叫 [**StartTrace**](/windows/desktop/ETW/starttrace) 函式來建立 ETW 會話。 如需詳細資訊，請參閱 [控制事件追蹤會話](/windows/desktop/ETW/controlling-event-tracing-sessions)。 控制器可以使用 [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) 函式來列舉您所定義的篩選準則。 然後，控制器會在呼叫 [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) 函式來啟用您的提供者時，傳遞一或多個篩選準則。 您的提供者會在 [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) 回呼函式中接收篩選，以及其餘的 enable 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

