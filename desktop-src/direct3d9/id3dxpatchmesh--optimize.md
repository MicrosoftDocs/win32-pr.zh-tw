---
description: 將修補程式網格優化以進行有效率的鑲嵌。
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh：： Optimize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946262"
---
# <a name="id3dxpatchmeshoptimize-method"></a>ID3DXPatchMesh：： Optimize 方法

將修補程式網格優化以進行有效率的鑲嵌。

## <a name="syntax"></a>語法


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

目前未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ CANNOTATTRSORT。

## <a name="remarks"></a>備註

在應用程式產生網格的相鄰資訊之後，可以將網格資料優化 (重新排列) ，以提升繪製效能。 這個方法會判斷哪些修補程式在提供的容錯) 內 (相鄰。

相鄰資訊也可用來優化鑲嵌式。 藉由呼叫 [**ID3DXPatchMesh：： tessellate**](id3dxpatchmesh--tessellate.md)，重複產生相鄰資訊一次並 tessellate。 執行的優化與實際使用的鑲嵌層級無關。 但是，如果網格頂點變更，您就必須重新產生相鄰資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
