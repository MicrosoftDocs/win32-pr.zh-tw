---
title: 'D3D12DecomposeSubresource 函式 (D3dx12) '
description: 輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource 函式
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986495"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource 函式

輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。

## <a name="syntax"></a>語法


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*子資源* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Subresource 的索引。

</dd> <dt>

*MipLevels* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Subresource 中 mipmap 層級的最大數目。

</dd> <dt>

[陣列大小] 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

陣列中的項目數。

</dd> <dt>

*MipSlice* \[out、ref\]
</dt> <dd>

類型： **T**

輸出對應至指定之 subresource 索引的 mip 配量。

</dd> <dt>

*ArraySlice* \[out、ref\]
</dt> <dd>

類型： **U**

輸出對應至指定之 subresource 索引的陣列配量。

</dd> <dt>

*PlaneSlice* \[out、ref\]
</dt> <dd>

類型： **V**

輸出對應至指定之 subresource 索引的平面配量。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此函數會決定哪一個 mip 配量、陣列配量和平面配量對應到指定的 subresource 索引。 這是很實用的公用程式，但它是 c + + 特有的。

此函式的宣告方式如下： **T**、 **U** 和 **V** 類型的 c + + 範本化參數：


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)

[子資源](subresources.md)
