---
description: 建立 ID3DXKeyframedAnimationSet 索引鍵的框架動畫集合介面。
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: 'D3DXCreateKeyframedAnimationSet 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4fbfb31b712e1521930fa468bae315a443105f3a6bc0863fe3267f9586f874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804564"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>D3DXCreateKeyframedAnimationSet 函式

建立 [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) 索引鍵的框架動畫集合介面。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
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

*NumAnimations* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

調整規模、旋轉和轉譯 (SRT) 動畫組的數目。

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

類型： **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

[**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md)主要框架動畫集合介面指標的位址。

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

 

 
