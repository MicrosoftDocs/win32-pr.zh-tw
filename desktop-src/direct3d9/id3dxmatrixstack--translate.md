---
description: ID3DXMATRIXStack：：：：轉譯方法 (D3dx9math) -決定目前矩陣的乘積，以及由指定因數 (x、y 和 z) 所決定的計算轉譯矩陣。
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'ID3DXMATRIXStack：：轉譯方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093336"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a>ID3DXMATRIXStack：：轉譯方法 (D3dx9math .h) 

決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT Translate(
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

這個方法會將目前的矩陣與計算的轉譯矩陣以右相乘 (轉換與目前的世界原點) 有關。


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
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

[**ID3DXMATRIXStack::TranslateLocal**](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
