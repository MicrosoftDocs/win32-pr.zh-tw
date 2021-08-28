---
title: 'CD3DX12_NODE_MASK_SUBOBJECT 類別 (D3dx12) '
description: Helper 類別，用於建立狀態子物件，以識別要套用狀態物件的 GPU 節點。
keywords:
- CD3DX12_NODE_MASK_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_NODE_MASK_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: bfa1c5ce1facb946b060bf7501c09c6c13cfca13
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812908"
---
# <a name="cd3dx12_node_mask_subobject-class"></a>CD3DX12_NODE_MASK_SUBOBJECT 類別

Helper 類別，用於建立狀態子物件，以識別要套用狀態物件的 GPU 節點。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_NODE_MASK_SUBOBJECT
{
    CD3DX12_NODE_MASK_SUBOBJECT() noexcept;
    CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetNodeMask(UINT NodeMask) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_NODE_MASK& () const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_NODE_MASK_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_NODE_MASK_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_NODE_MASK_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetNodeMask(UINT)`

用於設定節點遮罩的函式。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_NODE_MASK&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_NODE_MASK](/windows/win32/api/d3d12/ns-d3d12-d3d12_node_mask) 物件的參考。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
