---
title: 'CD3DX12_HIT_GROUP_SUBOBJECT 類別 (D3dx12) '
description: 建立點擊群組狀態子物件的 helper 類別。
keywords:
- CD3DX12_HIT_GROUP_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: dd2b396e1305d2cf21cb2121aaa6a186c47d7677
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813093"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>CD3DX12_HIT_GROUP_SUBOBJECT 類別

建立點擊群組狀態子物件的 helper 類別。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>成員

`CD3DX12_HIT_GROUP_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_HIT_GROUP_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_HIT_GROUP_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetHitGroupExport(LPCWSTR)`

用於設定點擊群組名稱的函式。

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

用來設定 [D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) 列舉值的函式，指定點擊群組的類型。

`SetAnyHitShaderImport(LPCWSTR)`

可選擇性地設定與點擊群組相關聯之任何點擊著色器名稱的函式。

`SetClosestHitShaderImport(LPCWSTR)`

可選擇性地設定與點擊群組相關聯之最接近點擊的著色器名稱的函式。

`SetIntersectionShaderImport(LPCWSTR)`

可選擇性地設定與點擊群組相關聯之交集著色器選用名稱的函式。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator const D3D12_HIT_GROUP_DESC&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) 物件的參考。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
