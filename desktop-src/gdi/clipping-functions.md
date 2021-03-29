---
description: 下列函式會與裁剪一起使用。
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: 裁剪函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf202d5ba102095c6bfddb3c3928cab1e55a230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972756"
---
# <a name="clipping-functions"></a>裁剪函式

下列函式會與裁剪一起使用。



| 函式                                       | 描述                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | 建立新的裁剪區域，其中包含現有的裁剪區域減去指定的矩形。                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | 使用指定的模式結合指定的區域與目前的裁剪區域。                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | 抓取可在裝置上的目前可見區域周圍繪製之嚴謹周框的尺寸。                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | 抓取控制碼，該控制碼會識別指定之裝置內容目前應用程式定義的裁剪區域。                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | 抓取指定之裝置內容的目前 metaregion。                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | 將指定之裝置內容的系統裁剪區域複製到特定區域。                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | 從目前裁剪區域和指定矩形的交集建立新的裁剪區域。                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | 依據指定的位移移動裝置內容的裁剪區域。                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | 判斷指定的點是否在裝置內容的裁剪區域內。                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | 判斷指定的矩形是否有任何部分位於裝置內容的裁剪區域內。                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | 選取目前的路徑作為裝置內容的裁剪區域，並使用指定的模式結合新區域與任何現有的裁剪區域。                               |
| [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | 選取區域做為指定之裝置內容的目前裁剪區域。                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | 使用目前的 metaregion 與指定之裝置內容的目前裁剪區域交集，並將結合的區域儲存為指定之裝置內容的新 metaregion。 |



 

 

 



