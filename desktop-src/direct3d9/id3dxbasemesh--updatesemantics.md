---
description: 這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。 只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh：： UpdateSemantics 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035365"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>ID3DXBaseMesh：： UpdateSemantics 方法

這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。 只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

宣告 \[in、out\]
</dt> <dd>

類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述網格頂點的頂點格式。 此宣告子陣列的上限是 [**\_ FVF \_ DECL \_ SIZE 的最大**](./max-fvf-decl-size.md)值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

[**ID3DXBaseMesh：： CloneMesh**](id3dxbasemesh--clonemesh.md) 是用來重新格式化及變更頂點資料版面配置。 例如，您可以使用它來新增不存在之法線、材質座標、色彩、權數等的空間。

**ID3DXBaseMesh：： UpdateSemantics** 是使用不同的語義資訊來更新頂點宣告的方法，而不需要變更頂點緩衝區的版面配置。 例如，使用它將3D 紋理座標重定為 binormal 或正切函數，反之亦然。

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

 

 
