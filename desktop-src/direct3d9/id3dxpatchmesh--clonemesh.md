---
description: 使用指定的頂點宣告來建立新的 patch 網狀。
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh：： CloneMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322707"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>ID3DXPatchMesh：： CloneMesh 方法

使用指定的頂點宣告來建立新的 patch 網狀。

## <a name="syntax"></a>語法


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，這些旗標會指定網格的建立選項。

</dd> <dt>

*pDecl* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，可指定輸出網格中頂點的頂點格式。

</dd> <dt>

*pMesh* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示複製的網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

**CloneMesh** 會將頂點緩衝區轉換成新的頂點宣告。 對原始網格而言，頂點宣告中的專案會設定為0。 如果目前的網格具有連續的，則新的網格也會有連續的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
