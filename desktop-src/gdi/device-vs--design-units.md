---
description: 只有在將字型選取至裝置內容之後，應用程式才能取得實體字型的字型度量。
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: 裝置與設計單位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ac0ed7ad02ced5390201000fbc76217b8c579116bf36b356b13880d5d0158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354408"
---
# <a name="device-vs-design-units"></a>裝置與設計單位

只有在將字型選取至裝置內容之後，應用程式才能取得實體字型的字型度量。 在裝置內容中選取字型時，會針對裝置進行縮放。 裝置特定的字型計量稱為裝置單位。

字型中的可攜計量稱為「設計單位」。 若要套用至指定的裝置，設計單位必須轉換成裝置單位。 使用下列公式將設計單位轉換成裝置單位。

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*dialog*/72) \* *DeviceResolution*

此公式中的變數具有下列意義。



| 變數           | 描述                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | 指定轉換成裝置單位的 *DesignUnits* 字型度量。 此值的單位與針對 *DeviceResolution* 指定的值相同。                          |
| *DesignUnits*      | 指定要轉換成裝置單位的字型度量。 這個值可以是任何字型指標，包括字元寬度或整個字型的 ascender 值。 |
| *unitsPerEm*       | 指定字型的 em 正方形大小。                                                                                                                                 |
| *Dialog*        | 指定字型的大小（以點為單位）。  (一點等於1/72 英寸。 )                                                                                                  |
| *DeviceResolution* | 指定每英寸 (圖元) 的裝置單位數目。 雷射印表機的一般值可能是300，而針對 VGA 螢幕則是96。                                                |



 

此公式不能用來將裝置單位轉換回設計單位。 裝置單位一律會四捨五入至最接近的圖元。 傳播的舍入錯誤可能會變得非常大，特別是當應用程式使用螢幕大小時。

若要要求設計單位，請建立其高度指定為 *unitsPerEm* 的邏輯字型。 應用程式可以藉由呼叫 [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)函式並檢查 [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **NtmSizeEM** 成員，來取得 *unitsPerEm* 的值。

 

 



