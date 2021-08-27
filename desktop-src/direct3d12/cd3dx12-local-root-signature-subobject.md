---
title: 'CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT 類別 (D3dx12) '
description: 用來建立本機根簽章狀態 suboject 的 helper 類別。
keywords:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT 類別
topic_type:
- apiref
api_name:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 85aee6a1697bdbcf01a741437da076f705731947
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813070"
---
# <a name="cd3dx12_local_root_signature_subobject-class"></a>CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT 類別

用來建立本機根簽章狀態 suboject 的 helper 類別。

如需有關 D3DX12 狀態物件建立協助程式的詳細資訊，請參閱 [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
{
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT() noexcept;
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetRootSignature(ID3D12RootSignature* pRootSig) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator ID3D12RootSignature* () const noexcept { return D3DX12_COM_PTR_GET(m_pRootSig); }
};
```

## <a name="members"></a>成員

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT`

預設建構函式。 建立 **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT** 預設初始化的新實例。

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

建立新實例的函式， **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT** 以 [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) 物件的內容初始化。

`SetRootSignature(ID3D12RootSignature*)`

用來將根簽章以指標形式設定為參數傳遞 [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) 的函式。

`Type`

抓取子物件的類型，由 [D3D12_STATE_SUBOBJECT_TYPE_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) 常數表示。

`operator const D3D12_STATE_SUBOBJECT&`

轉換運算子，會傳回描述狀態物件之常數 [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) 物件的參考。

`operator ID3D12RootSignature*`

轉換運算子，傳回 [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)指標形式的根簽章。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
