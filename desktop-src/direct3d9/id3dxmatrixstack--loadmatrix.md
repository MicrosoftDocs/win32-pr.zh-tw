---
description: ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) -將指定的矩陣載入至目前的矩陣。
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d34a8feff249471363d1b22f94bcd71128e512ab4bb9d506a99c4d2741020bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095888"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) 

將指定的矩陣載入至目前的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMat* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

載入至目前矩陣的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

請注意，這個方法不會將專案新增至堆疊。相反地，它會將目前的矩陣取代為提供的矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




