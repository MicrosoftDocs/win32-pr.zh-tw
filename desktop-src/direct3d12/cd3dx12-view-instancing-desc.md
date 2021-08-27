---
title: 'CD3DX12_VIEW_INSTANCING_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) 結構。
keywords:
- CD3DX12_VIEW_INSTANCING_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813254"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>CD3DX12_VIEW_INSTANCING_DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構。

## <a name="syntax"></a>語法

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_VIEW_INSTANCING_DESC`

預設建構函式。 建立新的、未初始化的 **CD3DX12_VIEW_INSTANCING_DESC** 實例。

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

建立新實例的函式， **CD3DX12_VIEW_INSTANCING_DESC** 以 [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構的內容初始化。

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

建立新實例的函式， **CD3DX12_VIEW_INSTANCING_DESC** 以這些值初始化。

|資料成員|值|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Flags|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

建立新實例的函式， **CD3DX12_VIEW_INSTANCING_DESC** 以傳遞給它的參數初始化。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
