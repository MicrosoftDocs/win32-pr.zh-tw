---
title: WMDM_PROP_CONFIG 結構
description: WMDM 屬性 \_ \_ 設定結構會針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。 此結構在 WMDM 屬性 DESC 結構的陣列中包含許多屬性 \_ 描述 \_ 。
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e50cd18f5b7646934a6add71674f93ebaae700ab39e57f833e555ea3688ecb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862818"
---
# <a name="wmdm_prop_config-structure"></a>WMDM \_ \_ 配置設定結構

**WMDM 屬性 \_ 設定 \_** 結構會針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。 此結構在 [**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md) 結構的陣列中包含許多屬性描述。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>成員

<dl> <dt>

**nPreference**
</dt> <dd>

裝置針對此設定的喜好設定層級。 最小值表示最慣用的設定。

</dd> <dt>

**nPropDesc**
</dt> <dd>

此設定中包含的屬性描述數目。 針對指定的格式所支援的每個屬性都有一個屬性描述。

</dd> <dt>

**pPropDesc**
</dt> <dd>

[**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md)結構陣列的指標，其中包含屬性描述。 陣列的大小等於 **nPropDesc** 的值。 應用程式必須在完成時釋放此記憶體。

</dd> </dl>

## <a name="remarks"></a>備註

[**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)針對特定格式所傳回的 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)結構包含一些屬性設定。 **WMDM \_配置 \_ 設定結構描述** 這些設定。

屬性設定會描述指定之格式支援的所有屬性值。 單一設定中不同屬性的值彼此相容。 例如，對於音訊檔案，設定將包含有效的取樣率和有效的位元速率值，讓這些範例和位元速率的所有組合都可以在裝置上播放。

需要呼叫端才能釋放 **pPropDesc** 所使用的記憶體。 如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。

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

[**WMDM 的一種 \_ \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





