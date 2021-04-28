---
description: D3DXSHPRTCompSuperCluster 函式-搭配預先計算 radiance 傳輸 (PRT) 模擬器的頂點版本壓縮結果使用。
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: 'D3DXSHPRTCompSuperCluster 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117856"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster 函式

搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。 產生 "superclusters"，這是可在相同繪製呼叫中繪製的群集群組。 將過度繪製降至最低的貪婪演算法會用來將叢集分組。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClusterIDs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

NumVerts 叢集識別碼的指標 (從壓縮的緩衝區解壓縮。 ) 

</dd> <dt>

*pScene* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

表示傳遞給模擬器之複合場景的網格指標。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> <dt>

*MaxNumClusters* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個超級叢集配置的最大叢集數。

</dd> <dt>

*NumClusters* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

在模擬器中計算的群集數目。

</dd> <dt>

*pSClusterIDs* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

長度 *NumClusters* 陣列的指標。 包含指派給對應叢集之超級叢集的索引。

</dd> <dt>

*pNumSCs* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

配置的超級叢集數目。

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

 

 
