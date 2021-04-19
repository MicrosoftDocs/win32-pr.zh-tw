---
description: 在螢幕空間中繪製帶狀線。 輸入的格式為數組，可定義 D3DXVECTOR2) 在行條紋 (的點。
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: 'ID3DXLine：:D 原始方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975707"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine：:D 原始方法

在螢幕空間中繪製帶狀線。 輸入的格式為數組，可定義 [**D3DXVECTOR2**](d3dxvector2.md)) 在行條紋 (的點。

## <a name="syntax"></a>語法


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVertexList* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

構成線條的頂點陣列。 請參閱 [**D3DXVECTOR2**](d3dxvector2.md)。

</dd> <dt>

*dwVertexListCount* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點清單中的頂點數目。

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

 

 
