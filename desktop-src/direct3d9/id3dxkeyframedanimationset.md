---
description: 應用程式會使用這個介面的方法來執行主要畫面格動畫集。
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: 'ID3DXKeyframedAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001793"
---
# <a name="id3dxkeyframedanimationset-interface"></a>ID3DXKeyframedAnimationSet 介面

應用程式會使用這個介面的方法來執行主要畫面格動畫集。

## <a name="members"></a>成員

**ID3DXKeyframedAnimationSet** 介面繼承自 [**ID3DXAnimationSet**](id3dxanimationset.md)。 **ID3DXKeyframedAnimationSet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXKeyframedAnimationSet** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**壓縮**](id3dxkeyframedanimationset--compress.md)                                 | 將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。<br/> |
| [**GetCallbackKey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | 取得動畫集中特定回呼的相關資訊。<br/>                                                                        |
| [**GetCallbackKeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | 使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。<br/>                                                                     |
| [**GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | 取得動畫集中的回呼索引鍵數目。<br/>                                                                                  |
| [**GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | 取得指定主要畫面格動畫中的旋轉索引鍵數目。<br/>                                                                  |
| [**GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | 取得指定主要畫面格動畫中的小數位數索引鍵數目。<br/>                                                                     |
| [**GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | 取得指定主要畫面格動畫中的轉譯鍵數目。<br/>                                                               |
| [**GetPlaybackType**](id3dxkeyframedanimationset--getplaybacktype.md)                   | 取得動畫集合播放迴圈的型別。<br/>                                                                                       |
| [**GetRotationKey**](id3dxkeyframedanimationset--getrotationkey.md)                     | 取得動畫集中特定主要畫面格的旋轉資訊。<br/>                                                                 |
| [**GetRotationKeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | 使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。<br/>                                                                   |
| [**GetScaleKey**](id3dxkeyframedanimationset--getscalekey.md)                           | 取得動畫集中特定主要畫面格的縮放資訊。<br/>                                                                    |
| [**GetScaleKeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | 使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。<br/>                                                                        |
| [**GetSourceTicksPerSecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | 取得每秒發生的動畫主要畫面格刻度數目。<br/>                                                                     |
| [**GetTranslationKey**](id3dxkeyframedanimationset--gettranslationkey.md)               | 取得動畫集中特定主要畫面格的翻譯資訊。<br/>                                                              |
| [**GetTranslationKeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | 使用主要畫面格動畫所用的平移按鍵資料來填滿陣列。<br/>                                                                |
| [**RegisterAnimationSRTKeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | 註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。<br/>                                                        |
| [**SetCallbackKey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | 設定動畫集中特定回呼的相關資訊。<br/>                                                                        |
| [**SetRotationKey**](id3dxkeyframedanimationset--setrotationkey.md)                     | 設定動畫集中特定主要畫面格的旋轉資訊。<br/>                                                                 |
| [**SetScaleKey**](id3dxkeyframedanimationset--setscalekey.md)                           | 設定動畫集中特定主要畫面格的縮放資訊。<br/>                                                                    |
| [**SetTranslationKey**](id3dxkeyframedanimationset--settranslationkey.md)               | 設定動畫集中特定主要畫面格的翻譯資訊。<br/>                                                              |
| [**UnregisterAnimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | 從動畫集合中移除動畫資料。<br/>                                                                                       |
| [**UnregisterRotationKey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | 移除位於指定主要畫面格的旋轉資料。<br/>                                                                                   |
| [**UnregisterScaleKey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | 移除位於指定主要畫面格的尺規資料。<br/>                                                                                      |
| [**UnregisterTranslationKey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | 移除位於指定主要畫面格的翻譯資料。<br/>                                                                                |



 

## <a name="remarks"></a>備註

使用 [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md)建立 keyframed 動畫集。

LPD3DXKEYFRAMEDANIMATIONSET 型別定義為這個介面的指標。


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
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

 

 




