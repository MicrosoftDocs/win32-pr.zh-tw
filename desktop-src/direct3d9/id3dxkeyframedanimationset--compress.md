---
description: 將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet：：壓縮方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d444ffde525677715f64bd9641cc8fb3cf9513e2c8805a6be28b280aaa12e015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802385"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>ID3DXKeyframedAnimationSet：：壓縮方法

將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。

## <a name="syntax"></a>語法


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

其中一個 [**D3DXCOMPRESSION \_ 旗標**](./d3dxcompression-flags.md) 值，這些值會定義用於儲存壓縮動畫集資料的壓縮模式。 D3DXCOMPRESS \_ 預設值是目前唯一支援的值。

</dd> <dt>

*Lossiness* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

所需的壓縮遺失比例，範圍介於0到1之間。

</dd> <dt>

*pHierarchy* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)**

[**D3DXFRAME**](d3dxframe.md)轉換框架階層的指標。 可以是 **Null**。

</dd> <dt>

*ppCompressedData* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

指向 [**ID3DXBuffer**](id3dxbuffer.md) 壓縮動畫集之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
