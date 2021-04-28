---
description: ID3DXMATRIXStack：： Scale 方法 (D3dx9math) -調整目前有關全局座標原點的矩陣。
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'ID3DXMATRIXStack：： Scale 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093366"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a>ID3DXMATRIXStack：： Scale 方法 (D3dx9math .h) 

調整目前的矩陣與全球座標原點的大小。

## <a name="syntax"></a>語法


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* \[ 于\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

X 方向的縮放比例元件。

</dd> <dt>

*y* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

Y 方向的縮放比例元件。

</dd> <dt>

*z* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

Z 方向的縮放比例元件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

這個方法會將目前的矩陣與計算的刻度矩陣向右相乘。 轉換與目前的世界原點有關。


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::ScaleLocal**](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
