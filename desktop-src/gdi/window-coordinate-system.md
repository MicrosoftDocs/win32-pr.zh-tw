---
description: 視窗的座標系統是以顯示裝置的座標系統為基礎。
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: 視窗座標系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692592"
---
# <a name="window-coordinate-system"></a>視窗座標系統

視窗的座標系統是以顯示裝置的座標系統為基礎。 基本測量單位是裝置單位 (通常是圖元) 。 畫面上的點會以 x 和 y 座標配對來描述。 X 座標會增加到右邊;y 座標從上到下增加。 系統的源 (0、0) 取決於所使用的座標類型。

系統和應用程式會在螢幕上以 *螢幕座標* 指定視窗的位置。 若為螢幕座標，則原點是畫面的左上角。 視窗的完整位置通常是由 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構描述，其中包含定義視窗左上角和右下角的兩個點的螢幕座標。

系統和應用程式會使用 *用戶端座標* 來指定時間點在視窗中的位置。 在此案例中，原點是視窗或工作區的左上角。 無論視窗在螢幕上的位置為何，用戶端座標都能確保應用程式在視窗中繪製時，可以使用一致的座標值。

工作區的維度也會由包含區域之用戶端座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構描述。 在所有情況下，矩形的左上座標都會包含在視窗或工作區中，而右下角座標則會被排除。 視窗或工作區中的圖形作業會從封閉矩形的右和下邊緣中排除。

有時候，應用程式可能需要將一個視窗中的座標組應到另一個視窗中的座標。 應用程式可以使用 [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) 函數來對應座標。 如果其中一個視窗是桌面視窗，此函式會有效地將螢幕座標轉換成用戶端座標，反之亦然。桌面視窗一律會以螢幕座標指定。

 

 
