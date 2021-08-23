---
description: 下列函式可用於繪製和繪製。
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: 繪製和繪製函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51b8acb0ea187c17d220d80f105ad6ae49371688d4eb8671c2a8eb5949b6e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666618"
---
# <a name="painting-and-drawing-functions"></a>繪製和繪製函數

下列函式可用於繪製和繪製。



| 函式                                       | 描述                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | 準備視窗進行繪製。                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | 繪製矩形並以動畫顯示，以表示圖示或視窗活動。                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | 繪製視窗標題。                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | 繪製矩形的一或多個邊緣。                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | 以表示矩形具有焦點的樣式來繪製矩形。                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | 繪製框架控制項。                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | 顯示影像，並套用視覺化效果以表示狀態。                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | 為 [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)呈現複雜影像的回呼函式。                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | 在視窗中標示繪製的結尾。                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | 防止在視窗的無效區域內進行繪圖。                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | 清除呼叫執行緒的目前批次。                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | 傳回可在呼叫執行緒的目前批次中累積的函式呼叫數目上限。 |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | 設定可在呼叫執行緒的目前批次中累積的函式呼叫數目上限。    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | 傳回裝置內容的背景色彩。                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | 傳回裝置內容的背景混合模式。                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | 取得裝置內容的累積周框。                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | 取得裝置內容的前景混合模式。                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | 取得包圍視窗更新區域之最小矩形的座標。                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | 取得視窗的更新區域。                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | 取得視窗的裝置內容，包括標題列、功能表和捲軸。                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | 取得視窗視窗區域的複本。                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | 取得視窗視窗區域的嚴謹周框的維度。                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | 在位置繪製灰色文字。                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | 將矩形新增至視窗的更新區域。                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | 使區域內的工作區失效。                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | 停用或啟用視窗中的繪圖。                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | 搭配 [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa) 函數使用的回呼函數。 它是用來繪製字串。   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | 使用模式填滿裝置內容中的裁剪區域。                                               |
| [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | 更新視窗工作區中的區域。                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | 將背景設定為色彩值。                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | 設定裝置內容的背景混合模式。                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | 控制裝置內容之周框的累積資訊。                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | 設定前景混合模式。                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | 設定視窗的視窗區域。                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | 更新視窗的工作區。                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | 驗證矩形內的工作區。                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | 驗證區域內的工作區。                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | 傳回與裝置內容相關聯的視窗控制碼。                                            |



 

 

 



