---
description: 載入至記憶體中的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: 'D3DXLoadPRTBufferFromFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322667"
---
# <a name="d3dxloadprtbufferfromfile-function"></a>D3DXLoadPRTBufferFromFile 函式

載入至記憶體中的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要從中載入緩衝區資料的檔案名。

</dd> <dt>

*ppBuffer* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXLoadPRTBufferFromFileW。 否則，函式呼叫會解析為 D3DXLoadPRTBufferFromFileA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
