---
description: 建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。 此函式應該用來建立每個圖元的緩衝區。
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: 'D3DXCreatePRTBufferTex 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44bddffded189ce747491a4c3d9c08195c9817cfb1a578136f9c025231760cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299263"
---
# <a name="d3dxcreateprtbuffertex-function"></a>D3DXCreatePRTBufferTex 函式

建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。 此函式應該用來建立每個圖元的緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質的寬度（以圖元為單位）。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

紋理的高度（以圖元為單位）。

</dd> <dt>

*NumCoeffs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個樣本位置的係數數目。 使用球面調和 (SH) PRT 時，係數的數目應該是 Order ²，其中 Order 是 SH 評估的順序。 順序必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估的程度是順序-1。

</dd> <dt>

*NumChannels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要在網格中設定的色彩通道數目。 設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。

</dd> <dt>

*ppBuffer* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

所建立之 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

建立緩衝區時，所有值都會初始化為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
