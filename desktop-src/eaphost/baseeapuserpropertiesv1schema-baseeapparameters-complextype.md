---
title: BaseEapParameters 複雜類型-使用者屬性
description: 定義專案，指定選取的舊版方法和方法特定的認證。
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106985919"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>BaseEapParameters 複雜類型-使用者屬性

**BaseEapParameters** 複雜型別會定義指定舊版方法的元素，以及特定方法的認證。

方法可以定義 **BaseEapParameters** 內的組成元素;方法也會對 **BaseEapParameters** 中的元素執行架構驗證。

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



| 元素                                                                      | 類型    | Description                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**類型**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | 整數 | 定義所選方法類型的預留位置元素，以及方法特定的認證。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1 架構](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





