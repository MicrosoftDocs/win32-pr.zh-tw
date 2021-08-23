---
description: 與 DC 相關聯的畫筆、筆刷、點陣圖、調色板、區域和路徑稱為其繪圖物件。 下列屬性與每個物件相關聯。
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: 圖形物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf256cd8eafd6ee346c12f6658a7c3dd388c94fb4107b010528e47c126fce2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831958"
---
# <a name="graphic-objects"></a>圖形物件

與 DC 相關聯的畫筆、筆刷、點陣圖、調色板、區域和路徑稱為其繪圖物件。 下列屬性與每個物件相關聯。



| 繪圖物件 | 相關聯的屬性                                                               |
|----------------|-------------------------------------------------------------------------------------|
| 點陣圖         | 大小，以位元組為單位;維度（以圖元為單位）。色彩格式;壓縮配置;依此類推。 |
| 筆刷          | 樣式、色彩、模式和原點。                                                  |
| 調色盤        | 色彩和大小 (，或) 的色彩數目。                                              |
| 字型           | 字型名稱、寬度、高度、權數、字元集等等。                     |
| 路徑           | 形狀。                                                                              |
| 手寫筆            | 樣式、寬度和色彩。                                                            |
| 區域         | 位置和維度。                                                            |



 

當應用程式建立 DC 時，系統會自動將一組預設物件儲存 (沒有預設的點陣圖或路徑) 。 應用程式可以藉由呼叫 [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) 和 [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) 函數來檢查預設物件的屬性。 應用程式可以藉由建立新的物件並將其選取到 DC，來變更這些預設值。 藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函數，將物件選取至 DC。

應用程式可以使用 [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)將目前的筆刷色彩設定為指定的色彩值。

[**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)函式會傳回 DC 筆刷色彩。 [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)函式會將畫筆色彩設定為指定的色彩值。 [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)函式會傳回 DC 畫筆色彩。

 

 



