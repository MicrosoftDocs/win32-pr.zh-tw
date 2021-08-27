---
title: WMDM_PROP_VALUES_ENUM 結構
description: WMDM \_ \_ \_ 屬性值列舉結構包含特定屬性設定中特定屬性的有效值列舉集合。
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35766ed71b864c5eb7f0bbbebf5eda384a25e174501aa2a56e790840a4c636c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004788"
---
# <a name="wmdm_prop_values_enum-structure"></a>WMDM \_ 的 \_ 值 \_ 列舉結構

**WMDM 屬性 \_ \_ 值 \_ 列舉** 結構包含特定屬性設定中特定屬性的有效值列舉集合。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>成員

<dl> <dt>

**cEnumValues**
</dt> <dd>

列舉值的計數。

</dd> <dt>

**pValues**
</dt> <dd>

值陣列的指標。 陣列的大小等於 **cEnumValues** 的值。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會在 WMDM 的 [描述] **\_ \_ DESC** 結構中用來描述有效值的列舉集合。 \_ \_ \_ \_ \_ 從 WMDM 列舉配置有效值（列舉為 **\_ 有效值） \_ \_ \_ \_ 表單** 列舉中選取了 WMDM 列舉配置值的列舉值時，可使用一組列舉的有效值。

需要呼叫端才能釋放 **pValues** 所使用的記憶體。 如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。

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

[**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





