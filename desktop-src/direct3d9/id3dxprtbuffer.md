---
description: ID3DXPRTBuffer 介面是用來儲存頂點和圖元資料的資料緩衝區，以搭配預先計算 radiance 傳輸 (PRT) 方法和函式使用。
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: 'ID3DXPRTBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69f4a40055adea1440436cc54cecc5735db95bc01787cb779cc8a7d6c51b0011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120542"
---
# <a name="id3dxprtbuffer-interface"></a>ID3DXPRTBuffer 介面

ID3DXPRTBuffer 介面是用來儲存頂點和圖元資料的資料緩衝區，以搭配預先計算 radiance 傳輸 (PRT) 方法和函式使用。

## <a name="members"></a>成員

**ID3DXPRTBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXPRTBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXPRTBuffer** 介面具有這些方法。



| 方法                                                   | 描述                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | 將另一個緩衝區新增至 **ID3DXPRTBuffer** ，並將結果儲存在 **ID3DXPRTBuffer** 中。<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | 將 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件與 **ID3DXPRTBuffer** 物件建立關聯。<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | 將儲存的材質裝訂邊資料套用至 **ID3DXPRTBuffer** 材質緩衝區。<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | 從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | 從單一通道緩衝區解壓縮係數資料，並將資料加入至 [**ID3DXMesh**](id3dxmesh.md) 物件。<br/>                                                              |
| [**GetHeight**](id3dxprtbuffer--getheight.md)           | 抓取紋理的高度（以圖元為單位）。<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | 抓取記憶體中用來儲存範例的色彩通道數目。<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | 抓取記憶體中用來儲存範例的每個顏色通道的純量數目。<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | 抓取取樣 (或材質) 的頂點數目。<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | 抓取紋理的寬度（以圖元為單位）。<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | 指出緩衝區是否包含材質。<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | 鎖定某個範圍的頂點或材質範例資料，並取得緩衝區記憶體中位置的指標。<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Unassociates 具有 **ID3DXPRTBuffer** 物件的附加 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件。<br/>                                                   |
| [**調整大小**](id3dxprtbuffer--resize.md)                 | 變更緩衝區中包含的樣本數目。<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | 將緩衝區中的每個值乘以常數值。<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | 結束 [**ID3DXPRTBuffer：： LockBuffer**](id3dxprtbuffer--lockbuffer.md)所傳回之 ppData 指標的存留期。<br/>                                                              |



 

## <a name="remarks"></a>備註

**ID3DXPRTBuffer** 介面是藉由呼叫 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)或 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)函數來取得。

LPD3DXPRTBUFFER 型別定義為 **ID3DXPRTBuffer** 介面的指標。


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
