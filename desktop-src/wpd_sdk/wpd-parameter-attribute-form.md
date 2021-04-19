---
description: 描述 (方法或事件) 參數如何儲存其值。
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: 'WpdParameterAttributeForm 列舉 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989513"
---
# <a name="wpdparameterattributeform-enumeration"></a>WpdParameterAttributeForm 列舉

[**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85))列舉型別描述 (方法或事件) 參數如何儲存其值。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_ \_ 未指定 WPD 參數屬性 \_ 表單 \_**
</dt> <dd>

未指定參數的格式。

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 範圍**
</dt> <dd>

參數會指定範圍。

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 列舉**
</dt> <dd>

參數是列舉。

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式**
</dt> <dd>

參數是正則運算式。

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD \_ 參數 \_ 屬性 \_ 物件 \_ 識別碼**
</dt> <dd>

參數是物件識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



 

