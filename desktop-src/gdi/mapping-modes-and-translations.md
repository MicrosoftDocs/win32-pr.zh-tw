---
description: 下表說明對應模式。
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: 對應模式和翻譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219bfe2f587ef9bc66f53d6f08404a0448180512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191936"
---
# <a name="mapping-modes-and-translations"></a>對應模式和翻譯

下表說明對應模式。



| 對應模式    | Description                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ 各向異性 | 頁面空間中的每個單位會對應到裝置空間中的應用程式指定單位。 軸可能或可能無法平均調整 (例如，在世界空間中繪製的圓形可能會在指定的裝置) 上顯示為橢圓形。 軸的方向也是由應用程式所指定。                  |
| MM \_ HIENGLISH   | 頁面空間中的每個單位會對應到裝置空間中的0.001 英寸。 X 的值會從左至右增加。 Y 的值會從下到上遞增。                                                                                                                                                                 |
| MM \_ HIMETRIC    | 頁面空間中的每個單位會對應到裝置空間中的0.01 毫米。 X 的值會從左至右增加。 Y 的值會從下到上遞增。                                                                                                                                                            |
| MM \_ ISOTROPIC   | 頁面空間中的每個單位會對應到裝置空間中的應用程式定義單位。 軸一律會平均調整。 軸的方向可以由應用程式指定。                                                                                                                                     |
| MM \_ LOENGLISH   | 頁面空間中的每個單位會對應到裝置空間中的0.01 英寸。 X 的值會從左至右增加。 Y 的值會從下到上遞增。                                                                                                                                                                  |
| MM \_ LOMETRIC    | 頁面空間中的每個單位會對應到裝置空間中的0.1 毫米。 X 的值會從左至右增加。 Y 的值會從下到上遞增。                                                                                                                                                             |
| MM \_ 文字        | 頁面空間中的每個單位都對應到一個圖元;也就是說，完全不會執行任何調整。 當轉譯沒有作用時 (這是預設) ，MM 文字對應模式中的頁面空間 \_ 相當於實體裝置空間。 X 的值會從左至右增加。 Y 的值會從上到下增加。 |
| MM \_ 緹       | 頁面空間中的每個單位會對應至印表機的點 20 (1/1440 英寸) 。 X 的值會從左至右增加。 Y 的值會從下到上遞增。                                                                                                                                           |



 

若要設定對應模式，請呼叫 [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 函數。 藉由呼叫 [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) 函數，以抓取 DC 目前的對應模式。

頁面空間與裝置空間的轉換，是由由視窗和視口提供的點所計算的值所組成。 在此內容中，視窗是指頁面空間的邏輯座標系統，而此區則是指裝置空間的裝置座標系統。 每個視窗和視口都包含一個原點、水準 ( "x" ) 範圍，以及垂直 ( "y" ) 範圍) 。 視窗參數是以邏輯座標為單位;裝置中的區座標 (圖元) 。 系統會結合視窗和視口的來源和範圍來建立轉換。 這表示，每個視窗和視口都指定所需的一半因素，以定義用來將頁面空間中的點對應到裝置空間的轉換。 因此，系統會將視窗來源對應至區原點，並將視窗範圍對應至區的範圍，如下圖所示。

![圖例顯示頁面空間中的視窗來源，以及裝置空間中的觀點原點](images/cstrn-15.png)

視窗和視窗區範圍會建立頁面空間與裝置空間轉換所使用的比例或縮放比例。 針對六個預先定義的對應模式 (MM \_ HIENGLISH、mm \_ LOENGLISH、mm \_ HIMETRIC、MM \_ LOMETRIC、mm \_ TEXT 和 mm \_ 緹) ，當呼叫 [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 時，系統會設定範圍。 無法變更。 另外兩個對應模式 (MM \_ ISOTROPIC 和 mm 非 \_) 需要指定範圍。 這是藉由呼叫 **SetMapMode** 來設定適當的模式，然後呼叫 [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) 和 [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) 函數來指定範圍來完成。 在 MM \_ ISOTROPIC 對應模式中，請務必在呼叫 **SetViewportExtEx** 之前呼叫 **SetWindowExtEx** 。

視窗和視口來源會在頁面空間中建立用來轉換裝置空間的翻譯。 使用 [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) 和 [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) 函數來設定視窗和視口來源。 來源與範圍無關，而且應用程式可以設定它們，無論目前的對應模式為何。 變更對應模式不會影響目前設定的來源 (但它可能會影響範圍) 。 來源是以目前對應模式不會影響的絕對單位來指定。 若要改變來源，請使用 [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) 和 [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) 函數。

下列公式顯示將某個點從頁面空間轉換成裝置空間時所牽涉到的數學運算。

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

涉及下列變數。

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

Y 取代 x 的相同方程式會將 y componentof 點轉換。

公式會先從其座標原點位移點。 此值不會再由原點偏差，接著會依照範圍的比例調整為目的地座標系統。 最後，縮放值會以目的原點位移至其最終對應。

[**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)和 [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)函式可以用來分別從邏輯點轉換成裝置點，以及從裝置點轉換成邏輯點。

 

 



