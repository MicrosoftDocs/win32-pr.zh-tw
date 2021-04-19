---
title: WMDM_PROP_VALUES_RANGE 結構
description: WMDM 屬性 \_ \_ 值 \_ 範圍結構描述特定屬性設定中特定屬性的有效值範圍。
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992811"
---
# <a name="wmdm_prop_values_range-structure"></a>WMDM \_ 的 \_ 值 \_ 範圍結構

**WMDM 屬性 \_ \_ 值 \_ 範圍** 結構描述特定屬性設定中特定屬性的有效值範圍。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>成員

<dl> <dt>

**rangeMin**
</dt> <dd>

範圍中的最小值。

</dd> <dt>

**rangeMax**
</dt> <dd>

範圍中的最大值。

</dd> <dt>

**rangeStep**
</dt> <dd>

有效值從最小值遞增為最大值的步驟大小。 這允許在範圍內指定離散的允許值。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會在 WMDM 的 [描述] [**\_ \_ DESC**](wmdm-prop-desc.md) 結構中用來描述有效值的範圍。 \_ \_ \_ \_ \_ 從 [**WMDM 列舉值的有效值（列舉 \_ 值） \_ \_ \_ \_ 表單**](wmdm-enum-prop-valid-values-form.md)列舉中選取了 WMDM 列舉類型的有效值時，可使用有效的值範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ \_ 配置設定**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM 的一種 \_ \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





