---
description: 將另一個緩衝區新增至 ID3DXPRTBuffer，並將結果儲存在 ID3DXPRTBuffer 中。
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer：： AddBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989232"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>ID3DXPRTBuffer：： AddBuffer 方法

將另一個緩衝區新增至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) ，並將結果儲存在 **ID3DXPRTBuffer** 中。

## <a name="syntax"></a>語法


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBuffer* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

緩衝區的指標，其中包含要加入至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區之個別成員的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。

## <a name="remarks"></a>備註

pBuffer 和 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 必須有相同數目的樣本、係數和色彩通道;否則，方法將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




