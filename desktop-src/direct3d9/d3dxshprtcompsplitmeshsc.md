---
description: 搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: 'D3DXSHPRTCompSplitMeshSC 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386444"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>D3DXSHPRTCompSplitMeshSC 函式

搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。 呼叫 [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) 之後，可以使用此函式將網格分割成每個超級叢集的臉部/頂點群組。 每個超級叢集都包含所有包含分類于其中一個叢集中之頂點的臉部。 連接到這組臉部的所有頂點也會包含在傳回的陣列 ppVertStatus 中，指出頂點是否屬於超級叢集。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClusterIDs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

*NumVertices* 叢集識別碼 (從壓縮的緩衝區解壓縮。 ) 

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

原始網格中的頂點數目。

</dd> <dt>

*NumCs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

 (輸入參數壓縮的叢集數目。 ) 

</dd> <dt>

*pSClusterIDs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

將包含超級叢集識別碼的大小 *NumCs* 陣列。

</dd> <dt>

*NumSCs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

配置在 [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md)中的超級叢集數目。

</dd> <dt>

*pInputIB* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

網格的原始索引緩衝區。 格式取決於 *InputIBIs32Bit*。

</dd> <dt>

*InputIBIs32Bit* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，則索引緩衝區設定為32位;否則為16位。

</dd> <dt>

*NumFaces* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

原始網格 (*pInputIB* 的臉部數目是此長度的3倍。 ) 

</dd> <dt>

*ppIBData* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

將包含所產生之分割臉部的原始索引緩衝區。 由 *InputIBIs32Bit* 決定的格式。 由函數配置。

</dd> <dt>

*pIBDataLength* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

在函數中指派的 *ppIBData* 長度。

</dd> <dt>

*OutputIBIs32Bit* \[in、out\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，則配置不帶正負號的整數陣列;否則，會配置不帶正負號的簡短陣列。

</dd> <dt>

*ppFaceRemap* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

將 *ppIBData* 中的每個臉部對應至原始臉部。 長度為 \* *pIBDataLength*/3。

</dd> <dt>

*ppVertData* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

新的頂點資料結構。 *PVertDataLength* 的大小。

</dd> <dt>

*pVertDataLength* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

分割網格中的新頂點數目。 在函數中指派。

</dd> <dt>

*pSCClusterList* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

長度 *NumCs* 的陣列，可針對每個 supercluster *pSCData* (*pClusterIDs* \*) 欄位中的索引，其中包含依 supercluster 排序的群集。

</dd> <dt>

*pSCData* \[in、out\]
</dt> <dd>

類型： **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

每個超級叢集的結構。 包含 *ppIBData*、 *pSCClusterList* 和 *ppVertData* 的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
