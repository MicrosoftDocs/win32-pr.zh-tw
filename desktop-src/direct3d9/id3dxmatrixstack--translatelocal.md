---
description: ID3DXMATRIXStack：： TranslateLocal 方法 (D3dx9math .h) -決定由給定因數 (x、y 和 z) 和目前矩陣所決定的計算轉譯矩陣的乘積。
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'ID3DXMATRIXStack：： TranslateLocal 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9badd4b01d1245247766c750e2a2ea1f266d9e1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107366"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>ID3DXMATRIXStack：： TranslateLocal 方法 (D3dx9math .h) 

決定由給定因數決定的計算轉譯矩陣的乘積 (x、y 和 z) 和目前的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT TranslateLocal(
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

X 方向的平移因數。

</dd> <dt>

*y* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

Y 方向的平移因數。

</dd> <dt>

*z* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

Z 方向的平移因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

這個方法會將目前的矩陣與計算的轉譯矩陣相乘 (轉換是關於物件) 的本機來源。


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
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

[**ID3DXMATRIXStack：：轉譯**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
