---
description: 當您第一次建立顯示裝置內容時，系統會為屬性指派預設值 (也就是組成裝置內容) 的繪圖物件、色彩和模式。
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: 顯示裝置內容預設值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848561"
---
# <a name="display-device-context-defaults"></a>顯示裝置內容預設值

當您第一次建立顯示裝置內容時，系統會為屬性指派預設值 (也就是組成裝置內容) 的繪圖物件、色彩和模式。 下表顯示顯示裝置內容之屬性的預設值。



| 屬性                             | 預設值                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 背景色彩                      | 主控台 (的背景色彩設定，通常是白色) 。                                                                               |
| 背景模式                       | 不透明                                                                                                                                        |
| 點陣圖                                | 無                                                                                                                                          |
| 筆刷                                 | 白色 \_ 筆刷                                                                                                                                  |
| 筆刷來源                          |  (0、0)                                                                                                                                          |
| 裁剪區域                       | 以適當的方式裁剪更新區域的整個視窗或工作區。 也可以裁剪用戶端區域中的子視窗和快顯視窗。 |
| 調色盤                               | 預設 \_ 調色板                                                                                                                              |
| 目前的畫筆位置                  |  (0、0)                                                                                                                                          |
| 裝置來源                         | 視窗或工作區的左上角。                                                                                           |
| 繪圖模式                          | R2 \_ COPYPEN                                                                                                                                   |
| 字型                                  | 系統 \_ 字型                                                                                                                                  |
| Intercharacter 間距                | 0                                                                                                                                             |
| 對應模式                          | MM \_ 文字                                                                                                                                      |
| 手寫筆                                   | 黑色 \_ 畫筆                                                                                                                                    |
| [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) 填滿模式 | 互生                                                                                                                                     |
| Stretch 模式                          | BLACKONWHITE                                                                                                                                  |
| 文字色彩                            | 主控台的文字色彩設定 (通常是黑色) 。                                                                                     |
| 視口範圍                       |  (1，1)                                                                                                                                          |
| 視口來源                       |  (0、0)                                                                                                                                          |
| 視窗範圍                         |  (1，1)                                                                                                                                          |
| 視窗來源                         |  (0、0)                                                                                                                                          |



 

應用程式可以使用選取專案和屬性函式（例如 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)、 [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)和 [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)）來修改顯示裝置內容屬性的值。 例如，應用程式可以使用 **SetMapMode** 來變更對應模式，以修改座標系統中的預設測量單位。

對通用、父系或視窗裝置內容的屬性值所做的變更不是永久性的。 當應用程式釋放這些裝置內容時，當內容傳回快取時，目前的選取專案（例如對應模式和裁剪區域）將會遺失。 對類別或私用裝置內容的變更會無限期保存。 若要將它們還原為其原始預設值，應用程式必須明確設定每個屬性。

 

 



