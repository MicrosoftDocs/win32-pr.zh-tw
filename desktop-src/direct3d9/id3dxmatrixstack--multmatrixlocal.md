---
description: 決定給定矩陣和目前矩陣的乘積。
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979871"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3dx9math .h) 

決定給定矩陣和目前矩陣的乘積。

## <a name="syntax"></a>語法


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMat* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

要乘以目前矩陣的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會將指定的矩陣靠左乘以目前的矩陣 (轉換是關於物件) 的本機來源。


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為指定矩陣和目前矩陣的乘積。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




