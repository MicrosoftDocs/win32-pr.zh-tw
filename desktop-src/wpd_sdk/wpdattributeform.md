---
description: WpdAttributeForm 列舉型別描述屬性如何儲存其值。
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: 'WpdAttributeForm 列舉 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976272"
---
# <a name="wpdattributeform-enumeration"></a>WpdAttributeForm 列舉

**WpdAttributeForm** 列舉型別描述屬性如何儲存其值。

## <a name="syntax"></a>Syntax


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_ \_ 未指定 WPD 屬性屬性 \_ 表單 \_**
</dt> <dd>

未指定屬性資料的格式。

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 範圍**
</dt> <dd>

值是以值的範圍表示，最小值和最大值。

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 列舉**
</dt> <dd>

屬性有一系列的個別值。

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式**
</dt> <dd>

屬性值是正則運算式，而不是常值運算式。

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 物件 \_ 識別碼**
</dt> <dd>

屬性值代表物件識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

[WPD \_ 屬性 \_ 屬性 \_ 表單](attributes.md)屬性會使用這個列舉來描述屬性資料的儲存方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




