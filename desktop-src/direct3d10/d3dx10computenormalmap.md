---
description: D3DX10ComputeNormalMap 函式-將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: 'D3DX10ComputeNormalMap 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b719e1b40c3e8cd04ca0750e69c68bbd4a0a59394c3334818f091900606311af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634778"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap 函式

將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

ID3D10Texture2D 介面的指標，代表來源的高度地圖材質。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

\_控制正常對應產生的一或多個 D3DX NORMALMAP 旗標。

</dd> <dt>

*頻道* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

一個 D3DX \_ 通道旗標，指定高度資訊的來源。

</dd> <dt>

*振幅* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

常數值乘數，可增加 (或減少標準對應中的值) 。 較高的值通常會使凹凸變得更明顯，較低的值通常會讓顯示的偏低。

</dd> <dt>

*pDestTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

ID3D10Texture2D 介面的指標，表示目的地材質。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會使用核心大小為3x3 的中央差異來計算正常。 目的地中的 RGB 通道包含一般 (x、y、z) 元件的偏誤。 中央差異分母會硬式編碼為2.0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
