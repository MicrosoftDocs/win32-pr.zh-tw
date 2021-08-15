---
title: 'CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT 類別 (D3dx12) '
description: 用來建立子物件與匯出關聯狀態子物件的 helper 類別。
keywords:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 07fc8ba911e1f16c6cec96752b658b1578d998bd0d9a469016fb8506f3dbc85d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132294"
---
# <a name="cd3dx12_subobject_to_exports_association_subobject-class"></a>CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT 類別

用來建立子物件與匯出關聯狀態子物件的 helper 類別。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
{
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT() noexcept;
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT& SubobjectToAssociate) noexcept;
    void AddExport(LPCWSTR Export);
    template<size_t N> void AddExports(LPCWSTR(&Exports)[N]);
    void AddExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION& () const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT&)`

用來設定子物件的函式，以做為參數傳遞的 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 形式產生關聯。

`AddExport(LPCWSTR)`

新增要關聯的匯出。

`AddExports(LPCWSTR(&)[N]);`

新增要關聯的匯出陣列。 範本參數 *N* 指定陣列中的元素數目。

`AddExports(const LPCWSTR*, UINT)`

定義要關聯的 *N* 個匯出的陣列。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association) 物件的參考。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
