---
description: Resamples 輸入 ID3DXPRTBuffer 緩衝區，並將其儲存至輸出緩衝區。 這個方法可以用來將頂點緩衝區轉換成材質緩衝區，反之亦然。 它也可以用來將單一通道緩衝區轉換成3通道緩衝區，反之亦然。
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine：： ResampleBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696804"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>ID3DXPRTEngine：： ResampleBuffer 方法

Resamples 輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區，並將其儲存至輸出緩衝區。 這個方法可以用來將頂點緩衝區轉換成材質緩衝區，反之亦然。 它也可以用來將單一通道緩衝區轉換成3通道緩衝區，反之亦然。

## <a name="syntax"></a>語法


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBufferIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區的指標。

</dd> <dt>

*pBufferOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




