---
description: 根據目前的矩陣，將軟體外觀套用至目標頂點。
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo：： UpdateSkinnedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729450"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>ID3DXSkinInfo：： UpdateSkinnedMesh 方法

根據目前的矩陣，將軟體外觀套用至目標頂點。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBoneTransforms* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

骨骼轉換矩陣。

</dd> <dt>

*pBoneInvTransposeTransforms* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

骨骼轉換矩陣的反向變換。

</dd> <dt>

*pVerticesSrc* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含來源頂點的緩衝區指標。

</dd> <dt>

*pVerticesDst* \[在\]
</dt> <dd>

類型： **[ **PVOID**](../winprog/windows-data-types.md)**

包含目的地頂點之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

當用來處理具有兩個位置專案的面板頂點時，此方法會將第二個位置元素與骨骼的反函數（而非骨骼本身）搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
