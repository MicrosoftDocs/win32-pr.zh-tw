---
title: QueryType 複雜類型
description: 定義一組選取器和抑制器查詢，用來在結果集中包含或排除事件。
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6585b43e1e9e48bc0be69001d471c74e52506177250d66316273ca447b38084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587623"
---
# <a name="querytype-complex-type"></a>QueryType 複雜類型

定義一組選取器和抑制器查詢，用來在結果集中包含或排除事件。

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                    | 類型 | 描述                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**選擇**](queryschema-select-querytype-element.md)     |      | XPath 查詢，識別要包含在查詢結果集中的事件。 在此元素的文字本文中指定 XPath。 XPath 的限制為32個運算式。<br/>   |
| [**隱藏**](queryschema-suppress-querytype-element.md) |      | XPath 查詢，識別要從查詢結果集排除的事件。 在此元素的文字本文中指定 XPath。 XPath 的限制為32個運算式。<br/> |



## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 識別碼   | long   | 可在您的查詢清單中唯一識別此查詢的識別碼。 識別碼以零為基底。 如果您的查詢清單包含一個以上的查詢，則必須指定識別碼。<br/> |
| 路徑 | anyURI | 通道的名稱或包含事件之記錄檔的路徑。<br/>                                                                                                            |
| 路徑 | anyURI | 通道的名稱或包含事件之記錄檔的路徑。<br/>                                                                                                            |
| 路徑 | anyURI | 未使用。<br/>                                                                                                                                                                                |



## <a name="remarks"></a>備註

查詢必須至少有一個 select 語句。 針對每個隱藏語句，至少必須有一個指定相同路徑的 select 語句。 如果 select 和抑制查詢傳回相同的事件，則會優先使用隱藏語句。 如果您選取多個來源的事件，則會以時間戳記順序傳回事件。 如果您使用系統時間戳記，而事件率很高，則有一個以上的事件可能會有相同的時間戳記。 發生這種情況時，事件的順序會變得不明確，而且事件可能會依順序出現。

如果您為查詢清單中的其中一個查詢指定路徑，則所有查詢都必須指定路徑。 如果您未指定所有查詢的路徑，則必須在呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函式時指定路徑。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





