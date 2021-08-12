---
title: showMessageType 複雜類型
description: 定義代表顯示訊息方塊之動作的元素。
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- showMessageType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611240"
---
# <a name="showmessagetype-complex-type"></a>showMessageType 複雜類型

定義代表顯示訊息方塊之動作的元素。

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                            | 類型           | 描述                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**本文**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | 指定要顯示在訊息方塊主體中的文字。 <br/> |
| [**標題**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | 指定訊息方塊的標題。 <br/>                       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





