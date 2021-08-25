---
title: WMDM_PROP_DESC 結構
description: WMDM 屬性 \_ \_ DESC 結構描述特定屬性設定中的有效值。
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903938"
---
# <a name="wmdm_prop_desc-structure"></a>WMDM \_ \_ 架構 DESC 結構

**WMDM 屬性 \_ \_ DESC** 結構描述特定屬性設定中的有效值。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**pwszPropName**
</dt> <dd>

屬性的名稱。 應用程式必須在使用它完成時釋放此記憶體。

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

WMDM 列舉會描述數值型別的 [**\_ \_ \_ 有效 \_ 值 \_ 形式**](wmdm-enum-prop-valid-values-form.md) 列舉值，例如範圍或清單。 此列舉的值會決定要使用的成員變數。

</dd> <dt>

**ValidValues**
</dt> <dd>

在特定屬性設定中保存屬性的有效值。 這個成員有三個專案的其中一個：列舉值 WMDM ENUM 會將 \_ \_ 有效值的 \_ \_ 值 \_ 為 ANY、member **ValidValuesRange** 或 member **EnumeratedValidValues**。 值或成員會以 **ValidValuesForm** 表示。

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

包含有效值範圍的 [**WMDM 架構 \_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構。 只有當 **ValidValuesForm** 設定為 WMDM \_ 列舉 \_ 值的 \_ 有效值 \_ \_ 範圍時，才會出現此情況。 請參閱＜備註＞。

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

[**WMDM 的 \_ 規定 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)結構，其中包含有效值的列舉集合。 只有當 **ValidValuesForm** 設定為 WMDM \_ enum 的 \_ \_ VALID \_ 值 \_ 列舉時，才會出現這種情況。 請參閱＜備註＞。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**WMDM 屬性 \_ \_ DESC** 結構包含屬性描述，其中包含屬性名稱及其在特定設定中的有效值。

需要呼叫端才能釋放 **ValidValuesRange** 或 **EnumeratedValues** 所使用的記憶體。 如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。

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

[**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





