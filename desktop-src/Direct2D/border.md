---
title: 框線效果
description: 使用框線效果，從邊緣延伸影像。
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- 框線效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce125a96730ee59f63b18cfd1a08abd2432af6f3fdc6b5f06cfc2e9272a7a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928986"
---
# <a name="border-effect"></a>框線效果

使用框線效果，從邊緣延伸影像。 您可以使用此效果來重複影像邊緣的圖元、將圖元換成影像的另一端，或在點陣圖框線之間鏡像圖元以延伸點陣圖區域。

這項效果的 CLSID 是 CLSID \_ D2D1Border。

## <a name="example-images"></a>範例影像

此處的範例會使用每種模式來顯示框線效果的輸出。 輸出大小是無限的，但這些範例影像會裁剪成大小的兩倍。

### <a name="mirror"></a>鏡像



| 之前                                                    |
|-----------------------------------------------------------|
| ![顯示效果之前影像的螢幕擷取畫面。](images/border-before.jpg) |
| After                                                     |
| ![顯示轉換後影像的螢幕擷取畫面。](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| 之前                                                        |
|---------------------------------------------------------------|
| ![顯示夾具效果之前影像的螢幕擷取畫面。](images/border-before.jpg)     |
| After                                                         |
| ![顯示夾具轉換之後影像的螢幕擷取畫面。](images/10-border-clamp.png) |



 

### <a name="wrap"></a>包裝



| 之前                                                       |
|--------------------------------------------------------------|
| ![顯示環繞效果之前影像的螢幕擷取畫面。](images/border-before.jpg)    |
| After                                                        |
| ![顯示換行轉換之後影像的螢幕擷取畫面。](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                  | 描述                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 邊緣模式 X<br/> D2D1 \_ 框線 \_ 樣式 \_ 邊緣 \_ 模式 \_ X<br/> | 效果 X 方向的邊緣模式。 您可以將此設定為 [夾具]、[換行] 或 [鏡像]。 如需詳細資訊，請參閱 [邊緣模式](#edge-modes) 。<br/> 此類型為 D2D1 \_ BORDER \_ EDGE \_ 模式。<br/> 預設值為 D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具。<br/> |
| 邊緣模式 Y<br/> D2D1 \_ 框線 \_ 的 \_ 側邊 \_ 模式 \_ Y<br/> | 效果 Y 方向的邊緣模式。 您可以將此設定為 [夾具]、[換行] 或 [鏡像]。 如需詳細資訊，請參閱 [邊緣模式](#edge-modes) 。<br/> 此類型為 D2D1 \_ BORDER \_ EDGE \_ 模式。<br/> 預設值為 D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具。<br/> |



 

## <a name="edge-modes"></a>邊緣模式



| 顯示名稱和索引列舉                            | 描述                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具<br/>   | 重複影像邊緣的圖元。      |
| 包裝<br/> D2D1 \_ 框線 \_ 邊緣 \_ 模式 \_ 換行<br/>     | 使用影像之相對端邊緣的圖元。 |
| 鏡像<br/> D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 鏡像<br/> | 反映影像邊緣的圖元。         |



 

## <a name="output-bitmap"></a>輸出點陣圖

除了0大小的輸入影像之外，所有輸入的輸出點陣圖大小都是無限的。 如果輸入影像的高度或寬度為0，則輸出大小為0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

