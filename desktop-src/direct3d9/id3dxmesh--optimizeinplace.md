---
description: 產生具有重新排序臉部和頂點的網格，以將繪製效能優化。 這個方法會重新排序現有的網格。
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh：： OptimizeInplace 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0075e7a0b823f0d747859a4717a440e0c244fde76076e4b285c7d1b2a7e78d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120802"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>ID3DXMesh：： OptimizeInplace 方法

產生具有重新排序臉部和頂點的網格，以將繪製效能優化。 這個方法會重新排序現有的網格。

## <a name="syntax"></a>語法


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXMESHOPT**](./d3dxmeshopt.md) 旗標的組合，指定要執行的優化類型。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，其會為來源網格中的每個臉部指定三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。

</dd> <dt>

*pAdjacencyOut* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

指標，指向每個臉部的三個 Dword 陣列，以指定優化網格中每個臉部的三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。 如果提供給這個引數的值為 **Null**，則不會傳回相鄰資料。

</dd> <dt>

*pFaceRemap* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

Dword 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。 如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。

</dd> <dt>

*ppVertexRemap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。 如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。 如果提供給這個引數的值為 **Null**，則不會傳回頂點重新對應資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ CANNOTATTRSORT、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

執行 **ID3DXMesh：： OptimizeInplace** 之前，應用程式必須藉由呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)來產生連續的緩衝區。 鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。

> [!Note]  
> 如果網格與另一個網格共用其頂點緩衝區，則此方法將會失敗，除非在 \_ 旗標中設定了 D3DXMESHOPT IGNOREVERTS。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
