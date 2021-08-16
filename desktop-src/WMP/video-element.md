---
title: 影片元素
description: 影片元素
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player 的外觀、影片元素
- 外觀、影片元素
- 影片元素
- 外觀的參考、影片元素
- 元素、影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b72df7472829fe9979c9f7a30558e340a69aeb2f7024641623ba6be1a46424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054196"
---
# <a name="video-element"></a>影片元素

**影片** 元素提供一種方式，可讓您使用下列屬性和事件，在面板中操作影片視窗。 為了方便起見，也提供預先定義的 **影片** 元素。

**VIDEO** 元素支援下列屬性。



| 屬性                                            | 描述                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](video-backgroundcolor.md)         | 指定或抓取影片控制項的背景色彩。                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | 指定或抓取當滑鼠停留在影片的可點按區域時，所使用的資料指標值。                                                                                                                               |
| [全屏](video-fullscreen.md)                   | 指定或抓取值，指出影片是否以全螢幕模式顯示。 只有在執行時間才可設定。                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | 指定或抓取值，指出影片是否會在嘗試符合為控制項定義的寬度和高度時維持外觀比例。                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | 指定或抓取值，指出影片是否會壓縮成針對影片控制項定義的寬度和高度。                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | 指定或抓取值，指出影片是否將本身延展至為影片控制項定義的寬度和高度。                                                                                                   |
| [提示](video-tooltip.md)                         | 指定或抓取影片視窗的工具提示文字。                                                                                                                                                                            |
| [無視窗](video-windowless.md)                   | 指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。 只能在設計階段設定。 |
| [縮放](video-zoom.md)                               | 指定縮放影片的百分比。                                                                                                                                                                                    |



 

**影片** 元素可以執行下列事件處理常式。



| 事件處理常式                          | Description                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | 處理當影片停止轉譯並卸載時所發生的事件。 |
| [onvideostart](video-onvideostart.md) | 處理載入影片並開始轉譯時所發生的事件。  |



 

**VIDEO** 元素支援環境屬性，而且可以執行環境事件處理常式（除非有注明）。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

預先定義的影片專案是一般的 **影片** 元素，預設會指定各種不同的通用屬性設定。 您可以使用下列預先定義的影片元素。



| 預先定義的影片         | Description                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | 調整大小後，自動調整影片的 **影片** 元素。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




