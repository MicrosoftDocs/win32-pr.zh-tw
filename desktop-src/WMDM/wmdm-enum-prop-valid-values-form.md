---
title: WMDM_ENUM_PROP_VALID_VALUES_FORM 列舉
description: WMDM \_ 列舉 \_ \_ 屬性有效的 \_ 值 \_ 表單列舉型別描述了可能的屬性有效值形式。
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982271"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>WMDM \_ 列舉 \_ \_ 值的 \_ 有效值 \_ 表單列舉

**WMDM \_ 列舉屬性 \_ 有效 \_ 的 \_ 值 \_ 表單** 列舉型別描述了可能的屬性有效值形式。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ 列舉會將 \_ 有效值的 \_ 有效值 \_ \_**
</dt> <dd>

所有值都是有效的。

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 範圍**
</dt> <dd>

有效的值會以範圍表示。 如需詳細資訊，請參閱 WMDM 的「 [**\_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構」。

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 列舉**
</dt> <dd>

有效的值為列舉集合。 如需詳細資訊，請參閱 WMDM 的「內容」 [**\_ \_ 值 \_ 列舉**](wmdm-prop-values-enum.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

[**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md)結構中會使用這個列舉來指定屬性的有效值格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ \_ 配置設定**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM 的一種 \_ \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





