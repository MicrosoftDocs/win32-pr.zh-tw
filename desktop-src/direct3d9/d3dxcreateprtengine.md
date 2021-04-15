---
description: 建立 ID3DXPRTEngine 物件，該物件可以有效率地產生3D 場景的預先計算 radiance 傳輸 (PRT) 模擬。
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: 'D3DXCreatePRTEngine 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514612"
---
# <a name="d3dxcreateprtengine-function"></a>D3DXCreatePRTEngine 函式

建立 [**ID3DXPRTEngine**](id3dxprtengine.md) 物件，該物件可以有效率地產生3d 場景的預先計算 radiance 傳輸 (PRT) 模擬。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標，該物件會將3d 場景模型。 這個網格必須有一個屬性工作表，其中頂點位於唯一的屬性中。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

選擇性的指標，指向每個臉部的三個 Dword 陣列，以填滿連續的臉部索引。 此陣列中的位元組數目必須至少為 ( (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD) ) 。 可能是 **Null**。

</dd> <dt>

*ExtractUVs* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，則會使用紋理來儲存 ALBEDOS 或 PRT 向量。

</dd> <dt>

*pBlockerMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

封鎖3D 場景之選擇性 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。 可能是 **Null**。

</dd> <dt>

*ppEngine* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

輸出 [**ID3DXPRTEngine**](id3dxprtengine.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) 將多個網格合併為單一網格介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
