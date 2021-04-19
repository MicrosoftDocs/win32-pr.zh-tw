---
description: 使用彈性頂點格式來複製網格 (FVF) 程式碼。
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh：： CloneMeshFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976702"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>ID3DXBaseMesh：： CloneMeshFVF 方法

使用彈性頂點格式來複製網格 (FVF) 程式碼。

## <a name="syntax"></a>語法


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。

</dd> <dt>

*FVF* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

FVF 碼的組合，指定輸出網格中頂點的頂點格式。 如需程式碼的值，請參閱 [D3DFVF](d3dfvf.md)。

</dd> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與網格相關聯的裝置物件。

</dd> <dt>

*ppCloneMesh* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示複製的網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

**ID3DXBaseMesh：： CloneMeshFVF** 是用來重新格式化及變更頂點資料版面配置。 這是藉由建立新的網格物件來完成。 例如，您可以使用它來新增不存在之法線、材質座標、色彩、權數等的空間。

[**ID3DXBaseMesh：： UpdateSemantics**](id3dxbasemesh--updatesemantics.md) 會使用不同的語義資訊來更新頂點宣告，而不會變更頂點緩衝區的版面配置。 這個方法不會修改頂點緩衝區的內容。 例如，使用它將3D 紋理座標重定為 binormal 或正切函數，反之亦然。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
