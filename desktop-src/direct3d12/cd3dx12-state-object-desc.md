---
title: 'CD3DX12_STATE_OBJECT_DESC 類別 (D3dx12) '
description: D3DX12 狀態物件建立協助程式的 central 類別，這是用來從任意一組子物件建立狀態物件的 helper 類別。
keywords:
- CD3DX12_STATE_OBJECT_DESC 類別
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813072"
---
# <a name="cd3dx12_state_object_desc-class"></a>CD3DX12_STATE_OBJECT_DESC 類別

D3DX12 狀態物件建立協助程式的 central 類別，這是用來從任意一組子物件建立狀態物件的 helper 類別。

## <a name="syntax"></a>語法

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>成員

`CD3DX12_STATE_OBJECT_DESC`

預設建構函式。 建立 **CD3DX12_STATE_OBJECT_DESC** 預設初始化的新實例。

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

建立新實例之 **CD3DX12_STATE_OBJECT_DESC** 的函式，其會以對應至傳遞給它的 [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) 值的 subjobject 類型來初始化。

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

方法，將 subjobject 類型設定為傳遞給它的 [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) 的值。

`operator const D3D12_STATE_OBJECT_DESC&`

轉換運算子，會傳回描述狀態物件之常數 [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) 物件的參考。

`operator const D3D12_STATE_OBJECT_DESC*`

轉換運算子，會傳回描述狀態物件之常數 [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) 物件的指標。

`CreateSubobject`

建立 sububject helper 的函式範本，其存留期是由這個類別所擁有。

範本參數 *T* 會指定 subjobject helper 類型，例如 [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md)。

## <a name="remarks"></a>備註

若要使用 D3DX12 狀態物件建立協助程式，請先將 **CD3DX12_STATE_OBJECT_DESC** 物件具現化，然後呼叫其 **CreateSubobject** 函數來建立子物件。 子物件協助程式各自具有該子物件專用的方法來設定其內容。

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

或者，您也可以明確地具現化物件協助程式，例如透過本機變數傳遞狀態物件 desc (應指向該物件的) 至 helper 函式 (或呼叫 `mySubobjectHelper.AddToStateObject(Collection1)`) 。

在這個替代案例中，您需要讓子物件保持運作，只要與其相關聯的狀態物件處於作用中狀態，否則它的指標參考將會過時。

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
