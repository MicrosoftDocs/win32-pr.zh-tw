---
description: 使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine：:D rawTransform 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000623"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine：:D rawTransform 方法

使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。

## <a name="syntax"></a>語法


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVertexList* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

構成線條的頂點陣列。 請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。

</dd> <dt>

*dwVertexListCount* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點清單中的頂點數目。

</dd> <dt>

*pTransform* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

調整、旋轉和轉譯 (SRT) 矩陣以轉換點。 請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。 如果此矩陣是投射矩陣，則會以觀點正確的 stippling 模式繪製任何 stippled 線。 或者，您可以轉換頂點並使用 [**ID3DXLine：:D raw**](id3dxline--draw.md) ，以 nonperspective 正確的 stipple 模式繪製行。

</dd> <dt>

*色彩* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

線條的色彩。 請參閱 [**D3DCOLOR**](d3dcolor.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
