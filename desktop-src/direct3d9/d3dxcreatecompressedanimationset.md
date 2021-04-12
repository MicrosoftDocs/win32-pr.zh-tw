---
description: 建立 ID3DXCompressedAnimationSet 索引鍵框架動畫集介面，以壓縮格式儲存主要畫面格資料。
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: 'D3DXCreateCompressedAnimationSet 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946126"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>D3DXCreateCompressedAnimationSet 函式

建立 [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) 索引鍵框架動畫集介面，以壓縮格式儲存主要畫面格資料。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

動畫集合名稱的指標。

</dd> <dt>

*TicksPerSecond* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

每秒經過的主要畫面格刻度數目。

</dd> <dt>

*播放* \[在\]
</dt> <dd>

類型： **[ **D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)**

動畫集合播放迴圈的型別。 請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。

</dd> <dt>

*pCompressedData* \[在\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

[**ID3DXBuffer**](id3dxbuffer.md)緩衝區的指標，此緩衝區會將動畫設定為壓縮的資料。

</dd> <dt>

*NumCallbackKeys* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

回呼金鑰數目。

</dd> <dt>

*pCallKeys* \[在\]
</dt> <dd>

類型： **Const [**LPD3DXKEY \_ 回呼**](d3dxkey-callback.md) \***

儲存使用者回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構指標。

</dd> <dt>

*ppAnimationSet* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)介面的指標位址，此介面會以壓縮格式儲存主要框架動畫設定的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
