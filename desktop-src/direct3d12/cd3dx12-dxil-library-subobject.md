---
title: 'CD3DX12_DXIL_LIBRARY_SUBOBJECT 類別 (D3dx12) '
description: 用來建立 DXIL 程式庫狀態子物件的 helper 類別。
keywords:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 33ec22dd722469ce131bc58d5aca83f0aed4edf0
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812549"
---
# <a name="cd3dx12_dxil_library_subobject-class"></a>CD3DX12_DXIL_LIBRARY_SUBOBJECT 類別

用來建立 DXIL 程式庫狀態子物件的 helper 類別。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_DXIL_LIBRARY_SUBOBJECT
{
    CD3DX12_DXIL_LIBRARY_SUBOBJECT() noexcept;
    CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    void SetDXILLibrary(const D3D12_SHADER_BYTECODE* pCode) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_LIBRARY_DESC& () const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_DXIL_LIBRARY_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_DXIL_LIBRARY_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_DXIL_LIBRARY_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetDXILLibrary(const D3D12_SHADER_BYTECODE*)`

以指標形式將 DXIL 程式庫設定為參數傳遞 [D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 的函式。

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

定義從子物件匯出的符號。 接受 [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) 作為選擇性參數。

`DefineExports(LPCWSTR(&)[N]);`

定義從子物件匯出之 *N* 符號的陣列。 範本參數 *N* 指定陣列中的元素數目。

`DefineExports(const LPCWSTR*, UINT)`

定義從子物件匯出的符號陣列。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_DXIL_LIBRARY](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_DXIL_LIBRARY_DESC&`

轉換運算子，會傳回描述狀態物件之常數 [**D3D12_DXIL_LIBRARY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_library_desc) 物件的參考。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
