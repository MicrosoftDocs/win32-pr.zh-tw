---
description: 使用宣告子複製網格。
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh：： CloneMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fec8b0881cdef43051afcb06d63ec20284cb116299912ce0acf7ac4c54a0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521861"
---
# <a name="id3dxbasemeshclonemesh-method"></a>ID3DXBaseMesh：： CloneMesh 方法

使用宣告子複製網格。

## <a name="syntax"></a>語法


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。

</dd> <dt>

*pDeclaration* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，可指定輸出網格中頂點的頂點格式。

</dd> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與網格相關聯的裝置物件。

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

**ID3DXBaseMesh：： CloneMesh** 是用來重新格式化及變更頂點資料版面配置。 這是藉由建立新的網格物件來完成。 例如，您可以使用它來為不存在的法線、材質座標、色彩、加權等新增空間。

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

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
