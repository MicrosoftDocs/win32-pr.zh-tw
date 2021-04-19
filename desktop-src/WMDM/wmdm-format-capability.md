---
title: WMDM_FORMAT_CAPABILITY 結構
description: WMDM \_ 格式 \_ 功能結構描述特定格式之裝置的功能。
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993961"
---
# <a name="wmdm_format_capability-structure"></a>WMDM \_ 格式 \_ 功能結構

**WMDM \_ 格式 \_ 功能** 結構描述特定格式之裝置的功能。 此結構在 **WMDM \_ \_ 配置** 結構的陣列中包含一組屬性設定。 每個屬性設定都代表一組相容的屬性值，這些屬性值橫跨指定格式支援的所有屬性。 應用程式可以藉由呼叫 **IWMDMDevice3：： GetFormatCapability** 方法並傳入格式代碼，來取得此結構。 如需格式代碼的清單，請參閱 [**WMDM \_ FORMATCODE**](wmdm-formatcode.md)。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>成員

<dl> <dt>

**nPropConfig**
</dt> <dd>

**PConfigs** 陣列中的屬性設定數目。

</dd> <dt>

**pConfigs**
</dt> <dd>

[**WMDM \_ \_ 配置**](wmdm-prop-config.md)結構的陣列指標。 陣列的大小等於 **nPropConfig** 的值。

</dd> </dl>

## <a name="remarks"></a>備註

**WMDM \_ 格式 \_ 功能** 結構提供了彈性的機制，可針對特定的格式來表示裝置的功能。

如果內容是要由裝置轉譯 (例如，裝置) 要播放的音訊檔案，則內容屬性必須符合 **WMDM \_ 格式 \_ 功能** 結構中 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)所傳回的其中一個屬性設定。 例如，對於音訊檔案，位元速率和取樣率必須符合其中一個傳回的屬性設定。

呼叫端負責釋放配置給此結構的記憶體。 下列函式示範如何清除 **WMDM \_ 格式 \_ 功能** 結構。


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



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

[**WMDM \_ \_ 配置設定**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM 的一種 \_ \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





