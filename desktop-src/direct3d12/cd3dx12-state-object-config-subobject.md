---
title: 'CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT 類別 (D3dx12) '
description: Helper 類別，用於建立子物件，以定義狀態物件的一般屬性。
keywords:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 294dda04f9550e437f91f6f5595206a4113a975ee182ac900b6c4804b3100fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346556"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT 類別

Helper 類別，用於建立子物件，以定義狀態物件的一般屬性。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

函數，可透過 [D3D12_STATE_OBJECT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) 物件指定狀態物件的需求。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_STATE_OBJECT_CONFIG&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) 物件的參考。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
