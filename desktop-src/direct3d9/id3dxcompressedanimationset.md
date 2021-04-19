---
description: 應用程式會使用這個介面的方法，來執行以壓縮資料格式儲存的主要畫面格動畫集合。
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: 'ID3DXCompressedAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993885"
---
# <a name="id3dxcompressedanimationset-interface"></a>ID3DXCompressedAnimationSet 介面

應用程式會使用這個介面的方法，來執行以壓縮資料格式儲存的主要畫面格動畫集合。

## <a name="members"></a>成員

**ID3DXCompressedAnimationSet** 介面繼承自 [**ID3DXAnimationSet**](id3dxanimationset.md)。 **ID3DXCompressedAnimationSet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXCompressedAnimationSet** 介面具有這些方法。



| 方法                                                                                  | 描述                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetCallbackKeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | 使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。<br/>   |
| [**GetCompressedData**](id3dxcompressedanimationset--getcompresseddata.md)             | 取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。<br/> |
| [**GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | 取得動畫集中的回呼索引鍵數目。<br/>                |
| [**GetPlaybackType**](id3dxcompressedanimationset--getplaybacktype.md)                 | 取得動畫集合播放迴圈的型別。<br/>                     |
| [**GetSourceTicksPerSecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | 取得每秒發生的動畫主要畫面格刻度數目。<br/>   |



 

## <a name="remarks"></a>備註

使用 [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md)建立壓縮格式的主要畫面格動畫。

LPD3DXCOMPRESSEDANIMATIONSET 型別定義為這個介面的指標。


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




