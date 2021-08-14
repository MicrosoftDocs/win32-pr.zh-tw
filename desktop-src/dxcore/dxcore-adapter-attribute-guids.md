---
title: DXCore 介面卡屬性 GUID
description: 下列 adapter 屬性 Guid 是在中宣告 `dxcore_interface.h` ，而且會與 [IDXCoreAdapterFactory：： CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) 和 [IDXCoreAdapter：： IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) 方法搭配使用。
keywords:
- DXCore，adapter 屬性，Guid
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279658"
---
# <a name="dxcore-adapter-attribute-guids"></a>DXCore 介面卡屬性 GUID

下列 adapter 屬性 Guid 是在中宣告 `dxcore_interface.h` ，而且會與 [IDXCoreAdapterFactory：： CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) 和 [IDXCoreAdapter：： IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) 方法搭配使用。 針對任何指定的介面卡，可能會套用一或多個屬性。

| GUID | 值 |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. 指定支援與 [Direct3D 11](/windows/win32/direct3d11) 圖形 api 搭配使用的介面卡。 不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。 | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. 指定支援與 [Direct3D 12](/windows/win32/direct3d12) 圖形 api 搭配使用的介面卡。 不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。 | 0x0c9ece4d、0x2f6e、0x4f01、0x8c、0x96、0xe8、0x9e、0x33、0x1b、0x47、0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. 指定支援與 [Direct3D 12 核心](../direct3d12/core-feature-levels.md) 計算 api 搭配使用的介面卡。 不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。 | 0x248e2800、0xa793、0x4724、0xab、0xaa、0x23、0xa6<、0xde、0x1b、0xe0、0x90 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | dxcore_interface。h |

## <a name="see-also"></a>另請參閱

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [DXCore 參考](./dxcore-reference.md)
* [使用 DXCore 來列舉介面卡](./dxcore-enum-adapters.md)
* [Direct3D 12 圖形](../direct3d12/direct3d-12-graphics.md)
