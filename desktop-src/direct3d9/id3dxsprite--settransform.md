---
description: 設定 sprite 轉換。
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'ID3DXSprite：： SetTransform 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fba7c21d0ba0e99aefc5c4d5dfd69301bb706f804e736badcbe0227d58aca81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292615"
---
# <a name="id3dxspritesettransform-method"></a>ID3DXSprite：： SetTransform 方法

設定 sprite 轉換。

## <a name="syntax"></a>語法


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTransform* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

[**D3DXMATRIX**](d3dxmatrix.md)的指標，其中包含原始世界空間中 sprite 的轉換。 您可以使用此轉換來調整、旋轉或轉換 sprite。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[轉換 (Direct3D 9) ](transforms.md)
</dt> </dl>

 

 




