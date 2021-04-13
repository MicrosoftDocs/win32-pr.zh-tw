---
description: 載入至記憶體中已壓縮的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: 'D3DXLoadPRTCompBufferFromFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323303"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>D3DXLoadPRTCompBufferFromFile 函式

載入至記憶體中已壓縮的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要從中載入壓縮緩衝區資料的檔案名。

</dd> <dt>

*ppBuffer* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

輸出 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXLoadPRTCompBufferFromFileW。 否則，函式呼叫會解析為 D3DXLoadPRTCompBufferFromFileA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
