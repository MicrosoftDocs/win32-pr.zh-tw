---
title: comHandlerType 複雜類型
description: 定義 ComHandler 元素的子項目和排序資訊。
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- comHandlerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fb8fdaf16213f70a33ebefdead7b73df6645f3f10489add7bda419c71a8b277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943130"
---
# <a name="comhandlertype-complex-type"></a>comHandlerType 複雜類型

定義 [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                               | 類型                                                         | 描述                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | 指定處理常式類別的識別碼。<br/>          |
| [**資料**](taskschedulerschema-data-comhandlertype-element.md)       | [**dataType**](taskschedulerschema-datatype-complextype.md) | 指定與處理常式相關聯的其他資料。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





