---
description: 使用與裝置內容相關聯的字型，建立包含指定文字的網格。
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: 'D3DXCreateText 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9db7cc6fa89f8f102cabccdebd14852a50f60576b6135ae52e4cc9fada494812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732292"
---
# <a name="d3dxcreatetext-function"></a>D3DXCreateText 函式

使用與裝置內容相關聯的字型，建立包含指定文字的網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

建立網格之裝置的指標。

</dd> <dt>

*hDC* \[在\]
</dt> <dd>

類型： **HDC**

裝置內容，包含輸出的字型。 裝置內容所選取的字型必須是 TrueType 字型。

</dd> <dt>

*pText* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

字串的指標，指定要產生的文字。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*偏差* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

TrueType 字型大綱的最大 chordal 偏差。

</dd> <dt>

*延伸* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

要以負 z 方向凸出的文字數量。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

傳回之網格的指標。

</dd> <dt>

*ppAdjacency* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含相鄰資訊之緩衝區的指標。 可能是 **Null**。

</dd> <dt>

*pGlyphMetrics* \[擴展\]
</dt> <dd>

類型： **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

[**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)結構陣列的指標，其中包含圖像度量資料。 每個元素都包含字串中相對應圖像的位置和方向的相關資訊。 陣列中的元素數目應等於字串中的字元數。 請注意，每個結構中的原點都不是相對於整個字串，而是相對於該字元儲存格。 若要計算整個周框方塊，請在往返字串時加入每個圖像的遞增。 如果您不在意圖像大小，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextW。 否則，函式呼叫會解析為 D3DXCreateTextA，因為正在使用 ANSI 字串。

此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9shape。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[圖形繪圖函數](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
