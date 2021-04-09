---
title: 影片影像轉換
description: 影片影像轉換
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK、影片影像轉換
- Advanced Systems Format (ASF) 、影片影像轉換
- ASF (Advanced 系統格式) 、影片影像轉換
- 影片影像轉換
- Windows Media 視訊9映射 v2 編解碼器
- 編解碼器，Windows Media 視訊9映射 v2 編解碼器
- 影片串流，Windows Media 視訊9映射 v2 編解碼器
- 影片串流，影像轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021256"
---
# <a name="video-image-transitions"></a>影片影像轉換

Windows Media 視訊9映射 v2 編解碼器會將一系列的影像動畫，並產生影片串流。 編解碼器可以一次管理兩個影像，並將它們結合在一起，並根據您所提供的設定，建立從另一個影像轉換。 本節說明支援的轉換和它們所需的參數。

轉換依其全域識別碼列于下表中。



| 轉換識別碼                                                                           | Description                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 凸起 \_ 系結**](wmt-videoimage-transition-bow-tie.md)              | 新的影像會顯示在框架相反邊的一組三角形中。                                                                  |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 圓形**](wmt-videoimage-transition-circle.md)                 | 新的影像會顯示在圓形中。                                                                                                           |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 交叉 \_ 淡化**](wmt-videoimage-transition-cross-fade.md)        | 沒有特殊轉換，這兩個影像的 blend 係數會決定交叉淡化 (溶解) 。                                         |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 對角線**](wmt-videoimage-transition-diagonal.md)             | 新的影像會沿著框架的一個角落以對角線線顯示。                                                          |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 鑽石**](wmt-videoimage-transition-diamond.md)               | 新的影像會顯示在菱形中。                                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 淡化 \_ 成 \_ 色彩**](wmt-videoimage-transition-fade-to-color.md) | 從影像到純色框架的溶解。                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ 轉換已 \_ 填滿 \_ V**](wmt-videoimage-transition-filled-v.md)            | 新的影像會顯示在來自框架某一端的三角形中。                                                                  |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 翻轉**](wmt-videoimage-transition-flip.md)                     | 舊影像會在 y 軸上透過框架的中心旋轉。 新映射會顯示為舊影像的背面。                    |
| [**WMT \_ VIDEOIMAGE \_ 轉換內 \_ 凹**](wmt-videoimage-transition-inset.md)                   | 新的影像是由框架的一個角落的矩形所顯示。                                                               |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 鳶尾花**](wmt-videoimage-transition-iris.md)                     | 沿著 X 軸和 y 軸顯示新的影像。                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 頁面 \_ 滾動**](wmt-videoimage-transition-page-roll.md)          | 舊影像會在頁面翻轉效果中轉換，並在下方顯示新的影像。                                                      |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 矩形**](wmt-videoimage-transition-rectangle.md)           | 框架內的矩形會顯示新的影像。                                                                                       |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 顯示**](wmt-videoimage-transition-reveal.md)                 | 新的影像會沿著來自框架一端的直線來顯示。                                                          |
| [**WMT \_ VIDEOIMAGE \_ 轉換投影 \_ 片**](wmt-videoimage-transition-slide.md)                   | 舊的影像會滑出畫面格，並在下方顯示新的影像。                                                                       |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 分割**](wmt-videoimage-transition-split.md)                   | 新的影像會顯示在舊影像中的水準或垂直分割。 分割會沿著框架內的直條顯示。 |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 星星**](wmt-videoimage-transition-star.md)                     | 新的影像會顯示在框架內由五個指向的星星。                                                                               |
| [**WMT \_ VIDEOIMAGE \_ 轉換 \_ 輪子**](wmt-videoimage-transition-wheel.md)                   | 有四個具有一般軸的旋轉輪輻可顯示新的影像。                                                                     |



 

每個轉換都是在它自己的主題中完整說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




