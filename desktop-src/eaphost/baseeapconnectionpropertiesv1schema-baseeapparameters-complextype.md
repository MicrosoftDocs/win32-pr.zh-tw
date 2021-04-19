---
title: BaseEapParameters 複雜類型-連接屬性
description: 定義方法類型和特定方法設定的預留位置元素。
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106992356"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>BaseEapParameters 複雜類型-連接屬性

**BaseEapParameters** 複雜型別會定義方法類型和特定方法設定的預留位置元素。

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                            | 類型    | Description                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**類型**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | 整數 | 此處允許任何架構實例。<br/> |



## <a name="remarks"></a>備註

在 **BaseEapParameters** 中，方法可以定義構成元素。 方法也會對 **BaseEapParameters** 中的元素執行架構驗證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 架構](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





