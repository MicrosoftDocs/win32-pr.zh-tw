---
title: Morphology 效果
description: 在影像中使用 morphology 效果來精簡或加厚邊緣界限。
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- morphology 效果
- dilate 效果
- 瓦解效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104729"
---
# <a name="morphology-effect"></a>Morphology 效果

在影像中使用 morphology 效果來精簡或加厚邊緣界限。 此效果會建立一個核心，其為您所指定之寬度和高度值的2倍。 此效果會將核心放在其所計算的圖元上，如果核心 (中的 dilating) 或最小值，則會傳回最大 (值（如果 eroding) 的話）。

這項效果的 CLSID 是 CLSID \_ D2D1Morphology。

## <a name="example-images"></a>範例影像

此範例顯示使用瓦解模式時的效果輸出。



| 之前                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| After                                                      |
| ![轉換後的影像。](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                          | 類型和預設值                                                     | 描述                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [模式]<br/> D2D1 \_ MORPHOLOGY \_ 的 \_ 模式<br/>     | D2D1 \_ MORPHOLOGY \_ 模式<br/> D2D1 \_ MORPHOLOGY \_ 模式 \_ 瓦解<br/> | Morphology 模式。 可用的模式有瓦解 (簡維) 和 dilate (加厚) 。<br/> 如需詳細資訊，請參閱 [Morphology 模式](#morphology-modes) 。<br/> |
| 寬度<br/> D2D1 \_ MORPHOLOGY \_ 的 \_ 寬度<br/>   | UINT<br/> 1<br/>                                               | 以 X 方向的核心大小。 單位為 Dip。 值必須介於1到100（含）之間。                                                         |
| 高度<br/> D2D1 \_ MORPHOLOGY \_ 的 \_ 高度<br/> | UINT<br/> 1<br/>                                               | 核心在 Y 方向的大小。 單位為 Dip。 值必須介於1到100（含）之間。                                                         |



 

## <a name="morphology-modes"></a>Morphology 模式



| Name                           | 描述                                                    |
|--------------------------------|----------------------------------------------------------------|
| D2D1 \_ MORPHOLOGY \_ 模式 \_ 瓦解  | 使用核心中每個 RGB 通道的最大值。 |
| D2D1 \_ MORPHOLOGY \_ 模式 \_ DILATE | 使用核心中每個 RGB 通道的最小值。 |



 

## <a name="output-bitmap"></a>輸出點陣圖

若為 DILATE 模式，輸出點陣圖大小會增加： 

| 需求 | 值 |
|--------------------------|-----------------------------------------|
| 輸出點陣圖成長 X = | 整數 (浮點數 (寬度) \* ( (使用者 DPI) /96) )   |
| 輸出點陣圖成長 Y = | INT (FLOAT (Height) \* ( (使用者 DPI) /96) )  |



 

針對瓦解模式，輸出點陣圖大小會縮小：

| 需求 | 值 |
|--------------------------|------------------------------------------|
| 輸出點陣圖成長 X = | INT (FLOAT ( 寬度) \* ( (使用者 DPI) /96) )   |
| 輸出點陣圖成長 Y = | INT (FLOAT (-Height) \* ( (使用者 DPI) /96) )  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

