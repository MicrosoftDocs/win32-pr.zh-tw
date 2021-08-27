---
title: 'CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT 類別 (D3dx12) '
description: 用來建立具有旗標之 raytracing 管線設定狀態子物件的 helper 類別。
keywords:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: fc2049f6a800891e165f57099ad7f9b0bbaba263
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812185"
---
# <a name="cd3dx12_raytracing_pipeline_config1_subobject-class"></a>CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT 類別

用來建立具有旗標之 raytracing 管線設定狀態子物件的 helper 類別。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
{
public:
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxTraceRecursionDepth, D3D12_RAYTRACING_PIPELINE_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_PIPELINE_CONFIG1& () const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`Config(UINT, D3D12_RAYTRACING_PIPELINE_FLAGS)`

用來設定 raytracing 管線的光線遞迴限制的函式。 也會採用 [D3D12_RAYTRACING_PIPELINE_FLAGS](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_flags) 參數。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_RAYTRACING_PIPELINE_CONFIG&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) 物件的參考。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
