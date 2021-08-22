---
description: ID3DXMesh：： Optimize 方法-產生具有重新排列臉部和頂點的新網格，以將繪製效能優化。
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh：： Optimize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4ea03bcaaab492ec09dd24ec93c6a9c9ca393c1399b05e12096a8ba1f4f9aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493098"
---
# <a name="id3dxmeshoptimize-method"></a>ID3DXMesh：： Optimize 方法

產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。

## <a name="syntax"></a>語法


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定要執行的優化類型。 這個參數可以設定為 [**D3DXMESHOPT**](./d3dxmeshopt.md) 和 [**D3DXMESH**](./d3dxmesh.md) (的一或多個旗標的組合，除了 D3DXMESH \_ 32 位、D3DXMESH \_ IB \_ WRITEONLY 和 D3DXMESH \_ WRITEONLY) 之外。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，其會為來源網格中的每個臉部指定三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。 請參閱＜備註＞。

</dd> <dt>

*pAdjacencyOut* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

指標，指向每個臉部的三個 Dword 陣列，以指定優化網格中每個臉部的三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。

</dd> <dt>

*pFaceRemap* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

Dword 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。 如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。

</dd> <dt>

*ppVertexRemap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。 如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。

</dd> <dt>

*ppOptMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示優化的網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會產生新的網格。 執行 Optimize 之前，應用程式必須藉由呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)來產生連續的緩衝區。 鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。

這個方法與 [**ID3DXBaseMesh：： CloneMesh**](id3dxbasemesh--clonemesh.md) 方法非常類似，不同之處在于它可以在產生新的網格複製時執行優化。 輸出網格會繼承輸入網格的所有建立參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
