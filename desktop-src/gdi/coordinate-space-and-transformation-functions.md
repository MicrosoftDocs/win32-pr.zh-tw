---
description: 下列函式會搭配座標空間和轉換使用。
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: 座標空間和轉換函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe24e78002393d7a840e99d33840dfa4ba0d9e2ac89d941f998261955683e13f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718078"
---
# <a name="coordinate-space-and-transformation-functions"></a>座標空間和轉換函式

下列函式會搭配座標空間和轉換使用。



| 函式                                                                       | 描述                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | 將指定點的工作區座標轉換為螢幕座標。                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | 串連兩個世界空間與頁面空間的轉換。                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | 將裝置座標轉換為邏輯座標。                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | 以邏輯座標抓取目前的位置。                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | 取得顯示的方向喜好設定。                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | 抓取指定之裝置內容的目前圖形模式。                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | 抓取目前的對應模式。                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | 針對指定的裝置內容，抓取目前視窗區的 x 範圍和 y 範圍。                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | 抓取所指定裝置內容之區原點的 x 座標和 y 座標。                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | 針對指定的裝置內容，捕獲視窗的 x 範圍和 y 範圍。                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | 針對指定的裝置內容，抓取視窗原點的 x 座標和 y 座標。                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | 抓取目前的世界空間到頁面空間轉換。                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | 將邏輯座標轉換成裝置座標。                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | 將 (對應從相對於一個視窗的座標空間，轉換成相對於另一個視窗的座標空間，) 一組點。 |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | 使用指定的模式變更裝置內容的世界轉換。                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | 使用指定的水準和垂直位移，修改裝置內容的視口原點。                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | 使用指定的水準和垂直位移來修改裝置內容的視窗原點。                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | 使用指定的 multiplicands 和除數所形成的比例，修改裝置內容的區區。                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | 使用指定的 multiplicands 和除數所形成的比例，修改裝置內容的視窗。                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | 將畫面上指定點的螢幕座標轉換成用戶端座標。                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | 設定顯示器的方向喜好設定。                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | 設定指定之裝置內容的圖形模式。                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | 設定指定之裝置內容的對應模式。                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | 使用指定的值，設定裝置內容之區的水準和垂直範圍。                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | 指定對應至視窗來源的裝置點 (0、0) 。                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | 使用指定的值，設定裝置內容視窗的水準和垂直範圍。                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | 指定對應至區原點的視窗點 (0、0) 。                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | 針對指定的裝置內容，設定全球空間與頁面空間之間的二維線性轉換。                |



 

 

 
