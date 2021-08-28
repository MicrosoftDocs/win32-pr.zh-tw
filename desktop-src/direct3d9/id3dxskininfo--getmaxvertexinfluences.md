---
description: 取得網格中任何頂點的最大影響數目。
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'ID3DXSkinInfo：： GetMaxVertexInfluences 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cd33155ba5b306fc24e345f535a083c78031da243b291f2c36c5894561e270d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095708"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a>ID3DXSkinInfo：： GetMaxVertexInfluences 方法

取得網格中任何頂點的最大影響數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*maxVertexInfluences* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

頂點影響最大值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
